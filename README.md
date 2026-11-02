<div align="center">

# Ezz elden Hisham | Offensive Security Researcher & Web Penetration Tester

[![GitHub](https://img.shields.io/badge/GitHub-tlvxyou-181717?style=for-the-badge&logo=github)](https://github.com/tlvxyou)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail)](mailto:ezzelden.hisham.mohamed@gmail.com)
[![HTB](https://img.shields.io/badge/HackTheBox-Rank_1461%2F6744-9FEF00?style=for-the-badge&logo=hackthebox)](https://github.com/tlvxyou)

</div>

---

## 🎯 Core Expertise

```
Hybrid White-Box Source Code Auditing (PHP/Laravel · Python/Flask · Java Bytecode)
         ↕
Black-Box Web & API Exploitation (OWASP Top 10 · Supply-Chain Security · CTF)
```

Specializing in **hybrid security assessment methodology** — combining static source code analysis with dynamic black-box exploitation to uncover vulnerabilities that either approach alone would miss.

---

## 📋 Published Security Audits & Research

| # | Project | Tech Stack | Focus Areas |
|---|---------|-----------|-------------|
| 🔴 | [**Leantime v3.4.12 White-Box & Black-Box Security Assessment**](https://github.com/tlvxyou/offensive-security-research) | PHP / Laravel | IDOR (CWE-639), File Upload (CWE-434), Weak Crypto (CWE-327/330) |
| 🟠 | [**GigSphere Web Application Security Lab**](https://github.com/tlvxyou/GigSphere-Web-Security-Lab) | Python / Flask | OS Cmd Injection · SSRF · SSTI · SQLi · XSS · CSRF · Path Traversal |
| 🟡 | [**Java Agent Supply-Chain & Runtime Malware Audit**](https://github.com/tlvxyou/java-agent-supply-chain-audit) | Java Bytecode | JADX + strace + tcpdump — static + dynamic forensic analysis |
| 🟢 | [**White-Box Python eval() Filter Bypass**](https://github.com/tlvxyou/scriptCTF-2026-wpm-game) | Python / PyJail | scriptCTF 2026 · 441 pts · bytes() ASCII math payload |
| 🔵 | [**Web Exploitation Research**](https://github.com/tlvxyou/offensive-security-research) | Architecture | DNS Rebinding · Cookie Sandwiching · Blind SSRF → RCE chains |
| ⚪ | [**Subdomain Enumeration & Recon Automation**](https://github.com/tlvxyou/subdomain-tool) | Python / CLI | Automated recon tooling for attack surface mapping |

---

## 🏆 CTF & Recognition

-  **HTB Cyber Apocalypse 2026** — Rank **1461 / 6,744** teams | *Team Koshary* (Team Lead)
-  **TechTrek Web Application Security Track** — 2-month professional training

---

## 🛠️ Toolkit

```
Static Analysis    → JADX · Ghidra · Source Code Review (PHP/Python/Java)
Dynamic Analysis   → Burp Suite · strace · tcpdump · Wireshark
Recon & OSINT     → ffuf · nmap · Custom Python Automation
Exploitation       → OWASP Top 10 · SSRF/SSTI/IDOR chains · PyJail escapes
```

---

## 📂 Portfolio Highlights

<details>
<summary><b>🔴 Leantime Security Assessment (CWE-434, CWE-639, CWE-327)</b></summary>

**Target:** Leantime v3.4.12 — PHP/Laravel open-source project management platform

**Key Findings:**
- **Critical** — Unrestricted file upload (CWE-434): MIME type spoofing bypass enabling server-side code execution
- **High** — IDOR via sequential project IDs (CWE-639): horizontal privilege escalation across tenant boundaries
- **High** — Insufficient randomness in session tokens (CWE-330/338): token predictability under brute-force

📄 [Full Report PDF](https://github.com/tlvxyou/offensive-security-research/blob/main/assessments/Leantime-Whitebox-Security-Assessment-Report.pdf)

</details>

<details>
<summary><b>🟠 GigSphere Web Security Lab (8 Vulnerability Categories)</b></summary>

**Dual-instance Flask application** (vulnerable on :5000, hardened on :5001) covering:

| Attack | Endpoint | Payload Example |
|--------|----------|----------------|
| OS Command Injection | `/tools/ping` | `127.0.0.1; whoami` |
| SSRF | `/portfolio/fetch` | `http://169.254.169.254/meta-data/` |
| SSTI | `/profile/badge/preview` | `{{ config.items() }}` |

📄 [OS Command Injection Report](https://github.com/tlvxyou/GigSphere-Web-Security-Lab/blob/main/docs/solutions/OS-Command-Injection-Report.pdf) | [SSRF Report](https://github.com/tlvxyou/GigSphere-Web-Security-Lab/blob/main/docs/solutions/SSRF-Report.pdf) | [SSTI Report](https://github.com/tlvxyou/GigSphere-Web-Security-Lab/blob/main/docs/solutions/SSTI-Report.pdf)

</details>

<details>
<summary><b>🟡 Java Agent Audit (JADX + strace + tcpdump)</b></summary>

**Forensic Verdict:** Benign — License patcher with zero network exfiltration, no malware indicators.

Three-layer analysis methodology: static bytecode decompilation → dynamic kernel tracing → network packet capture.

📄 [Full Audit Report](https://github.com/tlvxyou/java-agent-supply-chain-audit/blob/main/Report.pdf)

</details>

---

<div align="center">

*"The best vulnerability is the one hiding in plain sight — visible only when you read the source."*

</div>
