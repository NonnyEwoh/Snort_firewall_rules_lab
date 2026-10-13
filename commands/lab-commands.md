# Lab Command Reference

These commands are drawn from the supplied lab handout. Execute them only inside the intended CyberOps/Mininet training environment. Check the handout for exact prompts, paths, privileges, and ordering.

## Part 1 — Network setup

```bash
sudo ./lab.support.files/scripts/configure_as_dhcp.sh
```

Verify the assigned address using the tools available in the VM, then test connectivity as the handout instructs.

## Part 2 — Start topology and terminals

```bash
sudo ./lab.support.files/scripts/cyberops_extended_topo_no_fw.py
```

At the `mininet>` prompt:

```text
xterm R1
xterm H5
xterm H10
```

## Start Snort on R1

```bash
./lab.support.files/scripts/start_snort.sh
```

In a separate R1 terminal, monitor alerts:

```bash
tail -f /var/log/snort/alert
```

## Start and verify the lab server on H10

```bash
./lab.support.files/scripts/mal_server_start.sh
netstat -tunpa
```

## Capture the lab traffic on H5

```bash
tcpdump -i H5-eth0 -w nimda.download.pcap &
```

After the test request, stop the background capture by bringing it to the foreground and pressing Ctrl+C:

```bash
fg
ls -l nimda.download.pcap
```

## Inspect and tune the firewall on R1

List rules:

```bash
sudo iptables -L -v
```

The lab handout's example rule:

```bash
sudo iptables -I FORWARD -p tcp -d 209.165.202.133 --dport 6666 -j DROP
```

List rules again and repeat the lab's test request to verify the observed effect.

## Cleanup

At the main Mininet prompt:

```text
quit
```

Then in the CyberOps VM terminal, run the cleanup command as directed by the handout:

```bash
sudo mn -c
```

## Caution

The handout uses a malware-named test artifact. Do not execute the sample or move it outside the isolated lab. This command reference does not include the executable. Avoid publishing raw PCAPs without reviewing them for sensitive data.
