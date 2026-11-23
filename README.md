# Metasploitable 2 Security Assessment

![Security Assessment](https://img.shields.io/badge/Project-Authorized%20Lab-blue)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-black)
![Tool](https://img.shields.io/badge/Tool-Nmap-orange)
![Status](https://img.shields.io/badge/Status-Documented-success)

## Project Overview

An authorized security assessment of a Metasploitable 2 virtual machine using Kali Linux and Nmap.

This project demonstrates practical cybersecurity skills in network reconnaissance, TCP port scanning, service enumeration, preliminary risk assessment, security documentation, and evidence collection.

## Lab Environment

| Component | Details |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable 2 |
| Target IP | 192.168.56.102 |
| Virtualization | Oracle VirtualBox |
| Scanning Tool | Nmap 7.99 |
| Assessment Type | Authorized Lab Assessment |

## Project Objectives

- Identify active network services.
- Discover open TCP ports.
- Identify legacy services and software versions.
- Document potential security weaknesses.
- Perform preliminary risk assessment.
- Recommend defensive security improvements.
- Maintain professional technical documentation.

## Methodology

1. Laboratory preparation
2. Network connectivity verification
3. Target identification
4. TCP port discovery
5. Service and version detection
6. Security findings documentation
7. Preliminary risk assessment
8. Defensive recommendations
9. Final assessment reporting

## Key Findings

The initial Nmap scan identified:

- 23 open TCP ports within the top 1,000 scanned ports.
- Legacy remote access services, including Telnet and RSH-related services.
- FTP running vsftpd 2.3.4.
- Apache HTTP Server 2.2.8.
- MySQL 5.0.51a.
- PostgreSQL 8.3.0–8.3.7.
- Additional file-sharing and remote application services.

**Important:** Identifying an exposed service or outdated version does not independently confirm that a vulnerability is exploitable.

## Repository Structure

```text
Ethical-Hacking-Project/
│
├── recon/
│   ├── ping-results.txt
│   └── target-neighbor.txt
│
├── scans/
│   ├── initial-port-scan.txt
│   ├── legacy-services.txt
│   └── web-database-services.txt
│
├── evidence/
│   ├── 01-connectivity.png
│   ├── 02-port-scan.png
│   ├── 03-legacy-services.png
│   ├── 04-web-database.png
│   └── evidence-index.txt
│
├── reports/
│   ├── final-assessment-report.md
│   ├── risk-assessment.txt
│   ├── security-findings.txt
│   ├── security-recommendations.txt
│   └── service-analysis.txt
│
├── .gitignore
└── README.md
```

## Project Documentation

The detailed reports are available below:

- [Final Security Assessment](reports/final-assessment-report.md)
- [Security Findings](reports/security-findings.txt)
- [Risk Assessment](reports/risk-assessment.txt)
- [Security Recommendations](reports/security-recommendations.txt)
- [Service Analysis](reports/service-analysis.txt)

## Evidence Collection

Screenshots documenting the assessment are stored in the `evidence/` directory.

| Evidence | Description |
|---|---|
| 01 | Network connectivity |
| 02 | Initial port scan |
| 03 | Legacy service detection |
| 04 | Web and database service detection |

## Tools and Technologies

- Kali Linux
- Nmap 7.99
- Oracle VirtualBox
- Linux Terminal
- Markdown
- Git and GitHub

## Assessment Limitations

- The initial scan covered the top 1,000 TCP ports.
- Version detection covered selected ports.
- Configuration-level weaknesses were not fully verified.
- No successful exploitation is claimed.
- Some discovered services require further identification.

## Disclaimer

This project was conducted for educational purposes within an authorized virtual laboratory environment.

Never scan or test systems without explicit permission.

## Skills Demonstrated

`Kali Linux` · `Nmap` · `Network Reconnaissance` · `TCP Scanning` · `Service Enumeration` · `Risk Assessment` · `Security Documentation` · `Git` · `GitHub`

---

**Project:** Metasploitable 2 Security Assessment
**Environment:** Authorized Virtual Lab
**Report Status:** Assessment Documented
