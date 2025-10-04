# 🧩 Basic Vulnerability Scan

## 🎯 Objective
To perform a basic vulnerability assessment on a local system using **Nessus Essentials** — a widely used vulnerability scanner — to identify common security weaknesses and potential misconfigurations.

---

## 🧰 Tools Used
- **Nessus Essentials** – Free vulnerability scanning tool by Tenable.  
- **Local Machine (Target):** IP – `172.16.xx.xxx`

---

## ⚙️ Implementation and Process

### 1. **Tool Setup**
Installed and configured **Nessus Essentials**, including downloading and initializing its latest plugin database for accurate detection.

### 2. **Scan Configuration**
Created a new scan profile named **`patch_finder`**.

### 3. **Target Selection**
Added the local machine IP (`172.16.xx.xxx`) as the scan target.

### 4. **Policy Applied**
Selected the **Basic Network Scan** policy for general vulnerability assessment.

### 5. **Scan Execution**
Executed the scan between **7:25 PM and 7:42 PM (17 minutes total)**.  
The scan completed successfully and generated detailed vulnerability results.

---

## 🧾 Vulnerability Findings

| Severity | Count | Example Issues |
|-----------|--------|----------------|
| Info | Majority | General system information, service banners |
| Medium | Few | SSL Certificate Cannot Be Trusted |
| Mixed | Present | Combination of various severity levels |

**Total Vulnerabilities Found:** 23  

### 🔍 **Key Vulnerability Groups**
- **Netstat Portscanner (SSH):** 30 occurrences  
- **SMB (Multiple Issues):** 6 occurrences  
- **SSL (Multiple Issues):** 4 occurrences *(includes the most severe finding)*

---

## 🚨 Most Severe Finding

**Vulnerability Title:** SSL Certificate Cannot Be Trusted  
**Severity Level:** Medium  
**CVSS v3.0 Base Score:** 6.5  

### **Root Cause**
- Broken or incomplete certificate chain (e.g., self-signed or missing intermediate CA).  
- Invalid or expired SSL certificate.  
- Unverified or bad digital signature.

### **Recommended Solution**
Obtain or generate a **valid SSL certificate** from a trusted Certificate Authority (CA) and correctly configure the service to use it.

---

## 🔐 Risk Impact
An untrusted SSL certificate can enable **man-in-the-middle (MITM) attacks**, allow **data interception**, and reduce **user trust** in secure communications.

---

## 🧠 Conclusion
This exercise provided hands-on experience with **Nessus Essentials** and basic vulnerability scanning methodology.  
It highlighted how scanners detect common misconfigurations and why maintaining valid SSL certificates and patching known vulnerabilities is critical for system security.

---

## 📂 Files & Artifacts
- Nessus Scan Report (`patch_finder_report.html`)  
- Screenshots: Scan Configuration, Scan Results Dashboard, Vulnerability Summary  

---

**Author:** Rahul Malatesh Sannapujar  
**Date:** 04/10/2025  
