# Limitations and Prioritized Next Steps

## Current limitations and open questions

- **GPO effect is unverified:** The Northstar Workstation Policy is configured and linked to Northstar Computers, but no domain-joined workstation result is recorded.
- **No end-to-end ticket set yet:** The account-access, DNS/connectivity, and GPO-behavior tickets are proposed future exercises, not completed incidents.
- **Historical OS version conflict:** The September 28 log body references Windows Server 2022; that log's title and screenshots, plus October 10 screenshots, identify Windows Server 2025. Confirm the historical installation/version record.
- **Host/guest script parity:** The October 10 notes describe confusion between host and guest script copies. Verify the exact script path/hash used in the guest when the workflow is repeated.
- **Privacy before portfolio publication:** Some source screenshots expose VM addresses, diagnostic output, or test-user display names. Do not publish them unredacted.
- **Diagnostic scope:** `Get-HelpdeskSystemInfo.ps1` collects basic state and recent System events; it does not establish root cause or perform remediation.

## Prioritized next steps

1. **Verify GPO application on a domain-joined workstation.** Confirm domain join and OU placement, run `gpresult` or Resultant Set of Policy, verify the expected setting, and capture sanitized evidence. If it fails, record the actual cause; do not mark the policy applied based only on its GPMC link.
2. **Complete one controlled account-access ticket.** Use a test account and a defined resource. Record symptom, safe checks, group/account state, authorized change, and successful access verification. Never store passwords.
3. **Complete one controlled DNS/connectivity ticket.** Reproduce a bounded failure, inspect client configuration and DNS resolution, run server-side checks, isolate the cause, and verify recovery.
4. **Complete one controlled Group Policy ticket.** Use the verified workstation, investigate a reproducible policy symptom, inspect scope/filtering and resultant policy, apply a scoped fix if needed, and verify the user-visible effect.
5. **Curate portfolio evidence.** Redact internal addresses and names, remove passive activity captures, keep the original evidence in the source repo, and update this evidence index with only reviewed material.
6. **Resolve documentation discrepancies.** Confirm the Server 2022/2025 historical note and ensure the script copy used in NS-DC01 matches the source version.
