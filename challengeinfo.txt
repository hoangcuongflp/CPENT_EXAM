Scope:
IP address range: 172.25.170.0/24
Exclusion: 172.25.170.1
This zone is an Active Directory forest that you need to identify the Domain Controller then use different techniques to assess it. As with an enterprise network the Domain Controller more than likely will not be directly reachable, you will have to leverage a machine to achieve visibility into the forest.

Challenge 1: (25 Points)
What is the 16th Byte NETBIOS name on the machine at 172.25.170.30?
 1A
 1B
 1C
 1D
Challenge 2: (25 Points)
What is the role of the machine at 172.25.170.30? Based on the 16th byte?
 Network browser
 Member server
 Standalone
 Domain Controller
Challenge 3: (50 Points)
What is the 16th Byte NETBIOS name of the machine at 172.25.170.200?
 1A
 1B
 1D
 1C
Challenge 4: (50 Points)
What is the status of the smb2 signing on the machine at 172.25.170.30?
 Enabled
 Disabled
 Not valid
 Unknown
Challenge 5: (50 Points)
What NetBIOS domain name for the machine connected at 172.25.170.30?
 COMMANDERTWO.LOCALNET
 CPENT.LOCALNET
 CPENTTWO.LOCALNET
 COMMANDER.LOCALNET
Challenge 6: (50 Points)
What is the NetBIOS name of the computer at 172.25.170.30?
 CPENT
 CPENTTWO
 COMMANDER
 COMMANDERTWO
Challenge 7: (50 Points)
What is the domain name on the machine at 172.25.170.200?
 CPENT.LOCALNET
 CPENTTWO.LOCALNET
 ECC.LOCALNET
 ECCTWO.LOCALNET
Challenge 8: (50 Points)
What is the status of the smb2 signing on the machine at 172.25.170.200?
 Enabled
 Disabled
 Not valid
 Unknown
Challenge 9: (50 Points)
What is the NetBIOS name of the machine located at 172.25.170.90?
 CPENT
 COMMANDER
 2012-DC
 LA
Challenge 10: (50 Points)
What is the last four hex numbers (just the numbers) for the hash of the adminflag.txt file on machine 172.25.170.20?
 09C5
 0854
 06FE
 07EA
Challenge 11: (50 Points)
What is the contents of the adminflagBRAVO at machine 172.25.170.70?
 SERVER2008-AD
 SERVER2008-DC
 SERVER2008-ADDC
 SERVER2008CHARLIE

Scope:
Target Machine 1: 172.25.120.210
Username: student
Password: studentpw
Target Machine 2: 172.25.120.220
Username: student
Password: studentpw
Target Machine 3: 172.25.120.100
Username: student
Password: studentpw
Username: cpent
Password: Pa$$w0rd123
Exclusion: 172.25.120.1, 10.1.120.0/24, 172.25.120.0/24, 192.168.120.0/24, 172.25.120.1, 10.1.120.0/24, 172.25.101.1
In this zone you will need to identify the target then map the attack surface and then gain access, once you gain the access then you need to reverse engineer the firmware and answer the questions about it. As you build your target database, make note of any hard-coded credentials. Once you find a firmware image, analyze the extracted file system and look at the code, which in many cases will be php etc. Additionally, in this zone, you need to identify the binary files and reverse engineer them to answer the questions and then to get the privilege flag you will have to create an exploit and then gain root level privileges. Protections may or may not be compiled into the binary.

Challenge 12: (40 Points)
What is the value in hex (include 0x) for the R8 register for BASH at run time on machine 172.25.120.210?
 0x206
 0x0
 0xFF20
 0x54FA
Challenge 13: (40 Points)
What are last 6 hex characters of the RootFlagTwo.txt on machine 172.25.120.220?
 24d7e0
 C10317
 103172
 9f9f7a
Challenge 14: (50 Points)
What are the last 6 hex characters of the RootFlag210.txt file md5 hash on machine 172.25.120.210?
 323C80
 721549
 C10317
 103172
Challenge 15: (30 Points)
On the Target Machine 2 (172.25.120.220), analyze level-two binary file and find the value of the ss register at run time (include the 0x)?
 0x2a
 0x2b
 0x2c
 0x23
Challenge 16: (30 Points)
On the Target Machine 2 (172.25.120.220), analyze level-two binary file and find the offset between the /bin/sh and the system() using dynamic analysis. (hint: /bin/sh is greater than system() - (include the 0x).
 0x149f32
 0x32456
 0x12445
 0x45678
Challenge 17: (30 Points)
What is the address of /bin/bash within the executable file binaries-two (use the first address in the executable, not the stack) - (include the 0x)?
 0x8048610
 0x8765430
 0x8732134
 0x8859234
Challenge 18: (30 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image FileOne.bin and identify the compression algorithm.
 RAR
 PK
 LZMA
 ZIP
Challenge 19: (30 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image FileOne.bin and enter the year of the image?
 2010
 2020
 2019
 2011
Challenge 20: (30 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image FileOne.bin and find the total number of inodes of the file system?
 1100
 1115
 1117
 1119
Challenge 21: (25 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image File2.bin and find the image CRC (include 0x).
 0x33
 0x40
 0x41
 0x43
Challenge 22: (25 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image File2.bin and determine the original file name.
 LMZA
 squash
 piggy
 file
Challenge 23: (40 Points)
What is the address (numbers only of the file system loader offset in File2.bin?
 1X
 1A
 1B
 1C
Challenge 24: (50 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image IOT.bin and find the password of the admin user. (hint: not the one in plain text)
 1234
 admin
 password
 blank
Challenge 25: (50 Points)
On the Target Machine 3 (172.25.120.100), analyze IOT firmware image IOT.bin, what is the web_passwd of the useranonymous (include all characters)?
 anon@localhost
 admin@127.0.0.1
 user@localhost
 none of the above


Scope:
IP address range: 172.25.20.0/24, 172.25.30.0/24
Exclusion: 172.25.20.1, 172.25.30.1
In this zone, you will deal with multiple web application vulnerabilities and security misconfigurations. Once you identify them and exploit them, you own the servers. Upon owning them, find the secret keys placed in them.

Challenge 26: (125 Points)
Compromise the machine with IP address 172.25.20.6, find the file secret.txt and enter its content as the answer.
 aksph47b6m2
 pskmt87h9y2
 kljhy97u9t2
 jklmu89u8g3
Challenge 27: (125 Points)
Compromise the machine with IP address 172.25.30.4, find the file secret.txt and enter its content as the answer.
 lux76hk5pp
 bux89kl9dd
 hus79ui0yy
 axm42fk2gp
Challenge 28: (125 Points)
Compromise the machine with IP address 172.25.30.5, find the file Secret.txt and enter its content as the answer.
 hb74kpm9h83
 lk69nod2j09
 mn89bod3k09
 jk89mod1j90
Challenge 29: (50 Points)
Compromise the machine with IP address 172.25.20.7, find the file userflag.txt and enter its content as the answer.
 bu79g82xap
 ky80i89pas
 ut90u70sap
 ot90k09sap
Challenge 30: (75 Points)
Compromise the machine with IP address 172.25.20.7, find the file rootflag.txt, and enter its content as the answer.
 b5ph89fg9i0
 i5op09hg7u0
 k5pl80gh7i0
 p5bh39md4k7


Scope:
IP address range: 172.25.100.0/24, 192.168.110.0/24
Exclusion: 172.25.100.1, 192.168.110.1, 10.1.110.0/24
In this zone you will need to first identify the IT side of the network then the OT network and map the attack surface, once you gain access to the machine(s) connected to the OT network you will have to identify the ICS/SCADA network traffic and analyze the protocol then read the data values at the registers and coils. The key is gaining access to the network traffic.

Challenge 31: (50 Points)
What is the MAC address of the vendor (6 digits only) for the MAC address that makes the ModBus Query?
 C5830A
 000AE4
 FFFFFF
 OOO3CF
Challenge 32: (50 Points)
In the ModBus traffic, what is the length of the value of the register at Transaction_Identifier: 209?
 1
 3
 5
 7
Challenge 33: (50 Points)
What is the value of the register 211 Trans: 1 in the ModBus response?
 0
 1
 2
 3
Challenge 34: (50 Points)
What is the register 0 value (UNIT16) in the Trans: 228 in hex?
 0000
 01C3
 4430
 41C8
Challenge 35: (50 Points)
What is the destination MAC address of all of the ModBus responses? (use hex, but do not put the colons)
 FFFFFFFFFFFF
 001CC05F490A
 EEDDCCBBAA11
 0034568909339
Challenge 36: (50 Points)
What is the protocol identifier of the Modbus/TCP response for Trans: 238?
 0
 1
 2
 3
Challenge 37: (40 Points)
Compromise the 192.168.110.230 machine to gain user-level access. Locate userflag.txt and submit the last 6 hex digits of the md5 hash of the file.
 008EA3
 A309D2
 66EEAB
 902AEB
Challenge 38: (60 Points)
Escalate your privilege to that of a Root user in the 192.168.110.230 machine, locate rootflag.txt and submit the last 6 hex digits of the md5 hash the file.
 008EA3
 66EEAB
 902AEB
 377EE5
Challenge 39: (40 Points)
Compromise the 172.25.100.105 machine to gain user-level access. Locate userflag.txt and submit the last 6 hex digits of the md5 hash of the file.
 ECFE85
 66EEAB
 902AEB
 377EE5
Challenge 40: (60 Points)
Escalate your privilege to that of an Administrator in the 172.25.100.105 machine, locate adminflag.txt and submit the last 6 hex digits of the md5 hash of the file.
 008EA3
 A309D2
 82FC58
 902AEB


Scope:
IP address range: 172.25.65.0/24, 192.168.65.0/24, 192.168.5.0/24, 172.25.25.0/24, 192.168.25.0/24, 192.168.35.0/24, 192.168.45.0/24
Exclusion: 172.25.65.1, 192.168.65.1, 192.168.5.1, 10.1.65.0/24, 172.25.25.1, 192.168.25.1, 192.168.35.1, 192.168.45.1, 10.1.25.0/24
In this zone, you will need to map the network, identify the multi-homed machine, gain access, and then pivot into the connected network. Once there, you will have to map that network and gain access to get the files' contents. Some of the networks might require more than one pivot.


Challenge 41: (25 Points)
What is the last four hex digits of the RSA ssh-hostkey at machine 192.168.65.200? (Hint: do not enter the colon, just characters)
 7781
 4AFE
 3DCE
 BC32
Challenge 42: (50 Points)
What is the root password of the user at the machine located at the IP address of 192.168.65.200?
 puppettwo
 aspentwo
 cpentwo
 lpttwo
Challenge 43: (50 Points)
What is the domain NAME of the machine at IP address 192.168.35.100?
 CPENT.LOCALNET
 ECC.LOCALNET
 LA.LOCALNET
 UK.LOCALNET
Challenge 44: (50 Points)
What is the NetBIOS 16th Byte with the type of UNIQUE on the machine at the 192.168.35 network? (Hint: starts with 1)
 1E
 1C
 1D
 1A
Challenge 45: (50 Points)
What are the last 6 characters of the ssh ECDSA private key on the 192.168.5.230 machine?
 ABCEEE
 ECAwQF
 5byea0
 YWItu3
Challenge 46: (40 Points)
Compromise the 192.168.65.200 machine to gain user level access. Locate userflag.txt and submit the last 6 hex digits of the md5 hash of the file.
 078910
 123AA5
 A4A9CB
 2FEC38
Challenge 47: (60 Points)
Escalate your privilege to that of a root user in the 192.168.65.200 machine, locate rootflag.txt and enter the last 6 digits of the md5 hash.
 123AA5
 A4A9CB
 2FEC38
 C67F46
Challenge 48: (50 Points)
What port is the nodejs application running on in machine 192.168.65.250?
 9090
 8080
 8008
 8888
Challenge 49: (25 Points)
What is the last 4 hex digits of the 1024 DSA ssh key at 192.168.65.210?
 3AA5
 0CA7
 88A5
 C394
Challenge 50: (60 Points)
What is the last 6 hex digits of the md5 hash content of rootflag.txt on 192.168.65.210?
 123AA5
 5D4A27
 A4A9CB
 2FEC38
Challenge 51: (40 Points)
What is the last 6 hex digits of the hash content of the userflag.txt on machine 192.168.65.210?
 123AA5
 E86047
 A4A9CB
 2FEC38
