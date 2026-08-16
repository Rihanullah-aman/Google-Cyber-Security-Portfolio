# Security Incident Report — yummyrecipesforme.com

## Overview
This report investigates a fake browser-update malware campaign and a suspected brute force attack against the admin account of yummyrecipesforme.com, identified through DNS and HTTP traffic analysis.

## Summary of findings
- Users visiting yummyrecipesforme.com were prompted to download a file disguised as a browser update; after running it, their machines began running sluggishly.
- The website owner discovered they were locked out of their own admin account.
- Traffic captured with tcpdump in a sandboxed environment showed the browser initially connecting normally to yummyrecipesforme.com over HTTP, then — immediately after the malicious file was downloaded and run — issuing a new DNS lookup and redirecting all traffic to a lookalike site, greatrecipesforme.com, which offered the original site's paid content for free.
- Source code review confirmed the original site had been modified to serve the fake update prompt, and the admin lockout suggests the attacker used a brute force attack to change the admin password.

## Recommended remediations
- Two-factor authentication (2FA) on the admin account
- Login attempt limits / temporary lockout after repeated failures
- CAPTCHA on login forms sitewide

## File
- Security_Incident_Report_yummyrecipesforme.pdf — full incident report

## Tools used
- tcpdump (DNS/HTTP packet capture, sandboxed analysis)
