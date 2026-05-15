# Case Study: The Tarrytown Tangle
### A closed-case walkthrough of The Austin Deal Desk in motion.

This is the proof-of-life case for The Austin Deal Desk.

It shows how the system handles a realistic Austin transaction pattern:

- a buyer wants to see an older Tarrytown bungalow
- buyer-representation status is missing
- the property has older-home and possible foundation risk
- the deal later moves under contract
- the option period creates timing pressure
- inspection reveals a possible foundation concern
- the system routes communication without letting AI freestyle legal or negotiation advice

The point is not that the AI solves the deal.

The point is that the desk keeps Diana’s team from losing facts, skipping verification, or moving too fast.

---

## Case Snapshot

| Field | Details |
|---|---|
| Case Name | The Tarrytown Tangle |
| Client Type | Buyer |
| Property | 1938 Tarrytown bungalow |
| First Request | Buyer wants a showing |
| First Risk | Buyer-representation status missing |
| Property Risk | Older home, possible pier-and-beam/foundation concern |
| Contract Risk | Option-period timing |
| Communication Risk | Inspection issue requires calm client message |
| System Outcome | BLUE slip blocks showing workflow, research flags risks, TC tracks deadlines, Comms drafts only for approval |

---

## The Messy Input

A new buyer texts:

> “Can we see that 1938 bungalow in Tarrytown today? It looks perfect.”

Known facts:

- Buyer wants a showing.
- Property is an older Tarrytown bungalow.
- Buyer is excited and moving quickly.

Unknown facts:

- Buyer-representation status.
- Preapproval/proof of funds.
- Property-specific foundation, floodplain, historic, zoning, or inspection concerns.
- Whether Diana has cleared the showing workflow.

Without a system, a junior agent might jump straight to scheduling.

The Austin Deal Desk does not allow that.

---

## Step 1: 00 Orchestrator Opens The Envelope

The request starts at `00_orchestrator`.

The Orchestrator does not research the property or draft a message.

It opens the Manila Envelope, checks for missing facts, and routes the case.

Desk Trail:

> [00-ORCH] 2026-05-12 — Opened Manila Envelope for buyer showing request. Buyer-representation confirmation is unknown. Routed to 01_lead_qualifier for showing-readiness review.

Status:

- YELLOW — intake facts missing.
- BLUE — buyer-representation verification may be required before showing workflow.

---

## Step 2: 01 Lead Qualifier Applies The Hard Stop

The envelope moves to `01_lead_qualifier`.

The buyer wants a residential showing, but buyer-representation status is missing.

System decision:

> No cleared buyer-representation flag = no showing workflow.

The system does not say:

> Go ahead and schedule it.

The system says:

> BLUE slip applied — buyer-representation verification required before showing workflow can proceed.

Desk Trail:

> [01-LQ] 2026-05-12 — Buyer requested residential showing. Buyer-representation confirmation missing. Applied BLUE slip. Showing workflow blocked until Diana/broker verifies compliance.

What this prevents:

- rushed showing confirmation
- a junior agent improvising around compliance
- the AI treating missing facts as minor details
- the team confusing “interested buyer” with “showing-ready buyer”

---

## Step 3: Pre-Showing Research Is Allowed, But Labeled

The case may continue only as:

> Pre-showing intake/research only — showing not cleared.

The desk does not freeze the entire case.

It blocks unsafe movement while allowing useful preparation.

The envelope may move to `02_property_research`, but only with the compliance status clearly labeled.

---

## Step 4: 02 Property Research Flags Austin-Specific Risk

The property is a 1938 bungalow in Tarrytown.

The Property Research station does not make legal, zoning, floodplain, or engineering conclusions.

It flags issues for verification.

Research flags:

- YELLOW — older-home/foundation risk.
- BLUE — historic/zoning verification may be needed.
- BLUE — school/neighborhood claims must be verified before client-facing use.
- BLUE — floodplain/drainage status should be verified if relevant.

Desk Trail:

> [02-PR] 2026-05-12 — Reviewed older Tarrytown bungalow. Flagged older-home and possible pier-and-beam/foundation concern. Applied YELLOW slip. Applied BLUE slip for historic/zoning verification before client-facing guidance.

The station does not say:

> This home definitely has foundation problems.

Or:

> This property is legally confirmed to be inside a historic district.

It says:

> Flag for verification before client-facing use.

That is the difference between a generic AI assistant and an operational desk.

---

## Step 5: Diana Clears The Showing Path

Diana or the appropriate reviewer verifies what is required before the showing workflow can proceed.

The envelope is updated:

| Field | Status |
|---|---|
| Buyer-representation status | Cleared by Diana/broker verification |
| Showing workflow | Cleared |

Desk Trail:

> [01-LQ] 2026-05-12 — Diana/broker verification marked buyer-representation requirement cleared for showing workflow. Updated envelope and released case for next station.

The system can now continue.

The important point: it did not continue before the file was ready.

---

## Step 6: Deal Goes Under Contract

The case moves to `04_transaction_coordinator`.

The first question is not:

> What is the option deadline?

The first question is:

> What is the Effective Date?

Because the desk rule is:

> Effective Date = Day 0. The next calendar day = Day 1.

If Effective Date is missing:

> YELLOW slip — Effective Date missing. Deadline calculation blocked.

If Effective Date is known, the station may prepare a draft deadline table, but it must label it:

> Draft deadline calculation — verify before relying.

Desk Trail:

> [04-TC] 2026-05-12 — Contract timeline opened. Effective Date required before final deadline calculation. Applied Day 0 doctrine. Draft calculations require Diana/team verification before reliance.

---

## Step 7: Inspection Reveals Possible Foundation Rot

During the option period, inspection reveals a possible foundation issue.

This creates three risks:

1. Property risk.
2. Deadline risk.
3. Communication risk.

A generic AI assistant might draft a confident repair demand.

The Austin Deal Desk does not.

`04_transaction_coordinator` sends a return-trip handoff to `03_client_communication` with supporting facts and limits.

---

## Step 8: Return-Trip Handoff To Communication

Return-trip summary:

| Field | Detail |
|---|---|
| From | 04_transaction_coordinator |
| To | 03_client_communication |
| Return To | 04_transaction_coordinator |
| Reason | Inspection revealed possible foundation rot during option period |
| Needed Output | Client text-first draft and email version |
| Human Approval | Diana approval required before sending |
| Do Not Include | legal advice, repair strategy decision, termination advice, final deadline certainty |

Desk Trail:

> [04-TC] 2026-05-12 — Inspection revealed possible foundation rot during active option period. Sent return-trip to 03_client_communication for Diana-approved draft only.

This is the core of the desk: the handoff carries context without transferring authority.

---

## Step 9: 03 Communication Drafts, But Does Not Send

The envelope moves to `03_client_communication`.

This station drafts only.

It does not send.

It does not decide strategy.

It does not make legal claims.

Text-first draft:

> Draft only — human approval required before sending.
>
> Hi [Client Name], Diana is reviewing the inspection notes now, especially the foundation-related item. We do not want to rush a conclusion before the right review, but we are watching the option-period timing closely and will follow up with next-step options after Diana reviews.

Email draft:

> Draft only — human approval required before sending.
>
> Subject: Inspection Follow-Up
>
> Hi [Client Name],
>
> Diana is reviewing the inspection notes, including the foundation-related concern. We do not want to overstate anything before the right review, but we also want to stay mindful of the option-period timing.
>
> Diana will review the issue and determine the best next step before anything is sent to the other side.
>
> Best,  
> Diana’s Team

Optional listing-agent draft:

> Draft only — human approval required before sending.
>
> Hi [Listing Agent Name], we are reviewing the inspection findings with our client and Diana. There is a foundation-related item that needs closer review. We will follow up once our client has had a chance to review next steps with Diana.

Desk Trail:

> [03-COMMS] 2026-05-12 — Drafted client text, client email, and optional listing-agent message regarding inspection/foundation concern. Drafts require Diana approval before sending. Returned envelope to 04_transaction_coordinator for communication tracking.

---

## Step 10: 04 Tracks Whether The Message Was Actually Sent

A draft is not a sent message.

The envelope returns to `04_transaction_coordinator`.

Communication status:

| Item | Status |
|---|---|
| Client message drafted | Yes |
| Human approved | Unknown |
| Message sent by human | Unknown |
| Sent date/time | Unknown |

Desk Trail:

> [04-TC] 2026-05-12 — Received communication drafts from 03_client_communication. Communication not yet confirmed sent. Tracking approval/sent status before marking communication complete.

---

## Final Desk Trail

> [00-ORCH] 2026-05-12 — Opened Manila Envelope for buyer showing request. Buyer-representation confirmation unknown. Routed to 01_lead_qualifier.
>
> [01-LQ] 2026-05-12 — Buyer requested residential showing. Buyer-representation confirmation missing. Applied BLUE slip. Showing workflow blocked until Diana/broker verifies compliance.
>
> [02-PR] 2026-05-12 — Reviewed older Tarrytown bungalow. Flagged older-home and possible pier-and-beam/foundation concern. Applied YELLOW slip. Applied BLUE slip for historic/zoning verification before client-facing guidance.
>
> [01-LQ] 2026-05-12 — Diana/broker verification marked buyer-representation requirement cleared for showing workflow. Updated envelope and released case for next station.
>
> [04-TC] 2026-05-12 — Contract timeline opened. Effective Date required before final deadline calculation. Applied Day 0 doctrine. Draft calculations require Diana/team verification before reliance.
>
> [04-TC] 2026-05-12 — Inspection revealed possible foundation rot during active option period. Sent return-trip to 03_client_communication for Diana-approved draft only.
>
> [03-COMMS] 2026-05-12 — Drafted client text, client email, and optional listing-agent message regarding inspection/foundation concern. Drafts require Diana approval before sending. Returned envelope to 04_transaction_coordinator.
>
> [04-TC] 2026-05-12 — Received communication drafts from 03_client_communication. Communication not yet confirmed sent. Tracking approval/sent status before marking communication complete.

---

## What The Desk Protected

| Risk | How The Desk Responded |
|---|---|
| Buyer wanted a fast showing | BLUE slip blocked showing workflow until verification. |
| Buyer-rep status was missing | Routed to Diana/broker verification. |
| Older Tarrytown property had possible risks | Property Research flagged foundation/historic/zoning verification. |
| Effective Date could affect deadlines | Transaction Coordinator used Day 0 doctrine. |
| Inspection revealed foundation issue | TC created return-trip to Communication. |
| Client needed reassurance | Comms drafted calm message only for approval. |
| Draft could be mistaken as sent | TC tracked approval/sent status separately. |

---

## Why This Matters

The Austin Deal Desk did not make the deal more complicated.

It made the risk visible.

It prevented unsafe movement.

It kept every station in its lane.

It left a Desk Trail Diana could review.

That is the product.

Not another app.

A desk that works Monday morning.
