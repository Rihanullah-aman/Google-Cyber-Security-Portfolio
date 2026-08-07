# Botium Toys — Controls and Compliance Audit

Project completed as part of the Google Cybersecurity Professional Certificate
(Play It Safe: Manage Security Risks) capstone activity.

## Executive Summary

Botium Toys' internal audit scored an overall risk of 8/10, driven almost entirely by gaps in
administrative controls (access management) and technical controls (data protection) — not physical
security, which was already strong. Of the 14 controls assessed, 9 were not yet in place, most
critically least privilege access, encryption of cardholder data, and a disaster recovery plan. My top
recommendation: prioritize least privilege, encryption, and MFA first, since these close the most direct
compliance gaps (PCI DSS, GDPR) at the lowest implementation cost.


<img width="1050" height="630" alt="photo_2026-08-07_22-08-08" src="https://github.com/user-attachments/assets/44b2b49c-8b34-4cfe-a941-d21ec71680b6" />


## Contents

| File | What it is |
|---|---|
| Botium_Toys_Case_Study_Background.pdf | Provided scenario material. The scope, goals, and risk assessment audit report supplied by the course as background reading. Included for context only — not original work. |
| Botium_Toys_Controls_Compliance_Checklist.pdf | My work. Completed controls assessment, compliance checklist (PCI DSS, GDPR, SOC), and my own recommendations, based on the scenario above. |
| Stakeholder_Memorandum.pdf | My work. A memo summarizing the audit findings and recommendations for the IT manager and stakeholders. |
| Controls_Assessment_Priority.pdf | My work. My prioritization (High/Medium) of the controls not yet in place, with reasoning tied to the risk assessment findings. |
| controls_coverage_chart.png | My work. A chart visualizing in-place vs. not-in-place controls by category. |
| walkthrough-post.md | My work. A short write-up on a reasoning mistake I caught and corrected while working through the compliance checklist. |

## What I did

Using the provided Botium Toys risk assessment as the source of truth, I:

- Assessed 14 security controls (administrative, technical, and physical) and determined which are currently in place
- Evaluated compliance posture against PCI DSS, GDPR, and SOC best practices
- Wrote recommendations prioritizing the highest-risk gaps (e.g., MFA, encryption, least privilege, disaster recovery)
- Drafted a stakeholder memo translating audit findings into a concise summary and action plan for leadership
- Prioritized outstanding controls (High/Medium) based on risk severity and control type

## Skills demonstrated

Risk assessment interpretation, security control evaluation, regulatory compliance analysis (PCI DSS / GDPR / SOC), audit reporting, and stakeholder communication.

## What I'd do differently

Looking back, I'd push to get the data classification piece done first — several other gaps (least
privilege, encryption scope, access policies) are hard to fully scope without first knowing what data
exists and how sensitive it is. I'd also tie each recommendation to a rough cost/effort estimate next
time, since that's usually the first question a real stakeholder would ask.
