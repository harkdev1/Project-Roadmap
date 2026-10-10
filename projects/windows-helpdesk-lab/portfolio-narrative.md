# Portfolio Narrative

## Windows Helpdesk Lab

The Windows Helpdesk Lab is a small-business-style Northstar domain built to practice the work behind dependable IT support: understand the environment, gather the right evidence, test assumptions, make a scoped change, and verify its effect. The project has established a Windows Server domain-controller foundation with Active Directory and DNS, organized Northstar users and groups, and added a reusable PowerShell report for system, network, and recent Windows System-event context.

The lab has also moved from setup into administration validation. Recorded checks show DNS diagnostics passing on NS-DC01, core directory/network services running, and helpdesk/admin group memberships reviewed. The Northstar Workstation Policy is configured and linked to the Northstar Computers OU. Its guest-account rename setting is visible in Group Policy Management, but policy application on a domain-joined workstation remains unverified.

The project owner has confirmed the v1.0 lab complete. The GPO application gap remains an honest limitation, not a claimed success. Optional portfolio extensions are to verify the policy on a domain-joined workstation and build three controlled practice tickets: account access, DNS/connectivity, and Group Policy behavior. These are proposed exercises, not completed user incidents. Each should document a realistic symptom, evidence, diagnostic reasoning, a scoped change, and a repeatable outcome check.
