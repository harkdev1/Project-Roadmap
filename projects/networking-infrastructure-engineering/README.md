# Networking & Infrastructure Engineering

## Showcase

<!-- autodoc:project-showcase:start -->
**Status:** In progress
**Source repository:** [https://github.com/harkdev1/networking-infrastructure-engineering](https://github.com/harkdev1/networking-infrastructure-engineering)

## What I built
Verified OPNsense 26.7 interface assignments, confirmed WAN em0 at 192.168.148.129/24 and LAN em1 at 192.168.20.1/24, reviewed VMware VMnet2 host-only network configuration, identified and resolved an IP address conflict between the OPNsense LAN interface and the Windows host's VMnet2 adapter, changed the host adapter address from 192.168.20.1 to 192.168.20.2, verified OPNsense routing table and HTTPS listener, confirmed LAN interface status is active, successfully tested TCP connectivity from the physical Windows host to 192.168.20.1 on port 443.

Summary:
Systematic network troubleshooting was performed on a virtualized OPNsense 26.7 firewall environment to resolve critical management connectivity issues. The primary problem identified was an IP address conflict between the OPNsense LAN interface (192.168.20.1/24) and the VMware VMnet2 host-only adapter on the Windows host. This conflict was successfully resolved by reconfiguring the host's VMnet2 adapter to 192.168.20.2/24. Post-resolution, OPNsense interface assignments, routing, and HTTPS listener functionality were verified, and successful TCP connectivity to the firewall's web interface on port 443 was established from the physical Windows host. This work preserved the existing domain controller configuration and restored essential HTTPS reachability to the firewall.

Tasks Completed:
*   **OPNsense Interface Verification:** Confirmed OPNsense 26.7 interface assignments:
    *   WAN: `em0` at `192.168.148.129/24`
    *   LAN: `em1` at `192.168.20.1/24`
*   **VMware Network Configuration Review:** Reviewed the VMware `VMnet2` host-only network configuration on the Windows host.
*   **IP Address Conflict Resolution:**
    *   Identified an IP address conflict between the OPNsense LAN interface (`192.168.20.1`) and the Windows host's `VMnet2` adapter.
    *   Resolved the conflict by changing the Windows host's `VMnet2` adapter IP address from `192.168.20.1` to `192.168.20.2`.
*   **OPNsense System Verification:**
    *   Verified OPNsense routing table.
    *   Confirmed OPNsense HTTPS listener is active on the LAN interface.
    *   Confirmed LAN interface status is active.
*   **Connectivity Testing:** Successfully tested TCP connectivity from the physical Windows host to the OPNsense LAN interface (`192.168.20.1`) on port `443` (HTTPS).

Issues Encountered:
*   **IP Address Conflict:** A critical IP address conflict existed where the Windows host's `VMnet2` adapter shared the same IP address (`192.168.20.1`) as the OPNsense LAN interface, preventing proper network communication.
*   **HTTPS Access Timeouts:** Initial attempts to access the OPNsense web interface via HTTPS timed out directly as a symptom of the underlying IP address conflict.
*   **Troubleshooting Complexity:** Distinguishing between host network configuration issues and firewall configuration issues required focused troubleshooting efforts.

Next Steps:
*   Validate DHCP functionality on the OPNsense LAN interface.

Notes:
*   No AI-related errors or misses were identified during this process.
*   The troubleshooting process emphasized systematic verification of virtual network components and firewall configurations.
*   The environment involved OPNsense 26.7, a VMware virtual machine, and a physical Windows host.
*   Preservation of existing domain controller configuration was a key consideration; no changes to the DC were performed or required.

## Evidence gallery
### WAN DHCP Success
![WAN DHCP Success](screenshots/2026-10-13_142955_wan-dhcp-success.png)
Evidence copied from [logs/2026-10-13.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md) and verified against the source image.

### WAN Default Route Validated
![WAN Default Route Validated](screenshots/2026-10-13_143146_wan-default-route-validated.png)
Evidence copied from [logs/2026-10-13.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md) and verified against the source image.

### Network Topology Plan (Current)
![Network Topology Plan (Current)](screenshots/2026-10-13_143619_network-topology-plan-current.png)
Evidence copied from [logs/2026-10-13.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md) and verified against the source image.

### WAN External Connectivity
![WAN External Connectivity](screenshots/2026-10-13_143905_wan-external-connectivity.png)
Evidence copied from [logs/2026-10-13.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md) and verified against the source image.

### WAN DNS Resolution
![WAN DNS Resolution](screenshots/2026-10-13_144046_wan-dns-resolution.png)
Evidence copied from [logs/2026-10-13.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md) and verified against the source image.

### VMware DHCP Investigation
![VMware DHCP Investigation](screenshots/2026-10-12_043617_vmware-dhcp-investigation.png)
Evidence copied from [logs/2026-10-12.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-12.md) and verified against the source image.

### OPNsense Live Boot
![OPNsense Live Boot](screenshots/2026-10-11_131714_opnsense-live-boot.png)
Evidence copied from [logs/2026-10-11.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-11.md) and verified against the source image.

## Session highlights

### 2026-10-16 · 05:24 to 05:51
Recorded outcome: ❌ No. Systematic network troubleshooting was performed on a virtualized OPNsense 26.7 firewall environment to resolve critical management connectivity issues. The primary problem identified was an IP address conflict between the OPNsense LAN interface (192.168.20.1/24) and the VMware VMnet2 host-only adapter on the Windows host. This conflict was successfully resolved by reconfiguring the host's VMnet2 adapter to 192.168.20.2/24. Post-resolution, OPNsense interface assignments, routing, and HTTPS listener functionality were verified, and successful TCP connectivity to the firewall's web interface on port 443 was established from the physical Windows host. This work...
[Open the original AutoDoc log](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-16.md)

### 2026-10-13 · 14:00 to 14:42
Recorded outcome: ✅ Yes. This session successfully addressed and resolved critical network connectivity issues for an OPNsense virtual appliance. The primary cause was identified as an incorrect mapping of VMware virtual network adapters to OPNsense WAN/LAN interfaces. After systematically correcting these assignments, full network functionality was restored. WAN DHCP was successfully obtained, routing verified, and external IP connectivity confirmed. DNS resolution was also validated. The session concluded with a documented network topology, establishing a stable and reproducible foundation for subsequent implementation phases.
[Open the original AutoDoc log](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-13.md)

### 2026-10-12 · 04:27 to 05:39
Recorded outcome: ❌ No. This documentation outlines the initial phase of troubleshooting a persistent WAN DHCP failure experienced by an OPNsense virtual machine within a VMware environment. Despite a systematic approach to verifying both the OPNsense client's behavior and the VMware virtual network configuration, the issue remains unresolved. Limited visibility into the DHCP negotiation process has hindered fault isolation. Recognizing diminishing returns from further configuration checks, the focus is now shifting to evidence-based, packet-level analysis to pinpoint the root cause.
[Open the original AutoDoc log](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-12.md)

### 2026-10-11 · 11:44 to 15:04
Recorded outcome: ❌ No. Installed and configured OPNsense 26.7 as the foundation for an isolated enterprise-style virtual network, established the LAN gateway at 192.168.20.1/24 and configured the DHCP pool for future lab clients, assigned WAN and LAN interfaces and verified VMware NAT addressing, investigated missing WAN IPv4 connectivity through interface inspection, routing-table analysis, DHCP lease inspection, and packet capture, identified repeated DHCP Discover requests without a visible DHCP Offer, documented the unresolved WAN DHCP issue and established a targeted troubleshooting plan for the next session.
[Open the original AutoDoc log](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-11.md)

### 2026-10-10 · 15:59
Recorded outcome: ✅ Yes. Established Project 2 workspace at D:\Projects\Networking-Infrastructure-Engineering, initialized AutoDoc, installed GitHub CLI and authenticated with GitHub, created the public networking-infrastructure-engineering repository, configured the origin remote and main branch, pushed the initial AutoDoc project structure to GitHub, enabled AutoDoc automatic synchronization. Next: finalize README and CHANGELOG, set repository description, verify the initial commit and prepare for Project 2 Session 1. ### Tasks Completed established repo ### Notes --- ## Session – 15:58 to 16:00 ### Goal Establish the Project 2 GitHub repository, initialize AutoDoc, enable automatic...
[Open the original AutoDoc log](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-10.md)

## Current limitations and next steps
- Continue from the handoff notes and current project status.
- Capture final cleanup or deployment follow-up items as they are completed.

## Project files
- [Current project status](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/project-status.md)
- [Short project summary](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/docs/project-complete-short.md)
- [Full project history](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/docs/project-complete-long.md)
- [Evidence index](evidence-index.md)

---
Screenshots are copied only from image references present in AutoDoc logs. Review each image for private details before publishing.
Gallery folder: `projects/networking-infrastructure-engineering/screenshots/`.
<!-- autodoc:project-showcase:end -->
