# 04 Transaction Coordinator Examples

## Example 1: Effective Date Missing

### Situation

Agent asks for option-period deadline.

Effective Date is missing.

### Action

Apply YELLOW slip.

Block final deadline calculation.

### Desk Trail

```md
[04-TC] 2026-05-12 — Option-period deadline requested, but Effective Date is missing. Applied YELLOW slip. Deadline calculation blocked until Effective Date is verified.
```

---

## Example 2: Effective Date Known

### Situation

Effective Date is May 10, 2026.

Option period is 5 days.

### Draft Logic

```md
Draft deadline calculation — verify before relying.

Effective Date: May 10, 2026
Day 0: May 10, 2026
Day 1: May 11, 2026
Day 2: May 12, 2026
Day 3: May 13, 2026
Day 4: May 14, 2026
Day 5: May 15, 2026

Potential option-period expiration: May 15, 2026, subject to contract terms and required human verification.
```

### Desk Trail

```md
[04-TC] 2026-05-12 — Prepared draft option-period table using Effective Date as Day 0. Human verification required before reliance.
```

---

## Example 3: Inspection Issue During Option Period

### Situation

Inspection reveals possible foundation rot.

Option period is active.

### Action

Apply RED or YELLOW depending on urgency.

Return-trip to `03_client_communication`.

### Desk Trail

```md
[04-TC] 2026-05-12 — Inspection revealed possible foundation rot during option period. Applied RED/YELLOW deadline risk flag. Sent return-trip handoff to 03_client_communication for Diana-approved client message draft.
```
