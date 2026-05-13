# The Deal Desk Playbook

## The Operating Metaphor

The Austin Deal Desk works like a real office desk.

Each case is placed inside a Manila Envelope. The envelope moves from station to station. Each station does its assigned work, adds notes, applies status slips, and hands the envelope forward.

If the station cannot continue, it sends the envelope back with a clear reason.

---

## The Stations

### 00 Orchestrator

The front desk.

It receives the envelope, checks whether it is complete enough to route, and sends it to the correct station.

It protects the system from messy routing.

### 01 Lead Qualifier

The intake desk.

It checks whether the client is ready for the next step.

For buyer showing requests, it checks whether buyer-representation compliance is confirmed. If not confirmed, the showing workflow stops.

### 02 Property Research

The property risk desk.

It flags property-level issues that need Diana, broker, inspector, engineer, local-source, or licensed-professional review.

It does not make final legal, engineering, zoning, or floodplain conclusions.

### 03 Client Communication

The communication desk.

It drafts messages for clients, listing agents, co-op agents, vendors, inspectors, lenders, title contacts, and internal team members.

It never sends the message.

### 04 Transaction Coordinator

The deadline desk.

It tracks contract movement and deadline awareness. It treats Effective Date as Day 0.

It can draft a deadline table, but every deadline table must be verified before reliance.

---

## Standard Case Flow

```md
New Request
→ Manila Envelope
→ 00 Orchestrator
→ Normalize property identifier and capture first-touch urgency before research
→ Correct Station
→ Status Slip
→ Desk Trail Update
→ Handoff
→ Next Station
→ Human Approval When Required
```

First-touch acknowledgment may happen in parallel with intake, but only as a draft for human approval. It must not confirm a showing.

---

## Return-Trip Flow

Sometimes a station needs another station to complete a narrow task before it can continue.

Example:

```md
04 Transaction Coordinator finds inspection issue
→ Sends return-trip to 03 Client Communication
→ 03 drafts client/outside-agent message options
→ Diana approves and sends, if appropriate
→ 03 returns envelope to 04
→ 04 logs communication status
```

The return-trip must include the reason and supporting facts.

Bad:

```md
Draft inspection message.
```

Good:

```md
Inspection revealed possible foundation rot during option period. Option deadline is approaching. Draft a calm message for Diana’s approval explaining that Diana is reviewing the issue and next steps before the option period expires.
```

---

## Desk Trail And Desk Stamps

The Desk Trail is the audit log.

It answers:

- who touched the envelope
- what they did
- what was missing
- what was flagged
- what human approval is needed
- where the envelope went next

Every station must update it.

| Station | Stamp |
|---|---|
| 00 Orchestrator | `[00-ORCH]` |
| 01 Lead Qualifier | `[01-LQ]` |
| 02 Property Research | `[02-PR]` |
| 03 Client Communication | `[03-COMMS]` |
| 04 Transaction Coordinator | `[04-TC]` |

---

## Human Approval Gates

Human approval is required for:

- client-facing messages
- listing-agent or co-op-agent messages
- vendor/lender/title messages that affect deal posture
- legal/compliance questions
- buyer-representation uncertainty
- contract deadline risk
- pricing strategy
- negotiation strategy
- repair strategy
- TREC form/current-form questions
- RED slips
- BLUE slips

---

## One-Week Team Rollout

### Day 1

Read:

- `README.md`
- `START_HERE.md`
- `MANILA_ENVELOPE.md`
- `DESK_RULES.md`

### Day 2

Review all station identities.

### Day 3

Practice a buyer showing request.

### Day 4

Practice a property research request.

### Day 5

Practice a contract deadline scenario.

### Day 6

Practice a return-trip handoff.

### Day 7

Run the sample case:

`SAMPLE_CASE_TARRYTOWN.md`
