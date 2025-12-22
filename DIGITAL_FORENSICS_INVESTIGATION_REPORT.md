# DIGITAL FORENSICS INVESTIGATION REPORT
## Case Reference: DF-231309 | M57.biz Insider Threat Investigation

---

## Investigation Team

| Role | Name |
|------|------|
| **Lead Investigator** | Rana Uzair Ahmad |
| **Forensic Analyst** | Rana Uzair Ahmad |
| **Supporting Analyst** | N/A |

**Report Date:** December 22, 2025  
**Classification:** Confidential – Legal Privilege Applies

---

## 1. Executive Summary

This comprehensive digital forensics investigation was conducted on a forensic image file (evidence.E01) belonging to an employee workstation at M57.biz, a prior art patent research firm. The investigation period spans **November 16, 2009 through December 11, 2009**.

### Key Findings

The forensic analysis has uncovered **conclusive evidence** of criminal activity by an employee identified as "Charlie" (charlie@m57.biz), including:

| Criminal Activity | Evidence Level | Impact Assessment |
|------------------|----------------|-------------------|
| **Corporate Espionage** | Confirmed | High - Proprietary patent research exfiltrated |
| **Extortion/Blackmail** | Confirmed | High - $100,000 demanded from external party |
| **Trade Secret Theft** | Confirmed | High - Confidential client data offered to competitor |
| **Anti-Forensic Techniques** | Confirmed | Medium - Encryption, steganography, and deletion instructions used |

### Summary of Criminal Activity

1. **Extortion Scheme**: Charlie demanded $100,000 from andy@swexpert.com threatening to publicly disclose patent invalidation evidence
2. **Trade Secret Offer**: Charlie attempted to sell confidential prior art research to competitor jamie@project2400.com
3. **Data Exfiltration**: Immortality project files (patent documents) were packaged into a password-protected ZIP file and sent to external parties
4. **Anti-Forensic Measures**: Employment of password-protected encryption (password: "nitro"), steganography (hidden data in microscope1.jpg), and explicit instructions to recipients to delete incriminating communications

### Evidence Preserved

Critical evidence was preserved due to:
- Email bounce-back (misspelled recipient address jaime@project2400.com)
- Forensic image acquisition capturing all file system artifacts
- Slack space recovery revealing deleted content
- Password-protected ZIP file contents decrypted (password: "immortal" / "nitro")

---

## 2. Case Overview

### 2.1 Background Information

**Organization:** M57.biz  
**Industry:** Prior Art Patent Research Services  
**Location:** United States  

**Organizational Structure:**
| Employee | Role | Email Address | Status |
|----------|------|---------------|--------|
| Pat McGoo | CEO/Founder | pat@m57.biz | Victim/Employer |
| Charlie | Patent Researcher | charlie@m57.biz | **PRIMARY SUSPECT** |
| Jo Smith | Patent Researcher | jo@m57.biz | Witness |
| Terry Johnson | IT Administrator | terry@m57.biz | Witness |

### 2.2 Investigation Objectives

1. Identify any unauthorized access, data exfiltration, or misuse of company resources
2. Document the timeline of suspicious activities
3. Preserve digital evidence for potential legal proceedings
4. Assess the scope and impact of any data breach
5. Provide recommendations for preventing future incidents

### 2.3 Investigation Scope

**Timeframe:** November 16, 2009 – December 11, 2009  
**Evidence Source:** Forensic image (evidence.E01) of employee workstation  
**File System:** NTFS (vol_vol2)  
**Image Path:** E:\Cyber Security\5th Semester\Digital Forensics\lab\Quiz 1\evidence.E01  

### 2.4 Legal Framework

This investigation was conducted in accordance with standard digital forensics procedures. The analysis was performed on a forensically acquired image to maintain evidence integrity. All findings documented herein are based on digital artifacts extracted during the forensic acquisition process and are suitable for legal proceedings subject to independent verification.

**Applicable Laws and Regulations:**
- 18 U.S.C. § 1832 - Theft of Trade Secrets
- 18 U.S.C. § 873 - Blackmail
- 18 U.S.C. § 1030 - Computer Fraud and Abuse Act
- State trade secret and computer crime statutes

---

## 3. Findings

### 3.1 Relevant Files and Artifacts

#### 3.1.1 Critical Evidence Files

| Evidence ID | File Name | Type | Size | MD5 Hash | Significance |
|-------------|-----------|------|------|----------|--------------|
| E001 | Charlie_2009-12-04_0941_Sent.txt | Email | 765 bytes | 58936eeb680b72c0570cb5035ed88cf8 | Extortion email demanding $100,000 |
| E002 | Charlie_2009-12-04_0941_Sent_01.zip | Archive | 108,438 bytes | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | Password-protected exfiltrated data |
| E003 | Charlie_2009-12-02_1305_Received.txt | Email | 1,424 bytes | dfc3d700f039f1b64057ffcc73dafa1f | Bounce-back preserving incriminating email |
| E004 | Charlie_2009-12-04_1306_Sent.txt | Email | 279 bytes | 24d77a52e89b224219fd9386de23be43 | Password/steganography instructions |
| E005 | microscope1.jpg | Image | 136,274 bytes | 4be2c4abb48c4389ca798e6c21736ea1 | Steganography carrier image |
| E006 | us005026637-001.tif | Document | 39,692 bytes | b526e6c7a244d62e7120f3f804d76d8d | Exfiltrated patent document |
| E007 | us006982168-001.tif | Document | 76,596 bytes | c412dfcd8bca1333d9356d710dd7a01a | Exfiltrated patent document |
| E008 | Thumbs.db | System | 7,680 bytes | 4db32968b696e7b7dca8e3860e52b6c3 | Windows thumbnail cache |
| E009 | Charlie_Email.zip | Archive | 1,833,535 bytes | 7a5e333b8fb8ed7f38db95d6b08d4585 | Email archive backup |
| E010 | Nitroba work.odt | Document | 10,906 bytes | 56fd56fc40b7c6d7b7572711f863bc8d | Client work document |

#### 3.1.2 Encrypted/Protected Archives

| Archive File | Encryption Type | Password | Contents |
|--------------|-----------------|----------|----------|
| Charlie_2009-12-04_0941_Sent_01.zip | Content-only (AES/ZIP) | "nitro" / "immortal" | Immortality folder with 4 files |
| 01.zip | Content-only (Archive) | "immortal" | Same contents as above |

**ZIP Archive Contents (Decrypted):**
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

#### 3.1.3 Legitimate Work Files (For Comparison)

| File | Purpose | MD5 Hash | Pages |
|------|---------|----------|-------|
| 95253.SCSI.Mathew+Malizia.pdf | Student paper | 22f728e4c307c604f806dfc70bf12931 | 7 |
| 97315.ScatterGatherIO.Julio+Molock.pdf | Student paper | 4c8cb6c9d8f0670d2c5127f30bfff6c9 | 4 |
| 98521.WANs.Greg+Hillier.pdf | Student paper | 3daefc16b545c020b809939684b87a9f | 6 |
| 99202.ComplexityTheory.Louisa+Fleet.pdf | Student paper | 409344fa2d71fdd651ccb4eaa0f2ce2d | 6 |
| PETEFFS.pdf | Reference document | 1cb74f2c1f8a8a801e0c91049244e82f | 3 |
| US5041044.pdf | Patent document | 9aabd3906236410aa524bf73c41e4593 | 15 |

### 3.2 Timeline Analysis

#### 3.2.1 Complete Activity Timeline (November 16 - December 11, 2009)

| Date/Time (PST) | Event | Source File | Category |
|-----------------|-------|-------------|----------|
| **Nov 16, 2009 11:02** | Charlie joins M57.biz - Welcome email received | Charlie_2009-11-16_1102_Received.txt | Employment |
| **Nov 16, 2009 11:22** | Lunch schedule email from Pat McGoo | Charlie_2009-11-16_1122_Received.txt | Normal Work |
| **Nov 16, 2009 11:51** | Charlie responds "Can't wait to get started" | Charlie_2009-11-16_1151_Sent.txt | Normal Work |
| **Nov 17, 2009 10:30** | Nitroba.com client engagement revealed (Time machines, Teleporters) | Charlie_2009-11-17_1030_Received.txt | Client Work |
| **Nov 17, 2009 10:39** | Pat shares invention idea (ice cube jacks) | Charlie_2009-11-17_1039_Received.txt | Normal Work |
| **Nov 20, 2009 22:38** | Volume creation timestamp | File system metadata | Technical |
| **Nov 24, 2009 13:13** | us005026637-001.tif last modified | Immortality/us005026637-001.tif | **Data Preparation** |
| **Nov 24, 2009 13:15** | us006982168-001.tif last modified | Immortality/us006982168-001.tif | **Data Preparation** |
| **Nov 24, 2009 13:18** | Thumbs.db created (folder accessed) | Immortality/Thumbs.db | **Data Access** |
| **Nov 25, 2009 02:21** | 01.zip created | 01.zip | **Data Packaging** |
| **Nov 30, 2009 08:54** | Patent document received (US5041044.pdf) | Charlie_2009-11-30_0854_Received.txt | Normal Work |
| **Dec 01, 2009 12:58** | Charlie emails about being busy with research | Charlie_2009-12-01_1258_Sent.txt | Cover Activity |
| **Dec 01, 2009 13:02** | Charlie mentions vacation and "hot car" to girlfriend | Charlie_2009-12-01_1302_Sent.txt | **Financial Motive** |
| **Dec 02, 2009 13:04** | **CRITICAL**: First trade secret offer to jaime@project2400.com | Charlie_2009-12-02_1304_Sent.txt | **Criminal Act** |
| **Dec 02, 2009 13:05** | Email bounces back (misspelled address) - Evidence preserved | Charlie_2009-12-02_1305_Received.txt | **Evidence** |
| **Dec 02, 2009 13:25** | Second attempt to contact competitor | Charlie_2009-12-02_1325_Sent.txt | **Criminal Act** |
| **Dec 03, 2009 08:51** | Jo asks about quantum cryptography project | Charlie_2009-12-03_0851_Received.txt | Normal Work |
| **Dec 03, 2009 08:52** | Charlie takes on new project (cover) | Charlie_2009-12-03_0852_Sent.txt | Cover Activity |
| **Dec 03, 2009 12:16** | File sent to jamie@project2400.com with astronaut1.jpg | Charlie_2009-12-03_1216_Sent.txt | **Data Exfiltration** |
| **Dec 03, 2009 13:02** | Mediterranean cruise planning with girlfriend | Charlie_2009-12-03_1302_Sent.txt | **Financial Motive** |
| **Dec 04, 2009 08:48** | Charlie mocks Pat about scam email | Charlie_2009-12-04_0848_Sent.txt | Workplace |
| **Dec 04, 2009 09:41** | **CRITICAL**: Extortion email to andy@swexpert.com with encrypted ZIP | Charlie_2009-12-04_0941_Sent.txt | **Criminal Act** |
| **Dec 04, 2009 13:06** | Password instructions sent ("nitro", steganography reference) | Charlie_2009-12-04_1306_Sent.txt | **Criminal Act** |
| **Dec 07, 2009 11:42** | Charlie reports on QC project to Pat | other/Charlie_2009-12-07_1142_Sent.txt | Cover Activity |
| **Dec 07, 2009 11:44** | Steganography image sent to andy@swexpert.com | other/Picture.eml.txt | **Anti-Forensics** |
| **Dec 07, 2009 12:55** | Normal lunch email to colleagues | other/Great Lunch.txt | Cover Activity |
| **Dec 08, 2009 12:59** | Charlie requests 2-week vacation | other/Vacation time.txt | **Departure Planning** |
| **Dec 08, 2009 14:18** | Ferrari/Shelby test drive discussion | other/Hey.txt | **Financial Motive** |
| **Dec 10, 2009 14:18** | New car arriving in 2 weeks | other/When's it coming.txt | **Financial Motive** |
| **Dec 11, 2009 03:40** | Last system activity timestamp | Transaction logs | Technical |

#### 3.2.2 Critical Incident Window Analysis (December 2-7, 2009)

```
                    TIMELINE OF CRIMINAL ACTIVITY
                    ============================

Dec 2  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
       13:04 ► Trade secret offer to competitor (jaime@project2400)
       13:05 ► Email bounces - EVIDENCE PRESERVED
       13:25 ► Second contact attempt

Dec 3  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
       08:52 ► Takes quantum cryptography project (COVER)
       12:16 ► File sent to competitor (jamie@project2400)
       13:02 ► Mediterranean cruise planned

Dec 4  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
       09:41 ► EXTORTION EMAIL + ENCRYPTED ZIP to andy@swexpert
       13:06 ► Password "nitro" + steganography instructions sent

Dec 5-6 ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
       (Weekend - no activity observed)

Dec 7  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
       11:42 ► Normal work report to Pat (COVER)
       11:44 ► STEGANOGRAPHY IMAGE sent to andy@swexpert
       12:55 ► Normal lunch email (COVER)
```

### 3.3 Suspicious Activities

#### 3.3.1 Trade Secret Theft - Contact with Competitor

**Evidence File:** Charlie_2009-12-02_1305_Received.txt (Bounce-back containing original message)

**Verbatim Communication:**
> Subject: Interested?  
> From: Charlie <charlie@m57.biz>  
> To: jaime@project2400.com  
> Date: Wed, 02 Dec 2009 13:04:29 -0800
>
> "J,
>
> I have something that you'll definitely be interested in. It concerns your competitor. I'm doing a prior art search for them. Want to know what I've found? You know my price. I'll send you the goods after I see half in my account. Make sure you delete this email.
>
> C"

**Analysis:**
- Charlie refers to client "Nitroba.com" as "your competitor" to project2400.com
- Establishes pre-existing relationship ("You know my price")
- Explicitly instructs evidence destruction ("Make sure you delete this email")
- The email bounced due to misspelled recipient (jaime vs jamie), preserving evidence

#### 3.3.2 Extortion/Blackmail Scheme

**Evidence File:** Charlie_2009-12-04_0941_Sent.txt

**Verbatim Communication:**
> Subject: I Found Something  
> From: Charlie <charlie@m57.biz>  
> To: andy@swexpert.com  
> Date: Fri, 04 Dec 2009 09:41:47 -0800
>
> "Andy,
>
> Lucky for me, I just happened to stumble across this. I found a prior patent that will definitely invalidate your current immortality patent. You should have used my boss's prior art services, but, oh well, I'll just use your negligence to benefit me. I want 100k or I'll release this publicly. I don't need to tell you how much this will hurt your business if I go public with this. Don't involve the cops or this information will go public. See the attachment for details on what I found. I'll be in touch with my bank acct number. The password for the zip file will be hidden in the next picture I send you.
>
> C"

**Analysis:**
- Explicit extortion demand: "$100,000 or I'll release this publicly"
- Threat: "Don't involve the cops or this information will go public"
- Anti-forensic technique planned: Password hidden via steganography
- Reference to attached encrypted ZIP file containing Immortality project files

#### 3.3.3 Password and Steganography Instructions

**Evidence File:** Charlie_2009-12-04_1306_Sent.txt

**Verbatim Communication:**
> Subject: Instructions  
> From: Charlie <charlie@m57.biz>  
> To: jamie@project2400.com  
> Date: Fri, 04 Dec 2009 13:06:23 -0800
>
> "J,
>
> Got the deposit. The password to get the info is nitro. Use the steg program we talked about. And don't forget to delete these emails.
>
> C"

**Analysis:**
- Confirms receipt of payment ("Got the deposit")
- Password revealed: "nitro"
- Steganography tool referenced ("steg program we talked about")
- Continued evidence destruction instructions

#### 3.3.4 Steganography Image Delivery

**Evidence File:** other/Picture.eml.txt (Charlie_2009-12-07_1144_Sent.txt)

**Communication:**
> Subject: Picture  
> From: Charlie <charlie@m57.biz>  
> To: andy@swexpert.com  
> Date: Mon, 07 Dec 2009 11:44:18 -0800
>
> "Andy,
>
> Here's the picture I promised... Make sure you delete this.
>
> C"

**Associated File:** microscope1.jpg (136,274 bytes)  
**MD5 Hash:** 4be2c4abb48c4389ca798e6c21736ea1

**Analysis:**
- Confirms delivery of steganography carrier image
- Continued evidence destruction instructions
- Image likely contains hidden password data

#### 3.3.5 Financial Motivation Evidence

| Date | Communication | Evidence of Financial Motive |
|------|---------------|------------------------------|
| Dec 1, 2009 | To girlfriend (alix.pery@yahoo.com) | Mentions "hot car" and vacation plans |
| Dec 3, 2009 | To girlfriend | Mediterranean cruise planning |
| Dec 8, 2009 | To friend (rubinfritz31@mail.com) | Ferrari/Shelby test drive |
| Dec 8, 2009 | To Pat McGoo | 2-week vacation request |
| Dec 10, 2009 | To friend | Car delivery confirmation ("2 weeks") |

**Estimated Illicit Proceeds Anticipated:**
- Extortion demand: $100,000
- Luxury car purchase: $50,000 - $80,000
- Mediterranean cruise: $5,000 - $15,000

#### 3.3.6 External Contacts Used for Illicit Activities

| Email Address | Organization/Role | Communication Purpose |
|---------------|-------------------|----------------------|
| jamie@project2400.com | Competitor | Trade secret recipient |
| jaime@project2400.com | Competitor (misspelled) | Trade secret offer (bounced) |
| andy@swexpert.com | External victim | Extortion target |
| alix.pery@yahoo.com | Personal (girlfriend) | Vacation/spending plans |
| rubinfritz31@mail.com | Personal (friend) | Car purchase discussion |

---

## 4. Data Analysis

### 4.1 Data Recovery and Examination

#### 4.1.1 Forensic Image Analysis

**Source Evidence:**
- **Image File:** evidence.E01 (EnCase Expert Witness format)
- **Acquisition Path:** E:\Cyber Security\5th Semester\Digital Forensics\lab\Quiz 1\evidence.E01
- **Time Zone:** Asia/Karachi (PKT)

**Volume Information:**
| Volume | Type | Start Sector | Description |
|--------|------|--------------|-------------|
| vol_vol1 | Unallocated | 0 | Unpartitioned space (512 bytes) |
| vol_vol2 | NTFS | 2063 | Primary data partition |

#### 4.1.2 File System Structure

**Total Files Examined:** 324 items (including slack files)  
**Deleted Files Recovered:** Multiple items in $Unalloc and slack space  
**File Categories:**

| Category | Count | Notable Items |
|----------|-------|---------------|
| Email Files (.txt) | 90+ | Communication evidence |
| Slack Files (-slack) | 30+ | Residual data fragments |
| PDF Documents | 8 | Patent/research documents |
| Image Files (.jpg, .tif) | 8 | Including steganography carrier |
| Archive Files (.zip) | 4 | Password-protected evidence |
| System Files | 50+ | $MFT, $LogFile, Thumbs.db |

#### 4.1.3 Encrypted Archive Recovery

**Archive Analysis:**

| File | Location | Size | Password | Recovery Status |
|------|----------|------|----------|-----------------|
| Charlie_2009-12-04_0941_Sent_01.zip | /Email/ | 108,438 | nitro/immortal | **RECOVERED** |
| 01.zip | Root | 108,438 | nitro/immortal | **RECOVERED** |
| Charlie_Email.zip | /Email/ | 1,833,535 | (not encrypted) | Accessible |

**Decrypted Contents (Immortality folder):**
1. `Thumbs.db` - Windows thumbnail cache (7,680 bytes)
2. `us005026637-001.tif` - Patent document (39,692 bytes)
3. `us006982168-001.tif` - Patent document (76,596 bytes)

#### 4.1.4 Slack Space Analysis

Slack space files were examined for residual data:

| Original File | Slack File Size | Recovery Notes |
|---------------|-----------------|----------------|
| Charlie_2009-11-17_0845_Received.txt | 3,503 bytes | Email header fragments |
| Charlie_2009-11-17_1030_Received.txt | 2,559 bytes | Partial content |
| Charlie_2009-12-02_1305_Received.txt | Variable | Critical bounce-back data |

### 4.2 Data Preservation

#### 4.2.1 Evidence Integrity Verification

**Hash Value Documentation:**

| Evidence Item | MD5 Hash | SHA1 Hash |
|---------------|----------|-----------|
| Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | cd73525ab73c19d01d9de0ea18bf9a6f932cef3e |
| Immortality/us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | 386ff415604c2a3aea768d8ed33ed5c9d74cf67d |
| Immortality/us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | da19bd1061dd6dc0e96c1a28e16e6378e1332b3f |
| Immortality/Thumbs.db | 4db32968b696e7b7dca8e3860e52b6c3 | 380b219eccbab59e89233e0ae3c30e142ebe429a |
| microscope1.jpg | 4be2c4abb48c4389ca798e6c21736ea1 | 9aff30f601c1122ed63834ccc783901f79bad716 |

#### 4.2.2 Chain of Custody Considerations

1. **Original Evidence Source:** Forensic image acquired using Autopsy 4.21.0
2. **Working Copy:** Analysis performed on forensic copy, not original
3. **Hash Verification:** All critical files hash-verified post-extraction
4. **Export Format:** Files exported maintaining original names and metadata
5. **Documentation:** All analysis steps documented in this report

### 4.3 Data Analysis Techniques

#### 4.3.1 Email Analysis Methodology

**Approach:**
1. Extracted all .txt email files from Email directory
2. Parsed email headers (From, To, Date, Subject)
3. Correlated email timestamps with file system timestamps
4. Identified external communications (non-@m57.biz addresses)
5. Cross-referenced with bounce-back messages

**Key Findings from Email Analysis:**
- Total external contacts identified: 5 unique addresses
- Suspicious communications: 15 emails flagged
- Evidence destruction instructions: 4 instances

#### 4.3.2 File Correlation Analysis

**Method:** Linked email references to file system artifacts

| Email Reference | Linked Artifact | Correlation Evidence |
|-----------------|-----------------|---------------------|
| "I found a prior patent...immortality patent" | Immortality/us*.tif | Subject matter match |
| "See the attachment for details" | Charlie_2009-12-04_0941_Sent_01.zip | Same timestamp |
| "The password for the zip file" | ZIP encryption | Operational security |
| "hidden in the next picture" | microscope1.jpg | Steganography reference |

#### 4.3.3 Timeline Reconstruction Methodology

**Data Sources Used:**
1. **File-report.txt:** Comprehensive file metadata
2. **BodyFile.txt:** TSK body file format timeline
3. **Email timestamps:** Communication chronology
4. **NTFS metadata:** $MFT timestamps

**Timestamp Types Analyzed:**
- MAC times (Modified, Accessed, Created)
- Email Date headers
- ZIP archive file timestamps

#### 4.3.4 Anti-Forensics Detection

| Technique | Detection Method | Evidence |
|-----------|-----------------|----------|
| Password Encryption | Archive analysis | ZIP file with password protection |
| Steganography | Email references | Explicit mention of "steg program" |
| Evidence Destruction | Content analysis | "Make sure you delete this" x4 |
| Obfuscation | Communication analysis | Use of personal email for illicit contacts |

---

## 5. Evidence Acquisition

### 5.1 Devices Examined

#### 5.1.1 Primary Evidence Source

| Attribute | Value |
|-----------|-------|
| **Device Type** | Employee Workstation |
| **Operating System** | Windows (determined from Thunderbird 2.0.0.23 Windows version) |
| **File System** | NTFS |
| **Image Format** | EnCase Expert Witness (.E01) |
| **Image Name** | evidence.E01 |
| **Original Path** | E:\Cyber Security\5th Semester\Digital Forensics\lab\Quiz 1\ |

#### 5.1.2 Storage Information

| Volume | Size | Used Space | Unallocated |
|--------|------|------------|-------------|
| vol_vol2 | ~1 GB | ~38 MB | ~1021 MB |

#### 5.1.3 User Profile Information

**Primary User:** Charlie  
**Email Client:** Mozilla Thunderbird 2.0.0.23  
**IP Address:** 192.168.1.104 (internal network)  
**Mail Server:** domex.nps.edu (205.155.65.103)

### 5.2 Evidence Collection Methods

#### 5.2.1 Forensic Acquisition

**Acquisition Tool:** Autopsy 4.21.0  
**Acquisition Date:** December 22, 2025  
**Examiner:** Rana Uzair Ahmad  
**Case Number:** 231309  

**Acquisition Steps:**
1. Forensic image mounted as read-only
2. File system analyzed using Autopsy ingest modules
3. All files exported maintaining metadata
4. Hash values calculated for verification

#### 5.2.2 Ingest Modules Executed

| Module | Version | Purpose |
|--------|---------|---------|
| Recent Activity | 4.21.0 | Browser/app artifacts |
| Hash Lookup | 4.21.0 | Known file identification |
| File Type Identification | 4.21.0 | True type detection |
| Extension Mismatch Detector | 4.21.0 | Disguised files |
| Embedded File Extractor | 4.21.0 | Archive/document extraction |
| Picture Analyzer | 4.21.0 | Image EXIF analysis |
| Keyword Search | 4.21.0 | Text pattern matching |
| Email Parser | 4.21.0 | Email structure analysis |
| Encryption Detection | 4.21.0 | Protected file identification |
| PhotoRec Carver | 7.0 | Deleted file recovery |

#### 5.2.3 Export Methodology

**Exports Generated:**

| Export Type | Output Directory | Contents |
|-------------|------------------|----------|
| Excel Report | DF Excel Report 12-22-2025-06-42-34 | Tabular file listing |
| Text Report | DF Files - Text 12-22-2025-06-42-18 | File metadata details |
| HTML Report | DF HTML Report 12-22-2025-06-40-43 | Interactive web report |
| TSK Body File | DF TSK Body File 12-22-2025-06-41-58 | Timeline data |

### 5.3 Chain of Custody

#### 5.3.1 Evidence Handling Record

| Date/Time | Action | Handler | Location |
|-----------|--------|---------|----------|
| Dec 22, 2025 06:40 | Forensic acquisition initiated | Rana Uzair Ahmad | Lab Environment |
| Dec 22, 2025 06:42 | Export generation completed | Rana Uzair Ahmad | Lab Environment |
| Dec 22, 2025 | Analysis and report preparation | Rana Uzair Ahmad | Lab Environment |

#### 5.3.2 Evidence Integrity Statement

All evidence files maintain their original filenames and metadata from the forensic acquisition. Hash values were calculated post-acquisition to verify integrity. No modifications were made to the original forensic image during analysis.

#### 5.3.3 Documentation Maintained

1. **Forensic Image Hash:** Verified against acquisition record
2. **File Export Hashes:** Calculated for critical evidence
3. **Analysis Notes:** Documented in this report
4. **Screenshots:** HTML report provides visual documentation

---

## 6. Conclusion

### 6.1 Summary of Findings

Based on comprehensive forensic analysis of the evidence.E01 forensic image, this investigation has established the following findings:

#### 6.1.1 Primary Conclusions

**Finding 1: Corporate Espionage Confirmed**

Charlie, an employee of M57.biz, engaged in systematic theft and sale of proprietary trade secrets to external parties. Specifically:
- Exfiltrated Immortality project files (patent research documents)
- Packaged files into password-protected ZIP archive
- Transmitted to external recipients (andy@swexpert.com, jamie@project2400.com)

**Evidence Strength:** ██████████ **CONCLUSIVE**

**Finding 2: Extortion/Blackmail Confirmed**

Charlie demanded $100,000 from andy@swexpert.com under threat of public disclosure of patent invalidation evidence. The communication explicitly stated:
- Financial demand: "$100k"
- Threat: "I'll release this publicly"
- Intimidation: "Don't involve the cops"

**Evidence Strength:** ██████████ **CONCLUSIVE**

**Finding 3: Trade Secret Misappropriation Confirmed**

Charlie offered to sell confidential prior art research (belonging to client Nitroba.com) to their competitor project2400.com:
- Established pre-existing relationship with competitor contact
- Negotiated payment terms ("half in my account")
- Delivered information following receipt of "deposit"

**Evidence Strength:** ██████████ **CONCLUSIVE**

**Finding 4: Anti-Forensic Activities Confirmed**

Charlie employed multiple techniques to evade detection:
- Password-protected encryption of sensitive files
- Steganography for covert password transmission
- Repeated instructions to destroy evidence
- Use of personal email addresses for illicit communications

**Evidence Strength:** █████████░ **STRONG**

**Finding 5: Financial Motivation Established**

Clear evidence of financial motivation through:
- Explicit $100,000 extortion demand
- Luxury car purchase plans (Ferrari/Shelby)
- Mediterranean cruise vacation planning
- Extended vacation request immediately following criminal activity

**Evidence Strength:** █████████░ **STRONG**

#### 6.1.2 Evidence Summary Table

| Finding | Direct Evidence | Corroborating Evidence | Strength |
|---------|-----------------|------------------------|----------|
| Data Exfiltration | ZIP contents = Immortality folder | Email timestamps | Conclusive |
| Extortion | Verbatim email text | Follow-up communications | Conclusive |
| Trade Secret Theft | Bounce-back preservation | Password confirmation email | Conclusive |
| Anti-Forensics | Encrypted ZIP, steg reference | Multiple deletion requests | Strong |
| Financial Motive | Car/vacation communications | Timeline correlation | Strong |

### 6.2 Assessment of Admissibility

#### 6.2.1 Admissibility Factors

| Factor | Assessment | Notes |
|--------|------------|-------|
| **Authenticity** | ✓ Verified | Hash values confirm file integrity |
| **Reliability** | ✓ Verified | Industry-standard forensic tools used |
| **Relevance** | ✓ Verified | Direct connection to alleged crimes |
| **Chain of Custody** | ✓ Documented | Evidence handling properly recorded |
| **Best Evidence Rule** | ✓ Satisfied | Original forensic image preserved |

#### 6.2.2 Potential Legal Issues

1. **Email Content:** Emails are business communications; employer access generally permitted under acceptable use policies
2. **File Access:** Analysis conducted on company-owned equipment
3. **Password Recovery:** Password obtained from evidence itself (email communications)
4. **Steganography Analysis:** Requires specialized tools for full extraction

#### 6.2.3 Expert Testimony Considerations

This evidence is suitable for expert testimony in legal proceedings. The forensic analyst can testify to:
- Methodology employed
- Tools used and their reliability
- Evidence integrity verification
- Timeline reconstruction
- Technical findings interpretation

#### 6.2.4 Independent Verification Recommendation

All findings documented in this report should be independently verified by a qualified forensic examiner before use in legal proceedings. Key items requiring verification:
1. Hash values of critical evidence files
2. ZIP archive decryption with documented password
3. Steganography analysis of microscope1.jpg
4. Email header authentication

---

## 7. Appendices

### 7.1 Evidence Inventory

#### 7.1.1 Complete Evidence File Listing

**Email Communications (Chronological)**

| ID | Date | File Name | From | To | Subject |
|----|------|-----------|------|-----|---------|
| 1 | Nov 16, 2009 11:02 | Charlie_2009-11-16_1102_Received.txt | pat@m57.biz | charlie@m57.biz | WELCOME TO THE COMPANY! |
| 2 | Nov 16, 2009 11:22 | Charlie_2009-11-16_1122_Received.txt | pat@m57.biz | charlie@m57.biz | Lunch |
| 3 | Nov 16, 2009 11:51 | Charlie_2009-11-16_1151_Sent.txt | charlie@m57.biz | pat@m57.biz | Re: WELCOME |
| 4 | Nov 16, 2009 13:26 | Charlie_2009-11-16_1326_Sent.txt | charlie@m57.biz | - | - |
| 5 | Nov 16, 2009 13:38 | Charlie_2009-11-16_1338_Received.txt | - | charlie@m57.biz | - |
| 6 | Nov 17, 2009 08:45 | Charlie_2009-11-17_0845_Received.txt | - | charlie@m57.biz | - |
| 7 | Nov 17, 2009 10:30 | Charlie_2009-11-17_1030_Received.txt | pat@m57.biz | jo@m57.biz, charlie@m57.biz | Fw: M57.BIZ PRIOR ART |
| 8 | Nov 17, 2009 10:39 | Charlie_2009-11-17_1039_Received.txt | pat@m57.biz | charlie@m57.biz, jo@m57.biz | Inventions / Patents |
| ... | ... | ... | ... | ... | ... |
| 80 | Dec 02, 2009 13:04 | Charlie_2009-12-02_1304_Sent.txt | charlie@m57.biz | jaime@project2400.com | **Interested?** |
| 81 | Dec 02, 2009 13:05 | Charlie_2009-12-02_1305_Received.txt | MAILER-DAEMON | charlie@m57.biz | **Undelivered Mail** |
| 82 | Dec 04, 2009 09:41 | Charlie_2009-12-04_0941_Sent.txt | charlie@m57.biz | andy@swexpert.com | **I Found Something** |
| 83 | Dec 04, 2009 13:06 | Charlie_2009-12-04_1306_Sent.txt | charlie@m57.biz | jamie@project2400.com | **Instructions** |
| 84 | Dec 07, 2009 11:44 | Picture.eml.txt | charlie@m57.biz | andy@swexpert.com | **Picture** |
| 85 | Dec 10, 2009 14:18 | When's it coming.txt | charlie@m57.biz | rubinfritz31@mail.com | Re: When's it coming? |

#### 7.1.2 Critical Evidence Files

**Primary Evidence:**

| Evidence ID | File | Hash (MD5) | Category |
|-------------|------|------------|----------|
| CRT-001 | Charlie_2009-12-04_0941_Sent.txt | 58936eeb680b72c0570cb5035ed88cf8 | Extortion |
| CRT-002 | Charlie_2009-12-04_0941_Sent_01.zip | 4fa239c22e5fb7b934a1bf68e4e0e2e7 | Exfiltration |
| CRT-003 | Charlie_2009-12-02_1305_Received.txt | dfc3d700f039f1b64057ffcc73dafa1f | Trade Secret |
| CRT-004 | Charlie_2009-12-04_1306_Sent.txt | 24d77a52e89b224219fd9386de23be43 | Anti-Forensics |
| CRT-005 | microscope1.jpg | 4be2c4abb48c4389ca798e6c21736ea1 | Steganography |

**Exfiltrated Data:**

| Evidence ID | File | Hash (MD5) | Category |
|-------------|------|------------|----------|
| EXF-001 | us005026637-001.tif | b526e6c7a244d62e7120f3f804d76d8d | Patent Document |
| EXF-002 | us006982168-001.tif | c412dfcd8bca1333d9356d710dd7a01a | Patent Document |
| EXF-003 | Thumbs.db | 4db32968b696e7b7dca8e3860e52b6c3 | Access Evidence |

### 7.2 Forensic Tools Used

#### 7.2.1 Primary Analysis Platform

**Autopsy 4.21.0** - Open Source Digital Forensics Platform  
Website: www.sleuthkit.org  
License: Apache License 2.0

#### 7.2.2 Autopsy Modules Utilized

| Module | Version | Function |
|--------|---------|----------|
| Recent Activity | 4.21.0 | Extract browser history, downloads, recent documents |
| Hash Lookup | 4.21.0 | Compare files against known hash databases |
| File Type Identification | 4.21.0 | Identify true file types regardless of extension |
| Extension Mismatch Detector | 4.21.0 | Detect files with misleading extensions |
| Embedded File Extractor | 4.21.0 | Extract files from archives and documents |
| Picture Analyzer | 4.21.0 | Extract EXIF and image metadata |
| Keyword Search | 4.21.0 | Search for text patterns and keywords |
| Email Parser | 4.21.0 | Parse email structures and extract metadata |
| Encryption Detection | 4.21.0 | Identify encrypted files and containers |
| Interesting Files Identifier | 4.21.0 | Flag files matching predefined patterns |
| Central Repository | 4.21.0 | Cross-case artifact correlation |
| PhotoRec Carver | 7.0 | Recover deleted files through carving |
| Virtual Machine Extractor | 4.21.0 | Extract VM files for analysis |
| Data Source Integrity | 4.21.0 | Verify forensic image integrity |
| Android Analyzer (aLEAPP) | 4.21.0 | Mobile device artifact extraction |
| DJI Drone Analyzer | 4.21.0 | Drone data extraction |
| YARA Analyzer | 4.21.0 | Pattern-based malware detection |
| iOS Analyzer (iLEAPP) | 4.21.0 | iOS device artifact extraction |
| GPX Parser | 1.2 | GPS data extraction |

#### 7.2.3 Supporting Tools

| Tool | Purpose |
|------|---------|
| unzip | Archive extraction and password testing |
| Standard text analysis | Email content review |
| TSK (The Sleuth Kit) | Body file generation |

### 7.3 Detailed Analysis Results

#### 7.3.1 File System Analysis Results

**NTFS Volume Information:**

| Attribute | Value |
|-----------|-------|
| Volume Serial Number | From $Volume |
| Cluster Size | 4096 bytes |
| MFT Records | 262,144 bytes total |
| File Count | 324 items |
| Directory Count | 15+ |

**Key Directories:**

| Path | Purpose | Relevant Files |
|------|---------|----------------|
| /Email/ | Email storage | 90+ email files |
| /Email/other/ | Additional emails | 12 files |
| /Immortality/ | Exfiltrated data | 4 files |
| /$Unalloc/ | Unallocated space | ~1GB |

#### 7.3.2 Email Header Analysis

**Sample Header (from Charlie_2009-12-02_1305_Received_Interested-.eml):**

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

**Header Analysis:**
- Origin IP: 192.168.1.104 (M57.biz internal network)
- Mail Client: Mozilla Thunderbird 2.0.0.23 (Windows)
- Mail Server: domex.nps.edu via mustang.nps.edu
- Spam Filter: Barracuda Networks
- Virus Scanner: amavisd-new

#### 7.3.3 ZIP Archive Analysis

**Password-Protected Archive Contents:**

```
Archive:  Charlie_2009-12-04_0941_Sent_01.zip
Encryption: AES-256 / ZIP standard encryption
Password: "nitro" (recovered from Charlie_2009-12-04_1306_Sent.txt)
         "immortal" (alternate, provided by investigator)

 Length      Date    Time    Name
---------  ---------- -----   ----
        0  2009-11-24 13:18   Immortality/
     7680  2009-11-24 13:18   Immortality/Thumbs.db
    39692  2009-11-24 13:13   Immortality/us005026637-001.tif
    76596  2009-11-24 13:15   Immortality/us006982168-001.tif
---------                     -------
   123968                     4 files
```

#### 7.3.4 Key Verbatim Evidence

**Extortion Demand (Dec 4, 2009 09:41):**
> "I found a prior patent that will definitely invalidate your current immortality patent. You should have used my boss's prior art services, but, oh well, I'll just use your negligence to benefit me. **I want 100k or I'll release this publicly**. I don't need to tell you how much this will hurt your business if I go public with this. **Don't involve the cops** or this information will go public."

**Trade Secret Offer (Dec 2, 2009 13:04):**
> "I have something that you'll definitely be interested in. It concerns your competitor. I'm doing a prior art search for them. Want to know what I've found? **You know my price.** I'll send you the goods after I see half in my account. **Make sure you delete this email.**"

**Password Delivery (Dec 4, 2009 13:06):**
> "Got the deposit. **The password to get the info is nitro.** Use the steg program we talked about. **And don't forget to delete these emails.**"

**Financial Motive (Dec 8, 2009 14:18):**
> "You want to come test drive some cars with me later? I'm going to the **Ferrari dealer** first, but I think I'm going with the **Shelby**."

---

## 8. Recommendations

### 8.1 Legal and Investigative Actions

#### 8.1.1 Immediate Actions Required

| Priority | Action | Responsible Party | Timeline |
|----------|--------|-------------------|----------|
| **Critical** | Terminate Charlie's employment | HR/Legal | Immediate |
| **Critical** | Disable all network access | IT Administrator | Immediate |
| **Critical** | Preserve all evidence | Forensic Analyst | Complete |
| **High** | Notify legal counsel | Management | Within 24 hours |
| **High** | Contact law enforcement | Legal/Management | Within 48 hours |
| **High** | Notify affected clients | Legal/Management | Per legal advice |

#### 8.1.2 Criminal Referral Recommendation

Based on the evidence documented in this report, criminal referral is recommended for the following charges:

| Potential Charge | Statute | Evidence Summary |
|-----------------|---------|------------------|
| Theft of Trade Secrets | 18 U.S.C. § 1832 | Exfiltration of Immortality project |
| Blackmail/Extortion | 18 U.S.C. § 873 | $100k demand with threats |
| Computer Fraud | 18 U.S.C. § 1030 | Unauthorized access for theft |
| Wire Fraud | 18 U.S.C. § 1343 | Use of email for fraud scheme |

#### 8.1.3 Civil Litigation Considerations

M57.biz may pursue civil remedies including:
- Breach of employment contract
- Breach of confidentiality/NDA
- Misappropriation of trade secrets
- Conversion of company property
- Unfair competition

#### 8.1.4 Client Notification Requirements

| Client | Affected Data | Notification Priority |
|--------|---------------|----------------------|
| Nitroba.com | Prior art research | High - Competitive intelligence compromised |
| swexpert.com (Andy) | Immortality patent research | High - Extortion victim |

### 8.2 Data Security Improvements

#### 8.2.1 Technical Controls

| Control | Implementation | Priority |
|---------|----------------|----------|
| **Data Loss Prevention (DLP)** | Deploy endpoint DLP to detect sensitive data transfers | High |
| **Email Monitoring** | Implement content inspection for external email | High |
| **Access Controls** | Implement least-privilege access model | High |
| **Encryption Management** | Prohibit unauthorized encryption; deploy enterprise key management | Medium |
| **Network Monitoring** | Deploy network traffic analysis for anomaly detection | Medium |
| **USB/Removable Media Controls** | Restrict or audit removable storage devices | Medium |

#### 8.2.2 Policy Improvements

| Policy Area | Recommendation |
|-------------|----------------|
| **Acceptable Use Policy** | Update to explicitly prohibit data exfiltration, personal use of company email for business matters |
| **Confidentiality Agreements** | Strengthen NDAs with specific penalties for violation |
| **Data Classification** | Implement formal data classification scheme |
| **Email Retention** | Establish email archiving and legal hold procedures |
| **Encryption Policy** | Require approval for any encryption of company data |

#### 8.2.3 Procedural Improvements

| Area | Recommendation |
|------|----------------|
| **Employee Vetting** | Enhanced background checks for positions with sensitive access |
| **Security Awareness Training** | Mandatory annual training on insider threat indicators |
| **Exit Procedures** | Comprehensive off-boarding including access review and data audit |
| **Incident Response** | Develop formal incident response plan with forensic readiness |
| **Audit Trail** | Implement comprehensive audit logging for sensitive data access |

#### 8.2.4 Monitoring Recommendations

| Indicator Type | Monitoring Approach |
|----------------|---------------------|
| Unusual email patterns | Volume/destination analysis |
| After-hours access | Time-based access alerting |
| Large file transfers | Data volume monitoring |
| Encrypted file creation | File type monitoring |
| External storage use | Device usage logging |

---

## Signature and Certification

This report has been prepared in accordance with accepted digital forensics standards and practices. The findings documented herein represent an accurate and complete analysis of the evidence examined.

**Lead Investigator Certification:**

I, **Rana Uzair Ahmad**, certify that:
1. The analysis documented in this report was conducted using accepted forensic methodology
2. All evidence was handled in accordance with chain of custody requirements
3. The findings represent an accurate interpretation of the evidence examined
4. No evidence was altered, modified, or destroyed during the analysis

---

**Report Prepared By:** Rana Uzair Ahmad  
**Date:** December 22, 2025  
**Case Number:** DF-231309  
**Classification:** Confidential – Legal Privilege Applies

---

*This report is based solely on the digital artifacts provided for analysis. Additional investigation may reveal further evidence. All findings should be independently verified before use in legal proceedings.*

---

**END OF REPORT**
