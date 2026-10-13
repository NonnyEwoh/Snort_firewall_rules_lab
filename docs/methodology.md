# Methodology

## Source and scope

This workflow is based on the supplied **Lab - Snort and Firewall Rules** handout. Follow the official lab instructions for full topology details and any environment-specific adjustments. This file is a documentation guide, not a replacement for the handout.

## Part 1 — Prepare the virtual environment

1. Open the CyberOps Workstation VM in VirtualBox.
2. Check the network adapter configuration as directed by the handout.
3. Configure the VM network using the supplied DHCP script.
4. Verify that the VM has an IP address and test connectivity as instructed.
5. Record the network configuration and outcome in `docs/lab-report.md`.
6. Save a screenshot in `screenshots/01-environment/`.

## Part 2 — Firewall and IDS logs

### Step 1: Real-time IDS monitoring

1. Start the Mininet topology using the supplied lab script.
2. Open R1, H5, and H10 terminals from the Mininet prompt.
3. Start Snort on R1.
4. Start the handout's simulated server on H10 and verify the listening service.
5. Open another R1 terminal and monitor the Snort alert file.
6. From H5, perform the test HTTP request described in the handout.
7. Record the actual request result and any alert details.
8. Capture the traffic with `tcpdump`, stop the capture cleanly, and verify that the output file exists and is non-empty.
9. Record metadata and findings; do not automatically publish the raw PCAP.

### Step 2: Tune firewall rules based on IDS alerts

1. Open a separate R1 terminal and list current `iptables` rules.
2. Identify the chain that handles transit traffic.
3. Add the lab handout's TCP destination block rule to the appropriate chain in the lab environment.
4. Verify the rule and its counters.
5. Repeat the test request from H5 and record the actual outcome.
6. Capture screenshots of the rule and the test result.

## Part 3 — Terminate and clear Mininet

1. Enter `quit` at the main Mininet prompt.
2. Run the cleanup command as instructed by the handout.
3. Record the cleanup result and save a screenshot in `screenshots/06-cleanup/`.

## Evidence quality

- Show the command and relevant output in screenshots.
- Keep terminal text readable.
- Use numbered filenames and short captions.
- Record your own timestamps and outputs; do not claim example output as your own.
- Redact secrets and unrelated personal information.
