**AUTHENTICITY** - verify or validate yours identity
**AUTHORIZATION** - User's level of access
## Unit 1 INTRODUCTION TO SECURE SYSTEM

>
>An overview of Computer Security – Access Control matrix – Foundational results – Security Policies –
Confidentiality policies – Hybrid policies.

### Computer Security
  **What is computer security**
-  It is a practice of protecting network or computer from disclosure,identity theft and damages. 
- Key aspect :
	- Confidentiality
		- provide authorization,prevent unauthorized access
	- Integrity
		- Maintain accuracy and ensure data cant modified in unauthorized.
	- Availability
		- ensure that authorized user can access the resource needed.

**Important of computer security**
- Protecting personal information
- Business continuity
- National security
- Financial security

**Computer security application**
- Antivirus,firewall,ids/ips, encryption,2FA,OTP.

**Type of threats**
- *Malware*
	1. Viruses :
		- Virus is a malicious code attached with executable file.
		- It is more harmful
		- It spread slower compared to worm
		- `Eg:` Blaster ,slammer
		- *MyDoom* is considered one of the most destructive computer viruses ever, causing an estimated $38 billion in damage in 2004

	2. worms :
		- It replicate itself and spread to different computer via a network.
		- It is less harmful
		- It spread faster
		-  `Eg:` Morris worm
		- *MyDoom* is considered one of the most destructive computer viruses ever, causing an estimated $38 billion in damage in 2004
	    
	3. Trojan Horse:
		- It is like a legitimate program to deceive(fool) the users.The word comes from greek myth.
		- *Purpose:* steal data,create backdoor ,redirect traffic and monitor activity,delete files
		
    4. Ransomware:
     -  Encrypt the user file with key and demand for ransom(money).
- *Phishing*
		Phishing is a attack that deceive(fool) any one to provide their personal data by masquerading as trustworthy site.
	1. Email phishing
	2. Spear phishing
- *Denial of Service (DoS)Attack*:
- *Distributed Dos (DDos) Attack* ->Multiple infected or compromised system used as a botnet to perform DoS.
- *Man in the Middle(MitM) Attack*: Intercepting connection over public wi-fi.
- *Insider threat:*
	- Malicious Insider
	- Unintentional insider
- *Advanced Persistent Threat(APTs):*
	- The name was coined by US airforce in 2000s.
	- In 1996 the 1st APT attack **moonlight maze** was founded.
	 - In which the attacker gain the access of a system and remain undetected for extended period of time.
	 - It was sponsored by nation to steal or perform attacks on other country infrastructures.
	 - `Eg:` **Stuxnet** 2010 ,It down the iran nuclear power plant sent by israeli cyberforces.
    - Mitigation Measures:
	    - Access control
	    - Endpoint security,Network security ,incident response etc.
--- 
### Access control
 Access control is providing privileges to user who is authorized to access the different resources in a organization.
 - Hardware 
 - OS
 - Middleware 
 - Application

- **Level of access control list**:
1.   *Hardware access control:*
- It is a set of security measures and protocols that manage and regulate the user access to hardware devices in a computing environment.
- *Policies:*
	- Protect os from app,protect application from others,
- *Mechanism:*
	- paging unit 
	- privilege ring 
		- Which show the different level of access to the resource or privileges available in the computer architecture.
			1. Ring 0-kernel
			2. Ring 3-application
			3. Protection 
	- Interrupts

 2. *Access control at OS level:*

	- Access control at os level regulate and manage the process ,files, who can uses and access.
	- *Policies:*
		- only authenticate user can access,one user file can be protected from other users.
		- process should protected from other user
		- fair allocation on resources(cpu,storage,network)
	- *Mechanism:*
		- user authentications,access control to files ,scheduling,deadlock detection/prevention.
		
3. *Middleware*
	- It is a s/w that lies b/w an OS and the application running on it.
	- It provide services to the client request by getting resource from the server side.
	- `Eg:` In OS kernel is a middleware b/w os and applications.

4. *Application*
	- It is the top layer that provide user interface to interact with os.

**Access Matrix in OS**

- Access matrix maintain and control the permissions.
- It is a table that shows what actions an individual or group or other can possible do in a system.
- *Actions:*  read,write and execute

    ![[Pasted image 20240918185453.png]] 
- Access matrix =A[x,y]  x->operation ,y->object on which operation to perform
- D - Domain ,F-files
- various implementation of access matrix
	- Global table
	- Access list for objects
	- Capability list for Domains

 - **Access control lists vs Capability lists** 
1. ACL
	 - Access control lists can be created by splitting the access matrix column-wise
	 - Each object has list of pairs of the form <subject,access rights>
	 - Everyone should be able to access a file
	 - It is simple.
	 - `Eg:` It is used in UNIX file system.
2. Capability lists:
	- It is row-wise
	- Each subject has a list of pairs of the form <object,access rights>
	- No one can be access the file unless they have the capability.
	- It is very secure 

--- 
### Security Policies:
- It is a written documents by the organization that contains actions or steps to be followed to protect organization from threat and what measure to taken after the such threat happened.
- It is aka "living documents " -> It  continuously updated based on the new threats.
**Type of security policy**
- An organizational security policy
- System-specific security policy
- Issue-specific security policy
**Need of security policy**
- It increase the efficiency
- It upholds discipline and accountability
- It educate the employee on security measures.
[**Element of security policy**](https://www.exabeam.com/explainers/information-security/the-12-elements-of-an-information-security-policy/)
- There are 12 elements in information security policy,they are
	- Purpose
	- Audience -who can access which resources.
	- Information security objectives -> CIA
	- Authority access control policy
		- Hierarchical Sec Policy
		- Network Sec Policy
	- Data Classification 
		- top secret
		- secret 
		- confidential
		- public
	- Data support & operations
	- Security awareness & behavior
	- Encryption policy
	- Data backup policy
	- Responsibility ,audit & duties of personnel
	- System hardening benchmark ->CIS benchmark
	- Reference to regulation and compliance standards.
		- HIPAA 
		- PCI DSS
		- GDPR 

### Confidentiality Policies:
- Confidentiality measures are designed to prevent unauthorized disclosure of information.
- Only authorized user can access the data for the functional requirement of the company
- One model of a confidential policy is the **Bel LaPadula (BLP)** security model.
- The Bell–LaPadula model leverages mandatory access control: the model does not give users power to alter access control in the system manifested in a principle called *tranquility*.
- BLP is multi-level security model that protect confidentiality.
- It states information cannot leak to subjects who are not cleared for the information.
[confidential policy](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.rose-hulman.edu/class/cs/csse442/current/notes/CIPoliciesNotes.pdf&ved=2ahUKEwib9vS40NCIAxXiSWwGHRvDLskQFnoECBwQAQ&usg=AOvVaw0T-3oZBdQ01KNkkZB_1BMC)

## Unit 2 BASIC CRYPTOGRAPHY AND KEY MANAGEMENT 

>Classical Crypto systems: Transposition ciphers, Substitution ciphers, Data Encryption Standard – Public Key
cryptography: RSA – Cryptographic checksums: HMAC – Key Management: Key Exchange, Cryptographic key
infrastructure – Digital Signature

**Classical Crypto  System:**

- Crypto system aka **cipher system** which implement different encryption techniques to safe the files or data.
- Components of crypto system
	- Plain text
	- Encryption algorithm
	- Cipher text
	- Decryption algorithm
	- Encryption key
	- Decryption key


- Types of crypto systems:
	- **Symmetric key encryption** 
		- Symmetric key cryptography is study of symmetric cryptosystems or secret key cryptosystem.
		- Digital/Data Encryption Standard (DES),AES (Advance Encryption standard),3DES,IDEA(International Data Encryption Standard) & BLOWFISH,Twofish,Threefish
		- *Features*
			- It is fast compare to asymmetric because of same key
			- For  `n` user it required n* (n-1)/2 keys to communicate with each other
			- It provide different bits of encryption (`eg:` AES provide 128,192,256 bit encryption)
			- It require less power to run symmetric algorithm in a computer
			- Quick,Easy to use,confidentiality, designed to withstand attacks
		- *Challenge of symmetric key cryptosystem*
			- Key establishment - Before communication both the sender and the user should have the secret key with us
			- Trust issues - If the key was stolen from one of the user then the message loss its confidentiality.
			- Key expiration - It don't have metadata so we need to separately track on key life cycle.
			- Key disclosure - if the secret key stolen from one user it will create threat to all the user using the same key for communication.
	
	- **Asymmetric Key Encryption(public key encryption):**
		- It is type of encryption method to encrypt the plain text or data to cipher text with private and public key.
		- Both key are different but mathematically its related.
		- It 
		- `Algo:` RSA(Rivest-shamir-Adleman),ECC(Elliptic Curve Cryptography), Digital Signature Algorithm(DSA)
		- *Features:*
			- Two keys
			- Mathematical complexity
			- Secure communication
			- Data integrity 
			- Key linkage
		-  *Challenges*
			- Speed
			- Resource consumption
			- Management
			- Adoption
			- Quantum computer - Asymmetric key can break by quantum computer.
	
	- **Transposition Cipher techniques in cryptography**
		- Systematic shuffling of plain text to character to secure data by altering their position based on some defined algorithm.
		- Types of transposition cipher techniques:
			- Rail fence transposition cipher
			- Block(single columnar) transposition cipher 
			- Double columnar transposition cipher 
	1. *Rail fence transposition cipher:*
		- It is aka `zigzag cipher `
		- For example, if the message is “GeeksforGeeks” and the number of rails = 3 then cipher is prepared as:
		- ![[Pasted image 20241013164322.png]]
		 - Cipher text ="GsGsekfrekeoe" and key=3
	2. *Block (single columnar) Transposition cipher*
		- Step 1: First we write the message in the form of rows and columns, and read the message column by column.
		- Step 2: Given a keyword, which we will use to fix the number of rows.
		- Step 3: If any space is spared, it is filled with null or left blank or in by (_).
		- Step 4: The message is read in the order as specified by the keyword.
		
			- ![[Pasted image 20241013165639.png]]
			- Cipher Text = IAN_RNANS_J_KHRA
	3. *Double columnar transposition cipher*
		-  It is similar to columnar transposition it perform the operation twice with same key or different keys.
		- Step 1: Follow same steps that are performed on single columnar transposition to generate the cipher text 
		- Step 2: provide the cipher text as input and follow the step 1
		- ![[Pasted image 20241013184658.png]]
		- Transposition 1 intermediate
		- ![[Pasted image 20241013184802.png]]

	- **Substitution Cipher** - The character in a text(plain text) substituted with other character to make the plain text as cipher text this process is called substitution cipher.
		- Caesar cipher
		- Mono alphabetic cipher
		- Poly alphabetic cipher 
		
	1. *Caesar cipher*
		- Encryption = $$ C= (P+k) \mod{26}$$
		- where ,
			- C is the cipher text
			- P is the plain text
			- K is the shift key

		- Decryption = $$ P=(C-k) \mod{26} $$
	2. *Feistel cipher*:
		- It is a design model from which many different block cipher are derived.It is not a specific encryption algorithm
		- DES is an example of Feistel cipher.
		- It use same algorithm for both encryption and decryption.
		- STEPS
			1. convert the plain text to ASCII code of each character 
			2. Split the plain text into two equal halves L0 and R0
			3. It under go 'n' times execution and each pass it use the same encryption function and different sub key from master key
			4. L(i+1)=R(i) and R(i+1)=F xor Li
			5. Encryption =$$ L_i+1 =R_i \\     R_i+1=L_i xor  F(R_i,K_i) $$
			7. After the last round combine Ln and Rn
			8. Decryption = $$ R_i =L_i+1 \\ L_i =R_i+1 xor F(L_i+1,K_i) $$
		- ![[Pasted image 20241013193725.png]]

	- **RSA algorithm**
		- RSA is an asymmetric Cryptographic algorithm used for secure data transmission.It use a pair of keys: public(Encryption) and private keys(Decryption).
		- P,Q are the large prime numbers 
		- $$n = P*Q$$
		- $$\phi(n)=(P-1)*(Q-1)$$
		- e is the smallest prime number satisfies the following conditions $$ \gcd(e,\phi(n)) =1 ,1<e<\phi(n) $$
		- $$d=(\phi(n)+1)/e$$
		- Encryption Formula = $$ M^e \mod{n} $$
			- where , M -Message(plain text)
		- Decryption Formula =$$ C^d \mod{n} $$

	- **HMAC(Hash-based message authentications code)**:
		- It is cryptographic algorithm that combines a Cryptographic hash function(SHA-256 MD5 etc) and secret key to generate a message authorization cod(MAC).
		- **SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, and SHA-512/256**
		- It verify both *data integrity* and *authenticity*.
		- Key Components:
			1. Message
			2. secret key
			3. Cryptographic Hash function
			4. Block size(SHA-256 has 64 bytes of block size(512 bits),SHA-)
			5. Output length(L) - for SHA-256 output length is 256 bits
			6. Inner padding(ipad) - `0x36` is XORed with the key in the inner hash function.
			7. Outer padding(opad) - `ox5c` is XORed with the key in the outer hash function.
			
			- $HMAC(K,M)= H((K \oplus opad)|| H((K \oplus ipad)|| M))$
			- $inner\_hash =H((K \oplus ipad )||M)$
			- $outer\_hash =H((K \oplus opad) || inner\_hash)$
			- where,
				- || -concatenation
				- $\oplus$ - xor
			9. Output is 256 bit message authentication code(MAC)
			
			- ![[Pasted image 20241014123417.png]]
			
		- Application:
			- MAC in API call 
			- TLS and SSL
			- JWT(JSON WEB TOKEN)
		- Features
			- Data integrity
			- security
			- Resistance to length extension attack


	- **Key Management & Exchange**
	
		- *Key Exchange and Key Management are crucial process in cryptography that ensure the secure generation,distribution,storage and disposal of Cryptographic
	
	1. **KEY MANAGEMENT:**
		- It refers to the complete lifecycle  Management of Cryptographic keys in Cryptographic system.It involve the following phase
			- Key Genearation
			- Key Storage
			- Key Distribution
			- Key Usage
			- Key Rotation
			- Key Revocation
			- Key Archival and destruction
		- Purpose of Key Management
			- CIA 
			- Authenticity
		- **Real time application:**
			- AWS and Azure offer services for key Management,including the ability to Genearate,store and manage Encryption.
			- `Ex` AWS key Management services(KMS)
	
	2. **KEY EXCHANGE**
	
		- It is the process of securely exchanging Cryptographic keys b\w two or more parities ,enabling them to communicate securely over an untrusted network.
		- It is particularly Important in symmetric key encryption because a common key is shared b/w two users.
		- The main idea is to share the key or Exchange without being intercepted by a malicious third party.
		
		- Types of key Exchange:
			- Symmetric key Exchange
			- Asymmetric key Exchange
			
		- Common Key Exchange
			- *Diffie-Hellman(DH) key Exchange:*
				- This algorithm allows two parities to generate a secret key over an insecure channel without sharing the actual key,
				- $g^a \mod{p} \;and \;g^b \mod{p}$ 
				- a&b - private values ,g&p - public values
			- *Elliptic Curve Diffie-Hellman(ECDH):*
				- It is a variation of Diffie-Hellman that combine Elliptic Curve cryptography
				- It is key-agreement protocol that allows two parites to establish a share secret over an insecure channel.
				- In this users know the public key before the execution of the protocol.
				- It involve two steps key generation and secret key calculation.
				- Key Generation:
					- Private key -> $1 \;to\; n_o -1$
					- Public Key  ->$P =nG$
				
			- *RSA key exchange:*
				- RSA can also be used for key exchange.
				- A party can encrypt a symmetric key with the recipient's public key and only the recipient can decrypt it using their private key.
				- It follow the same encryption and decryption algorithm used in RSA 
				- The sender generate the symmetric key to encrypt and decrypt the data.After that the sender use the receivers public key of asymmetric algorithm to encrypt the actual public key and sent it securely to receiver .The receiver then decrypt it using private key and use the actual public key.
				
				1. Security of symmetric key distribution
				2. Foundation of secure communication protocols
				3. Asymmetric Encryption efficiency.
			- `example:`
				- Real time use case: HTTPs( secure web browsing)
				- Virtual Private Networks(VPNs)

	3.  **DIGITAL SIGNATURE**
	
		- It is used to verify the authenticity and integrity of a message,s/w or Digital documents.
		- It is a public key cryptography.
		- The sender encrypt the raw data using his/her own private key and send it to receiver and then the receiver decrypt it using sender public key.
		- The encryption and decryption are opposite to normal one.
		- In this once the documents is digitally signed it has been sent to receiver cant stop
		
		- **Steps**
		
		- *Sender side:*
			- Generate the hash value of raw data 
			- Encrypt the data using the sender private key.
			- Send it to receiver
		- *Receiver side:*
			- The receiver decrypt the encrypted data using sender public key 
			- Compare the hash value obtain from decryption and the hash value present in the receiver end.If both are same data integrity is being maintained else it has been tampered.
			
		- Key Components:
			- Hash function (MD5,SHA-256)
			- Signing algorithm (RSA,DSA ,ECDSA)
			- Verification algorithm
			
		- Need for digital signature
			- Authentication
			- Integrity
			- Non repudiation
			- Confidentiality
		
		- Types of breaking a digital Signature:
			- Key only attack
			- Known message attack
			- Adaptive chosen message attack

		- **Direct Digital Signature:**
			- DDS involves the use Cryptographic algorithm like RSA to directly signed with the private key of the sender  and the receiver can verify the Signature using the sender public key.
			- In which the both parties trust each other 
			- It is prone to get corrupted
			- The sender can decline the message sent by him at any time but not possible in Digital Signature.
			- ![[Pasted image 20241014181728.png]]
			- Advantages:
				- Simplicity
				- Speed
				- security
			- Disadvantages:
				- Limited scope
				- lack of impartiality
			
		- Elgamal Digital Signature scheme:
			- It is an asymmetric key encryption algorithm for digital Signature based on the Elgamal encryption system and Diffie-Hellman key exchange.
			- ![[Pasted image 20241014185452.png]]

		- Schnorr Digital Signature Scheme
			- The **Schnorr Digital Signature Scheme** is an efficient signature algorithm based on the hardness of computing discrete logarithms. It’s known for being simpler and faster than many other algorithms.

		- Types of Attack:
			- Forgery attack
			- Replay attack
			- Chosen message attacks
			- Key substitution attacks

		- Use cases of Digital Signature in real life:
			- Email security- Pretty Good Privacy(PGP)
			- Documents signing
			- SSL/TLS in web security  
			- Blockchain and cryptocurrency

---
---
## Unit 3 INTRODUCTION TO ASSURANCE & EVALUATING system


>Assurance and Trust – Building secure and trusted systems: Life cycle, Waterfall life cycle model, Prototyping –
Evaluating Systems: Role of formal evaluation, TCSEC requirements, classes, processes, impact. FIPS requirements,
Security levels, impact

**1.ASSURANCE & TRUST:**

- *Assurance*
	- It is the degree of confidence that a system's security and operational objectives are being met.
	-  Trust cannot be quantified precisely.System specification,design and implementation can provide a basic for determining "how much" to trust a system.This aspect of trust is called **assurance**.
	- Security assurance or assurance is the confidence that an entity meets its security requirements ,based on specific evidence provided by the application of assurance techniques.
	- Information assurance refers to the ability to access information and preserve the quality of that information.
	- Assurance techniques *informal,semiformal,formal*
	- Designing and implementing system with assurance requires that every step of the process involves appropriate level of assurance 
	- It provide a system with assurance(promise or confidence on s/w)
	
	-   `objective` *Assurance aims to provide evidence that a system is free from vulnerabilities, operates reliably, and protects the confidentiality, integrity, and availability (CIA) of data.*
	
	- *Needed for assurance:*
	- *Assurance requirement*
	
	- Assurance Throughout the Life cycle
		- ![[Pasted image 20241015102542.png]]
	
	- Methods of Achieving Assurance:
		- Formal Verification
		- Testing
		- Audits and Assessments
	
- **TRUST**
	- Trust refers to the confidence that stakeholders(users,operators,administrator ) place in the system's behavior and its ability to operate securely.
	- Trust is built by ensuring transparency in the system design,operation ,robust security measures such as encryption ,access control and authentication.
	- It is an Important concept because it determine how much faith user have in the safety ,reliability and integrity of a system,application or network.
	- Maintaining the system properly is not only provide trust on user we also ensure some aspects like
		- Data integrity
		- Confidentiality
		- Availability
		- Authenticity
		
	- Steps to build trust in a system:
		- Design for security and Privacy
		- Authentication and Authorization
		- Auditability and transparency
		- Security Testing
		- Third party validation
		- Ongoing monitoring and incident response.


2. **BUILDING SECURE & TRUSTED SYSTEMS**
	- It is complex process involve implementation of security practices on each stages of SDLC
	- Key phase in build a secure systems:
		- *Requirements analysis* 
			- functional requirements like data encryption
		- *Design and Architecture* 
			- design architecture of system to met up with requirements and security
			- design a system with layered architecture to defense in every layer 
		- *Implementation:*
			- Secure coding practices and principles are applied during the s/w development.
			- Avoid the deprecated or easily crackable algorithm in security places. 
		- *Testing and Verification*
			- Test the software before deployment 
			- Perform assessment in software to find vulnerabilites
			- Testing of different attacks
		- *Deployment and operation*
			- After deployment continuous analysis of security issues and patches for that is necessary.
			- Update frequently
		- *Maintenance and Decommissioning*
			- Proper security maintenance for system
			- Secure decommissioning(removing or destroying) of files and information from hardware 

	- **System Development Life Cycle(SDLC):**
		- It is a framework that outline various stages involved in system development ,ensuring that security is incorporated from the outset.
		- Key phase:
			 - Planning,Analysis,Design,Implementation,
			 - Testing,Deployment and Maintenance

	- **WATERFALL LIFE CYCLE MODEL**
		- It is one of the oldest and simplest SDLC model ,
		- It follows a linear ,sequential design process where each phase must completed before moving on to the next phase .
		- It move downward like a waterfall after completing every steps in each stage.
		- Key phases:
			- Requirements
			- Design
			- Implementation
			- Testing
			- Deployment
			- Maintenance(aka *fielding the system*)
			
			 ![[Pasted image 20241015115159.png]]

	- **Other SDLC models**
		- Exploratory Programming 
			- This approach is used in AI system development ,in which the user not need to formulate the requirements.
			- In this method their is no requirements and design phases
			- It is not secure compare to Waterfall model.
		- Prototyping
			- It is similar to Exploratory programming in which the software or application is developed at first phase and later on changes and modification done over on it.
			- 
		








