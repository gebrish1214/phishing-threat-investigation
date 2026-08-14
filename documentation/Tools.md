# Tools Used

## Email Analysis

### Email Header Analysis
Used to inspect:

- SPF
- DKIM
- DMARC
- From address
- Reply-To address
- Sending IP
- Mailer artifacts

### Notepad / Text Editor
Used to inspect the raw `.eml` email header data in the Windows lab environment.

---

## File Analysis

### PowerShell
Used for:

- File identification
- Directory inspection
- Hash calculation
- Endpoint investigation
- BitLocker management
- Evidence collection

### Cryptographic Hashing
MD5, SHA1, and SHA256 were calculated for the investigated PDF to support file identification and integrity tracking.

---

## PDF Static Analysis

### Python
A Python-based structural scan was used to inspect the PDF for suspicious objects and keywords.

The analysis checked for:

- `/JS`
- `/JavaScript`
- `/OpenAction`
- `/EmbeddedFile`
- `/URI`

No live malware was executed.

---

## Antivirus Validation

### Microsoft Defender
Used to validate the suspicious PDF analysis.

The embedded EICAR test signature was detected as:

`Virus:DOS/EICAR_Test_File`

EICAR was used as a safe antivirus test instead of live malware.

---

## Data Protection

### BitLocker
Used to demonstrate encryption of sensitive workstation data at rest.

The investigation demonstrated:

1. Creating an encrypted virtual volume
2. Mounting the volume for authorized access
3. Accessing the protected test data
4. Locking the volume
5. Verifying that the protected data became inaccessible

---

## Investigation Approach

The tools were used together to support the following workflow:

```text
Phishing Email
      ↓
Email Header Analysis
      ↓
SPF / DKIM / DMARC
      ↓
Attachment Identification
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

---

## Safety

This project was conducted as a simulated cybersecurity lab.

- No live malware was executed.
- EICAR was used for antivirus testing.
- The PDF was analyzed statically.
- Endpoint activity described as assumed scenario telemetry is clearly identified as such in the investigation report.
