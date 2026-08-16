# DNS / ICMP Incident Report — Network Traffic Analysis

## Overview
This report investigates why a website (yummyrecipesforme.com) was failing to load for users. Network traffic was captured with tcpdump to identify the root cause.

## Summary of findings
- The client sent repeated DNS queries (A record lookups) to the DNS server for yummyrecipesforme.com.
- Every query was met with an ICMP error: "udp port 53 unreachable" instead of a normal DNS response.
- Port 53 is the standard port for DNS traffic, so this pointed to a DNS resolution failure rather than a problem with the web server itself.
- The failure repeated consistently across three separate attempts several minutes apart, indicating a persistent issue rather than a one-time glitch.

## Likely cause
The DNS server was down, misconfigured, or blocked by a firewall rule on UDP port 53 — preventing the browser from ever resolving the domain name to an IP address.

## File
- DNS_ICMP_Incident_Report.pdf — full incident report

## Tools used
- tcpdump (packet capture / log analysis)
