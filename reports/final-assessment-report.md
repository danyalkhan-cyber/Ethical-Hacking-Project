
# Metasploitable 2 Security Assessment Report

## 1. Project Information

- Project: Ethical Hacking Security Assessment
- Target: 192.168.56.102
- Target OS: Metasploitable 2
- Testing Machine: Kali Linux
- Primary Tool: Nmap 7.99
- Assessment Date: 23 November 2026
- Assessment Type: Authorized Laboratory Assessment

## 2. Executive Summary

An authorized security assessment was conducted
against a Metasploitable 2 virtual machine.

The assessment identified 23 open TCP ports
within the top 1,000 TCP ports scanned.

Several outdated software versions and legacy
network services were identified.

The main security concerns include:
- Unencrypted remote access protocols.
- Legacy FTP service.
- Outdated Apache web server.
- Exposed database services.
- Additional network and application services.

All findings are based on observed scan evidence.
Exploitability was not independently confirmed.

## 3. Scope and Authorization

Target IP: 192.168.56.102

Testing was limited to the authorized Metasploitable 2
virtual machine in a controlled laboratory environment.

### In Scope
- Host discovery
- TCP port scanning
- Service identification
- Version detection
- Preliminary risk assessment
- Defensive recommendations

### Out of Scope
- External network testing
- Third-party systems
- Denial-of-Service testing
- Unauthorized access attempts

## 4. Assessment Methodology

The assessment followed these stages:

1. Laboratory preparation
2. Network connectivity verification
3. TCP port scanning
4. Service enumeration
5. Preliminary risk assessment
6. Security documentation
7. Defensive recommendations

## 5. Network Scan Results

The initial Nmap scan examined the top 1,000 TCP ports.

Target: 192.168.56.102

Result: 23 open TCP ports identified.

| Port | Service |
|---|---|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 111 | RPCBind |
| 139 | NetBIOS |
| 445 | SMB |
| 512 | rexec |
| 513 | login |
| 514 | shell |
| 1099 | Java RMI Registry |
| 1524 | ingreslock |
| 2049 | NFS |
| 2121 | FTP |
| 3306 | MySQL |
| 5432 | PostgreSQL |
| 5900 | VNC |
| 6000 | X11 |
| 6667 | IRC |
| 8009 | AJP13 |
| 8180 | Unknown |

## 6. Confirmed Service Version Detection

Nmap version detection identified the following:

| Port | Service | Detected Version |
|---|---|---|
| 21 | FTP | vsftpd 2.3.4 |
| 23 | Telnet | Linux telnetd |
| 512 | rexec | netkit-rsh rexecd |
| 513 | login | OpenBSD or Solaris rlogind |
| 514 | shell | Netkit rshd |
| 80 | HTTP | Apache 2.2.8 (Ubuntu) |
| 3306 | MySQL | 5.0.51a-3ubuntu5 |
| 5432 | PostgreSQL | 8.3.0 - 8.3.7 |

Note: Version detection was performed on selected
ports, not all 23 discovered services.

## 7. Security Findings

### Finding 1: Legacy Remote Access

Affected ports:
- 23/tcp - Telnet
- 512/tcp - rexec
- 513/tcp - rlogin
- 514/tcp - rsh

Severity: High (Provisional)

Observation:
Legacy remote access protocols were identified.

Risk:
These protocols may expose sensitive communication
because they lack modern transport security.

Recommendation:
Disable unnecessary legacy services and use SSH.

### Finding 2: FTP Service

Port: 21/tcp
Version: vsftpd 2.3.4

Severity: Medium (Provisional)

Observation:
An outdated FTP service was detected.

Risk:
Traditional FTP does not encrypt credentials
or transferred data.

Recommendation:
Use SFTP or appropriately configured FTPS.

Note:
The historically reported backdoor issue associated
with this version was not independently verified.

### Finding 3: Legacy Web Server

Port: 80/tcp
Version: Apache 2.2.8 (Ubuntu)

Severity: Medium (Provisional)

Observation:
An outdated Apache version was detected.

Risk:
Outdated software may lack important security updates.

Recommendation:
Upgrade to a supported release and review
server configuration.

### Finding 4: Database Network Exposure

Affected ports:
- 3306/tcp - MySQL 5.0.51a
- 5432/tcp - PostgreSQL 8.3.0 - 8.3.7

Severity: Medium (Provisional)

Observation:
Two database services were accessible over the network.

Risk:
Improper access controls may expose database information.

Recommendation:
Restrict database access to authorized hosts.
Review authentication and user permissions.

### Finding 5: File Sharing and Infrastructure Services

Affected ports:
- 53/tcp - DNS
- 111/tcp - RPCBind
- 139/tcp - NetBIOS
- 445/tcp - SMB
- 2049/tcp - NFS

Severity: Requires Further Review

Observation:
Multiple infrastructure and file-sharing services
were identified.

Recommendation:
Review access controls, permissions and firewall rules.
Disable unnecessary services.

### Finding 6: Additional Remote and Application Services

Affected ports:
- 1099/tcp - Java RMI Registry
- 5900/tcp - VNC
- 6000/tcp - X11
- 8009/tcp - AJP13
- 8180/tcp - Unknown

Severity: Requires Further Review

Observation:
Additional remote and application-related services
were identified.

Recommendation:
Identify each service, review its configuration,
and restrict unnecessary network access.

## 8. Risk Summary

| Finding | Preliminary Severity |
|---|---|
| Legacy remote access | High |
| FTP service | Medium |
| Legacy Apache server | Medium |
| Database exposure | Medium |
| File sharing services | Further Review |
| Additional application services | Further Review |

All severity ratings are preliminary and require
additional verification.

## 9. General Security Recommendations

1. Disable unnecessary network services.
2. Replace insecure remote access protocols.
3. Upgrade outdated software.
4. Restrict database access.
5. Review SMB and NFS permissions.
6. Apply firewall restrictions.
7. Monitor system logs.
8. Maintain regular security updates.
9. Perform periodic security assessments.

## 10. Assessment Limitations

- The initial scan covered the top 1,000 TCP ports.
- Version detection covered selected ports only.
- Service banners do not independently prove vulnerabilities.
- Configuration-level weaknesses were not fully verified.
- No successful exploitation is claimed.
- Some services require further identification.

## 11. Conclusion

The assessment identified multiple exposed network
services and several outdated software versions
within the Metasploitable 2 laboratory environment.

The findings highlight the importance of secure
remote access, software maintenance, network
segmentation and access control.

Further configuration review would be necessary
to establish the actual security impact of each finding.

---

Report Status: Assessment Documentation Consolidated
Environment: Authorized Metasploitable 2 Lab
