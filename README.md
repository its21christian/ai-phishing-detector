# CyberGuard AI | Phishing & Threat Intelligence Suite

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Cybersecurity: Defensive](https://img.shields.io/badge/Domain-Cybersecurity%20%7C%20Blue%20Team-00f0ff.svg)](#)
[![Zero Dependency](https://img.shields.io/badge/Dependencies-None%20(Pure%20Client--Side)-brightgreen.svg)](#)
[![Platform](https://img.shields.io/badge/Platform-Modern%20Browsers-orange.svg)](#)

An open-source, client-side cybersecurity inspection engine and SOC incident triage dashboard designed to analyze suspicious emails, web domains, and SMS messages for social engineering vectors, credential theft patterns, and malicious intent.

---

## Key Features

- **Multi-Vector Analysis:**
  - **Email Analyzer:** Inspects body text and raw RFC-822 headers for sender impersonation, psychological urgency, and sensitive data solicitation.
  - **URL & Domain Scanner:** Analyzes hostnames, path depth, TLD reputation, brand typosquatting, and direct IP usage.
  - **SMS / Smishing Inspector:** Detects parcel delivery lures, financial alert impersonations, and redirect links.
- **Dynamic Threat Speedometer:** Real-time SVG radial gauge that sweeps and changes colors based on the confidence ratio:
  - `SAFE / LOW RISK` (0% – 29%)
  - `SUSPICIOUS` (30% – 69%)
  - `CRITICAL / MALICIOUS` (70% – 100%)
- **Payload X-Ray:** In-line tokenizer highlighting exact trigger phrases and patterns directly within the source text.
- **Automated SOC Incident Logging:** Hands-free background streaming of scan records to a centralized Google Sheets incident report dashboard via webhooks.
- **Admin Passkey Gate:** Secure client-side administrative lock preventing unauthorized tampering with sync endpoints on public deployments.
- **One-Click Forensics Export:** Instant incident report generation and export in structured JSON format.

---

## Live Threat Intelligence Pipeline

```text
[ Raw Input: Email / URL / SMS ]
                │
                ▼
  [ Heuristic Analysis Engine ] ──► [ Real-Time UI Telemetry & Gauge ]
                │
                ▼
     [ Incident JSON Object ]
                │
                ▼
   [ Background Apps Script Webhook ]
                │
                ▼
[ Google Sheets SOC Incident Dashboard ]
  ├── Real-Time Executive KPI Metric Cards
  ├── Color-Coded Threat Level Badges
  └── Auto-Wrapped Forensic Payload Audit Log
