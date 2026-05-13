# The Austin Deal Desk

**A folder-based AI operating system for a 4-person Austin residential real estate team.**

The Austin Deal Desk turns AI from a vague assistant into a practical operations desk. Every client request, property concern, communication need, or contract deadline moves through the system inside a **Manila Envelope**.

The folders are the desk stations.  
The Manila Envelope carries the case.  
The colored slips show risk.  
The Desk Trail proves what happened.

This is not software. It is not a CRM. It is not legal advice. It is a no-code, markdown-only operating system that Diana’s newest agent can learn in one day and the full team can learn in one week.

---

## What This System Does

The Austin Deal Desk helps Diana’s team:

- capture client and property requests in a consistent format
- route work to the correct AI station
- flag Austin/Texas verification issues without pretending to resolve them
- draft client and outside-agent communications for human approval
- track deadline risk using the **Effective Date = Day 0** doctrine
- preserve a clear Desk Trail for Diana to review

The system is designed for a real boutique real estate team, not for developers.

---

## The Core Metaphor

Every case travels inside a **Manila Envelope**.

The envelope carries:

- case ID
- client name
- request type
- current station
- current stage
- known facts
- missing facts
- risk flags
- compliance flags
- deadline flags
- next requested action
- human approval requirement
- Desk Trail / audit trail

No envelope, no work.

---

## The Desk Stations

| Station | Desk Role | Main Job |
|---|---|---|
| `00_orchestrator` | Front Desk | Opens envelopes, checks completeness, routes work. |
| `01_lead_qualifier` | Intake Desk | Checks client readiness and showing readiness. |
| `02_property_research` | Property Risk Desk | Flags property-specific Austin/Texas concerns. |
| `03_client_communication` | Communication Desk | Drafts client, outside-agent, vendor, and internal messages. |
| `04_transaction_coordinator` | Deadline Desk | Tracks Effective Date, option period, earnest money, financing, appraisal, and communication status. |

---

## Status Slips

Each Manila Envelope can carry one or more status slips.

| Slip | Meaning |
|---|---|
| **RED** | Urgent Diana/principal review required. |
| **YELLOW** | Missing information or timeline risk. |
| **BLUE** | Austin/Texas compliance, broker, local-source, or licensed-professional verification required. |
| **GREEN** | Ready for the next station. |

When in doubt, flag for verification instead of sounding certain.

BLUE slips point to verification destinations, not final conclusions. See `AUSTIN_RESOURCES.md` for a practical index of where to send each kind of BLUE-slip question.

---

## Non-Negotiable Rules

1. The AI never sends communications directly.
2. The AI never provides legal advice.
3. The AI never confirms compliance as final.
4. Unknown facts stay unknown.
5. RED slips require Diana/principal review.
6. BLUE slips require Diana, broker, local-source, or licensed-professional verification.
7. For deadline tracking, **Effective Date = Day 0**.
8. A residential showing workflow cannot advance until buyer-representation compliance is cleared.
9. Every station updates the Desk Trail.
10. Every station stays in its lane.

---

## Reference Files

Root markdown files Diana's team uses regularly:

- `START_HERE.md` — how to open a case.
- `MANILA_ENVELOPE.md` — envelope template.
- `DESK_RULES.md` — non-negotiable rules.
- `RED_FLAG_SLIPS.md` — status slips reference.
- `THE_DEAL_DESK_PLAYBOOK.md` — the operating playbook.
- `CASE_LOG_TEMPLATE.md` — quick case log template.
- `SAMPLE_CASE_TARRYTOWN.md` — canonical example case.
- `AUSTIN_RESOURCES.md` — verification destinations for BLUE slips.

---

## How To Use This Monday Morning

1. Open `START_HERE.md`.
2. Copy the template from `MANILA_ENVELOPE.md`.
3. Create one envelope for the case.
4. Send the envelope to `00_orchestrator`.
5. Follow the station handoffs.
6. Apply status slips when risk appears.
7. Keep the Desk Trail updated before every handoff.
8. Require human approval before relying on sensitive output.

---

## What This System Is Not

The Austin Deal Desk is not:

- legal advice
- broker supervision replacement
- contract interpretation authority
- engineering advice
- final zoning or floodplain determination
- pricing or negotiation authority
- a substitute for Diana’s judgment
- a system for sending messages automatically

The system helps the team see what needs attention. Humans decide what to do.
