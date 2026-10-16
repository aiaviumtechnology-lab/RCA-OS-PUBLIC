---
document_id: RCA-PUB-004
title: The Board of Directors — Constitution, Composition, and Ratification Authority
document_class: CONSTITUTIONAL_CHARTER
charter_id: EXEC-BOARD
version: 1.0.0
status: DRAFT
authority_basis:
  - "AM-XIX §3 — Board Authority (constitutional ratification and oversight authority)"
  - "AM-XIX §1 — Absolute Constitutional Supremacy"
  - "Invariant F-3 — the Board is the constitutional ratification and oversight authority"
  - "Invariant F-6 — constitutional amendments require Founder signature and Board ratification"
  - "AM-XXI §1 — Executive Directorate, the executive control layer"
  - "AM-XXII §1 — CEO office, subordinate to the Constitution and under Founder authority and Board oversight"
  - "Struct §2 — Executive Authority: Founder, Board of Directors, Executive Agents"
  - "Register §4 — Ratification Evidence Rule"
placement: "Executive layer — above the Directorates, subordinate to the Constitution"
precedence_rank: 2
binds: EXECUTIVE
mandatory: true
enforceable: false
invariants:
  - BD-1
  - BD-2
  - BD-3
  - BD-4
  - BD-5
  - BD-6
  - BD-7
  - BD-8
  - BD-9
  - BD-10
  - BD-11
  - BD-12
cross_references:
  articles: [III, VII, IX]
  amendments: [AM-XIX, AM-XX, AM-XXI, AM-XXII]
  reserve: [AM-XIII, AM-XIV, AM-XV, AM-XVI]
  rules: [CONST-FC-3, CONST-FC-4, CONST-CEO-1]
compiled_rules: []
source_path: "The founder"
source_digest: "sha256:adf88b0ff647658250839dd37c1b5f3677212fb5d46b8409d817d32a288fcb7a"
published_digest: "sha256:SELF_REFERENTIAL"
supersedes: []
superseded_by: null
ratification:
  evidence: NOT_REQUIRED_FOR_A_CHARTER_SELF
  ledger_ref: null
contradictions: [C1, C2, C9, C11]
trust: UNVERIFIED
editing_policy: RESTRUCTURED
publication_class: PUBLIC
copyright: "© 2025–2026 Aether Core Dynamics / AI.Avium Technology. All rights reserved."
date_of_issue: 2026-10-16
legacy_header:
  note: "No prior header. Composed from AM-XIX §3, AM-XXI, AM-XXII, STRUCTURE §2, the live Volume VI, and The founder."
---

# The Board of Directors

> **CHARTER · DRAFT · Executive layer · UNVERIFIED · RESTRUCTURED**

> **This charter is a draft.** It composes the Board's authority from instruments that already
> exist (`AM-XIX §3` creates it; `F-3` states it; `F-6` requires it) and makes it operative. It
> creates no new constitutional power. It carries four open contradictions, including the two
> the Board's own first meeting is supposed to close.

---

## 1. Jurisdiction

### 1.1 What the Board is

The **Board of Directors** is the constitutional **ratification and oversight authority** of
RCA-OS. It is not a management body, not an operational body, and not an executive body. Its
function is to **authorise** what others do, and to **review** what they did.

`AM-XIX §3` creates the office. `Invariant F-3` states it. `Invariant F-6` makes its ratification
a condition of constitutional change. `STRUCTURE OF THE CONSTITUTION §2` lists it as one of the
three executive authorities.

### 1.2 What the Board grants

- **Ratification** of proposed constitutional amendments (`AM-XIX §3`).
- **Ratification** of constitutional appointments, structures, and system-level authorities where
  the Constitution requires it (`AM-XIX §3`).
- **Approval** of new Directorates, Spines and Pillars, where their creation changes constitutional
  structure.
- **Fiduciary authority** — approval of annual budgets and capital expenditure
  (`Volume VI §1.8`, to be confirmed — see C9).
- **Oversight review** of Founder directives and emergency interventions (`AM-XIX §3`).
- **The power to require audits, corrective action, or recovery review** (`AM-XIX §3`).

### 1.3 What the Board does not grant — exclusions

- **Cannot override constitutional law** (`Volume VI §1.8`, consistent with `AM-XIX §1`).
- **Cannot make operational decisions** — those are Executive authority.
- **Cannot grant technical clearances** — those are Governance/CGO authority.
- **Cannot act outside the Constitution**, and Board authority *"cannot authorize an action that
  conflicts with the Constitution"* (`AM-XIX §3`, closing sentence).
- **Cannot amend the Constitution independently of the Founder** — `F-6` requires both.
- **Cannot erase audit lineage, conceal an action, or authorise prohibited harm.**

### 1.4 Overlaps, stated as rules

| Adjacent authority | Boundary |
|---|---|
| **Founder** | The Founder proposes, signs and submits; the Board ratifies, rejects, returns or requires revision. Neither is sufficient alone (`F-6`). |
| **Executive Directorate** | The Executive Directorate initiates appointments and structures; the Board ratifies them where the Constitution requires ratification. |
| **CEO** | The CEO reports to the Founder *and* to the Board (`AM-XXII §2`). The Board may require reports; it may not direct operations. |
| **Governance** | Governance validates constitutional compatibility; the Board ratifies. Validation is a technical finding, ratification is an authority act. **They may not be the same party** (`C14` separation, closed 2026-10-16). |

**Invariant BD-1 — Separation of validation from ratification.**
The party that validates constitutional compatibility is never the party that ratifies. A
ratification without an independent compatibility finding is void.

---

## 2. Constitutional basis

```
AM-XIX §3      creates the Board, enumerates its powers, and bounds them
Invariant F-3  states what the Board is
Invariant F-6  makes Board ratification a condition of constitutional change
STRUCTURE §2   lists Founder, Board and Executive Agents as the executive authorities
AM-XXI §1      places the Executive Directorate as the executive control layer
AM-XXII §1     places the CEO under Founder authority and Board oversight
Register §4    defines the evidence a ratification requires
```

**Invariant BD-2 — No authority without a basis.**
Every Board act must cite the constitutional provision that authorises it. An act that cannot
cite one is void, regardless of who performed it or how many members agreed.

---

## 3. Composition

### 3.1 The Board's relation to the Executive Directorate

The **Executive Directorate** is the executive control layer (`AM-XXI §1`). The **Board** sits
above it in oversight and below the Constitution in authority. The Board is therefore *not* a
Directorate and must not be built as one — see C9 for the counter-reading currently in the corpus.

### 3.2 Seat structure

| Seat class | Who | Authority at Inception | Authority at Formation |
|---|---|---|---|
| **Founder seat** | Samuel Stevenson | Sole seat; sole ratifying member | Retained |
| **Executive seats** | CEO, CFO, General Counsel, Chief Human Officer, Chief Governance Officer | **Not created** — the Directorate they belong to is Layer 4 | Created with Layer 4 |
| **Independent seats** | Reserved | **Not created** | Created only on a Founder appointment with Board ratification |

### 3.3 The Inception / Formation transition

Per the Founder's definition (`The founder`):

> *"The founder has supreme power in the forming of the corporation's structure... but their
> official role, power, changes once the company is legally formed and the exec board is
> confirmed."*

This charter records that transition as a **constitutional state change**, not a change of person:

| | **State INCEPTION** | **State FORMATION** |
|---|---|---|
| Trigger | structure is being built (Layers 1–4 incomplete) | Articles of Incorporation filed for **ai.aviumtechnology Inc.** and the Executive Board confirmed |
| Board composition | Founder, sole member | Founder + Executive seats + any Independent seats |
| Ratification | Founder alone (`RCA-RAT-001` Form B) | Board quorum, with the Founder as a member and not the whole |
| Founder authority | supreme in forming the structure | constitutional office — still supreme among human authorities (`F-2`), but exercised through the Board for constitutional change |
| Pending acts | carry `BOARD_REVIEW_DEBT` | debt cleared by Board review |

**Invariant BD-3 — The transition is a state change, recorded once.**
The move from INCEPTION to FORMATION is a named, dated, auditable constitutional event. Until it
is recorded, the Board operates in the INCEPTION state and every act it ratifies carries
`BOARD_REVIEW_DEBT`.

**Invariant BD-4 — No power is lost without an instrument.**
No Founder authority described in `AM-XIX §2` or `AM-XXI §2` lapses merely because FORMATION has
occurred. Each is either retained or transferred **explicitly**, by instrument, and the transfer
is recorded. "The company is now formed, so the Founder's role changed" is not a lawful transfer.

---

## 4. Duties and prohibitions

### Must

1. Ratify, reject, return, or require revision of every proposed constitutional amendment
   (`AM-XIX §3`).
2. Review every Founder directive and emergency intervention through the constitutional oversight
   process (`AM-XIX §3`).
3. **Review and close `BOARD_REVIEW_DEBT`** — the acts ratified in the INCEPTION state
   (`RCA-RAT-001`).
4. Approve annual budgets and capital expenditure where it holds fiduciary authority.
5. Conduct an annual compliance review.
6. Record every decision, with its authority basis, in the Audit Spine.
7. Require audits, corrective action, or recovery review where it finds cause.

### Must not

1. Override the Constitution, in any act, for any reason.
2. Make operational decisions.
3. Grant or revoke technical clearances.
4. Ratify an act it has not received with an independent compatibility finding (`BD-1`).
5. Act as a single member outside the INCEPTION state.
6. Conceal an action or suppress an audit record.

### On failure to perform

Where the Board cannot perform a required duty — no quorum, conflicting interest, missing
evidence — the act **fails closed**: it does not pass by default, and the matter escalates to the
Founder with the reason recorded.

**Invariant BD-5 — Silence is not ratification.**
An amendment not ratified is not active. A debt not reviewed is not cleared. Non-action by the
Board never constitutes approval.

---

## 5. Enforcement boundary

| Enforcement point | Behaviour | Triggered by |
|---|---|---|
| `pre_amendment` | **DENY** activation of any amendment lacking a Board ratification record | amendment submission without `ratification.board_ref` |
| `pre_structure_change` | **DENY** creation or alteration of a Directorate, Spine or Pillar lacking Board ratification | Layer 2–4 structural changes |
| `executive_appointment` | **DENY** appointment activation without a ratification record | appointments under `AM-XIX §3` |
| `oversight_review` | **REQUIRE** a recorded disposition for every Founder directive and emergency intervention | `AM-XIX §6` interventions |
| `debt_review` | **BLOCK** debt clearance on any act the Board has not reviewed | `BOARD_REVIEW_DEBT` markers |

**Escalation:** a denial the Board cannot resolve escalates to the Founder; a matter the Founder
cannot resolve escalates to **RRPO-SRE containment** (`AM-XIX §9`).

**Invariant BD-6 — The Board's denial is binding until lawfully reversed.**
A Board rejection or return is not a delay. The instrument is inactive until it is revised and
re-submitted, or the Board's decision is itself reversed through a lawful process.

---

## 6. Interfaces

### Consumes

| From | What |
|---|---|
| **Founder** | proposed amendments, emergency interventions, appointments, structure changes, reports |
| **Governance** | independent constitutional compatibility findings |
| **Audit** | lineage and evidence for each act under review |
| **CEO** | operating performance, material risks, incidents, unresolved conflicts, corrective actions (`AM-XXII §2`) |
| **Integrity / Verification** | signature verification and validation results |

### Exposes

| To | What |
|---|---|
| **Governance** | ratified instruments, with their ratification records |
| **Executive Directorate** | approval or rejection of appointments and structures |
| **Audit** | every decision, with authority basis and disposition |
| **Register** | ratification records, for the amalgamated evidence trail (Register §4) |

### Ledger obligations

Every Board act writes, **before it takes effect**: the act, the authority basis, the members
participating, the compatibility finding relied upon, the disposition, and the timestamp.

**Invariant BD-7 — No act without a record.**
A Board decision that is not recorded has not occurred — including decisions favourable to the
Founder.

**Invariant BD-8 — Every act is attributable.**
Each decision names the members who participated. "The Board decided" without a named majority is
not an attributable act and fails `Invariant F-5`.

---

## 7. Failure and recovery

| Failure | Required response |
|---|---|
| **No quorum** | no act; escalate to Founder; record the failure |
| **Conflict of interest** | the member recuses; the act proceeds without them, or fails if no quorum remains |
| **Ratification without validation** | void the act; reopen the instrument; record the breach (`BD-1`) |
| **Ratification of an unconstitutional act** | void on detection; Governance and RRPO-SRE notified (`AM-XIX §1`) |
| **Unauthorised single-member act** | void where the state is FORMATION; re-run with quorum |
| **Failure to review debt** | debt persists; every dependent instrument remains review-pending |
| **Board deadlock** | escalate to Founder; if the Founder is a party, escalate to RRPO-SRE containment |
| **Founder and Board in direct conflict** | the Constitution controls; the disputed act is suspended pending constitutional review |

**Invariant BD-9 — Void acts leave no shadow.**
An act voided under this section must be unwound, not merely marked. Any instrument, appointment
or structure activated by it is suspended until lawfully re-ratified.

---

## 8. Ratification mechanics

For a **Record** (a ratification of an act):

```
record_id:        RCA-RAT-NNN
instrument:       <document id and version>
authority_basis:  <the constitutional provision>
validation:       <independent compatibility finding, by a party other than the ratifier>
members:          <named participating members>
disposition:      RATIFIED | REJECTED | RETURNED | REVISION_REQUIRED
conditions:       <any conditions attached>
timestamp:        <UTC>
signatures:       <per member>
```

For a **Resolution** (a Board decision that is not a ratification):

```
resolution_id:    BR-NNN
subject:          <what is decided>
authority_basis:  <the constitutional provision>
members:          <named participating members>
disposition:      ADOPTED | NOT_ADOPTED | DEFERRED
effects:          <what changes as a result>
timestamp:        <UTC>
```

**Invariant BD-10 — Four dispositions, no fifth.**
Every instrument put to the Board receives exactly one of: **RATIFIED**, **REJECTED**,
**RETURNED**, **REVISION_REQUIRED**. "Noted", "accepted in principle", "approved subject to" are
not dispositions and are void (`AM-XIX §3` names exactly four).

**Invariant BD-11 — Conditions are recorded or they do not exist.**
A ratification with an unrecorded condition is an unconditional ratification. Conditions live in
the record, never in a conversation.

**Invariant BD-12 — Rollback is defined before adoption.**
Every ratified instrument states its rollback: what it supersedes and how it is reversed.

---

## 9. What the Board governs, and what it does not

| Subject | Board role |
|---|---|
| Constitutional amendments | **Ratify** (`F-6`) |
| Structures — Directorates, Spines, Pillars | **Ratify** (`AM-XIX §3`) |
| Executive appointments | **Ratify** (`AM-XIX §3`) |
| Founder emergency interventions | **Review** (`AM-XIX §3`, §6) |
| Annual budget and capital expenditure | **Approve** where fiduciary authority applies (C9) |
| Directorates' operations | **None** — Executive authority |
| Agent registration and clearances | **None** — Governance/Identity authority |
| Technical architecture | **None** — Executive/CTO authority |
| Day-to-day task routing | **None** — Supervisor/Execution authority |

**The Board's product is authorisation, not activity.** Where it starts making operational
decisions it has ceased to be the check it exists to be.

---

## 10. The Board's first three acts

The Board's constitution is not complete until it has performed these, in order. They are
recorded here so that the first Board does not have to invent its own mandate.

1. **Close the Inception Debt.** Review `RCA-RAT-001` (sole-member ratification, 2026-10-16) and
   either ratify it — clearing `BOARD_REVIEW_DEBT` on every instrument activated under it — or
   reverse it, which reopens the eleven closed contradictions and re-plans the build order.
2. **Adopt this charter.** The Board ratifies its own constitution, which is the first structure
   it ratifies and the precedent for how it ratifies.
3. **Close the reserved contradictions.** Decide **C2** (what the Safety Spine is), **C8** (are
   Data / Enforcement / Memory spines) and **C9** (the directorate model) — the three that block
   completion of Layers 2, 3 and 4. This is the Board's first substantive constitutional act, and
   it is the act that lets the rest of the framework be built.

---

## Invariants stated in this section

| ID | Statement |
|---|---|
| **BD-1** | Separation of validation from ratification — the validator is never the ratifier. |
| **BD-2** | No authority without a basis — every Board act cites its constitutional provision. |
| **BD-3** | The INCEPTION→FORMATION transition is a named, dated, auditable state change. |
| **BD-4** | No Founder power lapses without an explicit instrument of transfer. |
| **BD-5** | Silence is not ratification; non-action never constitutes approval. |
| **BD-6** | A Board denial is binding until lawfully reversed. |
| **BD-7** | No act without a record — an unrecorded decision has not occurred. |
| **BD-8** | Every act is attributable — no anonymous Board decisions. |
| **BD-9** | Void acts leave no shadow — they are unwound, not merely marked. |
| **BD-10** | Four dispositions, no fifth — RATIFIED / REJECTED / RETURNED / REVISION_REQUIRED. |
| **BD-11** | Conditions are recorded or they do not exist. |
| **BD-12** | Rollback is defined before adoption. |

These twelve invariants are **draft**. They are not registered in the canonical Constitution or in
`RULES.yaml`. Registering them is a Board act under `AM-XIX §3`.

**And the honest note:** `Invariant F-3` — the invariant that establishes this body — currently has
**no compiled rule and no enforcement point** (`RCA-FIX-002`). This charter gives it a document; it
does not yet give it an enforcer. See §11.

---

## 11. Open items

| # | Item | Note |
|---|---|---|
| **AMB-A** | **`AM-XIII`–`AM-XVI` are reserved.** The register reserves four amendment numbers and records no text. Whether the Board's charter is an *amendment* or a *ratified structure* determines whether it needs `F-6` ratification or `AM-XIX §3` ratification. This charter assumes the latter. | Founder decision |
| **AMB-B** | **`F-3` has no compiled rule.** The Board exists by invariant and by this charter, but nothing denies an act that bypasses it. `CONST-BD-*` rules are needed. | Layer 5 (Policy/Regulation) work |
| **AMB-C** | **Corporate/OS boundary.** The corpus does not state whether `ai.aviumtechnology Inc.`'s corporate board and the RCA-OS constitutional Board are the same body. This charter assumes **same members, two distinct capacities**, with the OS Board constrained by the Constitution and the corporate board by applicable corporate law. | Founder decision |
| **AMB-D** | **Quorum, terms and removal.** Not specified anywhere. Proposed: quorum = simple majority of seated members including the Founder; terms and removal follow corporate law for the corporate capacity. | Founder/Board decision |
| **AMB-E** | **Independent seats.** Undefined. Not created here. | Founder appointment + Board ratification |

## Contradictions carried

- **C1** — ACT clearance tiers. `Volume VI` gives the CEO "G1 (Executive)" clearance; the closed
  determination (`RCA-DEC-001`) fixes **three tiers G1/G2/G3** and holds that "full system access"
  is Founder authority, not a clearance. Board members' clearance class is unresolved.
- **C2** — what the Safety Spine is. The Board's safety oversight routes through an enforcement
  layer whose definition is still open.
- **C9** — directorate model. This charter places the Board **above** the Directorates as an
  oversight layer, which is one reading of the 14/7 conflict; the alternative (Board *as* the
  Executive Directorate) is not adopted here.
- **C11** — HallCo/HALLCO. Unresolved; no bearing on this charter, carried for completeness.

## Verification

```
sha256sum "The founder"
sha256sum "Constitution/PUBLICATION/4_EXECUTIVE-BOARD/BOARD-CHARTER.md"
```

Digests recorded in `P0_META/DIGESTS.txt`.

---

**Publication control notice.** Draft charter. It composes existing authority into an operative
body and creates no new constitutional power. It carries a published digest and four open
contradictions, and it requires Board adoption (§10 act 2) before it is the Board's constitution
rather than a proposal for one.
