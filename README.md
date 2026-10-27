# ClinicOps: Healthcare Identity Security and Incident Investigation

## Project Overview

ClinicOps is a hands-on lab project focused on systems administration, identity and access management, PowerShell automation, and security monitoring in a fictional healthcare environment.

The project explores how user accounts, security groups, access permissions, and audit data can support secure and organized IT operations. It also documents the configuration decisions, verification steps, and security observations made throughout the lab.

This is a learning project. It does not use real patient information or claim to establish HIPAA compliance.

## Project Objectives

- Configure and administer Windows Server and Active Directory.
- Organize user accounts and security groups to support role-based access.
- Use PowerShell to query, manage, and report on directory objects.
- Apply least-privilege principles and verify group membership changes.
- Explore Windows security auditing and incident investigation.
- Document technical findings and security considerations clearly.

## Lab Phases

### Phase 1 — Hyper-V and Active Directory Setup

The initial lab used Hyper-V to create a Windows Server 2025 virtual machine and establish a dedicated `clinicops.test` Active Directory domain.

Completed work includes:

- Creating and configuring a Generation 2 virtual machine.
- Installing Windows Server 2025 Standard Evaluation with Desktop Experience.
- Configuring static network settings for the isolated lab.
- Installing Active Directory Domain Services and promoting the server to a domain controller.
- Creating a `ClinicOps` organizational unit, security groups, and fictional user accounts.
- Using PowerShell to inspect directory information and export user, group, and group membership reports.
- Testing a group membership change, verifying the result, and restoring the original membership.
- Inspecting the domain's default password policy.

The first 10 screenshots document the original lab setup and its verification evidence.

### Phase 2 — Identity Administration and Security Controls

The next phase uses a dedicated `ClinicOps` organizational unit within the existing `adatum.com` training domain on `LON-SVR1`.

This approach allows the project to continue without creating another virtual machine in an environment that does not support the required nested virtualization capabilities.

Planned exercises include:

- Creating and managing project-specific directory objects within the dedicated OU.
- Automating identity administration tasks with PowerShell.
- Reviewing group membership and access-control decisions.
- Configuring and testing file-share and NTFS permissions.
- Exploring Windows security logs and investigating selected account or access events.

This phase uses an organizational unit within `adatum.com`, not a separate ClinicOps domain. The environment and results will be documented accordingly.

### Phase 3 — Security Monitoring and Investigation

The planned investigation phase will focus on collecting and interpreting relevant Windows security events, filtering results with PowerShell, and documenting findings.

Potential exercises include failed logon analysis, review of account activity, and investigation of unexpected access attempts where the lab environment supports them.

## Security Observation

During Phase 1, the default domain password policy reported a lockout threshold of `0`. In Active Directory, this means the configured domain policy does not lock accounts after a specified number of failed logon attempts.

This finding was documented as a security consideration for further analysis. It is a lab observation, not a claim that a production healthcare environment was assessed.

## Tools and Technologies

- Windows Server 2025
- Windows Server 2019 
- Hyper-V and virtual machine configuration
- Active Directory Domain Services (AD DS)
- PowerShell
- Active Directory users, groups, and organizational units
- Windows security auditing and event logs (planned)
- File-share and NTFS permissions (planned)

## Repository Contents

- `01-Architecture/` — architecture notes and environment documentation
- `02-PowerShell-Scripts/` — PowerShell commands and scripts
- `03-Test-Results/` — verification results and selected reports
- `04-Security-Investigations/` — investigation notes and findings
- `05-Azure/` — cloud lab documentation, if completed
- `06-Screenshots/` — selected screenshots showing configuration and verification

## Scope and Limitations

This project uses fictional accounts and training environments. The original `clinicops.test` lab and the subsequent `adatum.com` exercises are separate configurations and will be documented as such.

The project demonstrates selected technical skills and security concepts. It is not a production deployment, formal security assessment, or HIPAA compliance certification.

## Project Status

**Phase 1:** Completed
**Phase 2:** In progress
**Phase 3:** Planned

This README will be updated as additional exercises, scripts, verification evidence, and investigation reports are completed.
