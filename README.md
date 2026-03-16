![Status](https://img.shields.io/badge/Project%20Status-Completed-success)
![Domain](https://img.shields.io/badge/Domain-Cyber%20Forensics-blue)
![Focus](https://img.shields.io/badge/Focus-DFIR%20%7C%20Threat%20Intelligence-orange)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)

![Banner](banner.png)


# 🔍 Cyber Forensics Investigation Cases
### Real-World Digital Forensics | Malware Analysis | Memory Forensics

A curated collection of **hands-on cyber forensics investigations** designed to simulate real-world incident response and digital evidence analysis.  
Each case follows **ACPO & NIST forensic standards** and demonstrates how raw digital evidence is transformed into **actionable intelligence**.

---

## 🧭 What You’ll Find Here

✔ USB Forensics (Hidden data, steganography, encryption)  
✔ Malware Network Traffic Analysis (PCAP)  
✔ Memory Forensics (Malicious PDF exploitation)  
✔ Evidence integrity & chain of custody handling  
✔ IOC extraction & attacker behavior analysis  

---

## 📂 Case Portfolio

| Case | Title | Focus Area |
|-----|------|------------|
| 1 | USB Forensics – Bank Fraud | Steganography & Encryption |
| 2 | Malware Traffic Analysis | C2 Beacon Detection |
| 3 | Memory Forensics – Bad PDF | Exploit & Credential Theft |

---

## 🛠 Forensic Toolkit

FTK Imager  
Volatility Framework  
Wireshark / Tshark  
Zeek Network Monitor  
John the Ripper  
zsteg  
Kali Linux  

---

## 🧠 Skills Demonstrated

Digital Forensics & Incident Response (DFIR)  
Malware Traffic Analysis  
Memory Forensics  
Evidence Preservation  
Indicator of Compromise (IOC) Extraction  
Report Writing & Documentation  

---

## 🖼 Investigation Snapshots

![FTK](screenshots/usb-ftk.png)
![Steg](screenshots/steg-zsteg.png)
![John](screenshots/john-password.png)
![Wireshark](screenshots/wireshark-traffic.png)
![Volatility](screenshots/volatility-pslist.png)

---

## 🎯 What Makes This Repository Different?

Unlike theoretical projects, this repository focuses on **practical investigations**:
- Real evidence  
- Real artifacts  
- Real attacker techniques  
- Real forensic workflows  

This mirrors how DFIR teams operate in enterprise environments.

---

## 👨‍💻 Author

**Jegan Kamalnath**  
MSc Cybersecurity Threat Intelligence & Forensics  





🔍 USB Forensics Investigation

Digital Forensics Case Study | Tools: FTK Imager · John the Ripper · zsteg · Wireshark · Volatility
Standards: ACPO Good Practice Guide · NIST SP 800-86


📋 Objective
This investigation involved the forensic examination of a USB drive image suspected to contain concealed and encrypted evidence. The goal was to acquire a forensically sound image, verify its integrity, and conduct a thorough analysis to identify hidden data, encrypted content, and any associated network artefacts — following ACPO and NIST forensic standards throughout.

🛠️ Tools Used
ToolPurposeFTK ImagerForensic acquisition and hash verification of the USB imagezstegDetection and extraction of steganographic data hidden in image filesJohn the RipperCracking encrypted file passwords and OpenPGP passphrasesWiresharkAnalysis of any associated network traffic artefactsVolatilityMemory analysis to support findings where applicable

🔬 Methodology
This investigation followed a structured forensic process in line with the ACPO Good Practice Guide for Digital Evidence and NIST SP 800-86 (Guide to Integrating Forensic Techniques into Incident Response).
Phase 1 — Acquisition & Integrity Verification

Created a forensic bit-for-bit image of the USB drive using FTK Imager
Generated MD5 and SHA-256 hash values of both the original source and acquired image
Verified hash values matched — confirming the forensic image was an exact, unmodified copy
Maintained a full chain of custody log throughout

Phase 2 — File System Analysis

Mounted the image in read-only mode to preserve evidence integrity
Conducted timeline analysis of file creation, modification, and access timestamps
Identified files of interest including image files (PNG/BMP), documents, and encrypted containers

Phase 3 — Steganography Detection

Used zsteg to scan all image files on the USB for hidden data embedded using LSB (Least Significant Bit) steganography
Successfully identified and extracted concealed data from image files

Phase 4 — Encrypted File Analysis

Identified OpenPGP encrypted key files on the USB
Extracted password hashes using John the Ripper with a wordlist attack
Successfully recovered passphrases, enabling decryption and access to protected content

Phase 5 — Network Traffic Analysis

Analysed associated PCAP files using Wireshark
Examined traffic for indicators of data exfiltration or command-and-control communication
Applied display filters to isolate relevant traffic streams

Phase 6 — Reporting

Documented all findings with supporting evidence in a formal forensic report
Mapped findings to MITRE ATT&CK techniques (see below)
Maintained evidence integrity throughout — no write operations performed on the original image


🔑 Key Findings
FindingDetailSteganographyHidden data identified and extracted from image files using zsteg (LSB technique)Encrypted FilesOpenPGP encrypted key files discovered on the USBPassword RecoveryPassphrases successfully recovered using John the Ripper dictionary attackHash VerificationMD5 + SHA-256 hashes confirmed forensic image integrityTimeline AnalysisFile timestamps analysed to reconstruct activity sequence on the deviceNetwork ArtefactsAssociated network traffic examined in Wireshark for exfiltration indicators

🗺️ MITRE ATT&CK Mapping
Technique IDTechnique NameRelevanceT1027Obfuscated Files or InformationSteganography used to conceal data in image filesT1553Subvert Trust ControlsEncrypted OpenPGP keys used to protect dataT1052.001Exfiltration Over Physical Medium: USBData stored on USB for potential exfiltrationT1119Automated CollectionTimestamped file activity suggests automated or scripted collectionT1048Exfiltration Over Alternative ProtocolNetwork traffic analysed for exfiltration indicators

📁 Repository Structure
usb-forensics-investigation/
│
├── README.md                  ← This file
├── methodology/
│   └── forensic_process.md    ← Detailed step-by-step methodology
├── findings/
│   ├── timeline_analysis.md   ← File timestamp reconstruction
│   ├── steganography.md       ← zsteg findings and extracted data
│   ├── encryption_analysis.md ← OpenPGP key analysis and recovery
│   └── network_analysis.md    ← Wireshark traffic findings
├── screenshots/               ← Evidence screenshots (redacted where needed)
└── reports/
    └── forensic_report.md     ← Final formal report

⚖️ Legal & Ethical Considerations

This investigation was conducted in a controlled academic environment using a pre-prepared forensic image
All analysis was performed on a forensic copy — the original evidence was never modified
Full chain of custody was maintained throughout
Conducted in accordance with ACPO Principle 1: No action should change data on a digital device


📚 References

ACPO (2012). Good Practice Guide for Digital Evidence
NIST SP 800-86. Guide to Integrating Forensic Techniques into Incident Response
MITRE ATT&CK Framework — https://attack.mitre.org
Openwall John the Ripper — https://www.openwall.com/john/
zsteg — https://github.com/zed-0xff/zsteg


Conducted as part of MSc Cybersecurity Threat Intelligence & Forensics — University of Salford, UK
University of Salford  

---

⭐ If this repository helped you, consider giving it a star.
