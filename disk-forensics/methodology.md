# Disk Image Forensics – Methodology

## Overview

This investigation analyzed a forensic disk image to identify evidence related to identity theft and credit card fraud. The disk image was examined using standard digital forensic procedures to ensure evidence integrity and maintain forensic reliability.

The forensic image analyzed in this investigation:
CNF-ID-THEFT.E01


---

# Investigation Workflow

The analysis followed a structured forensic workflow:

1. Evidence acquisition and integrity verification
2. File system exploration
3. Artifact discovery and metadata analysis
4. Hidden data inspection
5. Timeline analysis
6. Deleted file recovery

---

# 1. Evidence Integrity Verification

Before conducting any analysis, the integrity of the disk image was verified using cryptographic hashing.

The provided hash values were:

| Hash Type | Value |
|-----------|------|
| MD5 | be05d22f918cfb0e600d578e01f81f1a |
| SHA1 | 2390770cc9de001ed4c13ecd09e59dbb941707ce |

The image was loaded into forensic tools and hashes were recomputed.

The computed hashes matched the original values, confirming that the forensic image had **not been altered or corrupted** and could be safely used for analysis. :contentReference[oaicite:0]{index=0}

---

# 2. Forensic Tools

The following tools were used during the investigation:

- **Autopsy**
- **FTK (Forensic Toolkit)**

These tools allow investigators to examine disk images without modifying the original evidence.

---

# 3. File System Analysis

The disk image was mounted in Autopsy to explore the file system structure.

Key tasks performed:

- Identifying user accounts
- Searching suspicious directories
- Reviewing desktop files
- Inspecting application artifacts

The following user accounts were discovered:

- Guest
- Administrator
- MWF GOBLIN
- Bad Guy 2K

<img width="755" height="113" alt="image" src="https://github.com/user-attachments/assets/7ae4b93d-18b3-4fba-9aa0-c2bc2c4e8cbf" />


The account **Bad Guy 2K** appeared to contain the most suspicious activity.

---

# 4. Artifact Analysis

Several forensic artifacts were examined:

- Documents
- Images
- Deleted files
- System configuration files

Special attention was given to files located in:
Documents and Settings/Bad Guy 2K/

These artifacts were analyzed using:

- metadata inspection
- content inspection
- hidden data analysis

---

# 5. Hidden Data Inspection

Suspicious files were examined for hidden content such as:

- embedded text
- alternate data streams
- concealed information within documents

This process revealed hidden text inside a Word document that contained stolen credit card numbers.

---

# 6. Timeline Analysis

File timestamps were analyzed to understand the sequence of events.

The following metadata fields were reviewed:

- Creation time
- Modification time
- Access time
---

# 7. Deleted File Analysis

The recycle bin and deleted files were examined to recover potential evidence.

This analysis revealed deleted system files related to:

- security configuration
- administrator credentials

These findings suggested attempts to manipulate system security.

---

# Summary

The forensic methodology ensured that:

- Evidence integrity was preserved
- Artifacts were analyzed systematically
- Suspicious activities were documented

The results of the investigation are presented in the **findings section**.
