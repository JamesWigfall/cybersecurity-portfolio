# AWS Cloud Strategy and Architecture

**Prepared by:** James Wigfall  

---

## Executive Summary

This cloud computing strategy outlines the organization’s transition to Amazon Web Services (AWS) to modernize infrastructure, reduce operational overhead, and improve scalability and security.

The proposed architecture leverages multiple AWS service models:
- **EC2 (IaaS)** for compute
- **S3 (IaaS)** for storage
- **RDS (PaaS)** for database management
- **IAM (SaaS-like)** for identity and access control  

The design follows AWS best practices, including the **Shared Responsibility Model**, **Well-Architected Framework**, and **FedRAMP Low baseline controls**.

Projected cost:
- **Monthly:** $260.97  
- **Annual:** $3,131.64  

---

## Cloud Overview

Cloud computing provides scalable, on-demand infrastructure without requiring physical hardware management.

### Service Models

- **IaaS:** Infrastructure control (EC2, S3)  
- **PaaS:** Managed platforms (RDS)  
- **SaaS:** Managed applications/services (IAM-like functionality)  

AWS handles infrastructure security, while the organization is responsible for securing:
- Data  
- Applications  
- Configurations  

---

## Business Justification

The transition to AWS provides:

- Increased scalability and flexibility  
- Reduced hardware and maintenance costs  
- Faster deployment cycles  
- Built-in redundancy and availability  

### Key Goals

- Improve system performance  
- Centralize secure data storage  
- Simplify application deployment  
- Enable future scalability  

---

## Security and Technical Requirements

### Network Security

- Use Security Groups and Network ACLs  
- Enforce encryption in transit  

---

### Application Security

- Encrypt data at rest (S3, RDS)  
- Enforce least-privilege IAM policies  
- Require multi-factor authentication (MFA)  

---

### Host Security

- Regular patching of EC2 instances  
- Host-based firewalls  
- Automated vulnerability scanning (Amazon Inspector)  

---

### Monitoring and Logging

- AWS Systems Manager for configuration  
- CloudWatch for monitoring  
- CloudTrail for auditing  
- VPC Flow Logs for network visibility  

---

### Compliance

- Align with **FedRAMP Low Baseline controls**  
- Protect sensitive data using:
  - Encryption  
  - IAM restrictions  
  - Private subnet isolation  

---

## Cloud Services Architecture

### Core Services

- **EC2** – Web application hosting  
- **S3** – Object storage for logs and backups  
- **RDS (MySQL)** – Managed relational database  
- **IAM** – Identity and access management  

---

### Shared Responsibility Model

| Service | AWS Responsibility | Customer Responsibility |
|--------|------------------|------------------------|
| EC2 | Infrastructure, hardware | OS, patching, security groups |
| S3 | Storage infrastructure | Permissions, encryption |
| RDS | Database engine, backups | Database access, schema security |
| IAM | Service availability | User roles, MFA, policies |

---

## Network Architecture

The architecture uses a **Virtual Private Cloud (VPC)** with layered security.

### Key Components

- **Public Subnet** – Hosts EC2 web server  
- **Private Subnet** – Hosts RDS database  
- **Internet Gateway** – Enables public access  
- **NAT Gateway** – Allows outbound updates securely  
- **Security Groups** – Control traffic access  
- **CloudWatch & CloudTrail** – Monitoring and logging  

---

## Cost Analysis

### Monthly Cost Breakdown

| Service | Monthly Cost | Description |
|--------|-------------|------------|
| EC2 (t2.micro) | $6.63 | Web server |
| S3 (100 GB) | $2.30 | Storage |
| RDS MySQL | $252.04 | Database + backups |
| **Total** | **$260.97** | Estimated monthly cost |

---

### Annual Cost

- **$3,131.64 per year**

---

### Cost Insights

- RDS is the highest cost due to managed services  
- EC2 and S3 provide cost-efficient scalability  
- Pay-as-you-go pricing ensures flexibility  

---

## VPN and Network Security Considerations

### Remote Access Security

- Require encrypted VPN connections  
- Enforce authentication and access control policies  
- Limit remote access based on role  

---

### Modern Security Approaches

- Transition toward **Zero Trust Architecture**  
- Continuously verify users and devices  
- Monitor access behavior in real time  

---

## Key Takeaways

- Cloud adoption improves scalability and efficiency  
- Security must follow a shared responsibility model  
- Identity and access control are critical  
- Monitoring and logging are essential for visibility  
- Cost management should align with workload growth  

---

## Conclusion

This AWS cloud strategy provides a secure, scalable, and cost-effective solution for modern application deployment. By implementing strong access controls, encryption, monitoring, and compliance standards, the organization can reduce risk while supporting long-term growth and operational resilience.
