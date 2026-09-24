# vapt-chime-com
vapt chime.com
# 🛡️ VAPT Project – chime.com

> Vulnerability Assessment & Penetration Testing (VAPT) of chime.com — a structured external security assessment simulating real-world reconnaissance, automated scanning, and manual validation.

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue)
![Type](https://img.shields.io/badge/Type-External%20VAPT-orange)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

---

## 📖 Overview

| Field | Details |
|---|---|
| **Target Domain** | chime.com (enforced via www.chime.com) |
| **Discovered Subdomain** | handbooks.chime.com |
| **Perimeter Defense** | Cloudflare Protected Edge Network |
| **Routing Endpoints** | 172.64.152.131 / 104.18.35.125 |
| **Testing Environment** | Kali Linux (mithu@kali) |
| **Methodology** | Layer 7 Protocol Analysis & Automated Signature Inspection |
| **Author** | Sangamithra |
| **Organization** | SLBS Marklance |
| **Date** | July 2026 |

---

## 🧭 Methodology

1. **Reconnaissance & Service Discovery** – DNS interrogation, host discovery, port scanning
2. **Automated Vulnerability Assessment** – Template-based scanners & web server auditors
3. **Manual Verification & Analysis** – HTTP stream parsing to validate findings

---

## 🔍 Key Findings

| SI.No | Vulnerability | Severity | Status |
|---|---|---|---|
| 1 | Express Framework Disclosure | Low | Identified |
| 2 | Missing Content Security Policy | Low | Identified |
| 3 | Cloudflare Protection | Informational | Verified |

> ✅ No critical vulnerabilities found. External perimeter is highly resilient.

---

## 🧰 Tools Used

| Tool | Purpose |
|---|---|
| `nslookup` / `dig` | DNS Reconnaissance |
| `httpx` | Live Host Discovery |
| `nmap` | Port Scanning & Service Fingerprinting |
| `WhatWeb` | Technology Profiling |
| `curl` | HTTP Header Parsing |
| `Gobuster` | Directory Enumeration |
| `Nikto` | Web Server Auditing |
| `Nuclei` | Template-Based Vulnerability Scanning |

---

## 📂 Repository Structure

- `docs/` → Full VAPT report (DOCX + PDF)
- `screenshots/` → Evidence of each phase
- `commands/` → All commands executed
- `findings/` → Vulnerability details & remediation
- `tools/` → Tools documentation

---

## 🛠️ Remediation Summary

### 1. Disable Express Framework Signature
```javascript
const express = require('express');
const app = express();
app.disable('x-powered-by');
