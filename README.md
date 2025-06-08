# Enterprise SOC Threat Intelligence Dashboard

An interactive, analyst-designed cybersecurity dashboard simulating the core functions of a modern Security Operations Center (SOC). It integrates incident response, vulnerability management, and compliance tracking into a unified interface, grounded in real-world operational needs and industry-standard security frameworks.

---

## Overview

This project is built from the perspective of a cybersecurity analyst with experience in enterprise SOC operations, combining visual clarity with the structure required to reflect actual threat environments.

Rather than just showcasing UI elements, this dashboard was designed to reflect:

- How security analysts prioritize threats across networks
- The way incidents are triaged and mapped to MITRE ATT&CK
- What KPIs matter in a mature cybersecurity program
- How Zero Trust and segmentation work in practice

---

## Key Capabilities

- **Real-Time Incident Simulation**  
  Simulates APT campaigns (e.g., APT29), lateral movement, data exfiltration, and privilege escalation attempts using structured threat scenarios.
  
- **Security Framework Mapping**  
  Every card reflects industry best practices:  
  - MITRE ATT&CK TTP mapping  
  - NIST Cybersecurity Framework (Identify → Recover)  
  - SOC 2 Type II & ISO 27001 metrics  
  - Zero Trust segmentation & access control

- **Threat Intelligence Visualization**  
  Dynamic threat charts display IOC detection, mitigation rates, and evolving attack trends using mock feeds (OTX, FireEye, MISP).

- **Simulated Scanning Engine**  
  Clicking **"Execute Full-Spectrum Security Scan"** triggers a multi-phase scan process (Nmap, Nessus, ZAP, Metasploit, etc.) with progress tracking and dynamic output.

- **Modular Security Cards**  
  The dashboard is organized into:
  - Incident Response & SIEM Alerts
  - Identity & Access Management
  - Vulnerability Management (CVEs, patch status, exploitability)
  - Data Loss Prevention
  - Threat Intel Dashboard
  - Governance, Risk, and Compliance

---

## Analyst Design Intent

This dashboard is informed by real-world SOC experience:

- Designed to reflect workflows of Level 1–3 analysts
- Emphasizes SLA-based triage, TTP attribution, and response metrics
- Incorporates metrics like MTTD, MTTR, patch coverage, and compliance scoring
- Simulates environments commonly found in financial, healthcare, and critical infrastructure sectors

---

## Architecture & Technologies

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Visualization**: Chart.js 3.9.1
- **Design Principles**:
  - No external data calls or server-side logic
  - Fully static, runs in-browser for demonstration
  - Responsive layout for desktop and tablet
- **Security Concepts Modeled**:
  - Network micro-segmentation (RFC 1918-compliant)
  - Privileged access monitoring (CyberArk-style logic)
  - Threat scoring and behavior analytics (UBA-style)
  - DLP and CASB policy simulation

---

## Sample Threat Scenarios Included

- **APT29 C2 Activity**  
  Beacon detection in VPN segment, tied to MITRE T1071.001  
- **Kerberoasting + Golden Ticket**  
  AD abuse simulation in internal LAN  
- **DNS Tunneling (Exfiltration)**  
  Lateral movement and stealthy exfiltration path detection  
- **IoT Segment Vulnerability**  
  Air-gapped OT network with default credentials issue  
- **CVE Exploits**  
  CVE-2024-3094 (XZ backdoor), CVE-2024-0012 (PAN-OS bypass), and more

---

## Getting Started

No backend or install required.

```bash
git clone https://github.com/Secu7/soc-threat-dashboard.git
cd soc-threat-dashboard

Then open index.html in your browser.

You can click the red "Execute Full-Spectrum Security Scan" button to start the interactive scan simulation and watch metrics update in real time.

Target Audience
SOC Analysts (Tier 1–3)

Incident Response and Threat Hunting Teams

Security Architects and Governance Leads

Candidates preparing for SC-200, AZ-500, or CISSP

Notes
Data is fully simulated for demonstration purposes.

Designed for desktop resolutions (optimal at 1920x1080).

All security scenarios, metrics, and mappings are modeled from actual operational practices.

