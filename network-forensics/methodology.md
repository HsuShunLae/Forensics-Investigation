# Network Forensics - Methodology

## Overview

This investigation analyzes a network packet capture file to identify suspicious or malicious activity within a corporate network environment.

The dataset analyzed: q3NetworkCapture.pcap


The objective of this investigation was to:

- Identify malicious hosts within the network
- Detect attack techniques used by the attacker
- Analyze network communication patterns
- Determine whether sensitive data was exfiltrated

---

# Investigation Workflow

The network forensic investigation followed a structured workflow:

1. Packet capture inspection
2. Protocol analysis
3. Identification of active hosts
4. Detection of reconnaissance activity
5. Session analysis
6. Detection of exploitation attempts
7. Identification of data exfiltration

---

# Tools Used

The following tools were used during the investigation:

- **Wireshark** – packet analysis

Wireshark allows investigators to analyze network traffic at the packet level without modifying the original capture.

---

# 1. Protocol Analysis

The packet capture was first analyzed to determine which protocols were present.

The most significant protocols identified were:

- SMB
- Telnet
- HTTP
- FTP

These protocols were examined to determine their role in the attack and to identify suspicious communication patterns. 

---

# 2. Host Identification

Network traffic analysis identified several active IP addresses exchanging large volumes of packets.

The main systems involved in the communication were:

| IP Address | 
|------------|
| 192.168.100.5 | 
| 192.168.100.26 | 
| 192.168.100.27 | 
| 192.168.100.28 | 

<img width="655" height="276" alt="image" src="https://github.com/user-attachments/assets/c4cc2bbe-e5d5-49c8-9873-b8d6ac0f8c1b" />

These systems became the primary focus of the investigation. 

---

# 3. Traffic Pattern Analysis

Packet flows were analyzed to identify abnormal patterns such as:

- High volumes of SYN packets
- Repeated connection attempts
- Unexpected protocol usage

These behaviors are commonly associated with reconnaissance or intrusion attempts.

---

# 4. Session Reconstruction

Telnet and HTTP sessions were reconstructed to examine attacker actions.

This process allows investigators to:

- view attacker commands
- analyze authentication attempts
- detect exploitation activity

---

# 5. Attack Path Analysis

The attack path was reconstructed by tracking communication between hosts.

This included identifying:

- the initial attacker system
- the compromised intermediate system
- the final target systems

This approach helps determine how the attacker moved laterally within the network.

---

# 6. Data Exfiltration Detection

The investigation also focused on identifying potential data exfiltration.

This involved analyzing:

- FTP sessions
- HTTP requests
- unusual file transfers

Evidence of file downloads and SQL injection activity was discovered during this phase.

---

# Summary

The network forensic methodology allowed the investigation to:

- identify the attacker system
- reconstruct the attack sequence
- detect data exfiltration activity
- determine which systems were compromised

The results of this analysis are presented in the **findings section**.
