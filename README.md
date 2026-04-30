# Web Application Security Assessment

## Overview
This project demonstrates a security assessment of a Python-based web application using industry-standard tools. The goal was to identify vulnerabilities, analyze risk, and provide remediation strategies.

## Tools Used
- OWASP ZAP (DAST)
- Bandit (SAST)
- OWASP Dependency-Check (SCA)

## Methodology
- Performed static code analysis using Bandit
- Conducted dependency scanning for vulnerable libraries
- Executed dynamic application testing using OWASP ZAP
- Reviewed findings and categorized by severity

## Key Findings
- Cross Site Scripting (Reflected) – High
- Missing Security Headers – Medium
- Insecure Dependencies (Log4j) – Critical
- Weak Cryptographic Usage – Medium

## Remediation
- Implement input validation and output encoding
- Apply Content Security Policy (CSP) headers
- Update vulnerable dependencies
- Enforce secure cookie configurations

## Screenshots
See `/assets/` for tool output and scan results.

## Skills Demonstrated
- Vulnerability Assessment
- Application Security (AppSec)
- Security Tool Usage (SAST, DAST, SCA)
- Risk Analysis and Mitigation
