
# FINAL SECURITY ASSESSMENT REPORT

## 1. Project Information

- Project: Ethical Hacking Security Assessment
- Target: 192.168.56.102
- Operating System: Metasploitable 2
- Testing Machine: Kali Linux
- Assessment Type: Authorized Lab Assessment
- Date: 23 November 2026

## 2. Executive Summary

A security assessment was performed against the
Metasploitable 2 laboratory environment.

The assessment identified several legacy network
services that could introduce security risks.

The primary concern is the availability of outdated
remote access services and traditional FTP.

## 3. Scope and Authorization

Target IP: 192.168.56.102

Testing was limited to the authorized Metasploitable 2
virtual machine in a controlled laboratory environment.

## 4. Network Connectivity

Target connectivity was successfully verified.

- Target IP: 192.168.56.102
- Ping Status: Successful
- Packet Loss: 0%

## 5. Confirmed Service Findings

### Finding 1: Legacy FTP Service

- Port: 21/tcp
- Service: vsftpd
- Version: 2.3.4
- Risk: Medium

Observation:
An outdated FTP service was identified.

Recommendation:
Replace traditional FTP with SFTP or another
encrypted file transfer solution.

Note:
No exploitation was confirmed.

### Finding 2: Telnet Service

- Port: 23/tcp
- Service: Linux telnetd
- Risk: High

Observation:
An unencrypted remote administration service
was identified.

Recommendation:
Disable Telnet and use SSH for secure administration.

### Finding 3: Legacy Remote Execution Services

- Port: 512/tcp — rexecd
- Port: 513/tcp — rlogind
- Port: 514/tcp — rshd
- Risk: High

Observation:
Legacy remote access and execution services
were identified.

Recommendation:
Disable unnecessary legacy services and use
secure alternatives.

## 6. Additional Security Review

The following areas require further verification:

- Apache web server configuration
- MySQL and PostgreSQL access controls
- Authentication policies
- Firewall configuration
- System patch management
- User permissions

These are review recommendations, not confirmed
configuration vulnerabilities.

## 7. Risk Summary

| Finding | Risk |
|---|---|
| FTP service | Medium |
| Telnet service | High |
| Legacy remote access | High |

## 8. General Security Recommendations

1. Disable unnecessary network services.
2. Replace insecure remote access protocols.
3. Apply security patches.
4. Restrict database access.
5. Configure firewall rules.
6. Monitor system logs.
7. Perform regular security assessments.

## 9. Assessment Limitations

This assessment documents observed network services.

Not every service configuration was independently
verified.

No successful exploitation is claimed in this report.

## 10. Conclusion

The assessment identified several legacy services
that should be reviewed and secured.

Disabling unnecessary services, replacing insecure
protocols, and applying security updates would
improve the security posture of the environment.

---

Report Status: Initial Assessment Completed
Environment: Authorized Metasploitable 2 Lab

### Finding 4: Legacy Web Server

- Port: 80/tcp
- Software: Apache httpd 2.2.8 (Ubuntu)
- Risk: Medium (provisional)

Observation:
An outdated Apache version was identified.

Recommendation:
Upgrade to a supported release and review
the server configuration.

### Finding 5: Database Network Exposure

- Port: 3306/tcp — MySQL 5.0.51a
- Port: 5432/tcp — PostgreSQL 8.3.0 - 8.3.7
- Risk: Medium (provisional)

Observation:
Both database services are accessible
through the network.

Recommendation:
Restrict database access to authorized hosts.
Review authentication and permissions.

Note:
Unauthorized database access was not verified.
