# Screenshot Evidence Guide

Save screenshots you capture yourself into the relevant subfolder. Empty directories are retained in Git using `.gitkeep` files.

## Suggested evidence plan

| Folder | Suggested screenshot filename | Evidence |
|---|---|---|
| `01-environment/` | `01-vm-network-configuration.png` | VM network mode and connectivity check |
| `02-mininet-topology/` | `02-mininet-topology-running.png` | Mininet prompt and topology startup |
| `03-snort-alerts/` | `03-snort-running-on-r1.png` | Snort startup |
| `03-snort-alerts/` | `04-snort-alert-log.png` | Actual Snort alert |
| `04-packet-capture/` | `05-tcpdump-capture.png` | Capture started/stopped and file verified |
| `05-firewall-rules/` | `06-iptables-forward-drop-rule.png` | Rule shown in the FORWARD chain |
| `05-firewall-rules/` | `07-blocked-request-result.png` | Actual request result after rule |
| `06-cleanup/` | `08-mininet-cleanup.png` | Cleanup output |

## Screenshot quality

- Keep command and relevant output visible.
- Ensure terminal text is readable.
- Use consistent numbered filenames.
- Add a short caption in your report.
- Redact credentials, tokens, and unrelated personal information.
- Do not use screenshots from another person's run as if they were yours.
