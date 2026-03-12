# Disk Image Forensics - Findings

## Overview

The forensic investigation revealed several artifacts indicating that the user account **Bad Guy 2K** was involved in identity theft and credit card fraud activities.

Evidence discovered during the analysis included:

- stolen credit card information
- fake identity images
- credit card generator software artifacts
- deleted security-related files

---

# 1. Suspicious Document Evidence

A suspicious document was discovered in the following directory:
Documents and Settings/Bad Guy 2K/Desktop/

File:
COOL WORD DOCUMENT.doc

Metadata analysis revealed:

<img width="531" height="353" alt="image" src="https://github.com/user-attachments/assets/b81d95c6-3404-47a3-9a92-6d84d674dfcc" />






| Property | Value |
|--------|------|
| Author | Keith Lockhart |
| User Account | Bad Guy 2K |

<img width="702" height="448" alt="image" src="https://github.com/user-attachments/assets/45dd646f-653b-46a3-ae57-cd8153a07715" />

At first glance, the document appeared normal. However, deeper analysis revealed hidden text inside the file.

<img width="428" height="591" alt="image" src="https://github.com/user-attachments/assets/42f71a39-6983-4c6b-a859-d0c7149ae358" />


The hidden content contained **multiple credit card numbers**, indicating involvement in credit card fraud. 

---

# 2. Credit Card Generator Evidence

Inside the directory: FAKE ID PIX

three files were discovered:

<img width="514" height="233" alt="image" src="https://github.com/user-attachments/assets/5ef64e65-85bf-4906-80c9-c69137520e82" />

CCG1.GIF


<img width="579" height="263" alt="image" src="https://github.com/user-attachments/assets/14b4a1d8-2d0b-4cd4-959c-e8209eac95aa" />

CCG2.GIF


<img width="293" height="429" alt="image" src="https://github.com/user-attachments/assets/3a15b853-ea25-4026-a1f1-11cbcf4e615e" />

CCG3.GIF


These images displayed the interface of a **credit card generator application**.

The generator allowed the user to:

- select card type (Visa, MasterCard, etc.)
- generate multiple card numbers
- produce lists of generated numbers

The presence of this software strongly suggests deliberate generation of fraudulent credit card numbers.

---

# 3. Fraud Research Evidence

Additional images suggest the suspect was researching credit card fraud cases.

Examples include:


<img width="664" height="566" alt="image" src="https://github.com/user-attachments/assets/79d120db-238e-4863-93c9-d24b16330558" />

This is why JCPENNY !!!.jpg


<img width="548" height="487" alt="image" src="https://github.com/user-attachments/assets/375a24b2-dc67-48c5-a296-8ec2e8a8bf52" />

made the news !!.jpg


<img width="640" height="292" alt="image" src="https://github.com/user-attachments/assets/31f6d1c0-c7e9-457e-bb84-543b608af726" />

Amex Login Template.jpg


These files contain:

- customer complaints about stolen credit cards
- news reports about credit card fraud
- login page templates

This indicates the suspect was researching financial systems and vulnerabilities.

---

# 4. Identity Theft Evidence

The **FAKE ID PIX** folder also contained multiple identity images such as:


<img width="235" height="175" alt="image" src="https://github.com/user-attachments/assets/757f7596-1380-4c84-9e26-78b285cfc10a" />

fake ids.jpg


<img width="538" height="273" alt="image" src="https://github.com/user-attachments/assets/ef298571-6f92-4001-9947-24a19516ab80" />

uk id.jpg


<img width="527" height="326" alt="image" src="https://github.com/user-attachments/assets/800aa316-6471-4ead-92d2-c7a75f60505f" />

uk id 2.jpg


<img width="367" height="310" alt="image" src="https://github.com/user-attachments/assets/b6e6c7ac-a32a-45c5-a4b2-2d150703e103" />

watch out.jpg


These images appear to be scanned identification documents.

The collection of these artifacts suggests the suspect was preparing for **identity theft operations**.

---

# 5. Attempted Credential Theft

Deleted files discovered in the recycle bin included:

<img width="498" height="297" alt="image" src="https://github.com/user-attachments/assets/3ff4fa9b-2f80-4797-ab5d-5e0f980447db" />

Dd4

Dd3.ini

Analysis revealed that:

- **Dd4** contained a copy of the **SAM (Security Account Manager) file**
- The SAM file stores password hashes for system users

Deleting this file suggests the suspect may have attempted to:

- extract password hashes
- gain administrator privileges

This represents a potential **credential theft attempt**.

---

# 6. Timeline of Activities

Based on timestamp analysis, the suspicious activities occurred primarily on:

29 November 2003

30 November 2003


These timestamps correspond to:

- creation of suspicious files
- generation of credit card artifacts
- modification of identity images

---

# Conclusion

The investigation uncovered strong digital evidence linking the account **Bad Guy 2K** to multiple fraudulent activities including:

- credit card fraud
- identity theft
- possible administrator credential theft

Artifacts also revealed the name **Keith Lockhart**, which may represent the real identity of the suspect.

The combination of stolen credit card data, fake identification artifacts, and credential-related files indicates deliberate preparation and execution of financial fraud activities.
