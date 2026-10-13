# Snort and Firewall Rules — Lab Documentation

A GitHub-ready repository template for documenting the Cisco CyberOps **Lab – Snort and Firewall Rules** activity, based on the supplied lab handout.

> **Documentation status:** Template only. Replace `TODO` fields with your own observations and add your own screenshots. Example values from the handout are not represented as results from your run.

## Lab goals

- Prepare the CyberOps Workstation virtual machine and verify network connectivity.
- Start the Mininet topology and monitor Snort IDS alerts.
- Observe the lab's simulated HTTP server and test traffic.
- Capture traffic with `tcpdump`.
- Inspect `iptables` rules, add a `DROP` rule to the `FORWARD` chain, and verify the effect.
- Terminate Mininet and clean up the environment.

## Repository map

```text
snort-firewall-rules-lab/
├── README.md
├── .gitignore
├── LICENSE
├── docs/
│   ├── lab-report.md
│   ├── lab-questions.md
│   ├── methodology.md
│   └── findings-template.md
├── commands/
│   ├── lab-commands.md
│   └── gitbash-publish.md
├── screenshots/
│   ├── README.md
│   ├── 01-environment/
│   ├── 02-mininet-topology/
│   ├── 03-snort-alerts/
│   ├── 04-packet-capture/
│   ├── 05-firewall-rules/
│   └── 06-cleanup/
└── evidence/
    ├── README.md
    ├── logs/
    ├── pcap/
    └── notes/
```

## Start here

1. Read [`docs/methodology.md`](docs/methodology.md).
2. Use [`commands/lab-commands.md`](commands/lab-commands.md) as a command reference while following the lab handout.
3. Record observations in [`docs/lab-report.md`](docs/lab-report.md) and answers in [`docs/lab-questions.md`](docs/lab-questions.md).
4. Save screenshots in the matching `screenshots/` subfolder.
5. Record evidence metadata in `evidence/`; review files for sensitive data before sharing.
6. Follow [`commands/gitbash-publish.md`](commands/gitbash-publish.md) to publish this repository.

## Environment record

| Field | Your details |
|---|---|
| Lab date | TODO: YYYY-MM-DD |
| Author / GitHub handle | TODO |
| Host operating system | TODO |
| VirtualBox version | TODO |
| CyberOps Workstation version | TODO |
| Lab status | Not started / In progress / Completed |

## Main concepts

- **IDS (Snort):** Inspects traffic and emits alerts when traffic matches configured signatures.
- **Firewall (`iptables`):** Filters packets using chains and rules.
- **`FORWARD` chain:** Handles traffic routed through the firewall rather than traffic addressed to the firewall itself.
- **Packet capture (`tcpdump`):** Records traffic for later investigation.

## Safety and evidence handling

- Perform the commands only in the intended, isolated CyberOps/Mininet lab environment.
- The handout uses a malware-named sample file to demonstrate detection. Do not execute it or move it outside the lab VM.
- Do not commit executable malware samples, credentials, tokens, private keys, or unreviewed packet captures.
- PCAPs may contain addresses and packet payloads. The `.gitignore` excludes common PCAP and executable extensions by default.
- Review `git status` before every commit.

## Results summary

Complete after running the lab:

- Snort alert observed: TODO
- Source and destination IP/port: TODO
- PCAP created and verified: TODO
- Firewall rule verified: TODO
- Request result after applying the rule: TODO
- Key lesson: TODO

## License

The repository template is provided under the included MIT license. The original lab handout remains the property of its respective publisher; this repository does not redistribute the handout.
