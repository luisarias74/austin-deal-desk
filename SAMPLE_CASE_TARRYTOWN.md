# Sample Case: The Tarrytown Tangle

This sample shows how a case moves through The Austin Deal Desk.

---

## Case Setup

A buyer texts Diana same-day: they want to see "that old Tarrytown bungalow this afternoon," say they are preapproved around $850K, and say they have not signed anything yet.

The buyer is excited and wants to schedule quickly.

Buyer-representation confirmation is missing.

The exact property address / MLS # is not provided — only "that old Tarrytown bungalow."

Later, the deal goes under contract.

Inspection reveals possible foundation rot during the option period.

---

# Manila Envelope

```md
# Manila Envelope

## Case Identity

Case ID:
AUSTIN-20260512-TARRYTOWN

Client Name:
Sample Buyer

Client Type:
Buyer

Request Type:
Residential showing request / property research / transaction coordination

Property Address:
1938 Tarrytown bungalow address placeholder

Current Station:
00_orchestrator

Current Stage:
New buyer showing request

Date Opened:
2026-05-12

Assigned Human Owner:
Diana

---

## Request Summary

Buyer wants to see a 1938 Tarrytown bungalow.

---

## Known Facts

- Buyer wants a same-day showing.
- Buyer states preapproval around $850K (lender/letter not provided).
- Buyer states they have not signed anything yet.
- Property is described only as an older Tarrytown bungalow.
- Buyer-representation confirmation is not currently documented.

---

## Missing Facts

- Buyer name and contact.
- Lender preapproval letter.
- Buyer-representation confirmation.
- Exact property address / MLS # / listing URL.
- Exact showing readiness.
- Current verified property-specific risks.

---

## Current Status Slips

RED:
No

YELLOW:
Yes — Missing intake facts (preapproval letter, address/MLS, buyer-stated urgency captured).

BLUE:
Yes — Buyer-representation verification needed before showing workflow proceeds. See AUSTIN_RESOURCES.md → TREC.

GREEN:
No

---

## Buyer Intake Flags

Preapproval Status:
Stated ~$850K — lender/letter not verified.

Budget / Price Range:
~$850K (buyer-stated).

Buyer-Stated Urgency:
Same-day — buyer asked to see property this afternoon.

First-Touch Acknowledgment Sent:
Drafted / Awaiting Human Approval

First-Touch Sent Timestamp:
Unknown

---

## Property Identifier

Street Address:
Unknown

MLS Number:
Unknown

Listing URL:
Unknown

Neighborhood Reference:
Tarrytown — older bungalow

Identifier Status:
Unknown — buyer referred to "that old Tarrytown bungalow"; awaiting confirmation from buyer.

Identifier Normalized By:
Pending

Identifier Normalized Timestamp:
Pending

---

## Desk Trail

[00-ORCH] 2026-05-12 — Opened envelope for same-day buyer showing request. Property identifier Unknown — did not route to 02_property_research for property-specific research. Routed to 01_lead_qualifier (intake) and parallel return-trip to 03_client_communication (first-touch acknowledgment draft). BLUE slip applied for buyer-representation; YELLOW slip applied for missing intake facts.
```

---

## Step 1: Orchestrator Routes The Case

`00_orchestrator` receives the request.

It does not research the property.

Property Identifier Status is Unknown, so the orchestrator does **not** route to `02_property_research` for property-specific research. It routes to `01_lead_qualifier` for intake and, in parallel, asks `03_client_communication` to draft a first-touch acknowledgment for Diana's approval (same-day urgency).

### Desk Trail

```md
[00-ORCH] 2026-05-12 — New same-day buyer showing request opened. Buyer-representation confirmation unknown. Property Identifier Status Unknown. Routed to 01_lead_qualifier for showing-readiness review and parallel return-trip to 03_client_communication for first-touch acknowledgment draft. Did not route to 02_property_research because identifier is Unknown.
```

---

## Step 2: Lead Qualifier Applies Showing Hard Stop

`01_lead_qualifier` sees that written buyer-representation/showing compliance is missing.

It applies a BLUE slip, naming the verification destination:

```md
BLUE slip — buyer-representation verification required before showing workflow proceeds.
This includes verification of current TREC Buyer Representation Agreement / IABS practices
and NAR-settlement written-agreement requirements effective Aug. 17, 2024, as applicable.
This is a compliance flag, not legal advice. Diana/broker/licensed professional must verify
current requirements.
See AUSTIN_RESOURCES.md → TREC.
```

It also captures the buyer intake flags:

- Preapproval Status: Stated ~$850K — lender/letter not verified.
- Budget / Price Range: ~$850K (buyer-stated).
- Buyer-Stated Urgency: Same-day.
- First-Touch Acknowledgment Sent: Drafted / Awaiting Human Approval (handled by 03_client_communication).

Showing workflow is blocked.

The case can continue only as:

```md
Pre-showing intake/research only — showing not cleared.
```

### Desk Trail

```md
[01-LQ] 2026-05-12 — Buyer requested same-day residential showing. Written buyer-representation/showing compliance missing. Applied BLUE slip with destination (AUSTIN_RESOURCES.md → TREC). Captured Preapproval Status (~$850K stated, unverified), Budget (~$850K), Buyer-Stated Urgency (same-day), First-Touch Acknowledgment (Drafted / Awaiting Human Approval via 03). Showing workflow blocked.
```

---

## Step 3: Diana Clears The Compliance Question

Diana or the appropriate reviewer confirms what is needed before moving forward.

The envelope is updated.

```md
Buyer-representation confirmation:
Cleared by Diana/broker verification.

Showing Workflow Status:
Cleared.
```

### Desk Trail

```md
[01-LQ] 2026-05-12 — Diana/broker verification marked buyer-representation requirement cleared for showing workflow. Applied GREEN slip and routed to 02_property_research.
```

---

## Step 3b: Client Communication Drafts First-Touch Acknowledgment

In parallel with the Lead Qualifier's intake work, `03_client_communication` drafts a fast acknowledgment for Diana's approval. The draft does not confirm a showing.

```md
## Text-First Draft

Draft only — human approval required before sending.

Hi! Thanks for reaching out about the Tarrytown bungalow — I'd love to help.
Before we set a time today, I need to take care of a couple of quick items on
my side: confirm a short written buyer-representation step, and grab a copy of
your preapproval letter. Once those are in hand, I can confirm the showing
window. Could you send the lender letter, and is there a specific address or
MLS # you have in mind?
— Diana
```

`03` updates the envelope:

```md
First-Touch Acknowledgment Sent:
Drafted / Awaiting Human Approval
```

It does **not** mark the acknowledgment Sent. Only the assigned human can confirm send and update the timestamp.

### Desk Trail

```md
[03-COMMS] 2026-05-12 — Drafted same-day first-touch acknowledgment for buyer. Draft only. Does not confirm a showing. Asks for lender letter and property address/MLS#. Diana approval required before sending. Marked First-Touch Acknowledgment Sent: Drafted / Awaiting Human Approval.
```

---

## Step 4: Property Research Limited Until Identifier Is Normalized

`02_property_research` receives the request, but `Identifier Status` is Unknown.

Per its defensive rule, it returns the envelope to `00_orchestrator` and provides only general neighborhood background:

```md
General background, not property-specific research.

- Older Tarrytown bungalows commonly involve pier-and-beam construction and Central Texas soil/foundation concerns.
- Some Tarrytown parcels are affected by Austin historic overlays; status varies parcel-by-parcel.
- School/neighborhood claims require verification before client-facing use.
- Floodplain and easement status must be verified parcel-by-parcel.
```

BLUE slips name destinations from `AUSTIN_RESOURCES.md`:

- foundation concern → inspector / engineer / licensed professional review
- historic/zoning → City of Austin zoning and historic preservation resources
- floodplain → FEMA Flood Map Service Center
- school zone → AISD attendance-zone lookup

### Desk Trail

```md
[02-PR] 2026-05-12 — Identifier Status Unknown. Returned envelope to 00_orchestrator. Provided general background, not property-specific research. Applied BLUE slips with destinations (AUSTIN_RESOURCES.md → inspector/engineer, City of Austin zoning/historic, FEMA, AISD).
```

---

## Step 4b: Identifier Resolved — Full Property Research Resumes

Once the buyer provides the property address or MLS #, the orchestrator normalizes the Property Identifier:

```md
Identifier Status:
Resolved — MLS#/address confirmed by buyer.

Identifier Normalized By:
00_orchestrator

Identifier Normalized Timestamp:
2026-05-12 [time]
```

Property-specific research at `02_property_research` may now proceed for the specific parcel. Flags from Step 4 are re-applied as parcel-specific BLUE slips with destinations.

### Desk Trail

```md
[02-PR] 2026-05-12 — Identifier resolved. Reviewed specific 1938 Tarrytown bungalow. Flagged older-home and pier-and-beam/foundation concern (BLUE → inspector/engineer). Flagged possible historic/zoning verification (BLUE → City of Austin). Applied YELLOW for public-record/MLS conflict review.
```

---

## Step 5: Deal Goes Under Contract

The case moves to `04_transaction_coordinator`.

The Effective Date must be identified before final deadline tracking.

### If Effective Date Is Missing

```md
[04-TC] 2026-05-12 — Contract timeline requested, but Effective Date is missing. Applied YELLOW slip. Deadline calculation blocked until Effective Date is verified.
```

### If Effective Date Is Known

Use Day 0 logic.

```md
Draft deadline calculation — verify before relying.

Effective Date:
May 10, 2026

Day 0:
May 10, 2026

Day 1:
May 11, 2026

Day 2:
May 12, 2026

Day 3:
May 13, 2026

Day 4:
May 14, 2026

Day 5:
May 15, 2026
```

### Desk Trail

```md
[04-TC] 2026-05-12 — Prepared draft deadline table using Effective Date as Day 0. Option-period risk flagged. Human verification required before relying on deadline calculation.
```

---

## Step 6: Inspection Reveals Foundation Rot

Inspection reveals possible foundation rot during the option period.

`04_transaction_coordinator` does not draft the client message.

It sends a return-trip handoff to `03_client_communication`.

### Return-Trip Handoff

```md
## Return-Trip Handoff

Original Requesting Station:
04_transaction_coordinator

Current Station:
04_transaction_coordinator

Return To Station:
04_transaction_coordinator

Send To:
03_client_communication

Case ID:
AUSTIN-20260512-TARRYTOWN

Client Name:
Sample Buyer

Why This Is Returning:
Inspection revealed possible foundation rot during the option period. Diana needs a calm client message draft for approval.

Supporting Facts:
- Inspection issue involves possible foundation rot.
- Option period is active.
- Deadline timing may matter.
- Diana must review before strategy is communicated.

Supporting Documents or Notes:
Inspection notes, if available.

Risk Flags:
Foundation concern.
Option-period timing risk.
Possible negotiation/repair strategy issue.

Status Slip:
RED or YELLOW depending on timing urgency.
BLUE if professional/legal verification is needed.

Draft/Work Product Needed:
Client text-first draft and email version.

Still Missing:
Diana’s chosen strategy.
Professional review status.
Whether message should also go to listing agent.

Human Approval Needed:
Diana approval required before sending.

Desk Trail Entry:
[04-TC] 2026-05-12 — Inspection revealed possible foundation rot during active option period. Sent return-trip to 03_client_communication for Diana-approved client message draft.

Desk Stamp:
[04-TC]
```

---

## Step 7: Client Communication Drafts The Message

`03_client_communication` drafts a calm message.

It does not send it.

### Text-First Draft

```md
Draft only — human approval required before sending.

Hi [Client Name], Diana is reviewing the inspection notes now, especially the foundation-related item. We do not want to rush a conclusion before the right review, but we are watching the option-period timing closely and will follow up with next-step options after Diana reviews.
```

### Email Draft

```md
Draft only — human approval required before sending.

Subject: Inspection Follow-Up

Hi [Client Name],

Diana is reviewing the inspection notes, including the foundation-related concern. We do not want to overstate anything before the right review, but we also want to stay mindful of the option-period timing.

Diana will review the issue and determine the best next step before anything is sent to the other side.

Best,  
Diana’s Team

[DIANA'S SIGNATURE]
```

### Optional Listing-Agent Draft

```md
Draft only — human approval required before sending.

Hi [Listing Agent Name], we are reviewing the inspection findings with our client and Diana. There is a foundation-related item that needs closer review. We will follow up once our client has had a chance to review next steps with Diana.
```

### Desk Trail

```md
[03-COMMS] 2026-05-12 — Drafted client text, client email, and optional listing-agent message regarding inspection/foundation concern. Drafts require Diana approval before sending. Returned envelope to 04_transaction_coordinator for communication tracking.
```

---

## Step 8: Transaction Coordinator Logs Communication Status

`04_transaction_coordinator` receives the envelope back.

It tracks whether Diana approved and sent the message.

### Communication Watch

```md
Client message drafted:
Yes

Human approved:
Unknown

Message sent by human:
Unknown

Sent date/time:
Unknown
```

### Desk Trail

```md
[04-TC] 2026-05-12 — Received communication drafts from 03_client_communication. Communication status not yet confirmed sent. Tracking approval/sent status before marking communication complete.
```

---

## Final Case Lesson

The Tarrytown Tangle shows the system working correctly:

- the same-day urgency was captured and produced a fast acknowledgment draft, not a showing confirmation
- the buyer-representation issue did not get ignored — BLUE slip named the verification destination (TREC) and the compliance reason (TREC Buyer Rep / IABS / NAR-settlement, as applicable)
- the buyer's preapproval claim and budget were captured but flagged unverified
- property-specific research was **not** performed while the property identifier was Unknown — `02_property_research` returned the envelope and provided only general background
- once the identifier was normalized, property research resumed with parcel-specific BLUE slips pointing at AUSTIN_RESOURCES.md destinations
- the inspection issue triggered a return-trip
- client and listing-agent messages were drafted but not sent by AI
- the Desk Trail preserved the story of the case

That is The Austin Deal Desk working as intended.
