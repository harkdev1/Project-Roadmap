# Roadmap

Starting from the fundamentals, building progressively, and following curiosity wherever it leads. A living record of projects, experiments, lessons learned, and the journey from beginner to builder.

## Gallery



<!-- autodoc:project:networking-infrastructure-engineering:start -->
### [Networking & Infrastructure Engineering](projects/networking-infrastructure-engineering/README.md)

**In progress** · [Source repository](https://github.com/harkdev1/networking-infrastructure-engineering)

Created WIN11-CLIENT01 in VMware Workstation, configured 4 GB RAM and 2 vCPUs, allocated a 64 GB virtual disk, connected the client to VMnet2 Host-only, installed Windows 11, assigned the hostname WIN11-CLIENT01, preserved the existing Windows Server domain controller and OPNsense network configuration. Summary: A new Windows 11 client endpoint, `WIN11-CLIENT01`, has been successfully deployed and configured...

[![OPNSense LAN DHCP Subnet](projects/networking-infrastructure-engineering/screenshots/2026-10-20_060316_opnsense-lan-dhcp-subnet.png)](projects/networking-infrastructure-engineering/README.md)
<!-- autodoc:project:networking-infrastructure-engineering:end -->

<!-- autodoc:project:project:start -->
### [Project](projects/project/README.md)

**In progress** · [Source repository](https://github.com/harkdev1/networking-infrastructure-engineering)

Created the Networking & Infrastructure Engineering project workspace, initialized AutoDoc, installed GitHub CLI and authenticated with GitHub, created the public networking-infrastructure-engineering repository, configured the origin remote and main branch, pushed the initial AutoDoc project structure, enabled automatic synchronization, generated the first engineering log and committed the initial documentation...
<!-- autodoc:project:project:end -->

<!-- autodoc:project:cyberops-sandbox:start -->
### [CyberOps Sandbox](projects/cyberops-sandbox/README.md)

**Main Homelab · In progress** · [Source repository](https://github.com/harkdev1/CyberOps-Sandbox)

Verified NS-DC01 configuration, confirmed Windows Server 2025 with AD DS and DNS, documented the northstar.local domain and network settings, confirmed VMware NAT mode, identified reusable Project 1 administration and PowerShell capabilities, reviewed Project 2 scope. Summary: Current efforts focused on establishing a verified baseline configuration for NS-DC01, documenting its existing state, and identifying...

[![Telemetry Visibility Gap](projects/cyberops-sandbox/screenshots/2026-10-08_053048_telemetry-visibility-gap.png)](projects/cyberops-sandbox/README.md)
<!-- autodoc:project:cyberops-sandbox:end -->

<!-- autodoc:project:windows-helpdesk-lab:start -->
### [Windows Helpdesk Lab](projects/windows-helpdesk-lab/README.md)

**Complete · v1.0** · [Source repository](https://github.com/harkdev1/Windows-Helpdesk-Lab)

The Northstar Windows domain lab documents its AD/DNS foundation, administration checks, reusable PowerShell diagnostics, and configured workstation policy. Client-side policy application remains unverified.

**[Open the Helpdesk gallery](projects/windows-helpdesk-lab/README.md)**. AutoDoc will add approved screenshots and session highlights after the next successful finish or project-completion sync.
<!-- autodoc:project:windows-helpdesk-lab:end -->

## How the gallery updates

`autodoc finish` refreshes the current project's showcase, and `autodoc project complete` updates it with the completed status. AutoDoc selects screenshots referenced in that project's logs, filters known private captures, asks once before publishing new images, verifies each copied image, and links it to its source GitHub log. Previously approved images are reverified and reused automatically. It pushes only the project's gallery folder and this index. Use `--skip-roadmap` to opt out or `--roadmap-dir` to select the gallery location.

Source code and full session logs stay in their project repositories. Roadmap is the visual showcase, not a second copy of project implementations.
