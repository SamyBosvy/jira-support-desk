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
| Refund / payment dispute | Summary, Transaction ID, Am
