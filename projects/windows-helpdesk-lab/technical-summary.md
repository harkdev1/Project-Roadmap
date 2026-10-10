# Windows Helpdesk Lab Technical Summary

## Verified lab context

- **Lab identity:** Northstar Solutions; domain `northstar.local`.
- **Domain controller:** `NS-DC01`.
- **Server version:** Current session screenshots show Windows Server 2025. The September 28 session body refers to Windows Server 2022, while its heading/captions refer to Windows Server 2025; the historical version discrepancy remains to be confirmed.
- **Virtualization:** VMware Workstation is named in the October 10 session notes.
- **Directory:** The logs record Northstar OUs, test users, `Employees Helpdesk` and `IT-Admins` groups, and membership validation. The ADUC screenshot visibly shows the OU tree and group membership; names are omitted here.

## Implemented components and observed behavior

### Active Directory and Group Policy

The project logs record AD DS promotion and directory setup. The Northstar Workstation Policy is configured with an account setting to rename the local guest account to `DisabledGuest`; Group Policy Management evidence shows the GPO linked and enabled under Northstar Computers. The October 10 reviewer explicitly states that application on a domain-joined workstation has not been verified. Therefore, the evidence supports **GPO configured and linked**, not **GPO effective on a workstation**.

### DNS and server health

The October 10 log records that `dcdiag /test:DNS` passed its checks and that NTDS, DNS, and Netlogon were running. The final DNS screenshot visibly shows successful connectivity and DNS tests for NS-DC01 / `northstar.local`. These are point-in-time lab checks, not a claim of continuous monitoring or production resilience.

### PowerShell diagnostic script

Source: [Get-HelpdeskSystemInfo.ps1](../../../Windows-Helpdesk-Lab/scripts/Get-HelpdeskSystemInfo.ps1).

The script collects selected computer/OS information, network configuration, and up to five recent System event records, then formats them for an operator. It is read-only reporting with permissive error continuation; it does not remediate issues, validate a user incident, test resource authorization, or prove that an event was caused by a particular action.

## Verification boundaries

- Server/AD/DNS foundation and administrative checks are recorded as completed in the source logs.
- The GPO link and configured setting are evidenced; client-side application is not.
- No account-access, DNS/connectivity, or GPO support-ticket scenario has been evidenced end to end as a completed incident.
- Screenshots show point-in-time state; they do not replace repeatable commands, client-side verification, or a reproducible ticket record.
