# CyberOps Homelab Evidence

The screenshots displayed here are copied from image references in the original AutoDoc logs. Source code and full session history remain in the [CyberOps-Sandbox GitHub repository](https://github.com/harkdev1/CyberOps-Sandbox).

## What the evidence establishes

- **Baseline, 2026-09-30:** A screenshot shows PowerShell queries of Northstar DNS zones and enabled Windows event-log record counts. It records the starting operational context; it does not establish an alerting pipeline.
- **Process telemetry, 2026-10-07:** The source log records inspection of security events and process-creation telemetry. It is exploratory evidence, not proof that every test action was reliably attributed.
- **Event distribution, 2026-10-07:** The screenshot shows counts of Security event IDs in a bounded recent sample. Counts are context, not detections or attribution.
- **Visibility gap, 2026-10-08:** The screenshot and log document that the tested process/file activity was not reliably visible with the then-current audit configuration. This negative result is a finding; it is not a successful detection claim.

## Source logs

- [Initial environment baseline, 2026-09-30](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-09-30.md)
- [Security-event and process-telemetry investigation, 2026-10-07](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-07.md)
- [Telemetry visibility-gap investigation, 2026-10-08](https://github.com/harkdev1/CyberOps-Sandbox/blob/main/logs/2026-10-08.md)

## Transferred screenshots

AutoDoc refreshes this section from image links in the source logs. Each image is copied into this Roadmap folder and checked against the source bytes before it is committed.
