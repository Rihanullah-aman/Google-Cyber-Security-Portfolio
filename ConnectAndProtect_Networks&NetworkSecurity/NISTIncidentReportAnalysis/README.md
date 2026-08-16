# Incident Report Analysis — NIST CSF (ICMP Flood / DoS Attack)

## Overview
Applies the NIST Cybersecurity Framework (CSF) — Identify, Protect, Detect, Respond, Recover — to a scenario where a company experienced a Denial of Service (DoS) attack caused by an ICMP flood through an unconfigured firewall.

## Summary
An unconfigured firewall allowed a flood of ICMP pings to overwhelm the network, disrupting business operations. The report walks through how each phase of the NIST CSF applies to identifying the affected assets, protecting the network going forward, detecting similar attacks earlier, responding effectively, and recovering services.

## NIST CSF breakdown

- **Identify** — Firewall, routers, servers, and network services were affected; business processes like web design, marketing, and internal communications were interrupted; network admins, cybersecurity staff, and IT staff needed access to respond.
- **Protect** — Restrict traffic to trusted sources, block unnecessary ICMP and spoofed IPs, train staff on DoS attacks and firewall security, secure data with access controls/encryption/backups, review firewall rules regularly, and keep systems patched.
- **Detect** — Use a SIEM and IDS/IPS to spot unusual traffic and suspicious ICMP activity, with continuous monitoring of traffic, bandwidth, and firewall logs.
- **Respond** — Maintain a DoS response plan, notify IT/management/affected employees quickly, analyze logs to find the attack source, block malicious traffic and isolate affected systems, then review and improve the response afterward.
- **Recover** — Restore critical services first, rely on backups and redundant systems (tested regularly), and keep employees and management informed as normal operations resume.

## Takeaway
Proper firewall configuration, continuous network monitoring, and a clear incident response plan are key to preventing and limiting the impact of future DoS/ICMP flood attacks.

## File
- `NIST_Incident_Report_Analysis.pdf` — full filled-in NIST CSF template
