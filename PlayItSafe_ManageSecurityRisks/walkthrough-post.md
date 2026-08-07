# What I Learned Auditing a Fictional Toy Company's Security Program

As part of the Google Cybersecurity Professional Certificate, I worked through a capstone case
study: Botium Toys, a small retailer with a security program that hadn't caught up to its growth.
The assignment sounds simple on paper — read a risk assessment, fill in a yes/no checklist. In
practice, the interesting part was the judgment calls buried inside "simple" questions.

Here's one I want to walk through, because it's a good example of how easy it is to get a checklist
item wrong even when you're reading carefully.

## The item that tripped me up

One line in the GDPR compliance checklist read:

> *"Enforce privacy policies, procedures, and processes to properly document and maintain data."*

My first instinct was No. Right above it, the checklist asks whether Botium Toys properly
classifies and inventories its data — and the answer to that is clearly no, since the risk
assessment says all employees have unrestricted access to sensitive data with no classification
system in place. It seemed logical: if a company hasn't even classified its data yet, how could it
have "enforced" privacy policies for handling that data?

That reasoning felt airtight. It was also wrong.

## Where the reasoning broke down

Data classification and privacy policy enforcement sound related, but they're actually two separate
controls that can exist independently of each other:

- Classification is about knowing *what* data you have and how sensitive it is.
- Policy enforcement is about *whether people follow the rules* for handling data, once those
  rules exist — regardless of how well-organized the underlying data inventory is.

A company can absolutely have the second without the first. Botium Toys' risk assessment report
said exactly that: privacy policies and procedures *have* been developed and *are* enforced among
staff — even though the company hasn't formally classified its data. It's not the tidiest state to
be in, but it's a real and common one: policy discipline moving faster than technical inventory work.

I'd built a plausible-sounding inference instead of just checking what the source document actually
said. The fix was simple — go back and read the sentence in the risk report directly rather than
reasoning by analogy from a neighboring checklist item.

## The takeaway

The broader lesson wasn't really about GDPR. It was about a habit: **when two checklist items feel
related, don't let that similarity substitute for checking each one against the source
individually.** In a real audit, that kind of assumption is exactly what turns a defensible
assessment into a wrong one — the kind that shows up in a compliance report and undermines trust
in the rest of the findings.

It's a small example, but it's the same skill that scales up to real audits: read the evidence,
not your assumptions about the evidence.

---
*Part of my [Botium Toys Controls and Compliance Audit](./README.md) portfolio project.*
