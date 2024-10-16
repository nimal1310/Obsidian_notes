## 1. Managing Firewall

   **IPtable**

- It is a tool which is present default on linux system to manage the incoming and outgoing network traffic of a system.
- It is used for the following purpose 
	- I/O and forwarding rules maintaining
	- Packets filtering
	- Different set of rules(filter,nat ,mangle ,raw ,security)
	- **Mangle** ->  It is a kind of marker added to the packet for the future processing of the packet with special marker. or modification of packet.
	- CHAIN 
		- INPUT -> for incoming traffic
		- OUTPUT -> for outgoing traffic 
		- FORWARD -> It is used in a system if its act as a router 


- **NOTE:**

	- IPtable rules are applied immediately after execution of code without needing to restart any services or reload configuration.
	- So one should add the rules carefully in iptable.
	- `Eg:` If suppose you configure the firewall accidentally deny all the ssh (port 22) incoming traffic to a system and your remotely configure the firewall  through ssh then it will refuse your connection after that you cant reconnect to that system remotely.
	- Always add the drop(deny) at bottom of list and accept's at first if you add the drop first if dont consider the following rules.


- **Good Practices**
	- Backup and Test Rules
	- Set default policies carefully( Accept ,Drop)
	- Use the stateful rules -> which helps manage connections securely( *eg:* allowing only established connections through ssh)
	- Test in a control environment
	- Use fail-safes
		- at or cron -> schedule automatic rollback of iptables in case of lockout.
	- Monitor logs

```bash

echo "iptables-restore < /root/iptables_backup.rules" | at now + 5 minutes

```

- **OPTIONS**
	- -L -> To list the rules in iptables
	- -A -> Append to add the rule at the end which is rarely used only once at a time to add deny rule at bottom.
	- -I -> Insert the rules from the top of the list
	- -P -> Port specification

	For more option - [click me](https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/4/html/reference_guide/s2-iptables-options-commands#s2-iptables-options-commands)

- **COMMANDS**
	- LIST
	- Allowing incoming ssh traffic
	- Deny all incoming traffic
	- Block traffic from a specific ip
	- Delete rule
	- Flush rule

```bash

sudo iptables -L
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT

sudo iptables -P INPUT DROP
sudo iptables -A INPUT -s 192.168.1.100 -j DROP/ACCEPT

sudo iptables -D INPUT [line_number]
sudo iptables -F

```


- **SAVE AND RESTORE**
	- It save the current or previous rules for backup can we restore in case of any misconfigurations in rules

```bash
#backup file
sudo iptables-save > /root/iptables_backup.rules

#restore file
sudo iptables-restore < /root/iptables_backup.rules


```

```bash
sudo iptables -A OUTPUT -p udp --dport 53 -m string --string "youtube.com" --algo bm -j REJECT
sudo iptables -A OUTPUT -p tcp --dport 53 -m string --string "youtube.com" --algo bm -j REJECT

```

where,
- -A => Append
- OUTPUT => output traffic
- UDP  => dns packets use port 53(UDP)
- -M   =>  String matching 
- string => It is module used to match the content of the packets
-  \ -- string "youtube.com" => match for string
- \ -- algo bm => It specify the matching algorithm to search for string in packet (bm - Boyer-Moore)
- -j REJECT =>reject the packet 