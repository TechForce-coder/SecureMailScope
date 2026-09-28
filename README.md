# SecureMailScope

### Passive Network Forensics • Cryptographic Security Assessment • AI Risk Intelligence

**AI-Assisted Passive Network Forensic Framework for Cryptographic Security Assessment of Enterprise Email Communications**

**Smart India Hackathon 2026 • SIH26159 • Team Tech Force**

---

## 📌 Table of Contents

* [Overview](#-overview)
* [Problem Statement](#-problem-statement)
* [Our Solution](#-our-solution)
* [Key Features](#-key-features)
* [How It Works](#-how-it-works)
* [System Architecture](#-system-architecture)
* [Technology Stack](#-technology-stack)
* [Security Model](#-security-model)
* [Cryptographic Analysis Pipeline](#-cryptographic-analysis-pipeline)
* [AI Risk & Reporting Engine](#-ai-risk--reporting-engine)
* [Dashboard](#-dashboard)
* [Demo](#-demo)
* [Use Cases](#-use-cases)
* [Impact](#-impact)
* [References](#-references)

---

## 🚀 Overview

**SecureMailScope** is an AI-assisted passive network forensic framework designed to provide **cryptographic security assessment and risk intelligence for enterprise email communications**.

The platform analyzes captured SMTP, IMAP, and POP3 traffic from PCAP/PCAPNG files without modifying or disrupting production network traffic.

It combines packet analysis, TCP stream reassembly, STARTTLS inspection, TLS handshake analysis, X.509 certificate validation, and AI-assisted risk scoring into a unified forensic platform.

### Core Components

* **PCAP / PCAPNG ingestion**
* **TCP stream reassembly**
* **SMTP / IMAP / POP3 protocol identification**
* **STARTTLS / STLS inspection**
* **TLS version and cipher-suite analysis**
* **X.509 certificate validation**
* **Isolation Forest anomaly detection**
* **Weighted cryptographic risk scoring**
* **SOC-oriented security dashboard**
* **JSON / PDF / HTML forensic reports**

---

## 🎯 Problem Statement

### SIH26159

**AI-Assisted Passive Network Forensic Framework for Cryptographic Security Assessment of Enterprise Email Communications**

Enterprise email systems may contain cryptographic weaknesses that are difficult to identify through conventional packet-analysis tools.

| **Challenge**                    | **Problem**                                                       |
| -------------------------------- | ----------------------------------------------------------------- |
| 🔓 **Obsolete TLS Versions**     | Legacy TLS versions may weaken communication security             |
| ⚠️ **Weak Cipher Suites**        | Weak or outdated cryptographic algorithms may be used             |
| 🔄 **STARTTLS Downgrade**        | Insecure upgrade behavior can expose email communication          |
| 📜 **Certificate Issues**        | Expired, weak, self-signed, or improperly configured certificates |
| 🔍 **Manual Analysis**           | Conventional tools require significant manual investigation       |
| 🤖 **Limited Risk Intelligence** | Lack of automated anomaly detection and prioritization            |
| 📊 **Complex Reporting**         | Raw packet data is difficult to convert into actionable findings  |

---

# 💡 Our Solution

SecureMailScope introduces a multi-layered passive forensic analysis pipeline:

```text
┌─────────────────────────────┐
│        PCAP / PCAPNG        │
│      Network Capture        │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│     PCAP INGESTION LAYER    │
│ Packet Parsing & Filtering  │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ TCP STREAM REASSEMBLY       │
│ Bidirectional Reconstruction│
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│ PROTOCOL IDENTIFICATION     │
│ SMTP • IMAP • POP3          │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│  CRYPTOGRAPHIC DPI ENGINE   │
│ TLS • Cipher • STARTTLS     │
└──────────────┬──────────────┘
               │
       ┌───────┴────────┐
       ▼                ▼
┌──────────────┐ ┌────────────────────┐
│ X.509        │ │ STARTTLS / TLS     │
│ VALIDATION   │ │ SECURITY ANALYSIS  │
└──────┬───────┘ └──────────┬─────────┘
       │                    │
       └──────────┬─────────┘
                  ▼
┌─────────────────────────────┐
│     AI / ML RISK ENGINE     │
│ Isolation Forest + Scoring  │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      SOC DASHBOARD          │
│ Findings • Risk • Analytics │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│     FORENSIC REPORTS        │
│ JSON • PDF • HTML           │
└─────────────────────────────┘
```

---

# ✨ Key Features

## 📦 1. Passive PCAP Analysis

SecureMailScope performs **out-of-band analysis** of captured network traffic.

Features include:

* PCAP / PCAPNG ingestion
* No modification of live traffic
* Packet filtering
* Ethernet/IP header processing
* TCP payload extraction
* Mail-protocol traffic identification
* Forensic session reconstruction

This allows security teams to analyze network captures without introducing latency into production email systems.

---

## 🔄 2. TCP Stream Reassembly

The framework reconstructs bidirectional TCP conversations before performing deep analysis.

Features include:

* TCP sequence-number ordering
* Bidirectional stream grouping
* Payload reconstruction
* Session identification
* Protocol detection
* Application-layer analysis

This provides the required context for analyzing SMTP, IMAP, and POP3 security negotiations.

---

## 🔐 3. TLS & STARTTLS Inspection

SecureMailScope analyzes cryptographic negotiation within email communication.

Features include:

* TLS version detection
* Cipher-suite identification
* Key-exchange analysis
* Perfect Forward Secrecy evaluation
* STARTTLS negotiation tracking
* STLS inspection
* Plaintext fallback detection
* Potential downgrade / stripping detection

Supported email protocols include:

* SMTP
* IMAP
* POP3

---

## 📜 4. X.509 Certificate Validation

The framework automatically extracts and evaluates certificate properties.

Validation includes:

* Certificate issuer
* Certificate subject
* Expiration date
* Trust-chain information
* Public-key length
* Signature algorithm
* Self-signed certificate detection
* Weak cryptographic configuration detection

The system can identify conditions such as:

```text
Expired Certificate
        +
Weak Public Key
        +
Legacy Signature Algorithm
        ↓
Cryptographic Risk Finding
```

---

## 🤖 5. AI / ML Risk Detection

SecureMailScope uses **Isolation Forest-based anomaly detection** together with weighted security heuristics.

The risk engine evaluates:

* TLS configuration
* Cipher strength
* Certificate properties
* STARTTLS behavior
* Protocol anomalies
* Cryptographic weaknesses
* Historical analysis features

The system produces a weighted risk score from **0–100** with severity levels:

```text
0 ───────────────────────────── 100

LOW → MEDIUM → HIGH → CRITICAL
```

---

## 📊 6. SOC Security Dashboard

The dashboard provides centralized visibility into:

* Email protocol distribution
* TLS configurations
* Certificate health
* Cryptographic findings
* AI anomaly results
* Risk scores
* Prioritized security findings
* Recommended hardening actions
* Analysis-session telemetry

---

## 📄 7. Automated Forensic Reporting

SecureMailScope converts technical analysis into structured reports.

Supported outputs include:

* JSON
* PDF
* HTML

Reports can contain:

* Session information
* TLS findings
* Certificate metadata
* Risk scores
* AI anomaly indicators
* Security recommendations
* Forensic metadata

---

# 🔄 How It Works

### Step 1 — PCAP Ingestion

The analyst uploads a:

```text
.pcap
.pcapng
```

file through the dashboard or command-line workflow.

---

### Step 2 — Packet Filtering

The system identifies traffic associated with:

```text
SMTP → 25 / 587 / 465
IMAP → 143 / 993
POP3 → 110 / 995
```

Relevant TCP packets are extracted for further analysis.

---

### Step 3 — TCP Stream Reassembly

Packets are ordered using TCP sequence numbers.

```text
Packets
   ↓
Sequence Ordering
   ↓
Bidirectional Grouping
   ↓
Reconstructed TCP Stream
```

---

### Step 4 — Protocol Identification

The framework identifies the application protocol using:

```text
Port Signatures
      +
Command Structures
      +
Payload Analysis
```

The system identifies:

```text
SMTP
IMAP
POP3
```

---

### Step 5 — STARTTLS / TLS Analysis

The reconstructed stream is inspected for:

```text
STARTTLS
STLS
TLS ClientHello
TLS ServerHello
Cipher Suite
Key Exchange
TLS Version
```

The framework checks whether encrypted communication is successfully established and identifies suspicious fallback or downgrade behavior.

---

### Step 6 — Certificate Analysis

X.509 certificate information is extracted and validated.

```text
Certificate
     ↓
Issuer
     ↓
Validity
     ↓
Public Key
     ↓
Signature Algorithm
     ↓
Trust Chain
```

---

### Step 7 — AI Risk Scoring

Extracted security features are passed to the risk engine.

```text
Security Features
       ↓
Isolation Forest
       ↓
Anomaly Detection
       ↓
Weighted Risk Scoring
       ↓
Risk Level
```

---

### Step 8 — Reporting & Visualization

The final results are presented through the SOC dashboard and can be exported as:

```text
JSON
PDF
HTML
```

---

# 🏗️ System Architecture

```text
┌─────────────────────────────────────────────────────────────┐
│                       INPUT LAYER                           │
│                                                             │
│              PCAP / PCAPNG / SPAN Capture                   │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                  INGESTION & BUFFERING                      │
│                                                             │
│                  React Dashboard / CLI                      │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│          STREAM REASSEMBLY & PROTOCOL IDENTIFICATION        │
│                                                             │
│             SMTP │ IMAP │ POP3 │ TCP                        │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
              ┌────────────┴────────────┐
              ▼                         ▼
┌──────────────────────────┐  ┌─────────────────────────────┐
│ CRYPTOGRAPHIC DPI ENGINE │  │ X.509 CERTIFICATE ENGINE    │
│                          │  │                             │
│ TLS Versions             │  │ Validity                    │
│ Cipher Suites            │  │ Public Key Length           │
│ STARTTLS                 │  │ Trust Chain                 │
│ Key Exchange             │  │ Signature Algorithm         │
│ PFS                      │  │ Certificate Health          │
└────────────┬─────────────┘  └──────────────┬──────────────┘
             │                               │
             └───────────────┬───────────────┘
                             ▼
┌─────────────────────────────────────────────────────────────┐
│                   AI / ML RISK ENGINE                       │
│                                                             │
│       Isolation Forest + Weighted Risk Scoring              │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    SOC ANALYTICS LAYER                      │
│                                                             │
│ Findings │ Risk Scores │ Anomalies │ Recommendations        │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                     DASHBOARD & REPORTS                     │
│                                                             │
│        React Dashboard │ JSON │ PDF │ HTML                  │
└─────────────────────────────────────────────────────────────┘
```

---

# 🧰 Technology Stack

| **Layer**                | **Technology**     | **Purpose**                             |
| ------------------------ | ------------------ | --------------------------------------- |
| **Frontend**             | React.js           | Security dashboard and interface        |
| **Styling**              | Tailwind CSS       | Dashboard styling                       |
| **Backend**              | Node.js            | Server runtime                          |
| **API Framework**        | Express.js         | REST APIs and business logic            |
| **Packet Analysis**      | Python             | Packet processing and forensic analysis |
| **Packet Library**       | Scapy              | Packet parsing and manipulation         |
| **Packet Analysis**      | PyShark            | PCAP inspection and packet dissection   |
| **AI / ML**              | scikit-learn       | Isolation Forest anomaly detection      |
| **Numerical Processing** | NumPy              | Feature processing                      |
| **Database**             | MongoDB / SQLite   | Session and finding storage             |
| **Real-Time**            | Socket.IO          | Live analysis updates                   |
| **Protocols**            | SMTP / IMAP / POP3 | Enterprise email protocols              |
| **Cryptography**         | TLS / X.509        | Secure communication analysis           |
| **Reporting**            | JSON / PDF / HTML  | Forensic report generation              |

---

#

---

>

---

# 🔐 Security Model

SecureMailScope follows a layered passive-security analysis approach:

```text
┌──────────────────────────┐
│   PASSIVE PCAP ANALYSIS  │
│   No Live Traffic Change │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│  PROTOCOL IDENTIFICATION │
│    SMTP / IMAP / POP3    │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│   TCP STREAM REASSEMBLY  │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│   TLS / STARTTLS CHECK   │
│ Versions • Ciphers • PFS │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│   X.509 VALIDATION       │
│ Certificate Health       │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│    AI RISK ANALYSIS      │
│ Isolation Forest + Score │
└────────────┬─────────────┘
             ▼
┌──────────────────────────┐
│   SECURITY FINDINGS      │
│ Critical → Low           │
└──────────────────────────┘
```

The framework also considers secure handling of captured packet data and supports role-based access to the analysis dashboard.

---

# 🔬 Cryptographic Analysis Pipeline

```text
┌─────────────────┐
│   PCAP Capture  │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Packet Filtering│
└────────┬────────┘
         ▼
┌─────────────────┐
│ TCP Reassembly  │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Protocol Detect │
└────────┬────────┘
         ▼
┌─────────────────┐
│ STARTTLS / STLS │
└────────┬────────┘
         ▼
┌─────────────────┐
│ TLS Handshake   │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Cipher / PFS    │
└────────┬────────┘
         ▼
┌─────────────────┐
│ X.509 Analysis  │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Security Finding│
└─────────────────┘
```

The pipeline provides cryptographic visibility across the complete email-session lifecycle.

---

# 🤖 AI Risk & Reporting Engine

The AI and risk engine combines machine-learning anomaly detection with weighted security rules.

```text
┌────────────────────────────┐
│   Extracted Security Data  │
└──────────────┬─────────────┘
               ▼
┌────────────────────────────┐
│       Feature Extraction   │
└──────────────┬─────────────┘
               ▼
┌────────────────────────────┐
│      Isolation Forest      │
│     Anomaly Detection      │
└──────────────┬─────────────┘
               ▼
┌────────────────────────────┐
│    Weighted Risk Engine    │
└──────────────┬─────────────┘
               ▼
┌────────────────────────────┐
│     Risk Score 0–100       │
└──────────────┬─────────────┘
               ▼
      ┌────────┴────────┐
      ▼                 ▼
┌──────────────┐ ┌───────────────┐
│ Risk Level   │ │ AI Anomaly    │
│ Critical     │ │ Flag          │
│ High         │ └───────┬───────┘
│ Medium       │         │
│ Low          │         │
└──────┬───────┘         │
       └──────────┬──────┘
                  ▼
┌────────────────────────────┐
│   Recommendations &        │
│   Forensic Reports         │
└────────────────────────────┘
```

The reporting layer provides actionable findings and supports JSON, PDF, and HTML output.

---

# 📊 Dashboard

The SecureMailScope dashboard provides:

### Protocol Analytics

Displays analyzed SMTP, IMAP, and POP3 sessions.

### TLS Analytics

Provides visibility into:

* TLS versions
* Cipher suites
* Key exchange
* Perfect Forward Secrecy
* STARTTLS state

### Certificate Health

Displays:

* Certificate issuer
* Expiration status
* Public-key length
* Signature algorithm
* Trust-chain information

### Risk Monitoring

Displays:

* Risk scores
* Risk levels
* AI anomaly flags
* Prioritized findings

### Security Findings

Provides visibility into identified cryptographic weaknesses and protocol anomalies.

### Hardening Guidance

Provides security recommendations aligned with relevant NIST and RFC guidance.

### Real-Time Analysis

WebSockets can provide live analysis telemetry while packet processing is underway.

---

# 🎥 Demo

### Prototype Demonstration

SecureMailScope is designed to demonstrate:

```text
PCAP Upload
     ↓
Email Session Detection
     ↓
TLS / STARTTLS Analysis
     ↓
Certificate Validation
     ↓
AI Risk Scoring
     ↓
SOC Dashboard
     ↓
Forensic Report
```

> Demo URL can be added here when the SecureMailScope prototype video or repository link is available.

---

# 🌍 Use Cases

## 🛡️ Government & Defense

* Enterprise email security assessment
* Cryptographic posture auditing
* Forensic PCAP investigation
* Detection of suspicious TLS behavior
* Certificate security assessment

## 🏢 Enterprise SOC

* Continuous cryptographic posture monitoring
* Email infrastructure security auditing
* STARTTLS security assessment
* TLS configuration analysis
* Prioritized vulnerability investigation

## 🚨 Incident Response

* Post-incident PCAP analysis
* Suspicious TLS session investigation
* Certificate anomaly investigation
* Potential downgrade analysis
* Forensic evidence generation

## 🎓 Academic & Security Research

* Network-forensics experimentation
* TLS security research
* Email protocol analysis
* AI-assisted anomaly detection
* Cryptographic configuration studies

---

# 📈 Impact

| **Area**                  | **Expected Impact**                                        |
| ------------------------- | ---------------------------------------------------------- |
| 🔐 **Security**           | Identifies cryptographic weaknesses in email communication |
| ⚡ **Efficiency**          | Automates packet and cryptographic analysis                |
| 🤖 **Intelligence**       | AI-assisted anomaly detection and risk prioritization      |
| 📋 **Forensics**          | Structured evidence and reproducible analysis              |
| 📊 **Visibility**         | Centralized SOC-oriented security dashboard                |
| 📜 **Compliance Support** | Supports assessment against NIST and relevant RFC guidance |

---

# 📚 References

# 📚 References

1. **NIST SP 800-52 Rev. 2 — Guidelines for the Selection, Configuration, and Use of Transport Layer Security (TLS) Implementations**
   [NIST SP 800-52 Rev. 2](https://csrc.nist.gov/pubs/sp/800/52/r2/final?utm_source=chatgpt.com)

2. **IETF RFC 3207 — SMTP Service Extension for Secure SMTP over Transport Layer Security (STARTTLS)**
   [RFC 3207 — SMTP STARTTLS](https://www.rfc-editor.org/info/rfc3207/?utm_source=chatgpt.com)

3. **IETF RFC 2595 — Using TLS with IMAP, POP3 and ACAP**
   [RFC 2595 — TLS with IMAP and POP3](https://www.rfc-editor.org/info/rfc2595/?utm_source=chatgpt.com)

4. **IETF RFC 8446 — The Transport Layer Security (TLS) Protocol Version 1.3**
   [RFC 8446 — TLS 1.3](https://www.rfc-editor.org/info/rfc8446/?utm_source=chatgpt.com)

5. **IETF RFC 5280 — Internet X.509 Public Key Infrastructure Certificate and Certificate Revocation List (CRL) Profile**
   [RFC 5280 — X.509 PKI Certificate Profile](https://www.rfc-editor.org/info/rfc5280/?utm_source=chatgpt.com)

6. **Scapy — Python Packet Manipulation and Network Analysis Library**
   [Scapy Documentation](https://scapy.readthedocs.io/?utm_source=chatgpt.com)

7. **PyShark — Python Wrapper for tshark / Wireshark Packet Analysis**
   [PyShark Repository](https://github.com/KimiNewt/pyshark?utm_source=chatgpt.com)

8. **scikit-learn — Machine Learning in Python**
   [scikit-learn Documentation](https://scikit-learn.org/stable/?utm_source=chatgpt.com)

9. **React.js — User Interface Library**
   [React Documentation](https://react.dev/?utm_source=chatgpt.com)

10. **Tailwind CSS — Utility-First CSS Framework**
    [Tailwind CSS Documentation](https://tailwindcss.com/docs?utm_source=chatgpt.com)

11. **MongoDB — Database Platform Documentation**
    [MongoDB Documentation](https://www.mongodb.com/docs/?utm_source=chatgpt.com)

12. **Node.js — JavaScript Runtime Documentation**
    [Node.js Documentation](https://nodejs.org/docs/latest/api/?utm_source=chatgpt.com)

13. **Express.js — Node.js Web Application Framework**
    [Express.js Documentation](https://expressjs.com/?utm_source=chatgpt.com)

14. **Socket.IO — Real-Time Bidirectional Communication**
    [Socket.IO Documentation](https://socket.io/docs/v4/?utm_source=chatgpt.com)

15. **Smart India Hackathon 2026 — SIH26159**
    [Smart India Hackathon Official Website](https://www.sih.gov.in/?utm_source=chatgpt.com)

