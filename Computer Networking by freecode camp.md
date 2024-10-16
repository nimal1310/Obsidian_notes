
## Part 1 
### OSI Layer:
**Layer 1 Devices** - Hub,Modem
**Layer 2 Devices** - Switch,Wireless Access Point
**Layer 3 Devices** 
- Multi layer Switch
	- Expensive ,used in larger enterprise or network
	- aka layer 3 switch 
	- It communicate with local area network
- Router 
	- It is used to connect the device to  outside the network. 
	- Use s/w to calculate the shortest path to route the data packet.
### Security Devices:
**Firewall** - s/w or h/w based firewall 
- LINUX: IPfire,pfSense,IPtables,OPNsense,firewalld,nfttables
- WINDOWS : palo alto network ,pfSense,Sophos
- Mac : Murus,Norton 360, cisco system
- Android

**Intrusion Detection System** :  
- snort
- suricata
**Intrusion Prevention System**

**Virtual Private Network**:
- It provide a protected network connection
- Encrypted connection
- Secure data transfer
- History - It was a project first started by US Department of Defense in 1960 ,in 1993 the first vpn named as *swlPe* was developed (Nord vpn)
- It has some disadvantages like speed ,high data usage
- L2TP and PTTP protocols
- Stable and seamless connection
- SOLUTION : use local vpn to increase speed.

**Proxies**

- It is similar to VPN ,it used to maintain the anonymity of every user
- It doesn't encrypt the data .
- It get the request from the client and search on the web behalf of client and provide the result to cliet
- Filter the content
- Bandwidth saving and speed improved 
- FTP,SMTP,HTTPS
- Unstable
- It stores the user browsing logs and proxy server risk.
- TYPES:
- Reverse proxy
- Rotating proxy
- Web proxy
- DNS proxy
1. **Forward proxy** :
	- It make the client anonymous by hiding the client IP from the web server or internet
	- cache the data to provide instant access to website which was previously visited
	- Encryption,traffic control
	- Req/Res Transformation,logging
	- Uses:schools,colleges and big org

1.   **Reverse Proxy**

		- It provide the server anonymity by hiding the IP address of the server machine to the user or client.
		- Load balancing
		- DDoS protection
		- URL content rewriting 
		- canary experiment (like beta testing of new s/w)
		- Uses: Server side


**Load Balancing**:
- Load balancer is a S/W or H/W networking device used to manage or balance the incoming traffic to a server. If a website has multiple server LB will efficiently distribute the traffic among multiple server.It ensure no request is in wait
- It's like a "traffic cop".
- It reduce the down time of the application by distributing the client request to different system.
- *Advantages:* Efficient load balance,utilization of server,high performance.
- *Issues*: 
	- Single point of failure
	- Overloaded servers

- **Key characteristics of load balancer**
	- Traffic distribution
	- High scalability
	- Optimization
	- Scalability -> Horizontal scaling
	- Health monitoring
 
- **Types of load balancing**
	- S/W based load balancing
	- S/W load balancers in services
	- H/W load balancers
	- Virtual load balancers
- **Load balancing algorithm**
	- Static
		- Round robin
		- Weighted round robin
		- Source IP hash
	- Dynamic
		- Least connection method
		- Least response time method
- **Drawback**
	- Single point failure
		- Single point failure not occur in servers it happen on load balancer .If the load balancer itself experience this issues it may disrupt traffic distribution
	- Complexity and cost ->Due to horizontal scaling
	- Configuration challenges
	- Potential overhead ,ssl inspeciton and learning curve

### Basics of the VPN:
- VPN TYPES:
	- site-to-site vpn
	- remote access vpn(host-to-site)
	- host-to-host(ssl vpn)
- PROTOCOLS:
	1. **IPsec**:
		- Most used protocol ,used in layer 3
		- Use authentication header (AH) ->no encryption
		- encapsulation security payload(ESP)-> authentication and encryption
		- Two modes-> transport and tunnel
		- ISAKMP
	2. **GRE**: 
		- It is unicast
	3. **Point to Point**
	4. **Transport layer security**
	5. **Secure socket layer**




### Content Delivery Network:

- Content delivery network(CDN) is a geographical distributed group of servers(Edge server) that caches content close to end users.
- It rely on a process called **Caching** that temporarily stores copies of file in the data centers *across the globe allowing you to access the content from a server near to you.*
- It reduces the page load times and show the result in faster in web page.
- CDN or Edge server will store the frequently or most searched content in the local or edges server present near to user and get the result from it.
- In a scenario of searching on google the user send the query /request to near by data center if it present in the **cache or copies** the CDN sent it back to user or it forward the user request to origin server somewhere around the world and retrieved it and store in edge server and sent it as response to user.
- The cache stored in edge server will erase after center amount of time (TTL)
- CDN stores the geo specific content permanently on edges server( eg: content related to india are stored permanently.) other country related data stored for some time with legal access.
- 





 
   
 
