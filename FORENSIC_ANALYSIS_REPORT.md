# Digital Forensics Analysis Report
## M57.biz Insider Threat Investigation
### Case Reference: M57-2009-Charlie

---

## Table of Contents
1. [Executive Summary](#1-executive-summary)
2. [Case Overview](#2-case-overview)
3. [Findings](#3-findings)
4. [Data Analysis](#4-data-analysis)
5. [Evidence Acquisition](#5-evidence-acquisition)
6. [Conclusion](#6-conclusion)
7. [Appendices](#7-appendices)
8. [Recommendations](#8-recommendations)

---

## 1. Executive Summary

This forensic investigation reveals a **premeditated insider threat and corporate espionage scheme** perpetrated by Charlie (charlie@m57.biz), an employee at M57.biz. The investigation has uncovered definitive evidence of:

- **Data Exfiltration**: Charlie systematically exfiltrated proprietary patent information (Immortality project files)
- **Extortion**: Charlie demanded $100,000 from an external party (andy@swexpert.com) in exchange for not disclosing prior art discoveries
- **Trade Secret Theft**: Charlie offered confidential prior art research to a competitor (jamie@project2400.com)
- **Use of Anti-Forensic Techniques**: Employment of steganography and password-protected encryption to conceal data transfers
- **Evidence Destruction Instructions**: Multiple explicit requests to recipients to delete incriminating communications

### Key Evidence Summary
| Evidence Type | File/Communication | Date | Significance |
|---------------|-------------------|------|--------------|
| Extortion Email | Charlie_2009-12-04_0941_Sent.txt | Dec 4, 2009 09:41 | $100k demand to andy@swexpert.com |
| Trade Secret Offer | Charlie_2009-12-02_1304_Sent.txt | Dec 2, 2009 13:04 | Offer to competitor |
| Password-Protected ZIP | Charlie_2009-12-04_0941_Sent_01.zip | Dec 4, 2009 09:41 | Encrypted Immortality files |
| Steganography Image | microscope1.jpg | Dec 7, 2009 11:44 | Hidden password delivery |

---

## 2. Case Overview

### 2.1 Background
M57.biz is a small startup specializing in prior art patent research services. The company employs:
- **Pat McGoo** - CEO (pat@m57.biz)
- **Charlie** - Patent Researcher (charlie@m57.biz) - **SUSPECT**
- **Jo Smith** - Patent Researcher (jo@m57.biz)
- **Terry Johnson** - IT Administrator (terry@m57.biz)

### 2.2 Investigation Scope
The investigation period spans **November 16, 2009 to December 10, 2009**, covering:
- Email communications from Charlie's account
- File system artifacts
- Attachments and metadata analysis
- Slack space recovery

### 2.3 Legal Considerations
This analysis was conducted on forensic exports provided for examination. All findings documented herein are based on digital artifacts extracted during the forensic acquisition process.

---

## 3. Findings

### 3.1 Data Correlation: Email-to-File System Linkages

#### Finding 1: Immortality Project Files
**Email Reference**: Charlie_2009-12-04_0941_Sent.txt
**Content Quote**: "I found a prior patent that will definitely invalidate your current immortality patent."

**Linked Files**:
| File Path | MD5 Hash | SHA1 Hash | Last Modified |
|-----------|----------|-----------|---------------|
| Immortality/us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d | Nov 24, 2009 13:13 |
| Immortality/us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f | Nov 24, 2009 13:15 |
| Immortality/Thumbs.db | 4db32968b696e7b7dca8e3860e52b6c3 | 380b219eccbab59e89233e0ae3c30e142ebe429a | Nov 24, 2009 13:18 |

**ZIP Archive Correlation**:
The files in the Immortality folder were packaged into a password-protected ZIP file:
| Archive | MD5 Hash | SHA1 Hash | Contents |
|---------|----------|-----------|----------|
| Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | cd73525ab73c19d01d9de0ea18bf9a6f932cef3e | 4 files (123,968 bytes) |

### 3.2 Timeline Reconstruction: Incident Window

#### Critical Incident Window: December 2-7, 2009

| Date/Time | Event | Evidence File | Significance |
|-----------|-------|---------------|--------------|
| **Dec 1, 2009 12:58** | Charlie mentions "patent research" keeping him busy | Charlie_2009-12-01_1258_Sent.txt | Cover story |
| **Dec 1, 2009 13:02** | Charlie emails girlfriend about upcoming vacation and "hot car" | Charlie_2009-12-01_1302_Sent.txt | Anticipation of illicit funds |
| **Dec 2, 2009 13:04** | **CRITICAL**: First approach to competitor (jaime@project2400.com) | Charlie_2009-12-02_1304_Sent.txt | Trade secret offer |
| **Dec 2, 2009 13:05** | Bounce-back reveals incriminating email | Charlie_2009-12-02_1305_Received.txt | Failed delivery preserved evidence |
| **Dec 2, 2009 13:25** | Second attempt to contact competitor | Charlie_2009-12-02_1325_Sent.txt | Persistence in scheme |
| **Dec 3, 2009 08:52** | Charlie takes on quantum cryptography project | Charlie_2009-12-03_0852_Sent.txt | Maintaining normal work facade |
| **Dec 3, 2009 12:16** | Charlie sends file to jamie@project2400.com | Charlie_2009-12-03_1216_Sent.txt | File exfiltration |
| **Dec 3, 2009 13:02** | Plans Mediterranean cruise with girlfriend | Charlie_2009-12-03_1302_Sent.txt | Spending plans |
| **Dec 4, 2009 09:41** | **CRITICAL**: Extortion email to andy@swexpert.com with ZIP attachment | Charlie_2009-12-04_0941_Sent.txt | $100k demand, encrypted attachment |
| **Dec 4, 2009 13:06** | **CRITICAL**: Password instructions sent (steganography reference) | Charlie_2009-12-04_1306_Sent.txt | "nitro" password, anti-forensics |
| **Dec 7, 2009 11:44** | Steganography image sent to andy@swexpert.com | other/Charlie_2009-12-07_1144_Sent.txt | Hidden data delivery |
| **Dec 8, 2009 12:59** | Charlie requests 2-week vacation | other/Charlie_2009-12-08_1259_Sent.txt | Planning departure |
| **Dec 8, 2009 14:18** | Ferrari/Shelby test drive discussion | other/Charlie_2009-12-08_1418_Sent.txt | Luxury purchases |
| **Dec 10, 2009 14:18** | New car arriving in 2 weeks | other/Charlie_2009-12-10_1418_Sent.txt | Confirmed purchase |

### 3.3 Artifact Analysis

#### 3.3.1 Suspicious Executable/Archive Artifacts

**Password-Protected ZIP File**
- **File**: Charlie_2009-12-04_0941_Sent_01.zip
- **Type**: Zip archive data, at least v1.0 to extract, compression method=store
- **Password**: "nitro" (revealed in Charlie_2009-12-04_1306_Sent.txt)
- **Contents**:
  ```
  Length      Date    Time    Name
  ---------  ---------- -----   ----
          0  2009-11-24 13:18   Immortality/
       7680  2009-11-24 13:18   Immortality/Thumbs.db
      39692  2009-11-24 13:13   Immortality/us005026637-001.tif
      76596  2009-11-24 13:15   Immortality/us006982168-001.tif
  ---------                     -------
     123968                     4 files
  ```

**Significance**: The Thumbs.db file indicates these files were viewed/accessed on a Windows system. The TIF files are patent documents related to the "Immortality" project that M57.biz was researching for a client.

#### 3.3.2 Steganography Image
- **File**: other/Charlie_2009-12-07_1144_Sent_microscope1.jpg
- **MD5**: 4be2c4abb48c4389ca798e6c21736ea1
- **SHA1**: 9aff30f601c1122ed63834ccc783901f79bad716
- **Size**: 136,274 bytes
- **Significance**: Email states "The password for the zip file will be hidden in the next picture I send you" and later references using a "steg program"

#### 3.3.3 Thumbs.db Analysis
- **File**: Immortality/Thumbs.db
- **Type**: Composite Document File V2 Document
- **MD5**: 4db32968b696e7b7dca8e3860e52b6c3
- **SHA1**: 380b219eccbab59e89233e0ae3c30e142ebe429a
- **Significance**: Windows thumbnail cache indicates file viewing activity; contains cached thumbnails of accessed images

### 3.4 Anti-Forensics Detection

#### 3.4.1 Evidence of Encryption
| Indicator | Location | Details |
|-----------|----------|---------|
| Password-protected ZIP | Charlie_2009-12-04_0941_Sent_01.zip | Password: "nitro" |
| Steganography | microscope1.jpg | Hidden data mentioned in emails |
| Reference to "steg program" | Charlie_2009-12-04_1306_Sent.txt | Explicit anti-forensics tool |

#### 3.4.2 Instructions to Delete Data
| Email | Date | Quote |
|-------|------|-------|
| Charlie_2009-12-02_1304_Sent.txt | Dec 2, 2009 | "Make sure you delete this email." |
| Charlie_2009-12-04_0941_Sent.txt | Dec 4, 2009 | "Don't involve the cops or this information will go public." |
| Charlie_2009-12-04_1306_Sent.txt | Dec 4, 2009 | "And don't forget to delete these emails." |
| other/Charlie_2009-12-07_1144_Sent.txt | Dec 7, 2009 | "Make sure you delete this." |

#### 3.4.3 Communication Obfuscation
Charlie used multiple external email addresses to conduct illicit communications:
- jaime@project2400.com (competitor contact - initial misspelling, caused bounce-back)
- jamie@project2400.com (competitor contact - corrected spelling used in subsequent emails)
- andy@swexpert.com (extortion victim)
- alix.pery@yahoo.com (personal - vacation plans)
- rubinfritz31@mail.com (personal - car purchase)

**Note**: The misspelling of jaime@project2400.com vs jamie@project2400.com is forensically significant. The initial email to jaime@ bounced back (Dec 2, 2009 13:05), which preserved the incriminating evidence. Charlie subsequently corrected the spelling to jamie@ in later communications.

---

## 4. Data Analysis

### 4.1 Email Analysis Summary

**Total Emails Analyzed**: 90+ email files and slack space files
**Suspect Communications**: 15 highly suspicious emails
**External Contacts Identified**: 5 non-company email addresses

### 4.2 File Metadata Analysis

#### PDF Attachments (Legitimate Work Files)
| File | MD5 | SHA1 | Pages |
|------|-----|------|-------|
| 95253.SCSI.Mathew+Malizia.pdf | 22f728e4c307c604f806dfc70bf12931 | fcd000a06a885c18e933dd4a9457d886f41bd403 | 7 |
| 97315.ScatterGatherIO.Julio+Molock.pdf | 4c8cb6c9d8f0670d2c5127f30bfff6c9 | e340ad755e86dc2c4cc95250dec16fc6dd2734db | 4 |
| 98521.WANs.Greg+Hillier.pdf | 3daefc16b545c020b809939684b87a9f | e96efeaa874def987c8807287417d6c885e11deb | 6 |
| 99202.ComplexityTheory.Louisa+Fleet.pdf | 409344fa2d71fdd651ccb4eaa0f2ce2d | c43f3ecc14879014b42e4e3ef85fe276efca7c65 | 6 |
| PETEFFS.pdf | 1cb74f2c1f8a8a801e0c91049244e82f | 91f3a62036c87983d528ecd869ce39e4b8c2dd7a | 3 |
| US5041044.pdf | 9aabd3906236410aa524bf73c41e4593 | 31f90827b4d210de673e2fbefbf23b11794a9066 | 15 |

#### Exfiltrated Files (Immortality Project)
| File | MD5 | SHA1 | Size |
|------|-----|------|------|
| us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d | 39,692 bytes |
| us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f | 76,596 bytes |

### 4.3 Slack Space Analysis

Multiple slack files were recovered containing residual data from deleted content:
- Total slack files: 30+
- Notable recovery: Email headers and partial content fragments
- Significance: Demonstrates data persistence despite user actions

### 4.4 Financial Motivation Analysis

| Evidence | Implied Amount | Source |
|----------|---------------|--------|
| Extortion demand | $100,000 | "I want 100k or I'll release this publicly" |
| Vacation plans | Mediterranean cruise | Multiple emails to alix.pery@yahoo.com |
| Car purchase | Ferrari/Shelby (~$50,000-$80,000) | Emails to rubinfritz31@mail.com |
| Extended vacation | 2 weeks off | Email to Pat McGoo |

---

## 5. Evidence Acquisition

### 5.1 Digital Evidence Inventory

| Evidence ID | File Path | MD5 Hash | SHA1 Hash | Type | Acquisition Note |
|-------------|-----------|----------|-----------|------|------------------|
| E001 | Charlie_2009-12-04_0941_Sent.txt | - | - | Email | Extortion communication |
| E002 | Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | cd73525ab73c19d01d9de0ea18bf9a6f932cef3e | Archive | Password-protected exfiltration |
| E003 | Charlie_2009-12-02_1304_Sent.txt | - | - | Email | Trade secret offer |
| E004 | Charlie_2009-12-02_1305_Received.txt | - | - | Email | Bounce-back preservation |
| E005 | Charlie_2009-12-04_1306_Sent.txt | - | - | Email | Password/steganography instructions |
| E006 | other/microscope1.jpg | 4be2c4abb48c4389ca798e6c21736ea1 | 9aff30f601c1122ed63834ccc783901f79bad716 | Image | Steganography carrier |
| E007 | Immortality/us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d | Document | Exfiltrated patent |
| E008 | Immortality/us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f | Document | Exfiltrated patent |
| E009 | Immortality/Thumbs.db | 4db32968b696e7b7dca8e3860e52b6c3 | 380b219eccbab59e89233e0ae3c30e142ebe429a | System | Windows artifact |
| E010 | Charlie_2009-12-01_1302_Sent.txt | - | - | Email | Financial motivation |
| E011 | Charlie_2009-12-03_1302_Sent.txt | - | - | Email | Travel plans with proceeds |
| E012 | Charlie_2009-12-02_1305_Received_Interested-.eml | - | - | Email | Raw email headers |

### 5.2 Chain of Custody
All evidence files maintain their original filenames and metadata from the forensic acquisition. Hash values were calculated post-acquisition to verify integrity.

---

## 6. Conclusion

### 6.1 Summary of Findings

The forensic analysis conclusively establishes that **Charlie (charlie@m57.biz)** engaged in:

1. **Corporate Espionage**: Exfiltrated proprietary Immortality project files containing patent research
2. **Extortion**: Demanded $100,000 from andy@swexpert.com to suppress disclosure of prior art findings
3. **Trade Secret Misappropriation**: Offered confidential work product to competitor jamie@project2400.com
4. **Anti-Forensic Activities**: Employed encryption, steganography, and instructed evidence destruction

### 6.2 Criminal Implications

Charlie's actions potentially violate:
- **18 U.S.C. § 1832** - Theft of Trade Secrets
- **18 U.S.C. § 873** - Blackmail
- **18 U.S.C. § 1030** - Computer Fraud and Abuse Act
- Various state trade secret and computer crime statutes

### 6.3 Evidence Strength Assessment

| Finding | Evidence Strength | Corroborating Evidence |
|---------|------------------|------------------------|
| Data Exfiltration | **STRONG** | ZIP file contents match Immortality folder |
| Extortion | **STRONG** | Multiple emails with explicit demands |
| Trade Secret Theft | **STRONG** | Email communications with competitor |
| Anti-Forensics | **STRONG** | Encryption, steganography, deletion instructions |
| Financial Motive | **STRONG** | Vacation/car purchase communications |

---

## 7. Appendices

### Appendix A: Complete Timeline of Suspicious Activity

```
Nov 16, 2009 11:02 - Charlie joins M57.biz
Nov 24, 2009 13:13 - Immortality/us005026637-001.tif last modified
Nov 24, 2009 13:15 - Immortality/us006982168-001.tif last modified
Nov 24, 2009 13:18 - Immortality folder/Thumbs.db created
Dec 01, 2009 13:02 - Charlie hints at upcoming money to girlfriend
Dec 02, 2009 13:04 - First contact with competitor (failed delivery)
Dec 02, 2009 13:05 - Bounce-back preserves evidence
Dec 02, 2009 13:25 - Second contact attempt with competitor
Dec 03, 2009 12:16 - File sent to competitor contact
Dec 03, 2009 13:02 - Mediterranean cruise planning
Dec 04, 2009 09:41 - Extortion email with encrypted ZIP sent
Dec 04, 2009 13:06 - Password instructions sent ("nitro")
Dec 07, 2009 11:44 - Steganography image sent
Dec 08, 2009 12:59 - 2-week vacation request
Dec 08, 2009 14:18 - Ferrari/Shelby test drive plans
Dec 10, 2009 14:18 - Car delivery confirmation
```

### Appendix B: Email Headers Analysis (Sample)

**From Charlie_2009-12-02_1305_Received_Interested-.eml:**
```
X-ASG-Debug-ID: 1259787905-6f178ea50001-ViaRji
Received: from domex (domex.nps.edu [205.155.65.103])
  by mustang.nps.edu with ESMTP id RkloEmAYo22C1XPU
  for <jaime@project2400.com>; Wed, 02 Dec 2009 13:05:05 -0800 (PST)
X-Barracuda-Envelope-From: charlie@m57.biz
Received: from [192.168.1.104] (unknown [192.168.1.104])
  by domex (Postfix) with ESMTP id 9AB35543CBE
Message-ID: <4B16D65D.4060604@m57.biz>
Date: Wed, 02 Dec 2009 13:04:29 -0800
From: Charlie <charlie@m57.biz>
User-Agent: Thunderbird 2.0.0.23 (Windows/20090812)
```

**Key Observations:**
- Origin IP: 192.168.1.104 (internal network)
- Mail Client: Thunderbird 2.0.0.23 on Windows
- Mail Server: domex.nps.edu (205.155.65.103)

### Appendix C: File Hash Registry

| File | MD5 | SHA1 |
|------|-----|------|
| Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | cd73525ab73c19d01d9de0ea18bf9a6f932cef3e |
| Immortality/us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d |
| Immortality/us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f |
| Immortality/Thumbs.db | 4db32968b696e7b7dca8e3860e52b6c3 | 380b219eccbab59e89233e0ae3c30e142ebe429a |
| other/microscope1.jpg | 4be2c4abb48c4389ca798e6c21736ea1 | 9aff30f601c1122ed63834ccc783901f79bad716 |
| 95253.SCSI.Mathew+Malizia.pdf | 22f728e4c307c604f806dfc70bf12931 | fcd000a06a885c18e933dd4a9457d886f41bd403 |
| 97315.ScatterGatherIO.Julio+Molock.pdf | 4c8cb6c9d8f0670d2c5127f30bfff6c9 | e340ad755e86dc2c4cc95250dec16fc6dd2734db |
| 98521.WANs.Greg+Hillier.pdf | 3daefc16b545c020b809939684b87a9f | e96efeaa874def987c8807287417d6c885e11deb |
| 99202.ComplexityTheory.Louisa+Fleet.pdf | 409344fa2d71fdd651ccb4eaa0f2ce2d | c43f3ecc14879014b42e4e3ef85fe276efca7c65 |
| PETEFFS.pdf | 1cb74f2c1f8a8a801e0c91049244e82f | 91f3a62036c87983d528ecd869ce39e4b8c2dd7a |
| US5041044.pdf | 9aabd3906236410aa524bf73c41e4593 | 31f90827b4d210de673e2fbefbf23b11794a9066 |

### Appendix D: Key Verbatim Evidence Quotes

**Extortion (Dec 4, 2009):**
> "I found a prior patent that will definitely invalidate your current immortality patent. You should have used my boss's prior art services, but, oh well, I'll just use your negligence to benefit me. I want 100k or I'll release this publicly. I don't need to tell you how much this will hurt your business if I go public with this. Don't involve the cops or this information will go public."

**Trade Secret Offer (Dec 2, 2009):**
> "I have something that you'll definitely be interested in. It concerns your competitor. I'm doing a prior art search for them. Want to know what I've found? You know my price. I'll send you the goods after I see half in my account. Make sure you delete this email."

**Anti-Forensics Instructions (Dec 4, 2009):**
> "Got the deposit. The password to get the info is nitro. Use the steg program we talked about. And don't forget to delete these emails."

---

## 8. Recommendations

### 8.1 Immediate Actions

1. **Preserve Evidence**: Ensure all forensic images and working copies are secured and hash-verified
2. **Legal Consultation**: Engage corporate counsel and consider law enforcement notification
3. **Access Revocation**: Immediately disable Charlie's network and system access
4. **Client Notification**: Assess obligation to notify clients whose data may have been compromised

### 8.2 Investigation Extensions

1. **Steganography Analysis**: Extract hidden data from microscope1.jpg using steganography tools
2. **ZIP File Decryption**: Verify contents of password-protected archive using password "nitro"
3. **Network Forensics**: Review firewall and proxy logs for additional data exfiltration
4. **Financial Investigation**: Subpoena bank records to trace payments

### 8.3 Security Improvements

1. **Data Loss Prevention (DLP)**: Implement DLP solutions to detect sensitive data transfers
2. **Email Monitoring**: Deploy content inspection for external email communications
3. **Access Controls**: Implement least-privilege access to confidential project files
4. **Employee Training**: Conduct regular security awareness training
5. **Exit Procedures**: Develop comprehensive off-boarding procedures for employee departures
6. **Encryption Controls**: Prohibit unauthorized encryption of company data

### 8.4 Policy Development

1. **Acceptable Use Policy**: Update to explicitly prohibit data exfiltration
2. **Confidentiality Agreements**: Strengthen non-disclosure agreements
3. **Incident Response Plan**: Develop formal incident response procedures
4. **Monitoring Disclosure**: Implement lawful employee monitoring with proper notification

---

**Report Prepared By:** Digital Forensics Analysis System  
**Date:** December 22, 2025  
**Classification:** Confidential - Legal Privilege Applies

---

*This report is based solely on the digital artifacts provided for analysis. Additional investigation may reveal further evidence. All findings should be independently verified before use in legal proceedings.*
