# Networking & Infrastructure Engineering

## Showcase

<!-- autodoc:project-showcase:start -->
**Status:** In progress
**Source repository:** [https://github.com/harkdev1/networking-infrastructure-engineering](https://github.com/harkdev1/networking-infrastructure-engineering)

## What I built
Audited VMware virtual network adapter assignments, identified the incorrect OPNsense WAN/LAN interface mapping, reassigned WAN to em0 on VMnet8 and LAN to em1 on VMnet2, obtained WAN DHCP lease 192.168.148.129/24, verified default gateway 192.168.148.2, confirmed gateway reachability with 4/4 replies and 0% packet loss, confirmed external IP connectivity to 1.1.1.1 with 4/4 replies and 0% packet loss, validated DNS resolution for example.com through the local resolver, documented the current network topology and addressing plan.

Summary:
This session successfully addressed and resolved critical network connectivity issues for an OPNsense virtual appliance. The primary cause was identified as an incorrect mapping of VMware virtual network adapters to OPNsense WAN/LAN interfaces. After systematically correcting these assignments, full network functionality was restored. WAN DHCP was successfully obtained, routing verified, and external IP connectivity confirmed. DNS resolution was also validated. The session concluded with a documented network topology, establishing a stable and reproducible foundation for subsequent implementation phases.

Tasks Completed:
*   Audited VMware virtual network adapter assignments for the OPNsense VM.
*   Identified and corrected the incorrect OPNsense WAN/LAN interface mapping:
    *   Reassigned the WAN interface to `em0` on `VMnet8`.
    *   Reassigned the LAN interface to `em1` on `VMnet2`.
*   Successfully obtained a WAN DHCP lease: `192.168.148.129/24`.
*   Verified the default gateway: `192.168.148.2`.
*   Confirmed gateway reachability with 4/4 replies and 0% packet loss.
*   Confirmed external IP connectivity to `1.1.1.1` with 4/4 replies and 0% packet loss.
*   Validated DNS resolution for `example.com` through the local resolver.
*   Documented the current network topology and addressing plan.

Issues Encountered:
*   Initial troubleshooting efforts prematurely focused on DHCP behavior before a complete validation of the network topology, including correlating VMware adapter MAC addresses with OPNsense interface names.
*   Incorrect assumptions were made regarding VMware virtual network adapter ordering and the corresponding OPNsense `emX` interface names.
*   The troubleshooting session extended without predefined time boundaries or clear stopping criteria, leading to prolonged diagnostic attempts and increased fatigue.
*   The troubleshooting sequence was inefficient due to a failure to prioritize a systematic topology audit upfront.

Next Steps:
*   Proceed with the next phase of OPNsense configuration and network implementation, building upon the established and verified network foundation.
*   Implement stricter time boundaries and earlier stopping criteria for future troubleshooting sessions to improve efficiency.

Notes:
This session highlighted the critical importance of a systematic infrastructure troubleshooting methodology, particularly the absolute necessity of validating the complete network topology and interface mappings *before* diving into service-specific issues like DHCP. The key to resolution was identifying and correcting the virtual interface mapping error. Establishing a reproducible topology reference and meticulously documenting the current state are essential for future work and maintaining a stable environment. Lessons learned include prioritizing a comprehensive topology audit, correlating MAC addresses, and implementing better session management practices (e.g., time boxing, defined stopping points) to prevent extended, less effective diagnostic efforts.

## Evidence gallery
### VMware DHCP Investigation
![VMware DHCP Investigation](screenshots/2026-10-12_043617_vmware-dhcp-investigation.png)
Evidence copied from [logs/2026-10-12.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-12.md) and verified against the source image.

### OPNsense Live Boot
![OPNsense Live Boot](screenshots/2026-10-11_131714_opnsense-live-boot.png)
Evidence copied from [logs/2026-10-11.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-11.md) and verified against the source image.

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

## Session highlights

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
