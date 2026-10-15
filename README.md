# Northwind Payments Support Desk

A customer support desk for a fictional fintech, built in Atlassian Customer Service Management (Jira Service Management family).

It's modelled on the EU/UK complaints process I ran as Complaints Manager at Square/Block, widened into a full support desk covering customer service, technical support and regulated complaints handling.

> Northwind Payments is an invented brand. All tickets and customers are fictional.

## The business problem

A payments company gets very different contacts through one front door: quick questions, technical faults, payment disputes and formal complaints. They need different fields, different routes and different deadlines. Complaints in particular carry regulatory deadlines (PSD2: final response within 15 business days for payment complaints). This desk separates them at intake so each one follows the right process and is tracked against the right clock.

## Design

### Request types and intake fields

| Request type | Fields |
|---|---|
| General enquiry | Summary, Description, Account email |
| Technical issue | Summary, Platform (Web / iOS / Android / Card terminal), Error message, Steps to reproduce |
| Refund / payment dispute | Summary, Transaction ID, Amount, Transaction date, Reason (Not received / Duplicate / Unauthorised / Wrong amount) |
| Complaint | Summary, Description, Product, Date of issue, Outcome wanted, Vulnerable customer (checkbox) |

### Workflows

- **Complaint:** Received → Acknowledged → Investigation → Final Response Sent → Closed
- **Technical issue:** Open → Triage → Escalated to Tech → Waiting for Customer → Resolved
- General enquiry and Refund / dispute use the default workflow.

### SLA targets

| Request type | Target |
|---|---|
| Complaint | Acknowledge within 3 business days; final response within 15 business days (PSD2) |
| Technical issue | First response within 4 hours |
| Refund / dispute | First response within 1 business day |
| General enquiry | First response within 8 hours |

### Queues

- Complaints – breaching soon
- Escalated to tech
- Refunds awaiting evidence
- Unassigned

### Automation

- On Complaint creation: automatic acknowledgement comment to the customer.

## Status

- [x] Site and "Northwind Payments Support" space created
- [x] Four customer-facing support forms built
- [x] Custom work types created (Complaint, Technical issue, Refund / payment dispute) and added to the space
- [x] Forms linked to their work types
- [x] New work types moved onto the main workflow
- [ ] Custom Complaint and Technical issue workflows
- [ ] SLA timers
- [ ] Queues
- [ ] Automation rule
- [ ] 12 test tickets submitted through the customer portal and worked through the queue
- [ ] Screenshots

## Build log

### Week 1 (8–15 Oct 2026) — logged when this repo was created
Set up the site and space, built the four support forms with their intake fields, created the three custom work types at site level, added them to the space and linked each form to its work type. Moved the new work types off the default read-only workflow onto the main workflow, ready for the custom Complaint and Technical issue workflows.

## Screenshots

Coming as the build progresses: customer portal, queue with SLA timers, complaint workflow, a completed complaint ticket.

## Tools

Atlassian Customer Service Management (Jira Service Management family), Free plan.
