# 00 Orchestrator Examples

## Example 1: New Buyer Showing Request

### Input

Buyer asks to see a Tarrytown bungalow.

Buyer-representation confirmation is unknown.

### Orchestrator Action

Route to `01_lead_qualifier`.

Apply possible BLUE slip.

### Desk Trail

```md
[00-ORCH] 2026-05-12 — New buyer showing request opened. Buyer-representation confirmation unknown. Routed to 01_lead_qualifier for showing readiness review.
```

---

## Example 2: Deadline Question With Missing Effective Date

### Input

Agent asks:

```md
When does the option period end?
```

Effective Date is missing.

### Orchestrator Action

Route to `04_transaction_coordinator`, but mark the envelope as blocked until Effective Date is known.

### Desk Trail

```md
[00-ORCH] 2026-05-12 — Option deadline question received. Effective Date missing. Applied YELLOW slip and routed to 04_transaction_coordinator for blocked deadline review.
```

---

## Example 3: Message Needed For Listing Agent

### Input

Diana needs a message to the listing agent about inspection concerns.

### Orchestrator Action

Route to `03_client_communication`.

### Desk Trail

```md
[00-ORCH] 2026-05-12 — Listing-agent message requested. Routed to 03_client_communication. Human approval required before sending.
```
