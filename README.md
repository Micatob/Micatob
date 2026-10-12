# Hi, I'm Micato 👋 — Network Engineer | SOC Analyst | Pen Tester | IT Support Specialist | CEO @ Micatech

[![Profile Views](https://komarev.com/ghpvc/?username=Micatob&color=0e75b6&style=flat)](https://github.com/Micatob)
[![Follow](https://img.shields.io/github/followers/Micatob?label=Follow&style=social)](https://github.com/Micatob?tab=followers)
[![X](https://img.shields.io/badge/X-%40Micatob-black?style=flat&logo=x)](https://x.com/Micatob)
[![Website](https://img.shields.io/badge/Web-hiresphere.com.ng-blue?style=flat&logo=google-chrome)](https://hiresphere.com.ng)
[![Micatech](https://img.shields.io/badge/Micatech-micatech.vercel.app-purple?style=flat&logo=vercel)](https://micatech.vercel.app)
<!-- TikTok / YouTube coming soon - uncomment when ready:
[![TikTok](https://img.shields.io/badge/TikTok-@YOURHANDLE-black?style=flat&logo=tiktok)](https://tiktok.com/@YOURHANDLE)
[![YouTube](https://img.shields.io/badge/YouTube-@YOURHANDLE-red?style=flat&logo=youtube)](https://youtube.com/@YOURHANDLE)
-->

> Network Engineer • SOC Analyst (Blue Team) • Junior Penetration Tester • IT Support Specialist • CEO of **Micatech** — I build and secure LANs, hunt threats with my own SIEM, test for holes with my own toolkit, fix IT end-to-end, and ship fast for clients.

## About Me

I'm **Micato (@Micatob)**, based in **Nigeria**. My goals are clear: **secure networks, detect attacks fast, test like an attacker, fix like IT.**

- **Networking:** LAN design & setup, TCP/IP, subnetting, routing & switching (Cisco-style), Wi-Fi, cabling, DHCP/DNS, VPNs, troubleshooting.
- **SOC / Defensive Security:** SOC workflows, log analysis, threat detection & triage, Wireshark, OSINT, vulnerability scanning, hardening — powered by **Chael SIEM**.
- **Penetration Testing (Offensive):** recon, vuln scanning, credential testing, enumeration, CVE mapping, reporting — powered by **Athena**.
- **IT Support:** Windows 10/11, Linux (Ubuntu/Kali), Active Directory, system setup, printers, helpdesk, backup & recovery, AnyDesk/RDP, end-user training.
- **Build (lean & fast):** Python security tooling, static landing pages (HTML/CSS/JS), Git & GitHub, Flutter/Dart basics, AI-assisted workflows.

As CEO of **Micatech**, I render tech services for businesses and individuals: **Web • Cyber • IT • Networking jobs.**

**Open to:** SOC / defensive security roles, network setup contracts, pentest / audit gigs (authorized only), IT support contracts, and Micatech client projects.

## 🚀 Flagship Project: CHAEL SIEM — Microservices Security Analytics Platform

> **[Micatob/chael](https://github.com/Micatob/chael)** — My biggest build. A modern, containerized SIEM for real SOC work on small networks.

**What it is:** FastAPI + OpenSearch + Redis + Nginx gateway + React dashboard. Real-time log ingestion, correlation-based detection, incident lifecycle, and SOAR automation — all Docker-Compose up.

**Why it's flagship:**
- Full SOC loop in one repo: `Agent → Gateway → Ingest → Correlate → Incidents → SOAR → Dashboard`
- Built for practical SOC monitoring, not a toy logger — JWT auth, agent registry, Redis counters, Prometheus metrics, NetFlow collector
- Shows my core goal: **defend systems with my own SIEM**

**Key capabilities:**
- **Log Ingestion:** normalized `/ingest` + auto-normalized `/raw/{source}` — auth failures never deduped so brute-force survives
- **Correlation Engine:** 5+ SSH fails / 60s → MEDIUM (risk 65), 15+ → HIGH (risk 85), internal ranges whitelisted via `config.yaml`, fatigue control (50/source/hr, 5-min cooldown)
- **Incidents:** triage, forensic investigate (MITRE mapping, IOC enrichment, FP checklist), analytics overview
- **SOAR:** trigger playbooks, manual approve, audit + notifications
- **Extras:** ML Analytics (UEBA), Threat Feed (IOC polling), Sigma → Chael converter, Data Archiver (retention/backup), AI Assistant (BYOK co-pilot), Flow Collector (:2055/udp)
- **Ops:** one-command Windows deploy `.\deploy.ps1`, gateway `:8001`/`:8443`, dashboard `:3000`, OpenSearch `:9200`, Prometheus `:9090`

**Stack:** Python FastAPI • OpenSearch • Redis • Nginx • React • Docker • Prometheus • Sigma • NetFlow

```bash
# flagship quickstart
.\deploy.ps1
# → http://localhost:3000 (admin / ADMIN_PASSWORD in .env)
```

👉 Dive in: **[github.com/Micatob/chael](https://github.com/Micatob/chael)** — see `AGENT_DEPLOYMENT.md`, `ROADMAP.md`, `HUNTING_ROADMAP.md`. Ideas on detection rules, parsing & dashboards welcome.

---

## What I Do — 4 Pillars

| Pillar | What I deliver |
| ------ | --------------- |
| 🌐 **Network Engineer** | LAN setup from scratch: planning, IP addressing, switch/router config, patching, testing, documentation. Small office / home / campus LANs that just work. |
| 🛡️ **SOC Analyst — Chael** | Defensive monitoring with **Chael SIEM**: log collection, detection tuning, incident triage, threat intel, SOAR response. Wireshark, log review, OSINT, hardening. |
| ⚔️ **Pen Tester — Athena** | Authorized offensive testing with **[Athena](https://github.com/Micatob/Athena)**: full PTES lifecycle discovery → vuln scan → creds → enum → CVE → report. See below. |
| 🧰 **IT Support Specialist** | Full desktop & user support: OS install, software/drivers, AD accounts, file sharing, network printers, remote support, maintenance, troubleshooting under pressure. |
| 🚀 **CEO — Micatech** | Tech startup for Web, Cyber, IT & Networking. Clear scope, fast delivery, support after deployment. |

### ⚔️ Pen Testing: Athena — All-in-One Pentest Toolkit

**[Micatob/Athena](https://github.com/Micatob/Athena)** — async Python 3 framework that automates discovery → vuln scan (30+ checks: SQLi, XSS, CMDi, LFI, SSRF, SSTI, XXE, etc.) → credential testing (FTP/SSH/SQL/Redis/Telnet + form stuffing) → SMB/SNMP/SMTP enum → CVE mapping (CVSS) → HTML/JSON/CSV/PDF reports.

- PTES-aligned 11-stage pipeline, safe-mode + auth gates, evasion (jitter, UA rotation, Tor/proxy, ~90 WAF fingerprints + tamper bypass), AI correlation (Gemini/Groq/DeepSeek failover), REST API + Chrome ext, post-exploit chain.
- **Use responsibly — authorized targets only.**

### 🛡️ SOC: Chael — Defend & Respond

SOC is my defensive core. Chael SIEM is how I practice it daily: ingest syslog/auth logs, write correlation rules, triage incidents, enrich IOCs, run SOAR playbooks, hunt with `HUNTING_ROADMAP.md`. Workflow: monitor → detect → investigate → contain → recover → lessons-learned. Tools: Chael + Wireshark + Nmap + OSINT + Linux hardening.

### 🧰 IT + 🌐 Networking: Keep Systems Running

IT + Networking is my foundation: LAN/WAN design, Cisco IOS routing/switching, subnetting, DHCP/DNS, VPN, Wi-Fi/cabling, Windows/Linux admin, AD, backup, printers, helpdesk. If it connects or boots, I fix it — documented and handed over clean.

## 🏢 Micatech — Tech Services

**Micatech** = your one-stop shop for:

- LAN design, installation & troubleshooting
- SOC monitoring, cybersecurity assessments & hardening (defensive)
- Authorized pentests & audit reports (via Athena)
- IT setup & managed support for small businesses
- Static websites & landing pages for businesses

👉 Hire / Contact via: **https://hiresphere.com.ng** • X: **[@Micatob](https://x.com/Micatob)**

> Want a Micatech job done? Send scope + location + timeline via hiresphere.com.ng and I’ll respond with plan + quote.

## 🛠️ Tech Stack

**Networking:** TCP/IP • Subnetting • LAN/WAN • Cisco IOS • Routing & Switching • DHCP/DNS • VPN • Wireshark • Nmap

**Defensive Security (SOC):** SOC workflows • Chael SIEM • Log Analysis • Correlation Rules • Incident Triage • SOAR • Wireshark • OSINT • Vulnerability Scanning • Linux Hardening • Sigma

**Offensive Security (Pentest):** Athena • Recon • Web Vuln Scanning • Bruteforce / Cred Stuffing • SMB/SNMP/SMTP Enum • CVE Mapping • Burp Suite (basics) • WAF Evasion

**IT Support:** Windows 10/11 • Linux (Ubuntu/Kali) • Active Directory • Helpdesk • Troubleshooting • Backup • Remote Tools (AnyDesk/RDP) • MS Office

**Build / Web / Tools:** Python (FastAPI, asyncio/aiohttp) • OpenSearch/Redis/Docker/Nginx • HTML/CSS/JavaScript • React (dashboard) • Git & GitHub • Flutter/Dart (basic) • AI-assisted development

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![OpenSearch](https://img.shields.io/badge/OpenSearch-005EB8?style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Networking](https://img.shields.io/badge/Networking-TCP%2FIP-blue?style=flat)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat&logo=wireshark&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-0E8320?style=flat)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## 📌 Featured Projects

| Project | What it is | Stack |
| ------- | ---------- | ----- |
| [⭐ chael — CHAEL SIEM](https://github.com/Micatob/chael) | **FLAGSHIP** — Microservices SIEM: ingest + correlation + incidents + SOAR + ML + Sigma + threat feed | Python FastAPI + OpenSearch + React + Docker |
| [Athena](https://github.com/Micatob/Athena) | All-in-one penetration testing toolkit — full PTES automation + reporting | Python asyncio |
| [Xss-Scanner](https://github.com/Micatob/Xss-Scanner) | Reflected XSS payload tester (3000+ payloads) with built-in AI assistant | Python + AI |
| [Deep-Directory](https://github.com/Micatob/Deep-Directory) | Next-gen directory enumeration: brute-force + crawling + fuzzing | Python |
| [Device-Monitor](https://github.com/Micatob/Device-Monitor) / [PDF-Lite](https://github.com/Micatob/PDF-Lite) | Lightweight mobile utilities | Dart/Flutter |

## 📊 GitHub Stats

![Micatob's GitHub stats](https://github-readme-stats.vercel.app/api?username=Micatob&show_icons=true&theme=dark)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Micatob&layout=compact&theme=dark)
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=Micatob&theme=dark)

## 🤝 Connect

- 🌍 Website / Hire me: **https://hiresphere.com.ng**
- 🌐 Micatech App: **https://micatech.vercel.app**
- ✖️ X (Twitter): **[@Micatob](https://x.com/Micatob)**
- 🎵 TikTok: *coming soon — send handle and I’ll link it*
- ▶️ YouTube: *coming soon — send channel and I’ll link it*
- 💼 Company: **Micatech — Web • Cyber • IT • Networking**
- 📍 Location: Nigeria (open to remote & on-site)

---

<!-- SEO: Network Engineer Nigeria, LAN Setup, Cisco, TCP/IP, Cybersecurity Analyst, SOC Analyst, Defensive Security, Blue Team, SIEM, Chael SIEM, Penetration Tester Athena PTES, IT Support Specialist, Windows Linux Support, Active Directory, Micatech CEO, Python Security Tools, OSINT -->
