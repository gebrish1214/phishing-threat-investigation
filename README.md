# Phishing Threat Investigation & Endpoint Hardening

## SOC / Incident Response Portfolio Project

A simulated SOC/incident response investigation of a phishing email,
malicious PDF attachment, threat indicators, and endpoint hardening.

> **Environment:** Simulated cybersecurity lab  
> **Classification:** Training / Portfolio Project  
> **No real victims or live malware were used.**

---

## Project Overview

This project simulates a phishing/BEC-style attack and follows the
investigation from the initial email through malicious PDF analysis,
threat detection, incident assessment, and security hardening.

The investigation demonstrates practical SOC and incident-response
skills in a controlled environment.

---

## Objectives

- Analyze a suspicious phishing email
- Investigate SPF, DKIM, and DMARC results
- Identify sender and Reply-To mismatches
- Analyze a suspicious PDF attachment
- Calculate file hashes
- Identify indicators of compromise
- Correlate multiple security findings
- Validate antivirus detection
- Reconstruct the suspected attack chain
- Demonstrate endpoint data protection
- Develop security hardening recommendations

---

## Skills Demonstrated

- SOC Analysis
- Incident Response
- Phishing Investigation
- Email Header Analysis
- SPF / DKIM / DMARC
- Static PDF Analysis
- Cryptographic Hashing
- IOC Extraction
- Microsoft Defender
- Python
- Windows Security
- BitLocker
- Security Documentation
- Threat Analysis

---

## Investigation Workflow

```text
Phishing Email
      ↓
Email Header Analysis
      ↓
SPF / DKIM / DMARC Investigation
      ↓
Malicious PDF Analysis
      ↓
Hash & IOC Extraction
      ↓
Microsoft Defender Detection
      ↓
Incident Assessment
      ↓
Endpoint Hardening
      ↓
Encrypted Data Protection
```

## Key Findings

### Phishing Email

The investigation identified multiple phishing indicators:

- SPF failure
- Missing DKIM
- DMARC failure
- Spoofed internal sender
- Mismatched Reply-To domain
- Look-alike domain
- Urgency-based social engineering
- Suspicious attachment

### PDF Analysis

Static analysis identified high-risk PDF structures including:

- `/OpenAction`
- `/JavaScript`
- `/EmbeddedFile`
- `/URI`

The embedded object also matched the EICAR antivirus test signature.

### Antivirus Validation

Microsoft Defender detected the EICAR test signature embedded
inside the PDF.

No live malware was executed during the investigation.

---

## Incident Response

The investigation included:

1. Evidence acquisition
2. Email header analysis
3. Cryptographic hashing
4. Static PDF analysis
5. Antivirus corroboration
6. IOC extraction
7. Attack-chain analysis
8. Security hardening

---

## Endpoint Hardening

The project demonstrated several security controls:

- Email authentication enforcement
- Suspicious domain blocking
- Attachment sandboxing
- PDF JavaScript restrictions
- Endpoint detection and response monitoring
- Malicious hash blocklisting
- Sensitive-data encryption
- Phishing awareness training

---

## Data Protection Demonstration

A BitLocker-encrypted virtual disk was used to demonstrate
protection of sensitive data at rest.

The volume was locked when not in use and temporarily mounted
only when authorized access was required.

---

## Important Investigation Note

The email and PDF findings were directly analyzed in the lab.

Endpoint persistence, unusual outbound TCP connections, and hidden
script behavior were part of the simulated scenario and were
treated as hypotheses rather than independently captured telemetry.

---

## Detailed Report

The complete investigation report is available here:

**[View Threat Investigation Report](report/Threat-Investigation-Report.pdf)**

---

## Project Status

**Completed — Simulated Cybersecurity Lab**

This project is intended for cybersecurity learning,
portfolio development, and SOC/incident-response demonstration.
