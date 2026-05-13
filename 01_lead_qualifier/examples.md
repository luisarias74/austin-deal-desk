# 01 Lead Qualifier Examples

## Example 1: Buyer Wants Showing, Buyer-Rep Unknown

### Situation

Buyer wants to see a 1938 Tarrytown bungalow.

Buyer-representation confirmation is missing.

### Action

Apply BLUE slip.

Block showing workflow.

Route to Diana/broker verification.

### Desk Trail

```md
[01-LQ] 2026-05-12 — Buyer requested residential showing. Buyer-representation confirmation missing. Applied BLUE slip. Showing workflow blocked until Diana/broker verifies compliance.
```

---

## Example 2: Buyer Has Preapproval And Buyer-Rep Cleared

### Situation

Buyer has confirmed buyer-representation status and preapproval.

### Action

Apply GREEN slip.

Route to `02_property_research` if property research is needed.

### Desk Trail

```md
[01-LQ] 2026-05-12 — Buyer intake complete. Buyer-representation status marked cleared by Diana. Preapproval noted. Applied GREEN slip and routed to 02_property_research.
```

---

## Example 3: Seller Intake Missing Motivation

### Situation

Seller asks for listing help, but motivation and timeline are unclear.

### Action

Apply YELLOW slip.

Request missing facts.

### Desk Trail

```md
[01-LQ] 2026-05-12 — Seller intake started. Timeline and motivation missing. Applied YELLOW slip and requested missing intake facts before routing.
```
