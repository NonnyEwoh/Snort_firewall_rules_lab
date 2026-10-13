# Evidence Handling

Use this folder to organize evidence metadata and carefully reviewed outputs.

- `logs/`: place only reviewed, sanitized logs you are authorized to share.
- `pcap/`: keep raw packet captures local by default; the root `.gitignore` excludes PCAP files.
- `notes/`: record evidence metadata, such as collection time, interface, filename, size, and analysis notes.

## Before sharing evidence

1. Check for credentials, tokens, personal data, internal IPs, hostnames, and packet payloads.
2. Confirm you have permission to publish the evidence.
3. Prefer summarized findings or screenshots over raw traffic when possible.
4. Do not add malware executables to this repository.
