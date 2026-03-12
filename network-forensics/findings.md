# Network Forensics - Findings

## Overview

Analysis of the network traffic revealed multiple malicious activities including:

- port scanning
- unauthorized remote access
- SQL injection attacks
- data exfiltration via FTP

The primary attacker was identified as the system with IP address: **192.168.100.26**

This host conducted reconnaissance and used another machine as an attack platform.

---

# 1. Port Scanning Activity

A large number of TCP SYN packets were observed originating from: 192.168.100.26

targeting the system: 192.168.100.27

The attacker scanned several ports including: 25, 110, 111, 139

<img width="916" height="284" alt="image" src="https://github.com/user-attachments/assets/6b49de67-c54d-415f-b8e7-c8554c391e05" />


This behavior indicates reconnaissance activity designed to identify open services. 

---

# 2. Telnet Foothold

After scanning the target, the attacker established a **Telnet connection** to the system: 192.168.100.27

<img width="925" height="35" alt="image" src="https://github.com/user-attachments/assets/c020858c-b9c4-4eba-8052-bd0ff409bc44" />


Authentication credentials were observed in the Telnet session:

Username: vilkp

Password: password

<img width="771" height="201" alt="image" src="https://github.com/user-attachments/assets/5ba97882-eafe-4ab5-9d98-2aeba0a6a3ad" />

Once authenticated, the attacker gained remote control of the system.

The compromised machine was then used as a platform to attack other systems within the network. 

---

# 3. Internal Reconnaissance

Using the compromised system (192.168.100.27), the attacker performed further reconnaissance.

The next target was: 192.168.100.28

Port scanning revealed open services: 22, 23, 80


<img width="919" height="353" alt="image" src="https://github.com/user-attachments/assets/6fdc8800-6bd9-4584-99d9-f551c30431aa" />


This information allowed the attacker to identify potential attack vectors on the internal server.

---

# 4. SQL Injection Attack

HTTP traffic analysis revealed a malicious POST request containing a **SQL injection payload**.

The payload attempted to execute a query designed to retrieve sensitive information such as:

- database usernames
- passwords
- system configuration files

<img width="926" height="401" alt="image" src="https://github.com/user-attachments/assets/f663487f-ba4e-4922-932c-a2b3adebb9e1" />

The server responded with: HTTP 200 OK

This indicates that the SQL injection attack was successful and data was retrieved from the system. :contentReference[oaicite:4]{index=4}

---

# 5. FTP Data Exfiltration

After gathering information from the internal server, the attacker targeted another system: 192.168.100.5

<img width="519" height="211" alt="image" src="https://github.com/user-attachments/assets/243310b2-572f-433c-951f-faaf40238a78" />

This host was identified as a **DHCP and FTP server**.

<img width="834" height="547" alt="image" src="https://github.com/user-attachments/assets/05ea17aa-814e-46ae-aba1-ac3546799dbf" />

The attacker connected to the FTP service using **anonymous login credentials**.

<img width="501" height="546" alt="image" src="https://github.com/user-attachments/assets/7f27cd1b-9279-46bf-87d9-2a4f1f4a9172" />

During the session, the attacker downloaded the file: Budget.txt

This file likely contained sensitive organizational data.

The download represents a clear case of **data exfiltration from the network**.

---

# 6. Attacker Exit

After completing reconnaissance and data exfiltration activities, the attacker terminated the connection.

<img width="828" height="240" alt="image" src="https://github.com/user-attachments/assets/ad6d5b69-e240-4ed3-a183-edff9d12797f" />

Network traffic indicates that the attacker released the DHCP lease and disconnected from the network.

This behavior suggests the attacker intentionally exited the environment after completing the intrusion.

---

# Attack Chain Summary

The reconstructed attack sequence is as follows:

1. Initial reconnaissance via port scanning
2. Telnet login to compromised host
3. Internal network reconnaissance
4. SQL injection attack against web server
5. Data exfiltration via FTP
6. Attacker disconnects from network

---

# Conclusion

The network forensic investigation identified a coordinated attack originating from the host: 192.168.100.26

The attacker compromised an internal machine using Telnet and leveraged it to conduct further attacks on the network.

Evidence confirms that the attacker successfully:

- performed reconnaissance
- executed SQL injection
- accessed internal systems
- exfiltrated sensitive files

These findings highlight significant security weaknesses including:

- insecure Telnet access
- lack of network segmentation
- vulnerable web applications






