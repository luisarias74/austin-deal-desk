# Manila Envelope Template

Use this template for every case.

Copy it into a new case file before routing work through the Deal Desk.

---

## Manila Envelope

```md
# Manila Envelope

## Case Identity

Case ID:
Client Name:
Client Type:
Request Type:
Property Address:
Current Station:
Current Stage:
Date Opened:
Assigned Human Owner:

---

## Request Summary

What is the client or team asking for?

---

## Known Facts

- 
- 
- 

---

## Missing Facts

- 
- 
- 

---

## Current Status Slips

RED:
YELLOW:
BLUE:
GREEN:

---

## Buyer Intake Flags

Preapproval Status:
Budget / Price Range:
Buyer-Stated Urgency:
First-Touch Acknowledgment Sent:
First-Touch Sent Timestamp:

First-Touch Acknowledgment Sent allowed values:
Unknown / Not Needed / Drafted / Awaiting Human Approval / Sent by Human

---

## Property Identifier

Street Address:
MLS Number:
Listing URL:
Neighborhood Reference:
Identifier Status:
Identifier Normalized By:
Identifier Normalized Timestamp:

---

## Compliance Flags

Buyer-representation confirmation:
TREC/current-form verification needed:
Broker/principal verification needed:
Licensed professional verification needed:
Other compliance concern:

---

## Deadline Flags

Effective Date:
Day Zero confirmed:
Earnest Money Deadline:
Option Fee Deadline:
Option Period Expiration:
Inspection Deadline/Risk:
Financing Deadline:
Appraisal Deadline:
Weekend/Legal Holiday Movement Flag:
Deadline Verification Status:

---

## Property Risk Flags

Foundation/Pier-and-Beam:
Central Texas Soil/Foundation:
Floodplain:
Historic District/Zoning:
School/Neighborhood Claim:
Public Record Conflict:
Inspection/Professional Review Needed:

---

## Communication Flags

Client message needed:
Listing-agent/co-op-agent message needed:
Vendor/lender/title message needed:
Internal team update needed:
Draft completed:
Human approved:
Message sent by human:
Sent date/time:

---

## Next Requested Action

What should the next station do?

---

## Human Approval Requirement

Who must approve before action?

---

## Desk Trail

[STATION-STAMP] YYYY-MM-DD — Entry.
```

---

## Field Rules

### Case ID

Use a simple format:

```md
AUSTIN-YYYYMMDD-CLIENTLASTNAME
```

Example:

```md
AUSTIN-20260512-RIVERA
```

### Current Station

Use one of:

```md
00_orchestrator
01_lead_qualifier
02_property_research
03_client_communication
04_transaction_coordinator
```

### Status Slips

Use:

```md
Yes / No / Unknown
```

Example:

```md
RED: No
YELLOW: Yes — Missing Effective Date.
BLUE: Yes — Buyer-representation verification needed.
GREEN: No
```

### Effective Date Rule

Effective Date is Day 0.

Do not calculate final deadlines if Effective Date is unknown.

### Human Approval Requirement

Examples:

```md
Diana approval required before client message is sent.
Broker verification required before buyer showing workflow proceeds.
Licensed professional verification required before advising on foundation concern.
```
