# Metasploitable 2 Security Assessment

## Project Overview

An authorized security assessment of a Metasploitable 2 virtual machine using Kali Linux and Nmap.

This project demonstrates practical skills in network reconnaissance, TCP port scanning, service enumeration, preliminary risk assessment, security documentation, and evidence collection.

## Lab Environment

| Component | Details |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable 2 |
| Virtualization | Oracle VirtualBox |
| Scanning Tool | Nmap 7.99 |
| Assessment Type | Authorized Lab Assessment |

## Project Objectives

- Identify active network services.
- Discover open TCP ports.
- Identify legacy services and software versions.
- Document potential security weaknesses.
- Perform preliminary risk assessment.
- Recommend security improvements.

## Methodology

1. Network connectivity verification
2. Target identification
3. TCP port discovery
4. Service and version detection
5. Security findings documentation
6. Preliminary risk assessment
7. Security recommendations
8. Final reporting

## Key Observations

The assessment identified:

- 23 open TCP ports in the initial scan.
- Legacy remote access services.
- An FTP service running vsftpd 2.3.4.
- An Apache HTTP server running version 2.2.8.
- MySQL and PostgreSQL services accessible over the network.

These observations do not independently establish exploitability.

## Repository Structure

```text
Ethical-Hacking-Project/
├── recon/
├── scans/
├── evidence/
├── reports/
├── .gitignore
└── README.md
```

## Reports

Detailed documentation is available in the `reports/` directory:

- Service analysis
- Security findings
- Risk assessment
- Security recommendations
- Final assessment report

## Evidence

The `evidence/` directory contains screenshots documenting connectivity checks and Nmap scanning activities.

## Limitations

- Assessment was conducted in an isolated laboratory.
- Findings are based on observed network services.
- Configuration-level weaknesses were not independently verified.
- No successful exploitation is claimed.

## Disclaimer

This project was conducted for educational purposes in an authorized virtual laboratory environment. Do not scan or test systems without explicit permission.

## Skills Demonstrated

Kali Linux | Nmap | Network Reconnaissance | TCP Scanning | Service Enumeration | Risk Assessment | Technical Documentation | Git
