# Incident Timeline

## Simulated Phishing Incident

This timeline documents the sequence of activities performed during the simulated phishing threat investigation.

|Stage|                   Activity                               |         Evidence              |
|----|-----------------------------------------------------------|-------------------------------|
| 1 | Suspicious phishing email identified                       | Email header analysis         |
| 2 | Sender and Reply-To addresses reviewed                     | Email header screenshot       |
| 3 | SPF, DKIM, and DMARC results investigated                  | Email header analysis         |
| 4 | Suspicious PDF attachment identified                       | PDF analysis                  |
| 5 | Cryptographic hashes calculated                            | Hash analysis screenshot      |
| 6 | PDF structure inspected for suspicious objects             | Static PDF analysis           |
| 7 | Suspicious PDF validated using Microsoft Defender          | Defender detection screenshot |
| 8 | Indicators of compromise documented                        | `indicators/IOCs.md`          |
| 9 | Endpoint security controls reviewed                        | Investigation evidence        |
| 10 | BitLocker protection demonstrated                         | BitLocker screenshots         |
| 11 | Sensitive test data protected using encryption            | BitLocker evidence            |
| 12 | Incident findings and security recommendations documented | Investigation report          |

---

## Investigation Sequence

```text
Phishing Email
      ↓
Email Header Analysis
      ↓
SPF / DKIM / DMARC
      ↓
PDF Attachment Identification
      ↓
Hash Calculation
      ↓
PDF Static Analysis
      ↓
Microsoft Defender Validation
      ↓
IOC Extraction
      ↓
Incident Assessment
      ↓
Endpoint Hardening
      ↓
Encrypted Data Protection
