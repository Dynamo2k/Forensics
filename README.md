# M57.biz Digital Forensics Investigation

## 📋 Case Overview

This repository contains digital forensic evidence and analysis reports from an **Insider Threat Investigation** at **M57.biz**, a small startup specializing in prior art patent research services.

### What Happened?

**M57.biz** was a startup company that hired employees to conduct patent prior art research for clients. One employee, known as **"Charlie"**, engaged in criminal activities including:

1. **Corporate Espionage** - Stealing and selling proprietary patent research
2. **Extortion/Blackmail** - Demanding $100,000 under threat of disclosure
3. **Trade Secret Theft** - Selling confidential client research to competitors
4. **Anti-Forensic Techniques** - Using encryption, steganography, and instructing evidence destruction

---

## 🏢 The Company & Personnel

| Employee | Role | Email | Status |
|----------|------|-------|--------|
| **Pat McGoo** | CEO/Founder | pat@m57.biz | Victim (Employer) |
| **Charlie** | Patent Researcher | charlie@m57.biz | **PRIMARY SUSPECT** |
| **Jo Smith** | Patent Researcher | jo@m57.biz | Witness |
| **Terry Johnson** | IT Administrator | terry@m57.biz | Witness |

---

## 📖 Detailed Scenario

### Timeline of Events

#### **Week 1: November 16-20, 2009 — The Beginning**

Charlie started working at M57.biz on November 16, 2009. The company was working on confidential prior art research for a client called **Nitroba.com**, which was applying for patents on:
- Time machines
- Teleporters

The client specifically requested confidentiality because they didn't want their competitor (**project2400.com**) to learn about their research interests.

#### **Week 2-3: November 21-30, 2009 — Preparation**

During this period, Charlie accessed files from a project called **"Immortality"** containing patent documents (TIF files). On November 24, 2009:
- Charlie accessed and prepared patent documents
- Created a Windows Thumbs.db thumbnail cache (evidence of file access)
- Packaged files into a ZIP archive

#### **Week 4: December 1-4, 2009 — The Crimes**

**December 1, 2009:**
- Charlie emailed his girlfriend Alix about upcoming money for a vacation and "hot car"
- This shows premeditation and financial motivation

**December 2, 2009:**
- **13:04** - Charlie sent an email to `jaime@project2400.com` (competitor, misspelled) offering to sell trade secrets
- The email stated: *"I have something that you'll definitely be interested in. It concerns your competitor. I'm doing a prior art search for them. Want to know what I've found? You know my price."*
- **13:05** - The email BOUNCED back because Charlie misspelled the address (jaime vs jamie) — **this preserved the evidence!**
- **13:25** - Charlie corrected the spelling and sent to `jamie@project2400.com` (correct spelling)

**December 3, 2009:**
- **09:51** - Competitor responded agreeing to pay "$50 large" with $10k upfront
- **12:16** - Charlie sent files to the competitor (data exfiltration)
- **13:02** - Charlie planned a Mediterranean cruise with his girlfriend

**December 4, 2009:**
- **09:41** - **THE EXTORTION EMAIL** - Charlie emailed `andy@swexpert.com`:
  > *"I found a prior patent that will definitely invalidate your current immortality patent. You should have used my boss's prior art services, but, oh well, I'll just use your negligence to benefit me. I want 100k or I'll release this publicly. Don't involve the cops or this information will go public."*
- He attached a **password-protected ZIP file** containing the stolen Immortality project files
- **13:06** - Charlie sent password instructions: *"The password to get the info is nitro. Use the steg program we talked about. And don't forget to delete these emails."*

#### **Week 5: December 7-11, 2009 — Aftermath**

**December 7, 2009:**
- Charlie sent a **steganography image** (`microscope1.jpg`) to hide the password

**December 8-10, 2009:**
- Charlie requested a 2-week vacation
- Made plans to test drive Ferrari and Shelby cars
- Confirmed car delivery in 2 weeks

---

## 🔍 Key Evidence Summary

### Critical Evidence Files

| File | Description | Significance |
|------|-------------|--------------|
| `Charlie_2009-12-04_0941_Sent.txt` | Extortion email | $100,000 demand |
| `Charlie_2009-12-04_0941_Sent_01.zip` | Password-protected archive | Contains stolen Immortality files |
| `Charlie_2009-12-02_1305_Received.txt` | Bounced email containing misspelled trade secret offer | Preserved original incriminating message |
| `Charlie_2009-12-04_1306_Sent.txt` | Password instructions | "nitro" password revealed |
| `other/Charlie_2009-12-07_1144_Sent_microscope1.jpg` | Steganography image | Hidden data carrier |
| `Immortality/` folder | Stolen patent documents | Exfiltrated data |

### Anti-Forensic Techniques Used

1. **Password Encryption** - ZIP files protected with password "nitro"
2. **Steganography** - Hidden data in images using "steg program"
3. **Evidence Destruction Instructions** - Multiple emails asking recipients to "delete this email"

---

## 📁 Repository Contents

```
├── README.md                              # This file
├── FORENSIC_ANALYSIS_REPORT.md            # Detailed forensic analysis
├── DIGITAL_FORENSICS_INVESTIGATION_REPORT.md  # Comprehensive investigation report
├── FORENSIC_INVESTIGATION_REPORT.tex      # LaTeX format report
├── Charlie_2009-*.txt                     # Email evidence files
├── Charlie_Email.zip                      # Email archive backup
├── Immortality/                           # Exfiltrated patent documents
│   ├── us005026637-001.tif
│   ├── us006982168-001.tif
│   └── Thumbs.db
├── other/                                 # Additional email evidence
├── DF Excel Report */                     # Autopsy export (Excel)
├── DF HTML Report */                      # Autopsy export (HTML)
├── DF Files - Text */                     # Autopsy export (Text)
└── DF TSK Body File */                    # Sleuth Kit body file
```

---

## 🎤 How to Present This Report

### 1. Executive Summary (5 minutes)

Start with the key findings:
- **Who:** Charlie, an employee at M57.biz
- **What:** Corporate espionage, extortion, and trade secret theft
- **When:** November-December 2009
- **How:** Used company email, encryption, and steganography
- **Impact:** $100,000 extortion attempt, client data compromised

### 2. Background & Context (5 minutes)

Explain:
- M57.biz was a prior art patent research company
- Charlie was hired as a patent researcher
- The company had confidential client relationships (Nitroba.com)
- Charlie had access to sensitive research

### 3. Timeline Presentation (10 minutes)

Walk through the timeline chronologically:
1. **Employment & Trust Building** (Nov 16-20)
2. **Data Access & Preparation** (Nov 21-30)
3. **Criminal Acts** (Dec 1-4)
4. **Aftermath & Cover-up Attempts** (Dec 5-11)

Use the timeline diagrams in the reports.

### 4. Evidence Presentation (10 minutes)

Show the key pieces of evidence:
1. **The Trade Secret Email** - Quote the original message embedded within the bounce-back in `Charlie_2009-12-02_1305_Received.txt`
2. **The Extortion Email** - Quote from `Charlie_2009-12-04_0941_Sent.txt`
3. **The Password Instructions** - Show how anti-forensics were used
4. **Financial Motive** - Vacation and car purchase plans

### 5. Technical Analysis (5 minutes)

Explain:
- How the bounce-back preserved evidence
- File hash verification methods
- ZIP archive analysis and decryption
- Timeline reconstruction methodology

### 6. Legal Implications (5 minutes)

Reference applicable laws:
- **18 U.S.C. § 1832** - Theft of Trade Secrets
- **18 U.S.C. § 873** - Blackmail
- **18 U.S.C. § 1030** - Computer Fraud and Abuse Act

### 7. Recommendations (5 minutes)

Present security improvements:
- Data Loss Prevention (DLP)
- Email monitoring
- Access controls
- Employee vetting
- Incident response planning

### 8. Q&A (5 minutes)

Be prepared to answer questions about:
- Chain of custody
- Evidence integrity
- Forensic tools used
- Admissibility in court

---

## 🛠️ Forensic Tools Used

| Tool | Purpose |
|------|---------|
| **Autopsy 4.21.0** | Primary forensic analysis platform |
| **The Sleuth Kit (TSK)** | File system analysis and body file generation |
| **PhotoRec** | Deleted file recovery |
| **Hash calculation tools** | MD5 and SHA1 verification |

---

## ⚖️ Legal Framework

This case involves potential violations of:

| Statute | Description | Evidence |
|---------|-------------|----------|
| 18 U.S.C. § 1832 | Theft of Trade Secrets | Immortality project files sent to competitor |
| 18 U.S.C. § 873 | Blackmail/Extortion | $100k demand to andy@swexpert.com |
| 18 U.S.C. § 1030 | Computer Fraud and Abuse Act | Unauthorized access for theft |
| State Laws | Trade secret misappropriation | Breach of employment duties |

---

## 📊 Evidence Integrity

All critical evidence files have been hash-verified:

| File | MD5 Hash | SHA1 Hash |
|------|----------|-----------|
| Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | cd73525ab73c19d01d9de0ea18bf9a6f932cef3e |
| us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d |
| us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f |
| microscope1.jpg | 4be2c4abb48c4389ca798e6c21736ea1 | 9aff30f601c1122ed63834ccc783901f79bad716 |

---

## 📝 About This Investigation

This is the **M57 Patents Scenario**, a well-known digital forensics case study created for educational purposes. It demonstrates:

- Insider threat detection
- Email forensics
- Timeline analysis
- Anti-forensic techniques
- Corporate espionage investigation

---

## 📚 Further Reading

- Review `FORENSIC_ANALYSIS_REPORT.md` for detailed technical analysis
- Review `DIGITAL_FORENSICS_INVESTIGATION_REPORT.md` for comprehensive investigation documentation
- Examine individual email files (`.txt`) for raw evidence
- Check the `Immortality/` folder for exfiltrated documents

---

**Case Reference:** M57-2009-Charlie  
**Classification:** Educational/Training Material  
**Report Date:** December 22, 2025

---

*This repository is for educational and training purposes in digital forensics.*
