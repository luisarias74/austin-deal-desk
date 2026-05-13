# Start Here

Use this file when a new case comes in.

A case can be:

- a buyer requesting a showing
- a seller asking about next steps
- a property that needs research
- a contract deadline question
- an inspection issue
- a client or outside-agent message that needs drafting
- a deal problem that needs routing

---

## Step 1: Open A Manila Envelope

Every case starts with a Manila Envelope.

Use the template in:

`MANILA_ENVELOPE.md`

Do not skip this. The envelope keeps Diana’s team from losing facts, deadlines, risks, and approval requirements.

---

## Step 2: Send The Envelope To The Orchestrator

Every new envelope starts at:

`00_orchestrator/`

The Orchestrator decides which station should handle the next step.

The Orchestrator does not do specialist work. It routes the case and protects the workflow.

---

## Step 3: Apply A Status Slip

Use one or more status slips:

| Slip | Use When |
|---|---|
| RED | Diana/principal needs to review urgently. |
| YELLOW | Information is missing or a deadline may be at risk. |
| BLUE | Compliance, broker, local-source, or licensed-professional verification is needed. |
| GREEN | The envelope is ready for the next station. |

---

## Step 4: Work The Correct Station

Each station has a folder.

Inside each folder:

- `identity.md` explains what the station is.
- `rules.md` explains what the station can and cannot do.
- `examples.md` shows how the station works.
- `handoff.md` explains how to pass the case forward or backward.

---

## Step 5: Update The Desk Trail

Every station must leave a Desk Trail entry.

Use this format:

```md
[STATION-STAMP] YYYY-MM-DD — What happened. What was flagged. Where the envelope went next.
```

Example:

```md
[01-LQ] 2026-05-12 — Buyer requested showing. Buyer-representation confirmation missing. Applied BLUE slip. Showing workflow blocked until Diana/broker verifies compliance.
```

---

## Step 5b: Same-Day Buyer Requests

If a buyer requests same-day action (showing, callback, urgent answer), the team may produce a **fast acknowledgment draft** in parallel with intake.

Rules:

- The acknowledgment is a draft for human approval, not an automatic send.
- A fast acknowledgment does **not** confirm a showing.
- Showing confirmation still requires buyer-representation/compliance and scheduling clearance per `DESK_RULES.md`.
- The acknowledgment may ask for the missing items (lender letter, written representation, property address/MLS#).

---

## Step 6: Do Not Guess

If a fact is unknown, write:

```md
Unknown.
```

Do not fill gaps with assumptions. Do not let the AI sound certain when the team has not verified the fact.

---

## The Most Important Rule

The AI helps Diana’s team organize, draft, flag, and route.

The AI does not approve, send, advise, negotiate, or confirm compliance.
