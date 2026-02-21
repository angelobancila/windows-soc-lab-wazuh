# Windows SOC Monitoring & Incident Investigation Lab (Wazuh)

This repository documents a structured Security Operations Centre (SOC) simulation conducted within a virtualised lab environment using Wazuh SIEM and a monitored Windows endpoint.

The purpose of this lab was to simulate real-world Tier 1 SOC investigations, focusing on authentication analysis, process monitoring, privilege escalation detection, and incident classification.

---

## Lab Environment

- SIEM Platform: Wazuh 4.x
- Endpoint: Windows 10
- Host System: Windows 11
- Hypervisor: VMware Workstation
- Log Source: Windows Security Event Logs
- Network: Isolated private lab environment (RFC1918 – 192.168.x.x)

---

## Key Windows Event IDs Analysed

- 4624 – Successful Logon
- 4625 – Failed Logon
- 4740 – Account Lockout
- 4672 – Special Privileges Assigned
- 4688 – Process Creation
- 4720 – User Account Creation

---

## Investigation Areas Covered

- Log ingestion validation
- Authentication failure detection
- Brute force simulation and analysis
- Account lockout verification
- Logon and process correlation using Logon ID
- Suspicious command execution investigation
- Privilege escalation assessment
- Timeline reconstruction
- Impact assessment and severity classification

---

## Skills Demonstrated

- Windows Security Event Analysis
- SIEM Monitoring and Alert Triage
- Event Correlation
- Tier 1 SOC Investigation Workflow
- Incident Classification
- Authentication Attack Detection
  
## Project Structure

- 01 – Log Monitoring Deployment
- 02 – Authentication Attack Detection
- 03 – Logon & Process Correlation
- 04 – Privilege Escalation Investigation
- 05 – Brute Force Behaviour Analysis
