# CyberOps Sandbox

**Main Homelab · In progress** · [Source repository](https://github.com/harkdev1/CyberOps-Sandbox)

A hands-on Windows security homelab built through controlled experiments. The current work studies what Windows Security telemetry actually records, using PowerShell and event logs to validate evidence rather than assume a detection succeeded.

The latest recorded test found that the configured Security log did not reliably expose the process/file activity under investigation. That visibility gap is a finding, not a completed detection capability. The next step is to review audit policy configuration and repeat the controlled tests.

## Showcase


<!-- autodoc:project-showcase:start -->
**Main Homelab · Status:** In progress
**Source repository:** [https://github.com/harkdev1/CyberOps-Sandbox](https://github.com/harkdev1/CyberOps-Sandbox)

## What I built
Reviewed the existing OPNsense WAN, LAN, and SERVERS network baseline, verified WIN11-CLIENT01 network identity and connectivity configuration, confirmed endpoint IPv4 address 192.168.20.165 with gateway 192.168.20.1, checked for Wazuh and Sysmon services with neither returned by the initial checks, verified Windows Security logging is enabled with 29,072 records, verified System logging is enabled with 1,792 records, verified PowerShell Operational logging is enabled with 483 records, established that elevated PowerShell is required to inspect the Security log, made no system or network configuration changes.

Summary:
Initial validation of the existing lab infrastructure was performed to establish an evidence-based starting point for the November CyberOps SIEM and detection engineering work. This involved reviewing network baselines, verifying endpoint network identity and connectivity, and confirming the status of core Windows event logging sources on a target workstation. A key finding was the absence of dedicated endpoint telemetry agents, identifying telemetry collection as the next critical technical milestone. No system or network configuration changes were made, preserving the existing infrastructure.

Tasks Completed:
*   Reviewed the existing OPNsense WAN, LAN, and SERVERS network baseline.
*   Verified WIN11-CLIENT01 network identity and connectivity configuration.
*   Confirmed WIN11-CLIENT01 endpoint IPv4 address (192.168.20.165) with gateway (192.168.20.1).
*   Checked for existing Wazuh and Sysmon service installations on the endpoint; neither were found.
*   Verified Windows Security logging is enabled (29,072 records observed).
*   Verified Windows System logging is enabled (1,792 records observed).
*   Verified Windows PowerShell Operational logging is enabled (483 records observed).
*   Established that elevated PowerShell privileges are required for inspecting the Security log.
*   Made no system or network configuration changes to the existing environment.

Issues Encountered:
*   Initial attempts to inspect the Windows Security log via PowerShell failed due to insufficient privileges, necessitating elevation.
*   The endpoint's operating system identification differed from the expected Windows 11 designation.
*   Available host memory is constrained while the existing virtual machines are running, potentially impacting future resource allocation for SIEM components.

Next Steps:
*   Deploy and configure endpoint telemetry agents (e.g., Wazuh, Sysmon) on WIN11-CLIENT01.
*   Further investigate the discrepancy in the endpoint's reported operating system identification.
*   Address host memory constraints to ensure adequate resources for upcoming SIEM and detection engineering tools.

Notes:
This initial validation effort successfully confirmed the foundational status of the lab environment prior to new deployments. The existing infrastructure, including network configuration, was preserved without modification. Confirmation of active Windows event sources provides a baseline for initial detection capabilities, pending the deployment of advanced telemetry agents.

## Evidence gallery
### Telemetry Visibility Gap
![Telemetry Visibility Gap](screenshots/2026-10-08_053048_telemetry-visibility-gap.png)
Evidence copied from [logs/2026-10-08.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-08.md) and verified against the source image.

### Process Creation Telemetry
![Process Creation Telemetry](screenshots/2026-10-07_052909_process-creation-telemetry.png)
Evidence copied from [logs/2026-10-07.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-07.md) and verified against the source image.

### Security Event Distribution
![Security Event Distribution](screenshots/2026-10-07_053206_security-event-distribution.png)
Evidence copied from [logs/2026-10-07.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-07.md) and verified against the source image.

### CyberOps Baseline v0.1
![CyberOps Baseline v0.1](screenshots/2026-09-30_065419_cyberops-baseline-v0-1.png)
Evidence copied from [logs/2026-09-30.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-09-30.md) and verified against the source image.

### Endpoint Baseline Initial Audit
![Endpoint Baseline Initial Audit](screenshots/2026-10-25_184357_endpoint-baseline-initial-audit.png)
Evidence copied from [logs/2026-10-25.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-25.md) and verified against the source image.

### Security Log Baseline
![Security Log Baseline](screenshots/2026-10-25_184616_security-log-baseline.png)
Evidence copied from [logs/2026-10-25.md](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-25.md) and verified against the source image.

## Session highlights

### 2026-10-25 · 18:32 to 18:48
Recorded outcome: ✅ Yes. Initial validation of the existing lab infrastructure was performed to establish an evidence-based starting point for the November CyberOps SIEM and detection engineering work. This involved reviewing network baselines, verifying endpoint network identity and connectivity, and confirming the status of core Windows event logging sources on a target workstation. A key finding was the absence of dedicated endpoint telemetry agents, identifying telemetry collection as the next critical technical milestone. No system or network configuration changes were made, preserving the existing infrastructure.
[Open the original AutoDoc log](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-25.md)

### 2026-10-11 · 10:55 to 11:07
Recorded outcome: ✅ Yes. Current efforts focused on establishing a verified baseline configuration for NS-DC01, documenting its existing state, and identifying reusable administrative assets from Project 1. This foundational work is crucial for preparing the environment for Project 2, with a strong emphasis on preserving current capabilities and avoiding premature changes.
[Open the original AutoDoc log](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-11.md)

### 2026-10-08 · 05:19 to 05:30
Recorded outcome: ✅ Yes. An initial experimental session was conducted within the CyberOps Sandbox on NS-DC01 to evaluate the reliability of existing Windows Security telemetry in observing intentional, simple process and file activities. The session established that the current Security log configuration does not reliably expose the tested activities, identifying significant visibility gaps. This work underscores a hands-on, experimental methodology focused on understanding and improving telemetry from the ground up, treating failures to observe expected activity as critical engineering findings.
[Open the original AutoDoc log](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-08.md)

### 2026-10-07 · 05:12 to 05:17
Recorded outcome: ❌ No. The previous work session has been deemed unsatisfactory and requires a complete re-execution. No tasks from this session can be considered successfully completed at this time.
[Open the original AutoDoc log](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-07.md)

### 2026-09-30 · 06:46 to 06:55
Recorded outcome: ✅ Yes. Initial project baselining activities have been completed, with key specifications documented.
[Open the original AutoDoc log](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-09-30.md)

## Current limitations and next steps
- Continue from the handoff notes and current project status.
- Capture final cleanup or deployment follow-up items as they are completed.

## Project files
- [Current project status](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/project-status.md)
- [Short project summary](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/docs/project-complete-short.md)
- [Full project history](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/docs/project-complete-long.md)
- [Evidence index](evidence-index.md)

---
Screenshots are copied only from image references present in AutoDoc logs. Review each image for private details before publishing.
Gallery folder: `projects/cyberops-sandbox/screenshots/`.
<!-- autodoc:project-showcase:end -->

AutoDoc adds images referenced by the project's logs and session highlights here after a successful `autodoc finish` or `autodoc project complete` sync.
