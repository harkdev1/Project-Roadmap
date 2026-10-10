# Windows Helpdesk Lab

> **Status:** In progress
> **Last reviewed:** 2026-10-10
> **Source checkout:** `../Windows-Helpdesk-Lab` from the Roadmap repository root
> **Next milestone:** Verify the Northstar Workstation Policy on a domain-joined workstation and capture sanitized result evidence.

## Overview

A hands-on small-business Windows domain lab using the Northstar Solutions identity and host naming. Its portfolio goal is to demonstrate a disciplined helpdesk workflow: establish the environment, reproduce a user-facing problem, gather evidence, diagnose the cause, apply a scoped fix, and verify the result.

The infrastructure foundation is established. The project has not yet completed the three proposed end-to-end support-ticket scenarios as a set. Those scenarios remain proposed work, not completed incidents.

## Current status

**Completed foundation:** Windows Server domain-controller environment, Active Directory structure and test groups, DNS configuration and health checks, reusable system-information diagnostics, and creation/linking of the Northstar Workstation Policy.

**Open verification:** The Northstar Workstation Policy is linked to the Northstar Computers OU and contains the configured guest-account rename setting, but its application on a domain-joined workstation has not been verified.

## Portfolio narrative

See [the professional narrative](portfolio-narrative.md), [technical summary](technical-summary.md), and [evidence index](evidence-index.md).

## Planning and history

- [Phase-based roadmap](roadmap.md)
- [Accomplishments and milestone history](milestones.md)
- [Limitations and prioritized next steps](limitations-and-next-steps.md)

## Source and privacy

This folder contains planning and history, not a second copy of the Helpdesk implementation. Links resolve locally when `roadmap` and `Windows-Helpdesk-Lab` are sibling folders under `D:\Projects`. Several source screenshots expose internal network details or test-user names; the evidence index marks those for redaction or local-only review. No AutoDoc state, credentials, virtual environments, or source screenshot binaries are included here.
