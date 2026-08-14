# Indicators of Compromise (IOCs)

## Case Information

- Case Reference: IR-2024-0603-INVOICE
- Scenario: Simulated phishing / malicious PDF investigation
- Classification: Training / Portfolio Project

> No live malware was executed. The PDF was analyzed statically and the EICAR test signature was used for safe antivirus validation.

---

## 1. Network Indicators

| Type | Indicator | Description |
|---|---|---|
| IP Address | `185.220.101.47` | External sending IP associated with the phishing email |
| Domain | `corp-invoice-verify[.]com` | Look-alike phishing domain |
| Email | `accounts.payable@corp-invoice-verify[.]com` | Suspicious Reply-To address |

---

## 2. File Indicators

| Type | Indicator |
|---|---|
| Filename | `Invoice_2024_Q2.pdf` |
| MD5 | `1424b33d26bfed31579ac6dc0e8e2f6a` |
| SHA1 | `faa591df84d70d6330efb10d95bd9e86feccbd32` |
| SHA256 | `30b8cb81af807165ce5dc09d0daf0b1af75ab1fd00dea91907688384bee0b6ca` |

---

## 3. PDF Structural Indicators

The static analysis identified the following potentially dangerous PDF structures:

- `/OpenAction`
- `/JavaScript`
- `/EmbeddedFile`
- `/URI`

The `/JavaScript` structure was referenced multiple times.

The `/EmbeddedFile` object contained the EICAR antivirus test signature.

---

## 4. Antivirus Indicator

**Detection:**

`Virus:DOS/EICAR_Test_File`

The EICAR test signature was embedded inside the PDF and was detected by Microsoft Defender.

EICAR was used instead of live malware so that antivirus detection could be safely demonstrated.

---

## 5. Email Authentication Indicators

| Control | Result |
|---|---|
| SPF | FAIL |
| DKIM | NONE |
| DMARC | FAIL |
| DMARC Policy | REJECT |
| From Domain | `corp-example.com` |
| Reply-To Domain | `corp-invoice-verify[.]com` |
| X-Mailer | PHPMailer 5.2.9 |

---

## 6. Social Engineering Indicators

- Urgency-based language
- Threat of service suspension
- Threat of late-penalty charges
- Generic salutation
- External account-verification link
- Internal-looking sender identity
- Look-alike Reply-To domain
- Suspicious invoice attachment

---

## 7. Detection and Response

The investigation correlated:

1. Phishing email indicators
2. Failed email authentication
3. Suspicious Reply-To domain
4. Malicious PDF structures
5. File hashes
6. EICAR antivirus detection
7. Endpoint hardening controls

---

## 8. Recommended Actions

- Block `185.220.101.47`
- Block `corp-invoice-verify[.]com`
- Block the confirmed file hashes
- Search mailboxes for similar messages
- Enforce SPF/DKIM/DMARC
- Enable PDF attachment sandboxing
- Restrict PDF JavaScript execution
- Monitor suspicious child processes
- Monitor new service creation
- Protect sensitive data with encryption

---

## Disclaimer

This IOC list belongs to a simulated cybersecurity lab exercise.

The indicators are documented for cybersecurity training, SOC analysis, incident-response practice, and portfolio demonstration.
