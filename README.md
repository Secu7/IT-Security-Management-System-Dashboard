# IT-Security-Management-System-Dashboard

A browser-based cybersecurity dashboard that simulates the core functions of a modern Security Operations Center (SOC). This project was designed from the perspective of a security analyst with hands-on experience in threat detection, incident response, and compliance monitoring in enterprise environments.

---

## Overview

The dashboard provides a unified view of simulated threat intelligence, incident triage, vulnerability exposure, access control, and compliance status across segmented enterprise networks.

Rather than focusing on visuals, this system models how analysts make decisions. It combines real-world frameworks like MITRE ATT&CK, NIST CSF, Zero Trust, and SOC 2 into an interface built to support simulated security operations.

---

## Key Features

- Simulates detection of common threats: APTs, Kerberoasting, DNS tunneling, default credentials, CVE exploitation
- Uses MITRE ATT&CK techniques to categorize incidents
- Tracks SLA and response metrics (MTTD, MTTR)
- Highlights Zero Trust segmentation, remote access posture, and user behavior
- Visualizes CVSS-based vulnerabilities with patch coverage and exploit readiness
- Displays compliance metrics across SOC 2, ISO 27001, and internal audit readiness

---

## Designed for Security Analysts

Each component of the dashboard is based on operational workflows used by real analysts:

- Incident response triage with mapped tactics and techniques
- IAM views showing AD health, privilege levels, and MFA coverage
- Network segmentation monitoring aligned to RFC 1918 design
- Vulnerability scanning workflows (simulated Nmap, Nessus, ZAP, etc.)
- Compliance tracking linked to training, control tests, and audit metrics

For threat scenarios and how each part of the UI maps to real workflows, see:

- `/docs/use-cases.md`
- `/docs/architecture.md`

---

## System Architecture

- Static frontend built with HTML5, CSS3, JavaScript (ES6+), and Chart.js
- Runs entirely in the browser, no backend or installation required
- Responsive layout for 1920x1080 and tablets
- Secure by design: no telemetry, no external calls, no persistent storage

---

## Network Scope Simulated

| Segment           | Purpose                             | CIDR               |
|-------------------|-------------------------------------|--------------------|
| Internal LAN      | Finance and executive workstations  | 192.168.1.0/24     |
| DMZ               | Web, mail, and public servers       | 10.0.1.0/24        |
| Server Farm       | Application and database servers    | 172.16.0.0/16      |
| VPN Pool          | Remote access endpoint range        | 10.8.0.0/24        |
| IoT/OT            | Smart building and ICS              | 192.168.100.0/24   |
| Guest WiFi        | Visitor and unmanaged devices       | 192.168.200.0/24   |

Each segment is associated with simulated data to represent different risk levels and exposure points.

---

## Running the Dashboard

No installation required. Just clone and open the HTML file:

```bash
git clone https://github.com/Secu7/IT-Security-Management-System-Dashboard.git
cd IT-Security-Management-System-Dashboard
open index.html  

Click "Execute Full-Spectrum Security Scan" to start the interactive simulation.

Technical Details
Built with Chart.js for dynamic visualization

Custom scan logic simulates Nmap, Nessus, ZAP, SQLMap, AD tools, and threat correlation rules

Each security card and chart is tied to a use case based on real threat types

Clean modular structure for easy extension and theming
