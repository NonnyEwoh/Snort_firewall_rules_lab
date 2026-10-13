# Lab Report — Snort and Firewall Rules

## 1. Lab metadata

- **Date performed:** TODO
- **Author:** TODO
- **Host OS:** TODO
- **VirtualBox version:** TODO
- **CyberOps Workstation version:** TODO
- **Status:** TODO

## 2. Objective

Document how Snort IDS alerts can inform firewall rule tuning, how a packet capture preserves traffic for investigation, and how an `iptables` rule affects a test connection in the supplied Mininet topology.

## 3. Environment and connectivity

- VM network mode used: TODO
- IP address assigned to the VM: TODO
- Connectivity test and result: TODO
- Screenshot: `../screenshots/01-environment/`

## 4. Snort and simulated server

- Mininet topology started successfully: TODO
- R1 shell identity / prompt indicator: TODO
- Snort started successfully: TODO
- Simulated server listening state and port: TODO
- Test request outcome before firewall change: TODO
- Snort alert generated: TODO
- Alert timestamp: TODO
- Alert signature/message: TODO
- Source IPv4 and port: TODO
- Destination IPv4 and port: TODO

Evidence:
- `../screenshots/02-mininet-topology/`
- `../screenshots/03-snort-alerts/`

## 5. Packet capture

- Capture interface: TODO
- Capture filename: TODO
- Capture size (metadata only): TODO
- Capture stopped cleanly: TODO
- Why the capture may help an analyst: TODO

Evidence: `../screenshots/04-packet-capture/`

Do not commit the raw PCAP unless you have authorization and have reviewed it for sensitive content.

## 6. Firewall rule verification

- Initial chains and policies: TODO
- Rule inserted into chain: TODO
- Rule visible after insertion: TODO
- Packet/byte counters before test: TODO
- Packet/byte counters after test: TODO
- Test request outcome after rule: TODO
- Explanation of observed result: TODO

Evidence: `../screenshots/05-firewall-rules/`

## 7. Cleanup

- Mininet exited: TODO
- Cleanup command result: TODO
- Errors or issues: TODO

Evidence: `../screenshots/06-cleanup/`

## 8. Conclusion

Summarize how IDS alerts, packet captures, and firewall rules worked together in this lab. Use only results you observed.

**Conclusion:** TODO

## 9. Lessons learned / troubleshooting

- Issue encountered: TODO
- Diagnostic steps: TODO
- Resolution: TODO
- What I would improve next time: TODO
