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
		- *Purpose:* steal data,create backdoor ,redirect traffic and monitor activity,delete filesu
		
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
	- `Eg:` bios is a middleware b/w os and hardware.

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
- Strong tranquility - subject and object and compartment do not change 
- weak tranquility - subject or object and compartments don't change 
[confidential policy](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.rose-hulman.edu/class/cs/csse442/current/notes/CIPoliciesNotes.pdf&ved=2ahUKEwib9vS40NCIAxXiSWwGHRvDLskQFnoECBwQAQ&usg=AOvVaw0T-3oZBdQ01KNkkZB_1BMC)


### Chain Wall Model for Hybrid Policies

The **Chain Wall Model** in the context of hybrid policies refers to the concept of building multiple layers of defense, much like the walls of a fortress, to secure an organization's information assets. Each layer or "wall" represents a different type of security policy—preventive, detective, and corrective—that together form a cohesive and robust security framework.

In this model, no single wall is considered invulnerable, but by layering different security controls, the combined protection becomes much stronger, making it more difficult for an attacker to penetrate the entire system. This is akin to the concept of **"defense in depth"** where multiple barriers are placed in sequence, requiring an attacker to overcome each layer to breach the system.

#### **Key Elements of the Chain Wall Model:**

1. **Preventive Wall**:
    
    - Policies that are designed to prevent security breaches from happening in the first place.
    - Examples: Encryption, multi-factor authentication (MFA), firewalls, access controls.
2. **Detective Wall**:
    
    - Policies that detect any breach attempts or unauthorized access, ideally in real-time.
    - Examples: Intrusion detection systems (IDS), security monitoring, anomaly detection.
3. **Corrective Wall**:
    
    - Policies that help mitigate damage and recover from breaches or security incidents.
    - Examples: Incident response plans, disaster recovery, patch management.
4. **Operational Wall**:
    
    - Policies governing the day-to-day secure operation of the system.
    - Examples: Backup policies, system maintenance, and user behavior controls.

By creating a sequence of these walls, organizations can significantly strengthen their overall security posture, ensuring that if one wall is breached, the others can still protect the system.

### Integrity Policy: Biba Model

The **Biba Integrity Model** is one of the most recognized models for ensuring data integrity in a secure system. Unlike confidentiality models such as Bell-LaPadula (focused on preventing unauthorized access to data), the Biba model is designed to prevent unauthorized or improper modification of data.

#### **Key Concepts of the Biba Model:**

- The Biba model operates under the principle that users or subjects should not write data to a higher integrity level than they are cleared for, and they should not read data from a lower integrity level.
- **Main Goal**: Prevent data from being corrupted or altered by unauthorized individuals or processes.

#### **Biba’s Integrity Principles**:

1. **Simple Integrity Axiom (No Write Up)**:
    
    - A subject (user or process) cannot write to an object (data) at a higher integrity level than the subject’s own integrity level.
    - **Purpose**: This prevents lower-trust entities from corrupting higher-trust data.
    - **Example**: A junior staff member cannot update financial reports that only senior staff should have access to.
    - Si​ can write to Oj​⟺I(Si​)≥I(Oj​)
    
1. **Star Integrity Axiom (No Read Down)**:
    
    - A subject cannot read from a lower integrity level.
    - **Purpose**: This prevents higher-trust entities from being influenced by less trustworthy or corrupted data.
    - **Example**: An administrator cannot rely on unverified or untrusted logs that might contain false information from lower-level systems.
    - Si​ can read from Oj​⟺I(Si​)≤I(Oj​)
    
1. **Invocation Property (No Execute Up)**:
    
    - A subject at a lower integrity level cannot invoke (call or execute) a subject or program at a higher integrity level.
    - **Purpose**: This prevents untrusted users from executing privileged operations or commands.
    - Si​ can invoke Pj​⟺I(Si​)≥I(Pj​)

#### **Example of Biba Model in Use**:

Imagine an organization with multiple security levels for data integrity—such as "High," "Medium," and "Low":

- A **high-trust** subject (like a system administrator) can only read from high-trust data sources and cannot read or be influenced by lower-trust data (to avoid misinformation).
- A **low-trust** subject (like a user with limited access) cannot write data to higher-trust systems (e.g., production databases) to avoid corruption of critical information.

In practice, the Biba model helps maintain **data integrity** by ensuring that only trusted, authorized individuals and processes can modify sensitive data, and that higher integrity levels are not corrupted by lower-integrity input.

### **Integrity vs. Confidentiality:**

- The **Bell-LaPadula Model** focuses on **confidentiality**, ensuring that unauthorized individuals cannot access sensitive information ("no read up, no write down").
- The **Biba Model** focuses on **integrity**, ensuring that unauthorized or untrusted sources cannot modify critical data ("no write up, no read down").

---

### **Real-World Example of Biba Model**:

In a **government agency** managing classified documents, integrity is critical. If a **low-level employee** could modify high-level, classified documents, it could lead to unauthorized or malicious alterations. The Biba model ensures that:

- Low-level employees cannot **modify** classified documents.
- Higher-level employees cannot **read** unclassified or unreliable data that may contaminate decision-making

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
		- Digital/Data Encryption Standard (DES),AES (Advance Encryption  Standard),3DES,IDEA(International Data Encryption Algorithm) & BLOWFISH,Twofish,Threefish
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
		- It is cryptographic algorithm that combines a Cryptographic hash function(SHA-256 MD5 etc) and secret key to generate a message authorization code(MAC).
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

### Prototyping

**Definition**:  
Prototyping involves creating an early model of a system to explore ideas, validate requirements, and refine functionalities. It allows stakeholders to visualize, interact with, and provide feedback on a system before full-scale development.

---

#### **Steps in Prototyping**:

1. **Requirement Identification**:  
    Understand and document the key requirements of the system from users or stakeholders.
    
2. **Initial Prototype Development**:  
    Develop a basic, incomplete version of the system, focusing on core functionalities.
    
3. **User Interaction and Feedback**:  
    Present the prototype to users and gather feedback on usability, features, and performance.
    
4. **Refinement**:  
    Use the feedback to improve and add features to the prototype iteratively.
    
5. **Final Prototype Validation**:  
    Once the prototype meets expectations, validate it before starting full-scale development.
    

---

#### **Types of Prototypes**:

1. **Throwaway Prototype**:  
    A quick, disposable model to explore ideas. It is not part of the final system.
    
2. **Evolutionary Prototype**:  
    A continuously refined prototype that evolves into the final system.
    
3. **Incremental Prototype**:  
    Developed in increments, each focusing on specific system components.
    
4. **Extreme Prototyping**:  
    Used in web applications, with three phases: static mockups, functional screens, and integration.
#### **Benefits of Prototyping**:

- Improved understanding of user needs.
- Early detection of design flaws.
- Enhanced communication between stakeholders and developers.
- Cost and time savings by addressing issues early.

#### **Challenges in Prototyping**:

- Over-reliance on the prototype as the final product.
- Increased development time if iterations are excessive.
- Users may focus on aesthetic aspects over functionality.


---

### **Evaluating Systems**

**Definition**:  
System evaluation is the process of assessing a system's functionality, performance, and usability against predefined criteria to ensure it meets requirements

#### **Role of Formal Evaluation**:

1. **Verification**:  
    Ensures the system works as intended and complies with specifications.
    
2. **Validation**:  
    Confirms that the system meets user requirements and expectations.
    
3. **Performance Assessment**:  
    Measures system efficiency, speed, and reliability under various conditions.
    
4. **Security Assurance**:  
    Evaluates system resilience against threats and vulnerabilities.
    
5. **User Satisfaction**:  
    Assesses how well the system aligns with user needs and ease of use.
    

---

#### **Steps in Formal Evaluation**:

1. **Define Evaluation Criteria**:  
    Establish metrics like performance, reliability, and usability.
    
2. **Develop Evaluation Plan**:  
    Identify test cases, tools, and methods to evaluate the system.
    
3. **Perform Tests**:  
    Execute tests under controlled conditions to gather data.
    
4. **Analyze Results**:  
    Compare the system's performance against benchmarks or standards.
    
5. **Feedback and Recommendations**:  
    Use findings to improve or validate the system.

### **TCSEC Requirements, Classes, Processes, and Impact**

---

#### **What is TCSEC?**

**Trusted Computer System Evaluation Criteria (TCSEC)**, also known as the **Orange Book**, is a standard used for evaluating and classifying computer systems based on their security features and assurance levels. It was developed by the U.S. Department of Defense in 1983.

---

#### **TCSEC Classes**

The TCSEC defines four major classes, each with increasing levels of trust:

1. **D – Minimal Protection**
    
    - Systems that do not meet the requirements of higher classes.
    - **Example**: Basic personal computers without specialized security features.
2. **C – Discretionary Protection**
    
    - **C1 – Discretionary Security Protection**:  
        Basic access controls, ensuring users can protect their data.  
        **C2 – Controlled Access Protection**:  
        Stronger access control mechanisms and auditing.
        - **Example**: Multi-user systems with password protection.
3. **B – Mandatory Protection**
    
    - **B1 – Labeled Security Protection**:  
        Each data object has a label specifying security clearance levels.
    - **B2 – Structured Protection**:  
        More stringent security controls and less reliance on individual trust.
    - **B3 – Security Domains**:  
        Includes advanced security mechanisms for high assurance.
    - **Example**: Military systems requiring clearance levels.
4. **A – Verified Protection**
    
    - Systems that are formally verified to meet the highest security standards.
    - **Example**: High-security government or defense applications.

---

#### **Processes in TCSEC**

1. **Security Policy**:  
    Establish a clear policy for access control and system operation.
    
2. **Accountability**:  
    Ensure all system actions are attributable to specific users or processes.
    
3. **Assurance**:  
    Evaluate the system for its ability to enforce security policies reliably.
    
4. **Documentation**:  
    Maintain detailed documentation of system design, operation, and evaluation.
    

---

#### **Impact of TCSEC**

- **Improved Security Standards**: Systems adhering to TCSEC ensure better protection of sensitive data.
- **Defense Applications**: Widely used for military and government systems.
- **Global Influence**: Inspired similar standards, such as the Common Criteria.
- **Limitations**: Criticized for being too rigid and focused on specific use cases.


### **FIPS Requirements, Security Levels, and Impact**

---

#### **What is FIPS?**

**Federal Information Processing Standards (FIPS)** are U.S. government standards for cryptographic modules, ensuring secure processing and handling of sensitive information.

---

#### **FIPS 140-2 Security Levels**

FIPS 140-2, a widely recognized standard for cryptographic modules, defines four security levels:

1. **Level 1 – Basic Security**
    
    - Software-only cryptographic modules.
    - No physical security requirements.
    - **Example**: General-purpose encryption software.
2. **Level 2 – Enhanced Security**
    
    - Requires tamper-evident physical components and role-based authentication.
    - **Example**: Smartcards.
3. **Level 3 – High Security**
    
    - Adds tamper-resistance mechanisms.
    - Cryptographic keys are encrypted.
    - **Example**: Secure hardware tokens.
4. **Level 4 – Maximum Security**
    
    - Protects against environmental attacks (e.g., voltage, temperature changes).
    - **Example**: High-assurance cryptographic hardware for defense.

---

#### **FIPS Requirements**

1. **Approved Algorithms**:  
    Only FIPS-approved cryptographic algorithms (e.g., AES, SHA) are used.
    
2. **Key Management**:  
    Strong mechanisms for key generation, distribution, and storage.
    
3. **Testing and Validation**:  
    Modules must undergo testing by accredited labs.
    
4. **Auditing**:  
    Maintain logs for monitoring and detecting unauthorized access.
    

---

#### **Impact of FIPS**

1. **Government Compliance**:  
    Mandated for U.S. federal agencies handling sensitive data.
    
2. **Industry Adoption**:  
    Widely adopted in industries like finance and healthcare.
    
3. **Improved Trust**:  
    Ensures systems meet rigorous security standards.
    
4. **Global Recognition**:  
    Used internationally, especially in regions influenced by U.S. standards.



---
---
>**UNIT-IV AUDITING AND NETWORK SECURITY**
Auditing: Anatomy of an auditing system, Designing an auditing system, auditing mechanisms. Network Security:
Introduction, Policy Development, Network Organization anticipating attacks.


### **Auditing in System Security**

Auditing in system security is a systematic approach to monitoring, recording, and analyzing system activities. It ensures that systems comply with security policies, regulations, and standards. Auditing provides accountability by tracing user activities, detecting unauthorized access, and enabling system administrators to respond to potential breaches effectively.

---

### **Anatomy of an Auditing System**

The anatomy of an auditing system describes its structural and functional components, which work together to ensure robust monitoring and reporting of system activities.

---

#### **Key Components of an Auditing System**

1. **Audit Logs**:
    
    - **Definition**: A detailed record of events or activities occurring within a system.
    - **Contents**:
        - **Timestamps**: Indicate when an event occurred.
        - **User IDs**: Identify the user or system process responsible for the action.
        - **Event Types**: Specify the nature of the event, such as login attempts, file access, or configuration changes.
    - **Purpose**: Provide a granular view of system activities, enabling administrators to track and verify user actions.
    - **Example**: Logging every time a user logs in, creates, modifies, or deletes a file.
2. **Audit Trails**:
    
    - **Definition**: Chronological records that provide a complete sequence of user and system actions.
    - **Purpose**: Allow reconstruction of events to determine how and why incidents occurred.
    - **Example**: Tracking who accessed a specific database, what changes were made, and when they were implemented.
3. **Event Filters**:
    
    - **Definition**: Rules or criteria specifying which activities or events should be monitored and recorded.
    - **Purpose**: Focus on critical events to reduce noise in audit logs and improve efficiency.
    - **Example**: Configuring filters to log only failed login attempts or unauthorized file access.
4. **Data Storage**:
    
    - **Definition**: Mechanisms to securely store audit logs and trails for analysis, reporting, and compliance.
    - **Best Practices**:
        - Encrypt stored logs to prevent tampering.
        - Implement retention policies to ensure logs are kept for the required duration.
    - **Example**: Storing audit logs in a centralized, secure server accessible only to authorized personnel.
5. **Analysis Tools**:
    
    - **Definition**: Software or algorithms used to process and analyze audit logs for anomalies, patterns, or trends.
    - **Purpose**: Automate the detection of suspicious activities, reducing manual effort and improving accuracy.
    - **Example**: Using machine learning models to flag unusual login locations or patterns.
6. **Reporting Mechanisms**:
    
    - **Definition**: Tools for generating summaries or detailed reports of audit findings.
    - **Purpose**: Provide actionable insights for stakeholders, such as system administrators, compliance officers, or executives.
    - **Example**: Monthly compliance reports highlighting unauthorized access attempts or configuration changes.

---

#### **Purpose of an Auditing System**

1. **Detection of Unauthorized Activities**:
    
    - Detect potential breaches, policy violations, or misuse of resources.
    - Example: Identifying multiple failed login attempts as a potential brute-force attack.
2. **Ensuring Compliance**:
    
    - Verify adherence to industry regulations, such as:
        - **GDPR (General Data Protection Regulation)**: Protects personal data in the EU.
        - **HIPAA (Health Insurance Portability and Accountability Act)**: Ensures confidentiality of healthcare data.
        - **SOX (Sarbanes-Oxley Act)**: Regulates financial record-keeping in the U.S.
3. **Incident Investigation and Forensics**:
    
    - Reconstruct events to determine the cause and scope of security incidents.
    - Example: Analyzing audit trails to identify how a malware infection spread across the network.
4. **Accountability and Deterrence**:
    
    - Hold users accountable for their actions, discouraging unauthorized activities.
    - Example: Knowing activities are logged reduces the likelihood of insider threats.

---

#### **Use Case: Auditing System in Action**

**Scenario**:  
A financial services company needs to ensure secure handling of sensitive customer data and prevent unauthorized access to financial records.

**Implementation**:

1. **Audit Logs**: Track every administrative login, data access, and modification.
2. **Audit Trails**: Maintain a chronological record of all transactions for regulatory compliance.
3. **Event Filters**: Monitor activities like failed login attempts or changes to access permissions.
4. **Data Storage**: Store logs securely with encryption and retention policies aligned with compliance requirements.
5. **Analysis Tools**: Use anomaly detection to flag unusual behavior, such as an administrator accessing data outside business hours.
6. **Reporting Mechanisms**: Generate compliance reports for regulatory authorities.

**Outcome**:  
The auditing system detects an administrator attempting to access customer data at unusual hours, triggering an alert and preventing potential misuse.


---
---
#### **Designing an Auditing System**

Designing an auditing system involves identifying objectives, defining scope, and implementing tools to achieve effective monitoring and compliance.

1. **Steps in Designing an Auditing System**:
    
    - **Requirement Analysis**:
        - Identify compliance standards and security goals (e.g., PCI DSS, ISO 27001).
        - Determine what activities need monitoring.
    - **Define Audit Policies**:
        - Specify actions to log, like failed login attempts or changes to critical files.
        - Ensure policies cover all critical areas of the system.
    - **Tool Selection**:
        - Choose tools for logging and analysis (e.g., Splunk, Elastic Stack).
    - **Implementation**:
        - Configure logging mechanisms and set up alert systems.
        - Secure audit logs to prevent tampering.
    - **Testing and Validation**:
        - Test the system to ensure all required events are logged accurately.
        - Validate that alerts are triggered for policy violations.
    - **Periodic Review**:
        - Update policies and tools based on evolving threats and compliance needs.
2. **Example Use Case**:
    
    - A financial institution designs an auditing system to monitor transactions over a certain amount, flagging them for manual review to detect potential fraud.
---
---
#### **Auditing Mechanisms**

Auditing mechanisms are the methods and tools used to collect, analyze, and report data about system activities.

1. **Types of Auditing Mechanisms**:
    
    - **File Integrity Monitoring (FIM)**:
        - Detects unauthorized changes to critical system files.
    - **User Activity Monitoring (UAM)**:
        - Tracks user actions, including logins, command executions, and resource access.
    - **Network Auditing**:
        - Logs network activity to detect unusual traffic or unauthorized connections.
    - **Application Auditing**:
        - Monitors application-level activities, such as database queries and API calls.
    - **Access Auditing**:
        - Logs access attempts to systems, files, and applications.
    - **Post-Incident Auditing**:

		- Analyzes logs to investigate and respond to security incidents.
		- Example: Reconstructing events leading to a data breach.
		
1. **Automation Tools**:
    
    - **SIEM (Security Information and Event Management)**:
        - Centralized analysis and correlation of logs from multiple sources.
        - Example tools: Splunk, IBM QRadar, and ArcSight.
    - **Intrusion Detection Systems (IDS)**:
        - Detect suspicious patterns indicating potential security breaches.
3. **Challenges in Auditing**:
    
    - **Data Volume**:
        - Large systems generate immense amounts of log data, making analysis challenging.
    - **False Positives**:
        - Alerts for benign activities can lead to alert fatigue.
    - **Log Integrity**:
        - Logs must be protected against tampering.
4. **Use Case**:
    
    - An e-commerce platform uses a network auditing mechanism to detect unusual traffic spikes indicative of DDoS attacks.

---
---
### **Network Security**

Network security encompasses policies, processes, and technologies designed to protect network infrastructure, data, and resources from unauthorized access, misuse, or attacks.

---

#### **Introduction to Network Security**

1. **Definition**:
    
    - The practice of safeguarding a computer network and its data from breaches, intrusions, and other malicious activities.
2. **Objectives**:
    
    - **Confidentiality**: Ensure data is accessible only to authorized users.
    - **Integrity**: Protect data from unauthorized modifications.
    - **Availability**: Ensure network services are available when needed.
3. **Components of Network Security**:
    
    - **Physical Security**: Securing network devices against physical threats.
    - **Access Control**: Restricting network access to authorized users/devices.
    - **Firewalls**: Monitor and control incoming and outgoing network traffic.
    - **Encryption**: Protect data in transit from eavesdropping.
    - **Intrusion Detection/Prevention Systems (IDS/IPS)**: Detect and block malicious activities.
4. **Use Case**:
    
    - An organization deploys firewalls and VPNs to ensure secure remote access for employees.


### **Policy Development in Network Security**

Network security policies are critical for defining the rules, procedures, and mechanisms to protect an organization’s network and data. These policies ensure that all network activities align with the organization’s security objectives, regulatory requirements, and operational goals.

---

#### **Steps in Policy Development**

1. **Requirement Gathering**:
    
    - Identify security needs by understanding:
        - The organization’s mission and goals.
        - Compliance requirements (e.g., HIPAA, GDPR).
        - Industry best practices.
        - Results from risk assessments, which highlight vulnerabilities and threats.
    - Example: A financial institution may prioritize securing customer transaction data.
2. **Define Access Controls**:
    
    - Determine user roles and permissions:
        - Role-Based Access Control (RBAC): Assign permissions based on user roles (e.g., admin, user).
        - Principle of Least Privilege (PoLP): Limit access to only what is necessary for a user’s job.
    - Specify authentication mechanisms:
        - Two-Factor Authentication (2FA).
        - Biometric authentication.
    - Example: System administrators have access to critical servers, while employees access only their departmental data.
3. **Specify Security Measures**:
    
    - Define technical and procedural safeguards:
        - **Firewalls**: Filter traffic to block unauthorized access.
        - **Intrusion Detection/Prevention Systems (IDS/IPS)**: Detect and prevent malicious activities.
        - **Encryption Protocols**: Protect data in transit (e.g., TLS, VPNs).
        - **Incident Response Plans**: Procedures for identifying, containing, and mitigating security breaches.
        - **Backup and Recovery Plans**: Regular backups ensure data recovery in case of incidents.
4. **Implementation**:
    
    - Deploy security tools and solutions (e.g., firewalls, endpoint protection).
    - Educate users about security policies and practices:
        - Conduct training on phishing awareness, password hygiene, and reporting suspicious activities.
5. **Review and Update**:
    
    - Regularly review policies to address:
        - Emerging threats (e.g., new malware variants).
        - Changes in technology (e.g., adoption of cloud computing).
        - Updates to regulatory requirements.
    - Example: A company revises its BYOD policy to include security requirements for wearable devices.

---

#### **Types of Network Security Policies**

1. **Acceptable Use Policy (AUP)**:
    
    - Defines appropriate use of network resources (e.g., internet, email).
    - Examples:
        - Prohibit access to malicious or inappropriate websites.
        - Disallow the use of personal cloud storage for work files.
2. **Remote Access Policy**:
    
    - Establishes guidelines for secure remote connectivity.
    - Examples:
        - Require VPN usage for remote access.
        - Prohibit saving sensitive data on personal devices.
3. **Bring Your Own Device (BYOD) Policy**:
    
    - Outlines rules for using personal devices on the corporate network.
    - Examples:
        - Enforce device encryption.
        - Require mobile device management (MDM) solutions.

---

#### **Use Case**

**Scenario**: A healthcare organization aims to ensure patient data security during electronic transmissions.  
**Policy Action**:

- Enforce encryption for all data transfers using protocols like HTTPS and Secure File Transfer Protocol (SFTP).
- Require endpoint security for devices accessing patient records remotely.  
    **Outcome**: Compliance with HIPAA and enhanced protection against data breaches.

---

### **Network Organization and Anticipating Attacks**

Network organization involves structuring a network to optimize security, efficiency, and scalability while anticipating and mitigating potential attacks.

---

#### **Network Organization**

1. **Segmentation**:
    
    - Dividing a network into smaller, isolated segments to limit the spread of breaches.
    - **Techniques**:
        - Virtual Local Area Networks (VLANs): Separate internal departments like HR, IT, and Finance.
        - Subnetting: Divide IP address ranges to improve traffic management.
    - **Example**:
        - A manufacturing company segments its operational network (controlling equipment) from the corporate network (handling employee emails).
2. **Defense in Depth**:
    
    - Employing multiple layers of security to protect against different attack vectors.
    - **Layers**:
        - Perimeter Security: Firewalls and VPNs.
        - Internal Security: IDS/IPS and access controls.
        - Endpoint Security: Antivirus and patch management.
    - **Example**: Combining endpoint protection with network monitoring tools to detect insider threats.
3. **Redundancy and Failover**:
    
    - Implementing backup systems to ensure network reliability and minimize downtime during failures.
    - **Techniques**:
        - Backup Servers: Maintain real-time replicas of critical systems.
        - Load Balancers: Distribute traffic across multiple servers to prevent overload.
    - **Example**: An e-commerce platform uses redundant data centers to stay operational during outages.

---

#### **Anticipating Attacks**

1. **Common Network Threats**:
    
    - **Distributed Denial of Service (DDoS)**:
        - Overloading a network with excessive traffic to disrupt services.
        - **Example**: An attacker floods an online retailer’s website during a sale, causing downtime.
    - **Man-in-the-Middle (MITM) Attacks**:
        - Intercepting and altering communications between two parties.
        - **Example**: An attacker intercepts login credentials during a public Wi-Fi session.
    - **Phishing and Social Engineering**:
        - Trick users into divulging sensitive information (e.g., login credentials).
        - **Example**: Employees receive fake emails mimicking their IT department, asking for passwords.
2. **Proactive Measures**:
    
    - **Threat Modeling**:
        - Identify potential attack vectors and prioritize security measures.
        - **Example**: A bank models risks for mobile banking apps, focusing on account takeover attempts.
    - **Vulnerability Assessments**:
        - Conduct regular scans to identify and fix security gaps.
        - **Example**: A company scans its network for outdated software and unpatched vulnerabilities.
    - **Incident Response Plans**:
        - Define steps to detect, contain, and recover from attacks.
        - **Example**: A response plan for ransomware attacks includes isolating infected systems and restoring data from backups.

---

#### **Use Case**

**Scenario**: An e-commerce platform anticipates a surge in DDoS attacks during Black Friday sales.  
**Proactive Measures**:

- Deploy a Content Delivery Network (CDN) to distribute traffic across multiple servers.
- Implement rate-limiting to restrict excessive requests from individual IP addresses.
- Monitor network traffic in real time for anomalies.  
    **Outcome**: The platform remains operational despite increased attack attempts.



---
---
>**UNIT-V SYSTEM SECURITY, USER SECURITY AND PROGRAM SECURITY**
>
System Security: Introduction, Policy, Networks. User Security: Policy, Access, Processes. Program Security:
Introduction, Requirements and policy, Design, Refinement and Implementation.                                                                                                                        

### **System Security**

System security refers to the practices and technologies used to protect a computer system from unauthorized access, disruptions, or destruction of data and services. It encompasses a wide range of methods and tools to safeguard hardware, software, and data from cyberattacks and other threats.

---

#### **Key Areas of System Security**

1. **Introduction to System Security**
    - **Definition**: Ensuring the confidentiality, integrity, and availability (CIA) of systems and data.
    - **Goals**:
        - Protect sensitive information from unauthorized access (confidentiality).
        - Prevent unauthorized modifications to data (integrity).
        - Ensure systems and services are available to authorized users (availability).
    - **Common Threats**:
        - Malware (viruses, ransomware, trojans).
        - Unauthorized access (hacking, privilege escalation).
        - Denial-of-Service (DoS) attacks.
        - Insider threats.
    - **Components**:
        - Hardware security (physical devices).
        - Software security (applications, operating systems).
        - Data security (stored and transmitted information).

---

#### **Policy in System Security**

Policies serve as guidelines and rules to ensure secure system operation.

1. **Definition**: A set of formalized rules that define acceptable use, procedures, and practices for maintaining security.
    
2. **Types of Security Policies**:
    
    - **Access Control Policies**:
        - Rules governing who can access what resources.
        - Example: Role-Based Access Control (RBAC).
    - **Data Protection Policies**:
        - Guidelines for data encryption, backups, and retention.
    - **Incident Response Policies**:
        - Procedures for detecting, reporting, and responding to security breaches.
    - **Acceptable Use Policies**:
        - Rules for how users can interact with the system (e.g., no unauthorized software installations).
3. **Components**:
    
    - **Statement of Purpose**: Why the policy exists.
    - **Scope**: Systems, people, and data covered by the policy.
    - **Responsibilities**: Roles and duties of individuals or teams.
    - **Enforcement**: Consequences for non-compliance.
4. **Example Use Case**:
    
    - A company implements a policy requiring all employees to use multi-factor authentication (MFA) for system access, ensuring enhanced login security.

---

#### **Networks in System Security**

Network security focuses on protecting data during transmission and securing communication between systems.

1. **Definition**: Measures to safeguard the confidentiality, integrity, and availability of data in a network.
    
2. **Key Components**:
    
    - **Firewalls**: Filter incoming and outgoing traffic based on predefined rules.
    - **Intrusion Detection and Prevention Systems (IDPS)**:
        - Detect and block suspicious network activity.
    - **Encryption**:
        - Secures data in transit using protocols like SSL/TLS or IPsec.
    - **Access Controls**:
        - Restrict access to the network using authentication methods.
    - **Network Segmentation**:
        - Divide the network into isolated segments to limit the spread of attacks.
    - **VPNs (Virtual Private Networks)**:
        - Secure communication over public networks.
3. **Common Threats**:
    
    - **Man-in-the-Middle (MITM) Attacks**: Intercepting data between two systems.
    - **Phishing**: Deceptive attempts to steal sensitive information.
    - **DDoS (Distributed Denial-of-Service) Attacks**: Overloading the network with excessive traffic.
4. **Use Case**:
    
    - A financial institution uses network security measures like firewalls and encryption to protect online banking transactions.

---
---
### **User Security**

User security involves protecting the system from malicious or accidental actions by users that could compromise data, systems, or networks.

---

#### **Policy in User Security**

1. **Definition**: Policies are formalized rules and guidelines ensuring safe user behavior and system interaction.
2. **Examples of User Security Policies**:
    - Password Policies:
        - Require strong passwords (minimum length, complexity).
        - Enforce regular password changes.
    - Account Management:
        - Disable accounts for inactive users.
        - Ensure proper role-based access.
    - Multi-Factor Authentication (MFA):
        - Add layers of verification for user logins.
3. **Use Case**:
    - A company policy mandates MFA and auto-lock on idle user sessions, reducing the risk of unauthorized access.

---

#### **Access in User Security**

1. **Definition**: Controlling and monitoring user access to ensure only authorized individuals can interact with specific resources.
2. **Key Components**:
    - Authentication:
        - Verifies user identity (passwords, biometrics, MFA).
    - Authorization:
        - Determines user permissions based on roles (Role-Based Access Control - RBAC).
    - Auditing:
        - Tracks user activity to identify unauthorized actions.
3. **Example Use Case**:
    - Employees in an organization are granted access only to files necessary for their roles, adhering to the principle of least privilege.

---

#### **Processes in User Security**

1. **Definition**: Procedures and workflows ensuring secure user interaction with systems.
2. **Examples**:
    - User Education:
        - Train users on recognizing phishing attempts and secure practices.
    - Incident Response:
        - Outline steps users should follow when reporting suspicious activity.
3. **Use Case**:
    - A company sets up a helpdesk process for resetting forgotten passwords securely.
---
---
### **Program Security**

Program security focuses on ensuring software is designed, implemented, and maintained to prevent exploitation or misuse.

---

#### **Introduction**

1. **Definition**: The practice of building software that resists vulnerabilities, including bugs and malicious attacks.
2. **Goals**:
    - Protect software against unauthorized access and data breaches.
    - Ensure integrity and availability of program functions.

---

#### **Requirements and Policy in Program Security**

1. **Requirements**:
    - Adherence to secure coding practices.
    - Implement validation and error-handling mechanisms.
    - Use encryption for sensitive data.
2. **Policy**:
    - Define procedures for secure program design and maintenance.
    - Establish protocols for regular security updates and patches.
3. **Example Use Case**:
    - An e-commerce website implements input validation to prevent SQL injection attacks.

---

#### **Design, Refinement, and Implementation**

1. **Design**:
    - Follow security principles like modularity and minimal privilege.
    - Use threat modeling to anticipate potential vulnerabilities.
2. **Refinement**:
    - Perform code reviews and security audits during development.
    - Continuously test for vulnerabilities using tools like static and dynamic analysis.
3. **Implementation**:
    - Use secure libraries and frameworks.
    - Deploy secure DevOps pipelines (DevSecOps) to automate security checks.
4. **Example Use Case**:
    - A banking application undergoes rigorous penetration testing before deployment to ensure it meets security standards.