# Reusable Copilot Project Roadmap Prompt

Use this prompt from the Roadmap repository when reviewing one selected project. Replace the bracketed paths and name before starting.

```text
You are updating one project workstream in the standalone Roadmap repository.

Roadmap repository: [ABSOLUTE PATH TO ROADMAP CHECKOUT]
Selected source project: [ABSOLUTE PATH TO SOURCE PROJECT]
Project name: [PROJECT NAME]
Roadmap project folder: [PATH UNDER ROADMAP/projects/]

Work within the Roadmap repository only. Treat the selected source project as read-only unless I explicitly authorize source changes. Never combine Git repositories, move source files, or copy whole source trees into Roadmap. Do not inspect or modify other projects unless I explicitly request it.

Before drafting, inspect the selected project's actual README, source files, configuration, documentation, changelog, AutoDoc logs and status files, Git history and current status, scripts, tests, and available screenshots or other evidence. Review the contents of relevant screenshots rather than inferring their meaning from filenames. Do not open secret stores, credentials, API keys, .env files, virtual environments, AutoDoc private session state, personal host diagnostics, or unrelated private data. If a source file may contain sensitive data, inspect only what is needed and do not reproduce the sensitive values.

Use the inspected material as the source of truth. Distinguish clearly among:
- Completed: directly supported by implementation, successful verification, logs, or evidence.
- In progress: started but not yet accepted or fully verified.
- Deferred: deliberately postponed or blocked, including the reason when documented.
- Proposed: future work that has not happened; never describe it as a completed incident, feature, or result.

Preserve established project names, architecture, decisions, constraints, and terminology. Identify contradictions in source records and preserve the uncertainty instead of silently resolving it. Identify dependencies, risks, limitations, and testable acceptance criteria. Do not invent outcomes, performance data, users, incidents, screenshots, or validation.

Update the corresponding project folder in the Roadmap repository whenever a project is reviewed or a meaningful milestone is completed. Keep the central Roadmap index in sync with the project's current status, major accomplishments, and highest-value next milestone. Use the established template and keep the documentation maintainable. Include a phase-based roadmap with statuses, dependencies, acceptance criteria, and a Mermaid diagram only when it improves understanding.

Document the project overview, actual technical implementation, milestone history, evidence inventory, professional narrative, limitations, deferred items, and prioritized next steps. Link evidence to its real source location using relative links when the local workspace layout permits. State when links depend on sibling checkouts or are not hostable within the Roadmap repository. Avoid unnecessary duplication and large binary artifacts; prefer links to source files and evidence. Do not publish screenshots with internal addresses, real or unverified personal names, credentials, or other private details. Mark evidence requiring redaction or review.

For the selected project, provide:
1. A short current status and project overview.
2. An evidence-backed milestone history with dates where known.
3. A technical implementation summary and what remains unverified.
4. A phase-based roadmap with dependencies and acceptance criteria.
5. An evidence index explaining what each inspected artifact demonstrates and its limitations.
6. A technically honest professional narrative tailored to the intended audience.
7. Current limitations, deferred work, and a ranked next-step list.
8. A clear recommendation for the single highest-value next milestone.

Before finishing, validate local Markdown links, review Mermaid syntax where present, check diffs and Git status, inspect staged files before any commit, and check for secrets or unrelated content. Do not commit or push unless explicitly requested. If asked to publish, verify the destination belongs to this Roadmap repository and that permissions are clear; never overwrite or push to another project's remote.
```
