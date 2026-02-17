# 📄 Memory Forensics – Bad PDF Investigation

Memory forensic analysis of a compromised virtual machine after a malicious PDF was opened by an employee.

---

## 📌 Scenario Overview

A memory image was provided from an employee workstation suspected of being compromised after opening a PDF attachment.

---

## 🎯 Objectives

- Identify exploited process  
- Detect suspicious network connections  
- Extract credential hashes  
- Identify attacker activity  

---

## 🛠 Tools Used

Volatility Framework  
Kali Linux  

---

## 🔍 Investigation Workflow

1. Identified OS profile  
2. Enumerated running processes  
3. Analyzed process tree  
4. Identified network connections  
5. Scanned memory for URLs  
6. Extracted password hashes  

---

## 🧾 Key Findings

- Exploited Process: **AcroRd32.exe (Adobe Reader)**  
- Suspicious IPs: **212.150.164.203**, **193.104.22.71**  
- Outbound HTTP connections observed  
- Weak Administrator password recovered  

---

## 🧠 Interpretation

The malicious PDF exploited Adobe Reader and enabled outbound communication, likely for data exfiltration.

---

## ✅ Conclusion

Evidence confirms exploitation via malicious PDF leading to possible credential theft and attacker-controlled communication.

---

## 📷 Screenshots

(Add screenshots inside screenshots folder)
