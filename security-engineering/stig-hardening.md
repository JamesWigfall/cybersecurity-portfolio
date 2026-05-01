# STIG Compliance Assessment and Risk Analysis (Ubuntu & MySQL)

**Prepared by:** James Wigfall  

---

## Overview

This project documents the results of a Security Technical Implementation Guide (STIG) assessment conducted on an Ubuntu 18.04 operating system and a MySQL 8.0 database.

The objective was to identify Category I (CAT I) vulnerabilities, apply remediation strategies, and evaluate associated risks through a Risk Assessment Report (RAR).

---

## Ubuntu 18.04 STIG Findings (CAT I)

The following high-priority findings were identified:

### Key Vulnerabilities

- **FIPS Mode Not Enabled (V-219151)**  
  System not using NIST FIPS-validated cryptography  

- **PKI Authentication Mapping Missing (V-219316)**  
  Certificates not mapped to user identities  

- **SSH Misconfiguration (V-219314, V-219308, V-219313)**  
  - Weak SSH settings  
  - SSHv1 potentially allowed  
  - Lack of enforced encryption  

- **System Reboot Vulnerability (V-219212, V-219211)**  
  Ctrl-Alt-Delete enabled, allowing potential denial-of-service  

- **Boot Security Weakness (V-219148)**  
  No authentication required for single-user mode  

---

### Remediation Actions

- Enable FIPS mode (`fips=1`)  
- Configure SSH securely (disable weak settings, enforce SSHv2)  
- Disable Ctrl-Alt-Delete reboot functionality  
- Implement GRUB password protection  
- Configure PKI authentication mapping  

---

## MySQL 8.0 STIG Findings (CAT I)

### Key Vulnerabilities

- **FIPS Mode Disabled (V-235148, V-235189)**  
- **Weak Access Controls (V-235141)**  
- **Lack of External Authentication Integration (V-235095)**  
- **Unencrypted Data at Rest (V-235155)**  
- **Unencrypted Password Transmission (V-235139)**  
- **Weak Private Key Protection (V-235135)**  
- **Insufficient Password Policies (V-235137)**  

---

### Remediation Actions

- Enable FIPS mode (`ssl_fips_mode=ON`)  
- Enforce role-based access control (RBAC)  
- Integrate with LDAP / Active Directory  
- Enable encryption for:
  - Data at rest  
  - Logs  
  - Tablespaces  
- Require secure transport (SSL/TLS)  
- Restrict private key access (600 permissions)  
- Enforce strong password policies  

---

## Risk Assessment (RAR)

:contentReference[oaicite:0]{index=0}

---

### High-Risk Areas Identified

#### Cryptographic Weaknesses
- Use of non-FIPS validated algorithms  
- Risk of compromised confidentiality and integrity  

---

#### Authentication and Access Control
- Weak role enforcement  
- Lack of centralized authentication  
- Potential insider threats  

---

#### Data Protection Risks
- Unencrypted data at rest  
- Plaintext password transmission  

---

#### System Configuration Risks
- Misconfigured SSH  
- Unprotected boot processes  
- Improper key handling  

---

## Risk Summary

| Category | Risk Level | Description |
|--------|-----------|------------|
| Cryptography | Moderate | Weak or unvalidated encryption |
| Access Control | High | Unauthorized access risk |
| Data Protection | High | Exposure of sensitive data |
| System Security | Moderate | Misconfigurations and weak controls |

---

## Key Takeaways

- FIPS compliance is critical for federal-grade security  
- Strong access control and authentication are essential  
- Encryption must be enforced both at rest and in transit  
- System hardening reduces attack surface significantly  
- Continuous monitoring and auditing are necessary  

---

## Conclusion

This STIG assessment highlights critical vulnerabilities across both the operating system and database layers. By implementing the recommended remediation strategies, the system can significantly improve its security posture, reduce risk exposure, and align with federal security standards.

A layered security approach combining encryption, access control, system hardening, and continuous monitoring is essential for maintaining a secure environment.
