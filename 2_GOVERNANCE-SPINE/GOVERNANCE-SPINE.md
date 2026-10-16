---
document_id: RCA-PUB-002
title: Governance Spine
document_class: SPINE
spine_id: SPINE-GOVERNANCE
version: 1.0.0
status: DRAFT
authority_basis:
  - "Article III — Governance Authority and Enforcement Kernel"
  - "Article IX §9.2 — Hierarchy of Norms"
  - "Article XII — Spine Lattice Doctrine (Spine classification)"
  - "AM-XIX §4 — Authority Hierarchy"
  - "CONSTITUTIONAL REGISTER.md §1 (precedence), §5 (spine classification)"
placement: "rank 4 — Governance Spine specification (below the Constitution and ratified amendments; above policies, regulations, directives, configuration, and code)"
precedence_rank: 4
binds: ALL
mandatory: true
enforceable: false
invariants:
  - GS-1
  - GS-2
  - GS-3
  - GS-4
  - GS-5
  - GS-6
  - GS-7
  - GS-8
cross_references:
  articles: [III, IX, X, XI, XII, XIII, XIV]
  amendments: [AM-XIX, AM-XX, AM-XXI, AM-XXII]
  spines: [SPINE-UVS, SPINE-HALLCO, SPINE-DEEPGUARD, SPINE-RRPO-SRE, SPINE-REASONING, SPINE-EXECUTION, SPINE-AUDIT, SPINE-IDENTITY, SPINE-ARBITRATION, SPINE-VERIFICATION]
  pillars: [PILLAR-EXECUTION, PILLAR-SAFETY, PILLAR-AUDIT, PILLAR-IDENTITY, PILLAR-TEMPORAL, PILLAR-EVENT, PILLAR-WORLD-STATE]
compiled_rules:
  - CONST-HIER-1
  - CONST-HIER-2
  - CONST-HIER-3
  - CONST-G-1
  - CONST-G-2
  - CONST-FC-1
source_path: "Constitution/Governance and produce the fully formal constitutional document using the new metadata header you requested.docx.txt"
source_digest: "sha256:a90b1dca2ef437fb02ecc1b13c7c3fe3af838a32e06d412326f452be7f4ec40c"
published_digest: "sha256:SELF_REFERENTIAL"
supersedes: []
superseded_by: null
ratification:
  evidence: NOT_REQUIRED
  ledger_ref: null
contradictions: [C2, C7]
trust: UNVERIFIED
editing_policy: RESTRUCTURED
publication_class: PUBLIC
copyright: "© 2025–2026 Aether Core Dynamics / AI.Avium Technology. All rights reserved."
date_of_issue: 2026-10-16
legacy_header:
  Document Title: Governance Spine
  Document Class: Constitutional Spine
  Version: "1.0"
  Date of Issue: "July 31, 2026"
  Copyright: "© 2025–2026 Aether-Core Dynamics"
  Author: "Samuel Stevenson, Founder & Chief Architect"
  Document Status: Active
  Constitutional Binding: "Mandatory under Article XII — Spine Lattice"
---

# Governance Spine

> **SPINE · DRAFT · rank 4 (subordinate specification) · UNVERIFIED · RESTRUCTURED**

> **This document is a draft.** It is a restructured presentation of a source draft, not
> ratified constitutional text. It creates no authority, amends nothing, and enforces nothing.
> Two open contradictions are carried unmodified: **C2** (what the Safety Spine is) and
> **C7** (Volume vs Article namespace). See `P0_META/CONTRADICTIONS.md`.

---

## Status notice — read before citing

1. **Restructured, not transcribed.** The source is a 421-word run-on block with no headings,
   no sections and no rule identities. Making it "make sense" required inventing structure,
   scope boundaries, and eight invariant identities. Those are drafting acts, marked
   `editing_policy: RESTRUCTURED`, and they need the Founder's sign-off before this leaves
   `DRAFT`. The original wording is preserved in `legacy_header` and quoted where it carries
   meaning.
2. **Nothing here is enforced.** `enforceable: false`. The compiled rule set records
   governance constraints (`CONST-HIER-1/2/3`, `CONST-G-1/2`, `CONST-FC-1`) as `enforce: true`
   in `RULES.yaml`, but this Spine document is not itself an enforcement mechanism, and the
   policy engine it would drive is only partially implemented.
3. **Its own authority is derived, not sovereign.** Article III creates the Governance Kernel;
   Article IX §9.2 places this Spine *between* the Constitution and policy. A spine
   specification cannot create authority its superior does not grant (`CONST-HIER-1`).
4. **The source's own voice is absolute where it should be bounded.** It says "No agent, tool,
   or directorate may bypass governance" and "Governance is immutable in its authority". The
   first is consistent with Article IX; the second is not — governance authority is
   *subordinate* to the Constitution, and only its derivation is immutable. §1 and §8 below
   correct that framing explicitly rather than quietly.

---

## 1. Constitutional authority

### 1.1 What the Governance Spine is

The Governance Spine is the **constitutional interpretation and enforcement spine** of RCA-OS.
It is the mechanism by which the Constitution's will becomes a decision that binds an agent,
a Directorate, a tool or a subsystem.

It occupies the layer between supreme law and ordinary policy:

```
Constitution → Governance Spine → Policies → Regulations → Directives → Configurations → Code
```

### 1.2 What it is not

- It is **not** the Constitution, and it is not a second source of law. Where this document and
  the canonical Constitution conflict, **the Constitution controls and this document is void to
  the extent of the conflict** (`CONST-HIER-2`, `CONST-HIER-3`, Register §1).
- It is **not** a policy, a regulation, or a directive. Those are outputs of governance, not
  governance itself.
- It is **not** sovereign over the Founder, the Board, or any Article. It interprets and
  enforces; it does not legislate.
- It cannot create, amend, suspend or repeal constitutional text. Only the amendment process
  in the canonical Constitution and the Register can do that.

### 1.3 Authority chain

The Governance Spine derives its authority from Article III (Governance Authority and
Enforcement Kernel), Article IX (Sovereign Governance and Constitutional Supremacy), the
Spine Lattice doctrine of Article XII, and the authority hierarchy recorded in AM-XIX §4.
It has no authority that does not trace to one of them.

**Invariant GS-1 — Derived authority.**
The Governance Spine possesses no authority that does not derive from the Constitution.
Any governance decision, routing rule, clearance binding or precedence ruling that cannot be
traced to a constitutional provision is void and must fail closed.

---

## 2. Constitutional purpose

The Governance Spine exists to guarantee six properties:

1. **Constitutional interpretation** — that the meaning of constitutional text is resolved
   deterministically and on the record, never privately or implicitly.
2. **Precedence resolution** — that when two instruments conflict, the winner is determined by
   the Register's precedence order and nothing else.
3. **Binding** — that every policy, regulation, directive and task is bound to a named
   authority, a clearance, a scope and a duration.
4. **Compliance oversight** — that constitutional compliance is continuously evaluated rather
   than assumed.
5. **Provenance** — that every governance decision carries its interpretive basis and lineage.
6. **Determinism** — that the same question, put to the same governance state, yields the same
   answer.

**Invariant GS-2 — Determinism.**
Given identical constitutional text, identical active amendments, and identical inputs, the
Governance Spine must reach an identical decision. A non-deterministic governance decision is
a constitutional defect, not a judgement call.

---

## 3. Components

The source names five components without defining them. Defined here:

| Component | Function | Fails closed by |
|---|---|---|
| **Governance Kernel** | The constitutional core that evaluates policies, directives and invariants against the Constitution and produces binding decisions. Article III §3.1. | Refusing to issue a decision it cannot ground |
| **Precedence Engine** | Applies the Register's precedence order (rank 1–6) to resolve conflicts between instruments. | Declaring the conflict rather than merging texts |
| **Interpretation Engine** | Determines what constitutional text means when applied to a situation not explicitly addressed. Bounded by §7. | Escalating to Founder/Board rather than inferring |
| **Routing Matrix** | Determines which authority, Directorate or agent receives a governance decision, and along which authorised path. | Halting an unauthorised route |
| **Clearance Authority** | Binds decisions to identities and clearance levels; validates that the acting identity may receive and act on the decision. | Denying on any clearance mismatch |

**Invariant GS-3 — Single governance path.**
There is exactly one Governance Kernel. A second, parallel or shadow governance path — however
implemented, and including any prompt, profile or configuration that resolves constitutional
meaning independently — is unconstitutional. See `CONST-HIER-2`.

---

## 4. Responsibilities

The Governance Spine **must**:

1. Interpret constitutional text deterministically and record the interpretive basis.
2. Resolve conflicts by the Register's precedence order, and record the losing instrument.
3. Route governance decisions only along authorised paths (Routing Matrix).
4. Bind every policy and directive to a clearance level and a responsible identity.
5. Validate constitutional compliance before a decision takes effect.
6. Enforce the invariants in §8.
7. Maintain governance provenance per §6.

The Governance Spine **must not**:

1. Merge conflicting texts silently in order to produce a decision.
2. Issue a decision whose authority basis it cannot cite.
3. Grant a clearance, capability or exception on its own motion.
4. Resolve a contradiction that the Register records as open.
5. Accept a lower-level artifact's claim of supremacy.

---

## 5. Mutation rules

Governance decisions and governance machinery mutate under different rules; the source draft
conflates them. Separated:

### 5.1 Decision mutation (routine)

Every governance decision must be deterministic, auditable, reversible where technically
possible, provenance-bound, and arbitration-compatible. A decision that cannot be reversed must
say so and state its compensating action.

### 5.2 Machinery mutation (governed)

Changing the Governance Kernel, the Precedence Engine, the Interpretation Engine, the Routing
Matrix, or the Clearance Authority is a **governance-layer mutation** and requires all of:

- a constitutional basis that authorises the change;
- an amendment or an explicitly authorised consolidation decision where constitutional meaning
  would change;
- audit lineage for the change itself;
- arbitration compatibility review;
- signature provenance from the responsible authority.

### 5.3 Constitutional text mutation (prohibited here)

The Governance Spine **cannot** mutate constitutional text. Per AM-XIX §8, no component may
amend the Constitution by configuration, code, learned behaviour, policy, regulation or model
output. Governance mutation of the machinery is permitted; governance mutation of the
Constitution is not.

**Invariant GS-4 — No self-authorisation.**
The Governance Spine may not grant itself authority, clearance, or an exception, and may not
ratify its own decisions. Its decisions become effective only against a constitutional basis
that exists independently of them.

---

## 6. Provenance

Every governance event must be logged in the Audit Spine with sufficient detail to reconstruct
the decision. A governance event without provenance is not a lawful governance event.

Required provenance fields:

- **interpretive basis** — the constitutional provision relied upon;
- **precedence chain** — the instruments compared, and the rank applied;
- **routing lineage** — who received the decision, along which authorised path;
- **clearance lineage** — the identity and clearance that acted and that received;
- **decision ancestry** — the governance state the decision was made against.

**Invariant GS-5 — Provenance is mandatory.**
No governance decision takes effect before its provenance record is written. Where the audit
store is unavailable, governance halts rather than proceeding unlogged (`CONST-AU-1`).

---

## 7. Interpretation — scope and limits

Interpretation is where a governance spine can silently become a legislature. The limits:

1. **Text first.** Interpretation begins from the canonical text and the Register; it never
   begins from a preferred outcome.
2. **Narrowest reading.** Where text admits several readings, the narrower reading controls,
   unless a broader reading is required to satisfy a constitutional invariant.
3. **No new authority.** Interpretation may clarify what a provision means; it may not create a
   permission, a prohibition, a Directorate, a clearance or an exemption that the provision
   does not contain.
4. **Open contradictions stay open.** Where the Register records an open contradiction (see
   `P0_META/CONTRADICTIONS.md`), interpretation **must not** pick a winner. It records that the
   question is unresolved and escalates.
5. **Escalation over inference.** Where the constitutional basis is genuinely absent, the
   correct output is escalation to the Founder, the Board, or RRPO-SRE by severity — not a
   reasoned guess.
6. **Every interpretive ruling is itself a governed object.** It carries an ID, a basis, a
   scope, a validity window and an audit record, and it can be superseded by a later ruling.

**Invariant GS-6 — Interpretation cannot legislate.**
No interpretive ruling may have the effect of creating, amending or repealing constitutional
authority. A ruling that would do so is void and must be escalated as a proposed amendment.

---

## 8. Enforcement

The Governance Spine is enforced by the spines it binds, not by itself:

| Enforcer | Role |
|---|---|
| **Enforcement / Execution Spine** | Applies the governance decision to the execution path; refuses unauthorised execution. |
| **Verification Spine (UVS)** | Verifies that the decision, and the operation carrying it, are constitutionally valid. |
| **Arbitration Spine** | Resolves disputes over the meaning or application of a governance decision. |
| **Safety Spine** | Containment and escalation where a governance decision is itself a risk. |
| **Identity Spine** | Signature and clearance validation; establishes that the acting identity may act. |
| **Audit Spine** | Records the decision, its provenance, and its outcome. |

Governance decisions must be constitutional, lawful, deterministic, auditable and reversible.

**Invariant GS-7 — No bypass.**
No agent, tool, Directorate, spine, provider, subsystem or autonomous process may bypass a
governance decision, route around it, or act in its absence. Absence of a governance decision
is **not** permission to act; it is a condition that fails closed (`CONST-F-4`).

---

## 9. Failure modes

| Failure | Description | Required response |
|---|---|---|
| Unconstitutional interpretation | A ruling whose effect exceeds or contradicts the Constitution | Void the ruling; escalate as a proposed amendment |
| Precedence violation | A lower-ranked instrument applied over a higher-ranked one | Void the outcome; re-resolve by rank; record |
| Routing failure | A decision delivered along an unauthorised path, or not delivered | Halt the affected operation; re-route or escalate |
| Clearance mismatch | An identity acting above, or receiving beyond, its clearance | Deny; record; notify Governance and Identity |
| Rogue directive | A directive with no traceable authority basis | Quarantine; treat as null and void on detection |
| Governance bypass | Any component acting without or around governance | Containment; RRPO-SRE engagement; record |
| Silent text merge | A conflict "resolved" by blending instruments | Void; reopen the conflict in the Register |

Every governance failure must trigger arbitration, re-attestation, audit-lineage correction, or
a governance kernel reset — in that order of escalation, and never a silent continuation.

**Invariant GS-8 — Fail closed, always.**
Where constitutional validity cannot be established, governance denies and escalates. It never
proceeds on the assumption that silence, missing policy, or model output constitutes permission.

---

## 10. Recovery

Recovery returns the Governance Spine to a deterministic constitutional state through:

1. governance re-validation against the canonical text and the Register;
2. directive re-attestation (each directive re-proven against its authority basis);
3. clearance correction where a binding was wrong;
4. routing matrix recalibration;
5. provenance reconstruction from the Audit Spine;
6. audit spine reconciliation.

Recovery is a governed operation: it is TCO-bound, recorded, and subject to revalidation before
the Spine is declared fit to issue decisions again. Where recovery cannot establish a
deterministic state, the Spine remains in a contained posture and the matter escalates to the
Founder and Board rather than resuming.

---

## 11. Placement — what this Spine binds into

The source draft lists nine "Volumes". Those numbers do not match the canonical namespace
(see **C7**), so they are recorded here as **subject areas**, not as volume citations:

| Source label | Subject area | Canonical position |
|---|---|---|
| Volume I — Sovereignty | Constitutional Intent, Articles I–III, IX | canonical Constitution |
| Volume II — Agent Constitution | Article VII | canonical Constitution |
| Volume III — Tool Constitution | no canonical Article; TCO Contract Layer (AM-XX) | amendment |
| Volume IV — World-State Constitution | Article VI, World-State Spine | Article + spine spec |
| Volume V — Enforcement Protocols | UVS / Big-5 (Article X) | canonical Constitution |
| Volume VI — Arbitration Procedures | Arbitration Spine | spine spec (no Article) |
| Volume VII — Memory Constitution | Memory subsystem spec | **unregistered draft** |
| Volume VIII — Execution Constitution | Execution Spine | spine spec |
| Volume IX — Data Constitution | Storage/State (Article VI) | Article |

**Governance is the vertical layer that connects all of the above** — it is the one spine that
every other spine, pillar, Directorate and agent must consult, and the one that may not be
consulted in place of the Constitution.

---

## Invariants stated in this section

| ID | Statement |
|---|---|
| **GS-1** | Derived authority — no governance authority that does not trace to the Constitution. |
| **GS-2** | Determinism — same state, same question, same decision. |
| **GS-3** | Single governance path — one Kernel; no shadow governance. |
| **GS-4** | No self-authorisation — governance cannot grant itself authority or ratify its own acts. |
| **GS-5** | Provenance mandatory — no decision takes effect before its record is written. |
| **GS-6** | Interpretation cannot legislate — a ruling that creates authority is void. |
| **GS-7** | No bypass — absence of a decision is not permission. |
| **GS-8** | Fail closed — unestablished validity denies and escalates. |

These eight invariants are **draft** and are not registered in the canonical Constitution or in
`RULES.yaml`. Registering them is a Founder decision.

---

## Cross-references

- **Articles:** III (Governance Kernel), IX (supremacy, hierarchy of norms), X (UVS), XI (HALLCO),
  XII (DEEPGUARD, Spine Lattice), XIII (RRPO-SRE), XIV (Reasoning Engine).
- **Amendments:** AM-XIX (supremacy, Founder, Board), AM-XX (Contract Layer / TCO),
  AM-XXI (Executive Directorate, Founder command), AM-XXII (CEO).
- **Compiled rules:** `CONST-HIER-1`, `CONST-HIER-2`, `CONST-HIER-3`, `CONST-G-1`, `CONST-G-2`,
  `CONST-FC-1`.
- **Registered spine:** `SPINE-GOVERNANCE` in `SPINE_TRACEABILITY.yaml` (classification
  `canonical_named_concept`, `source: null`, `activation: design_baseline_only`).

## Contradictions carried

- **C2 — What is the "Safety Spine"?** The source draft's §7 says governance is enforced by a
  "Safety Spine (HALCO + DeepGuard)". The canonical Article X defines a five-stage Universal
  Verification Spine (HALLCO → DEEPGUARD → RRPO-SRE → Global Health Monitor → Reasoning Engine).
  §8 above names enforcers by their registered spine IDs and does **not** adjudicate. **Open.**
- **C7 — Volume vs Article namespace.** The source draft cites Volumes I–IX whose numbers name
  different bodies of law than the live repository's Volume VI (Directorates). §11 records
  subject areas instead of volume numbers. **Open.**

Both must be resolved by the Founder before this document can leave `DRAFT`. They may not be
resolved by editing this document.

## Verification

A file cannot contain its own hash: writing the digest changes it. Verification therefore
uses the digest ledger, not an inline field.

```
sha256sum "Constitution/Governance and produce the fully formal constitutional document using the new metadata header you requested.docx.txt"
sha256sum "Constitution/PUBLICATION/2_GOVERNANCE-SPINE/GOVERNANCE-SPINE.md"
```

- **Source digest:** `a90b1dca2ef437fb02ecc1b13c7c3fe3af838a32e06d412326f452be7f4ec40c`
  (421 words; a single unbroken block with no headings — which is why this section is
  `RESTRUCTURED`.)
- **Published digest:** recorded in `P0_META/DIGESTS.txt` at publication time.
- Verification is re-run before any republication of this section. If either digest has moved,
  the change is a new version, not an edit in place.
