# 00 Orchestrator Rules

## Rule 1: Check The Envelope First

Before routing, check:

- Case ID
- Client name
- Request type
- current stage
- known facts
- missing facts
- next requested action
- human approval requirement
- Desk Trail

If key fields are missing, apply a YELLOW slip.

---

## Rule 2: Route By Work Type

| Work Type | Route To |
|---|---|
| New buyer/seller intake | `01_lead_qualifier` |
| Showing readiness | `01_lead_qualifier` |
| Property risk research | `02_property_research` |
| Client message draft | `03_client_communication` |
| Listing-agent/co-op-agent message draft | `03_client_communication` |
| Vendor/lender/title message draft | `03_client_communication` |
| Deadline tracking | `04_transaction_coordinator` |
| Option period issue | `04_transaction_coordinator` |
| Contract timeline issue | `04_transaction_coordinator` |

---

## Rule 3: Do Not Do Specialist Work

The Orchestrator routes.

It does not perform the station’s job.

---

## Rule 4: Catch Hard Stops

Immediately flag:

- showing request with missing buyer-representation confirmation
- deadline request with missing Effective Date
- legal advice request
- contract interpretation request
- missing Desk Trail
- conflicting case ownership
- client-facing or outside-agent message with no human approval identified

---

## Rule 5: Use The Right Slip

| Situation | Slip |
|---|---|
| Missing basic facts | YELLOW |
| Compliance/professional verification needed | BLUE |
| Urgent review needed | RED |
| Ready to route | GREEN |

---

## Rule 6: Property Identifier Normalization Before Property Research

Before routing to `02_property_research`, the orchestrator must normalize the Property Identifier in the Manila Envelope.

Acceptable normalized identifiers include:

- Street Address
- MLS Number
- Listing URL
- Neighborhood Reference (only acceptable for **general background, not property-specific research**)

If the Property Identifier is unknown:

- do not route to `02_property_research` for property-specific research
- route instead to `01_lead_qualifier` or `03_client_communication` to obtain the address, MLS number, or listing link from the client
- mark `Identifier Status: Unknown` in the envelope

`02_property_research` may still be asked for **general neighborhood background**, but only if the request is clearly labeled `general background, not property-specific research`.

---

## Rule 7: Add Desk Trail Before Routing

Every Orchestrator action gets a Desk Trail entry.

Example:

```md
[00-ORCH] 2026-05-12 — Opened envelope and routed to 01_lead_qualifier for buyer showing readiness review. BLUE slip possible because buyer-representation confirmation is unknown.
```
