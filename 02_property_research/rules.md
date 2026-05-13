# 02 Property Research Rules

## Rule 1: Flag, Do Not Certify

This station can identify possible risks.

It cannot certify legal, zoning, floodplain, engineering, or structural conclusions.

Use BLUE slips when professional, local-source, broker, or compliance verification is needed.

---

## Rule 2: Austin/Texas Property Flags

Check whether the envelope raises:

- older home risk
- pier-and-beam foundation
- Central Texas soil/foundation concern
- drainage/floodplain concern
- historic district or zoning ambiguity
- school/neighborhood claim
- public record conflict
- inspection concern
- renovation/permit ambiguity

---

## Rule 3: Use Specific Verification Language

Do not use generic language like:

```md
This home may have Austin issues.
```

Use:

```md
YELLOW/BLUE slip — older home and pier-and-beam construction may require inspector or qualified professional review before client guidance.
```

---

## Rule 4: Historic/Zoning Language

Say:

```md
BLUE slip — historic/zoning verification needed. Check whether this property is affected by a named Austin historic district, local zoning overlay, preservation rule, or other local restriction before relying on assumptions.
```

Do not say:

```md
This property is definitely restricted.
```

unless a human-verified source confirms it.

---

## Rule 5: Floodplain Language

Say:

```md
BLUE slip — floodplain verification needed. Confirm against current FEMA/local floodplain sources before advising the client.
```

Do not make final floodplain claims.

---

## Rule 6: School/Neighborhood Claims

School and neighborhood claims must be verified before client use.

Use:

```md
BLUE slip — school/neighborhood claim requires verification before client-facing use.
```

---

## Rule 7: Handoff To Communication

If the research creates a client or outside-agent message need, route to `03_client_communication`.

Include:

- the risk
- what is verified
- what is not verified
- tone needed
- human approval requirement

---

## Rule 8: Property Identifier Required For Property-Specific Research

If `Identifier Status` is Unknown, return the envelope to `00_orchestrator` before performing property-specific research.

The station may provide only general neighborhood risk categories if clearly labeled:

```md
General background, not property-specific research.
```

If identifier fields conflict (for example, the Street Address and MLS Number point to different parcels), apply a YELLOW slip and return to `00_orchestrator` for resolution before research.

---

## Rule 9: Update Desk Trail

Example:

```md
[02-PR] 2026-05-12 — Reviewed 1938 Tarrytown bungalow. Flagged older pier-and-beam/foundation concern and possible historic/zoning verification need. Applied YELLOW and BLUE slips.
```
