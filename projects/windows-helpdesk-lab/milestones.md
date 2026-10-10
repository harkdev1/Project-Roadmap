# Windows Helpdesk Lab Milestones

Dates and outcomes below are drawn from the source project's logs, screenshots, and local Git history. Proposed ticket scenarios are intentionally not listed as completed milestones.

| Date | Status | Accomplishment | Evidence / caveat |
|---|---|---|---|
| 2026-09-23 | Completed | Prepared the virtualized lab and recorded Windows Server installation. | [Session log](../../../Windows-Helpdesk-Lab/logs/2026-09-23.md). The log says hardware details were redacted; no host specifications or activity-capture assets are reproduced. |
| 2026-09-28 | Completed | Established NS-DC01, static networking, AD DS, DNS, and the Northstar domain foundation. | [Session log](../../../Windows-Helpdesk-Lab/logs/2026-09-28.md). The session goal text says Server 2022 while the screenshot captions and current session evidence say Server 2025; confirm the historical version rather than silently reconciling the conflict. |
| 2026-10-05 | Completed | Created the initial AD organizational structure, test users, security groups, and group memberships. | [Session log](../../../Windows-Helpdesk-Lab/logs/2026-10-05.md) and [AD structure screenshot](../../../Windows-Helpdesk-Lab/screenshots/2026-10-05_052230_ad-structure-users-and-groups.png). The screenshot shows test-user names; redact before public release. |
| 2026-10-10, 09:17–10:02 | Completed | Created and linked the Northstar Workstation Policy, configured the guest-account rename setting, ran diagnostics, and created/executed `Get-HelpdeskSystemInfo.ps1`. | [Session log](../../../Windows-Helpdesk-Lab/logs/2026-10-10.md). Human review explicitly says client-side policy application is not verified. |
| 2026-10-10, 12:27–13:18 | Completed checks; GPO validation deferred | Checked AD/DNS health, NTDS/DNS/Netlogon service state, group membership, script execution, and final DNS diagnostics; deferred workstation-level GPO validation. | [Session log](../../../Windows-Helpdesk-Lab/logs/2026-10-10.md) and [final DNS check screenshot](../../../Windows-Helpdesk-Lab/screenshots/2026-10-10_131812_final-dns-health-check.png). Local source history records commits `89d8393` and `ff11187` ahead of its remote at review time; this Roadmap does not change or publish that source repository. |

## Status interpretation

- **Completed** means the source log or artifact records the work, and is not a claim of production readiness.
- **Deferred** means a recorded scope choice or open follow-up; it is not complete.
- **Proposed** means a future exercise with no existing completed-ticket evidence.
