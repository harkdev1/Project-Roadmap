# Networking & Infrastructure Engineering

## Showcase

<!-- autodoc:project-showcase:start -->
**Status:** In progress
**Source repository:** [https://github.com/harkdev1/networking-infrastructure-engineering](https://github.com/harkdev1/networking-infrastructure-engineering)

## What I built
Installed OPNsense 26.7 on a 20 GB virtual disk, configured the VM with 4 GB RAM and 2 CPU cores, established WAN/LAN interface assignments (em1 WAN and em0 LAN), created an isolated VMware Host-only network on VMnet2 using 192.168.20.0/24, configured the OPNsense LAN gateway as 192.168.20.1/24, enabled LAN DHCP with a pool of 192.168.20.100–192.168.20.199, verified VMnet8 NAT configuration using subnet 192.168.148.0/24 and gateway 192.168.148.2, inspected the VMware DHCP pool 192.168.148.128–192.168.148.254, confirmed the VMware DHCP service was running, inspected interface status and routing tables, captured WAN DHCP traffic using tcpdump, observed repeated IPv4 DHCP Discover requests without a visible DHCP Offer, documented the unresolved WAN addressing issue.

Summary:
Installed and configured OPNsense 26.7 as the foundation for an isolated enterprise-style virtual network, established the LAN gateway at 192.168.20.1/24 and configured the DHCP pool for future lab clients, assigned WAN and LAN interfaces and verified VMware NAT addressing, investigated missing WAN IPv4 connectivity through interface inspection, routing-table analysis, DHCP lease inspection, and packet capture, identified repeated DHCP Discover requests without a visible DHCP Offer, documented the unresolved WAN DHCP issue and established a targeted troubleshooting plan for the next session.

Tasks Completed:
Installed OPNsense 26.7 on a dedicated virtual machine, configured WAN and LAN interface assignments, created the isolated VMnet2 network using 192.168.20.0/24, assigned the LAN gateway 192.168.20.1/24, configured the LAN DHCP pool from 192.168.20.100 to 192.168.20.199, verified VMware VMnet8 NAT subnet and gateway settings, inspected VMware DHCP pool configuration and service status, inspected OPNsense interface status and routing tables, examined DHCP lease state, captured WAN IPv4 DHCP traffic with tcpdump, identified repeated DHCP Discover requests without a visible DHCP Offer, documented the unresolved WAN connectivity issue and next troubleshooting steps.

Issues Encountered:
WAN failed to obtain an IPv4 address through DHCP despite the virtual interface reporting an active link, repeated DHCP Discover requests were captured without a visible DHCP Offer, the WAN DHCP lease file was empty, the default IPv4 route was absent, the LAN virtual adapter was initially attached to VMnet0 instead of the intended VMnet2 and required correction, initial troubleshooting was slowed by incomplete inventory of the existing virtual network configuration, DHCPv6 log messages initially complicated interpretation of the IPv4 DHCP issue, Gemini AI generation encountered a temporary 503 service availability error and required manual documentation.

Next Steps:
Inventory and validate the existing VMware virtual network configuration before making further changes, investigate why OPNsense WAN (`em1`) sends IPv4 DHCP Discover requests without receiving a visible DHCP Offer, verify VMware NAT and DHCP service behavior, obtain a valid WAN IPv4 lease and confirm the default route, test upstream connectivity, verify OPNsense LAN gateway and DHCP functionality on VMnet2, connect a test client to the isolated lab subnet, validate permitted and blocked traffic through the firewall, capture screenshots and packet evidence at key milestones, document troubleshooting findings and configuration decisions, finalize the network topology diagram and session documentation.

Notes:
OPNsense installation and LAN configuration are complete, WAN is assigned to em1 and connected to VMware NAT, LAN is assigned to em0 on VMnet2, WAN currently has no IPv4 address, the DHCP lease file is empty, IPv4 DHCP Discover requests were captured on em1 without a visible Offer, the cause remains unresolved, do not mark WAN routing or firewall functionality as validated.

## Evidence gallery
### OPNsense Live Boot
![OPNsense Live Boot](screenshots/2026-10-11_131714_opnsense-live-boot.png)
Evidence copied from [logs/2026-10-11.md](https://github.com/harkdev1/networking-infrastructure-engineering/blob/main/logs/2026-10-11.md) and verified against the source image.

## Session highlights

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
