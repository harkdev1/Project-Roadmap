# Windows Helpdesk Lab Evidence Index

All links point to the original sibling `Windows-Helpdesk-Lab` checkout; assets are not copied into Roadmap. Screenshot contents were reviewed where noted. Relative links work in the local `D:\Projects` layout. They may not resolve in a hosted Roadmap rendering because they point outside this Git repository.

## Session logs and implementation

| Source | What it supports | Notes |
|---|---|---|
| [2026-09-23 session log](../../../Windows-Helpdesk-Lab/logs/2026-09-23.md) | Virtual lab preparation and Windows Server installation. | PC-spec image is intentionally omitted; the log says its real specs were redacted. Passive activity-capture images are not portfolio evidence. |
| [2026-09-28 session log](../../../Windows-Helpdesk-Lab/logs/2026-09-28.md) | NS-DC01 setup, AD DS/DNS foundation, and early server validation. | Internal IP/static network details are not reproduced. The log body says Server 2022 while its title/screenshots say Server 2025. |
| [2026-10-05 session log](../../../Windows-Helpdesk-Lab/logs/2026-10-05.md) | Initial OUs, test users/groups, and membership work. | A successful session record; it does not establish an end-to-end account-access ticket. |
| [2026-10-10 session log](../../../Windows-Helpdesk-Lab/logs/2026-10-10.md) | GPO configuration/link, script work, DNS/AD checks, friction, reviewer caveats, and deferred client verification. | Two sessions are present; the later review explicitly keeps workstation GPO application open. |
| [Diagnostic script](../../../Windows-Helpdesk-Lab/scripts/Get-HelpdeskSystemInfo.ps1) | Actual implementation of computer, network, and recent System-event reporting. | Link to source code instead of redistributing a screenshot containing VM network details. |

## Screenshots reviewed

| Source image | Observed evidence | Publication/privacy status |
|---|---|---|
| [Northstar Workstation Policy configured](../../../Windows-Helpdesk-Lab/screenshots/2026-10-10_094549_northstar-workstation-policy-configured.png) | Group Policy Management shows the Northstar Workstation Policy linked under Northstar Computers and the configured Accounts guest-name setting `DisabledGuest`. | Suitable as configuration evidence with the important caveat that client application is unverified. Review the visible domain label before public release. |
| [Final DNS health check](../../../Windows-Helpdesk-Lab/screenshots/2026-10-10_131812_final-dns-health-check.png) | `dcdiag /test:DNS` output shows the displayed connectivity and DNS tests passing for NS-DC01 / `northstar.local`. | Useful evidence; point-in-time result only. Check for internal identifiers before public release. |
| [AD structure, users, and groups](../../../Windows-Helpdesk-Lab/screenshots/2026-10-05_052230_ad-structure-users-and-groups.png) | Active Directory Users and Computers shows Northstar OUs, `Employees`, `Helpdesk`, and `IT-Admins` groups, and selected membership. | Local-review only until visible test-user names are redacted or confirmed as safe synthetic identities. |
| [Helpdesk system info script execution](../../../Windows-Helpdesk-Lab/screenshots/2026-10-10_095506_powershell-helpdesk-system-info-script-execution.png) | Shows the script source in an editor and successful formatted output in PowerShell, including network addresses and recent events. | **Do not publish unredacted:** contains VM IP/gateway and machine-specific diagnostic details. Source script and log are safer references. |
| [NS-DC01 PowerShell troubleshooting](../../../Windows-Helpdesk-Lab/screenshots/2026-10-10_095004_ns-dc01-powershell-system-troubleshooting.png) | Shows PowerShell diagnostics in the Windows Server VM. | **Hold back pending privacy review:** may expose internal network and host details. |
| [DNS forward lookup zone](../../../Windows-Helpdesk-Lab/screenshots/2026-09-28_164319_northstar-solutions-dns-forward-lookup-zone.png) | Screenshot caption and session log identify the Northstar DNS forward lookup zone. | Review records and IP addresses before any public use. |
| [AD domain controller verification](../../../Windows-Helpdesk-Lab/screenshots/2026-09-28_164213_northstar-solutions-active-directory-domain-cont.png) | Session evidence for the AD domain-controller setup/verification milestone. | Review visible host/domain details before public use. |
| [Northstar Group Policy environment](../../../Windows-Helpdesk-Lab/screenshots/2026-09-28_164430_northstar-solutions-group-policy-environment.png) | Session evidence for the initial Group Policy environment. | Configuration context only; not proof of workstation policy application. Review before public use. |

## Deliberately excluded from the portfolio package

- `2026-09-23_003451_pc-specs.png`: host specifications are personal machine diagnostics; source log says real specs were redacted.
- `activity_*.jpg`: passive activity captures are unrelated to technical proof and may expose personal activity.
- `2026-10-10_131044.png`: screenshot contains system/network diagnostic context; inspect and redact before any public link.
- Static-IP and broad desktop screenshots are not needed to support the current narrative and should be scrubbed for internal addresses and machine details before publication.
