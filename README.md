# Roadmap

A standalone, Git-backed home for portfolio planning and the evidence-based history of projects. Roadmap is independent of AutoDoc and does not replace, reorganize, or combine source project repositories.

## Project index

| Project | Status | Roadmap | Major accomplishments | Next milestone |
|---|---|---|---|---|
| Windows Helpdesk Lab | Complete (v1.0; owner-confirmed) | [Roadmap](projects/windows-helpdesk-lab/roadmap.md) | Northstar domain foundation, Active Directory structure, DNS and service checks, reusable PowerShell diagnostics, configured and linked GPO | Optional post-v1: verify GPO application on a domain-joined workstation |

This initial Roadmap repository documents only Windows-Helpdesk-Lab. Other project workstreams are intentionally not indexed in this initial version.

## How to use this repository

- Use [PROJECT_ROADMAP_PROMPT.md](PROJECT_ROADMAP_PROMPT.md) with GitHub Copilot when reviewing a project or completing a meaningful milestone.
- Start a new workstream from [the project documentation template](templates/PROJECT_DOCUMENTATION_TEMPLATE.md).
- Keep implementation and original evidence in each source repository. Roadmap stores concise project history, plans, and links rather than source copies or bulky artifacts.
- Update the relevant project folder and this index after each review or meaningful milestone. Keep proposed work clearly labeled as proposed until evidence confirms completion.

## Source links and privacy

Windows-Helpdesk-Lab evidence links are relative to the sibling checkout at `../Windows-Helpdesk-Lab`. They resolve in the local `D:\Projects` workspace and point to the original files; no source files or screenshot binaries are copied into this repository. Links that point outside this repository may not render on a hosted Git service. Replace them with verified source-repository links only after confirming the exact remote revision contains the target file and that the evidence is safe to publish.

Do not add credentials, API keys, environment files, AutoDoc local state, personal host diagnostics, or unreviewed screenshots. The Helpdesk evidence index marks material that needs redaction or a privacy review.
