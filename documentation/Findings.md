# Investigation Findings

## Executive Summary

A simulated phishing investigation was conducted to analyze a suspicious email and PDF attachment in a controlled lab environment.

The investigation included:

- Email header analysis
- SPF, DKIM, and DMARC validation
- PDF static analysis
- Cryptographic hash generation
- Antivirus validation using Microsoft Defender
- Indicator of Compromise (IOC) extraction
- Endpoint hardening with BitLocker encryption

No live malware was executed during the investigation.

---

## Key Findings

### Email Analysis

The phishing email displayed characteristics commonly associated with malicious campaigns:

- Suspicious sender information
- Reply-To mismatch
- Email authentication review
- Potential social engineering indicators

---

### Attachment Analysis

The PDF attachment was examined using static analysis techniques.

The analysis included:

- File identification
- Hash calculation
- Structural inspection
- Detection of suspicious PDF objects

---

### Antivirus Validation

Microsoft Defender detected the embedded EICAR antivirus test signature:

`Virus:DOS/EICAR_Test_File`

EICAR was used as a safe validation method instead of live malware.

---

### Indicators of Compromise

Indicators extracted during the investigation were documented separately in:

`indicators/IOCs.md`

---

### Endpoint Protection

BitLocker encryption was implemented to demonstrate:

- Data protection at rest
- Controlled access
- Encryption validation
- Secure storage of sensitive files

---

## Security Recommendations

The following security measures are recommended:

1. Enable SPF, DKIM, and DMARC enforcement.
2. Train users to identify phishing emails.
3. Scan email attachments automatically.
4. Maintain updated antivirus protection.
5. Use encryption for sensitive data.
6. Monitor indicators of compromise.
7. Apply endpoint hardening controls.

---

## Conclusion

The simulated investigation demonstrated a complete SOC and incident-response workflow, including threat identification, technical analysis, IOC extraction, antivirus validation, and endpoint protection.
