<div align="center">

# Ezz elden Hisham | Offensive Security Practitioner & Web Application Penetration Tester

[![GitHub](https://img.shields.io/badge/GitHub-tlvxyou-181717?style=for-the-badge&logo=github)](https://github.com/tlvxyou)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail)](mailto:ezzelden.hisham.mohamed@gmail.com)
[![HTB](https://img.shields.io/badge/HackTheBox-Rank_1461%2F6744-9FEF00?style=for-the-badge&logo=hackthebox)](https://github.com/tlvxyou)

*Focused on White-Box Source Code Review (Python/Flask, PHP/Laravel, Java Bytecode) & Black-Box Web/API Exploitation.*

</div>

---

## Core Expertise

```
White-Box Source Code Review (PHP/Laravel · Python/Flask · Java Bytecode)
         ↕
Black-Box Web & API Exploitation (OWASP Top 10 · Supply-Chain Security · CTF)
```

Combining static source code analysis with dynamic black-box testing to surface vulnerabilities that either approach alone would miss — then documenting findings with technically precise, reproducible reports.

---

## 📋 Published Security Audits & Research

| # | Project | Tech Stack | Focus Areas |
|---|---------|-----------|-------------|
| 🔴 | [**Leantime v3.4.12 — Source Code & Hardening Audit**](https://github.com/tlvxyou/offensive-security-research) | PHP / Laravel | IDOR (CWE-639), File Upload MIME validation (CWE-434), Token entropy (CWE-330/338) |
| 🟠 | [**GigSphere Web Application Security Lab**](https://github.com/tlvxyou/GigSphere-Web-Security-Lab) | Python / Flask | OS Cmd Injection · SSRF · SSTI · SQLi · XSS · CSRF · Path Traversal |
| 🟡 | [**Java Agent Supply-Chain & Runtime Audit**](https://github.com/tlvxyou/java-agent-supply-chain-audit) | Java Bytecode | JADX static decompilation + strace syscall tracing + tcpdump network capture |
| 🟢 | [**White-Box Python eval() Filter Bypass**](https://github.com/tlvxyou/scriptCTF-2026-wpm-game) | Python / PyJail | scriptCTF 2026 · 444 pts · bytes() ASCII math + open() exception-leak chain |
| 🔵 | [**Web Exploitation Research**](https://github.com/tlvxyou/offensive-security-research) | Architecture | DNS Rebinding · Cookie Sandwiching · Blind SSRF → RCE chains |
| ⚪ | [**Subdomain Enumeration & Recon Automation**](https://github.com/tlvxyou/subdomain-tool) | Python / CLI | Automated recon tooling for attack surface mapping |

---

## CTF & Recognition

- **HTB Cyber Apocalypse CTF 2026** — Ranked **1461 / 6,744 Teams** (Top 22% Globally, 6,150 pts) | Founder & Team Lead, Koshary CTF
- 🎓 **TechTrek Web Application Security Track** — 2-month professional training program

---

## 🛠️ Toolkit

```
Static Analysis    → JADX · Source Code Review (PHP/Python/Java) · Ghidra
Dynamic Analysis   → Burp Suite · strace · tcpdump · Wireshark
Recon & OSINT     → ffuf · nmap · Custom Python Automation
Exploitation       → OWASP Top 10 · SSRF/SSTI/IDOR chains · PyJail escapes
```

---

## 📂 Portfolio Highlights

<details>
<summary><b>🔴 Leantime — Source Code & Hardening Audit (CWE-434, CWE-639, CWE-330/338)</b></summary>

**Target:** Leantime v3.4.12 — PHP/Laravel open-source project management platform

**Scope:** Independent local source-code review and runtime hardening assessment evaluating token derivation (`SHA1(CONCAT(id, sessionPassword))`), file upload MIME/magic-byte normalization, avatar endpoint authorization, and CSPRNG controls (`random_bytes()` vs `str_shuffle()`).

**Architectural & Defense-in-Depth Hardening Findings:**
- **File Upload MIME Normalization (CWE-434):** Upload endpoint validated file type client-side only; server-side magic-byte normalization was absent. Exploitability requires write access to the upload directory to be meaningful.
- **Sequential Project ID Authorization (CWE-639):** Project access was gated by session authentication but not cryptographic ownership binding. Incrementing the numeric ID returns project metadata for other tenants — horizontal escalation within the authenticated tier.
- **Token Entropy (CWE-330/338):** `SHA1(CONCAT(id, sessionPassword))` — exploitability requires prior leakage of `sessionPassword`. The finding flags the derivation function as architecturally weaker than a CSPRNG-derived token.

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
<summary><b>🟡 Java Agent Audit — JADX + strace + tcpdump (Air-Gapped VM)</b></summary>

**Forensic Verdict:** Benign — License patcher with zero outbound network activity, no malware indicators.

Three-layer methodology: JADX static bytecode decompilation → strace syscall tracing (isolated VM, no WAN gateway) → tcpdump full packet capture. Dynamic execution targeted the standalone `KeygenForm` invocation; `-javaagent` instrumentation hooks were audited statically only.

📄 [Full Audit Report](https://github.com/tlvxyou/java-agent-supply-chain-audit/blob/main/Report.pdf)

</details>

---

<div align="center">

*"The best vulnerability is the one hiding in plain sight — visible only when you read the source."*

</div>
