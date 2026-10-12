# Networking & Infrastructure Engineering

## Showcase

<!-- autodoc:project-showcase:start -->
**Status:** In progress
**Source repository:** [https://github.com/harkdev1/networking-infrastructure-engineering](https://github.com/harkdev1/networking-infrastructure-engineering)

## What I built
Investigated OPNsense WAN DHCP failure, verified WAN interface em1 and repeated DHCP Discover transmissions, confirmed VMware VMnet8 NAT and DHCP configuration, checked VMware DHCP and NAT service status, restarted VMware DHCP without restoring the lease, examined Windows DHCP event channels and VMware lease records, started a PCAP capture for future Wireshark analysis

Summary:
This documentation outlines the initial phase of troubleshooting a persistent WAN DHCP failure experienced by an OPNsense virtual machine within a VMware environment. Despite a systematic approach to verifying both the OPNsense client's behavior and the VMware virtual network configuration, the issue remains unresolved. Limited visibility into the DHCP negotiation process has hindered fault isolation. Recognizing diminishing returns from further configuration checks, the focus is now shifting to evidence-based, packet-level analysis to pinpoint the root cause.

Tasks Completed:
*   Investigated the OPNsense WAN DHCP failure.
*   Verified the OPNsense WAN interface (em1) configuration and confirmed repeated DHCP Discover transmissions.
*   Confirmed the VMware VMnet8 NAT and DHCP configuration.
*   Checked the operational status of the VMware DHCP and NAT services.
*   Restarted the VMware DHCP service without restoring existing leases.
*   Examined Windows DHCP event channels on the host.
*   Reviewed VMware DHCP lease records for any relevant entries.
*   Initiated a PCAP capture for subsequent Wireshark analysis.

Issues Encountered:
*   Repeated configuration checks did not succeed in isolating the fault.
*   Limited visibility into whether the VMware DHCP server was receiving OPNsense DHCP broadcast messages.
*   Initial host-side packet captures proved inconclusive in diagnosing the problem.
*   The WAN DHCP failure for OPNsense persists.
*   A tendency to repeat verification steps without establishing new observation points or distinguishing clearly between confirmed findings and assumptions.

Next Steps:
*   Perform a detailed Wireshark analysis of the captured PCAP file to thoroughly examine DHCP negotiation packets and identify communication breakdowns.
*   Establish a more granular and effective observation point, potentially capturing traffic directly on the VMnet8 interface within the host, or within the guest VM itself (if feasible), to ensure visibility of DHCP Discover requests reaching the VMware DHCP server and its subsequent responses.
*   Based on the packet-level analysis, systematically isolate the fault to either the OPNsense client, the VMware virtual network's routing/bridging, or the VMware DHCP service itself.

Notes:

## Evidence gallery
### OPNsense Live Boot
![OPNsense Live Boot](screenshots/2026-10-11_131714_opnsense-live-boot.png)
Evidence copied from [logs/2026-10-11.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-11.md) and verified against the source image.

### VMware DHCP Investigation
![VMware DHCP Investigation](screenshots/2026-10-12_043617_vmware-dhcp-investigation.png)
Evidence copied from [logs/2026-10-12.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-12.md) and verified against the source image.

## Session highlights

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
