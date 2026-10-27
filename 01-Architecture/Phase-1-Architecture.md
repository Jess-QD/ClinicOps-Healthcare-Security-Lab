# Phase 1 — ClinicOps Lab Architecture

## Overview

This diagram documents the original ClinicOps lab environment. A Windows Server 2025 virtual machine was created on a Hyper-V host and configured as a domain controller for the isolated `clinicops.test` Active Directory domain.

## Architecture Diagram
![ClinicOps Phase 1 Architecture](ClinicOps%20Phase%201%20Architecture%20Diagram.png)


## What This Lab Demonstrates

- Creating and configuring a Windows Server virtual machine with Hyper-V.
- Configuring an isolated virtual network and static IP settings.
- Installing Active Directory Domain Services and promoting a server to a domain controller.
- Organizing fictional user accounts and security groups in an organizational unit.


## Environment Notes

The `ClinicOps-Private` switch was configured as a private virtual switch. The lab used a static IP address and did not have a configured default gateway.

This diagram represents the completed Phase 1 lab. Subsequent exercises will use a separate configuration within the existing `adatum.com` training domain and will be documented independently.
