# SYN Flood Incident Report

## Overview
This report investigates a website outage caused by a suspected Denial of Service (DoS) attack, identified through TCP/HTTP traffic analysis.

## Summary of findings
- An automated alert flagged a problem with the web server, and visitors began seeing connection timeout errors.
- Traffic logs showed a surge of TCP SYN requests coming from a single unfamiliar IP address.
- This pattern is consistent with a SYN flood attack, which abuses the TCP three-way handshake (SYN → SYN-ACK → ACK) by sending large volumes of connection requests that are never completed, exhausting the server's available ports.

## Impact
The server became overwhelmed responding to half-open connections, causing a slowdown and eventual operational failure — resulting in lost revenue, damaged customer trust, and risk to server infrastructure.

## Recommended mitigations
- Deploy a Next Generation Firewall (NGFW) for traffic monitoring.
- Use VPNs and encryption to help shield the web server's IP address.
- Segment the network into subnets to contain outages.

## File
- SYN_Flood_Incident_Report.pdf — full incident report

## Tools used
- Wireshark (TCP/HTTP log review)
