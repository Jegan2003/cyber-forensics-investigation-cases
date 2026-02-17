# 🏦 USB Forensics – Bank Fraud Investigation

A forensic investigation of USB image files to uncover concealed, encrypted, and manipulated data linked to a suspected bank fraud incident.

---

## 📌 Scenario Overview

A USB device suspected of containing evidence related to financial fraud was provided for forensic analysis.  
The objective was to recover files, identify hidden content, and extract any encrypted financial data while preserving evidential integrity.

---

## 🎯 Objectives

- Recover files from forensic image  
- Detect steganography  
- Identify encrypted artifacts  
- Crack protected documents  
- Extract potential financial evidence  

---

## 🛠 Tools Used

FTK Imager  
zsteg  
John the Ripper  
GPG  
Kali Linux  

---

## 🔍 Investigation Workflow

1. Mounted USB image using FTK Imager  
2. Exported files in read-only mode  
3. Inspected images for steganography  
4. Extracted hidden OpenPGP keys  
5. Cracked password-protected Excel file  
6. Analyzed decrypted financial records  

---

## 🧾 Key Findings

- PNG images contained hidden OpenPGP public & secret keys  
- Transfers.xlsx was encrypted  
- Password cracked: **langley**  
- Decrypted file revealed suspicious money transfers  
- Bitcoin wallet QR code discovered  

---

## 🧠 Interpretation

The suspect used **steganography and encryption** to conceal sensitive financial information, indicating deliberate anti-forensic behavior.

---

## ✅ Conclusion

Clear evidence of concealed and encrypted financial artifacts supports the hypothesis of intentional data hiding related to fraudulent activities.

---

## 📷 Screenshots

(Add screenshots inside screenshots folder)
