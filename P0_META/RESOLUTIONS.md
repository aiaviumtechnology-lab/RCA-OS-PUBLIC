# CONTRADICTION RESOLUTION REGISTER — PROPOSED DETERMINATIONS

**Document ID:** `RCA-PUB-META-008`
**Document Class:** Publication Control — Proposed Resolutions
**Version:** 1.0.0
**Status:** **PROPOSED — creates no authority until signed**
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`
**Register:** closes or reclassifies every entry in `CONTRADICTIONS.md` (C1–C15)

---

## How to read this document

Fifteen contradictions are open. Three of them (C2, C8, C13) require a decision that only the
Founder can make, because they change what RCA-OS *is*. The other twelve are **errors** — a
document disagreeing with the Register about its own status, a rule asserting an authority that
was never granted, a stale digest. Those can be corrected by applying the precedence rules that
already exist.

Every determination below is labelled:

- **`CORRECTION`** — an error. Applying an existing rule fixes it. Corrected here.
- **`RECLASSIFICATION`** — the artifact keeps its text but moves to its lawful layer.
- **`PROPOSED`** — a Founder decision. Recorded, not taken.

**Nothing here is in force.** These are determinations offered for signature. Where a
determination is `PROPOSED`, the contradiction stays open until the Founder signs.

---

## Part A — Determinations that apply existing authority

### A1. C1 — ACT clearance is three tiers
**Determination: `CORRECTION` — three tiers (G1/G2/G3) controls.**

Applied rule: Register §1 precedence (rank 1 canonical Constitution over rank 6 unregistered
draft). The canonical namespace `STRUCTURE OF THE CONSTITUTION §5` defines G1/G2/G3, and the
**active** amendment `AM-XX §5` uses those three tiers. Document #1 is rank 6 and unregistered.

**Consequences to be applied:**
- The five-tier table in Document #1 §2.7 is marked non-authoritative.
- `CONST-A-3` and every clearance-dependent rule resolve against three tiers.
- **Note:** "G1 Executive — full system access, ethics controls, kill switches" has no canonical
  equivalent. Full system access is not a clearance in the canonical model; it is Founder
  authority under `AM-XIX §2`. This distinction must be enforced, not glossed.

### A2. C4 — Document #1 has no authority
**Determination: `RECLASSIFICATION` — `DOCTRINE`, precedence rank 6.**

Applied rule: Register §1 and §5; `AM-XIX §8` ("no component may amend the Constitution by
configuration, code, learned behavior, policy, regulation, or model output").

Document #1's claims — *"the governing charter"*, *"all subsequent documents (2–∞) must comply
with this governance layer"* — are **struck as claims of authority**. The document's content is
preserved and published as doctrine.

### A3. C5 — The seven principles are policy, not invariants
**Determination: `RECLASSIFICATION` — foundational policy, not constitutional invariants.**

Applied rule: an invariant must be registered with an ID, an owning Article, and an enforcement
point (canonical practice: `I-1`, `E-1`, `UVS-1`…). The seven principles have none.

They are **binding policy** at rank 5. The words "cannot be overridden by any subsystem or
agent" are struck: a policy is overridden by the Constitution, by an amendment, and by a
superior policy. If the Founder wants any of the seven elevated, they must be registered as
invariants with enforcement points.

### A4. C6 — A2A is the transport; the Supervisor is the sole orchestrator
**Determination: `CORRECTION` — both are true; they answer different questions.**

Applied rule: `CONST-HIER-2` (a conflict may not be resolved by silently merging text), so the
two statements are separated by scope rather than blended.

- **Transport:** all agent-to-agent communication uses A2A. No proprietary or framework-specific
  messaging layer, and no unregistered message envelope. (Consistent with `A2A/` and
  `Constitution/a2a-message_protocol.py.txt`.)
- **Orchestration:** the Supervisor Agent is the sole **task orchestration and routing**
  authority. No agent creates work outside it.
- **`_#1` §2.5's "no direct peer-to-peer communication" is corrected** to **"no unregistered
  peer-to-peer *routing*"**. A2A messages between agents are lawful; *work* that is not routed
  through the Supervisor is not.

### A5. C7 — the canonical namespace is Articles I–XV
**Determination: `CORRECTION` — Articles only; "Volume" is descriptive.**

Applied rule: Register §2 (canonical article namespace) and §5 ("the word `Volume` is descriptive
unless the volume is listed in a ratified volume index").

- Published sections cite **Articles**, never volume numbers.
- Existing documents that use volume numbers are **not renumbered** — they keep their text and
  gain a mapping note. Renumbering a corpus that is cited by number would destroy traceability.
- `Vol 1.txt` retains its historical-draft status (Register §2).

### A6. C11 — HallCo and HALLCO are the same entity
**Determination: `PROPOSED` — but evidence strongly indicates one entity.**

Evidence: the canonical Article XI spells the gate **HALLCO** and the canonical text defines it
as *"Hallucination and Legality Compliance"*; the pillar drafts spell it **HallCo**; the UVS
document calls it *"HALLCO — Hallucination & Consistency Office"*.

**Three expansions of one acronym exist.** The Founder decides the expansion; the publication
treats them as one entity until told otherwise. The three candidate expansions are recorded as
an open terminology defect even after C11 closes.

### A7. C12 — there is no Governance Pillar
**Determination: `CORRECTION` — Governance is a Kernel (function), a Spine, and a Directorate.**

Applied rule: the canonical Constitution is the only instrument that can create a Pillar
(Register §2, §5), and it creates none. Article III §3.1 creates a **Governance Kernel** that
*"interprets policies, directives, and invariants"*.

- The phrase "Governance Pillar" in `Governance Directives …` is corrected to
  **"Governance Directorate"** (issuer) acting through the **Governance Spine**, executing the
  **Governance Kernel**.
- `PILLAR_TRACEABILITY.yaml` already registers seven pillars and excludes Governance. **The
  registry was right; the draft was wrong.**

### A8. C14 — the issuer may not sign what it interprets
**Determination: `CORRECTION` — separation of authority is mandatory.**

Applied rule: `AM-XIX §5` (universal subordination, fail-closed), `AM-XXI §4` (a freeze notifies
five authorities, none of them the actor), and `GS-4` (no self-authorisation).

- **Issuer ≠ Validator ≠ Registrar ≠ Auditor.** At least two of the four must sit outside the
  issuing authority.
- The lifecycle's own stage 2 (Validation by the Integrity Spine) is the intended separation and
  becomes mandatory rather than optional.
- **Rank correction:** directives are *binding but derived*, and rank **below policies**
  (Article III §3.2). "Henceforth law" is struck; "binding application of an existing policy" is
  substituted.

### A9. C15 — there is no Master Spine
**Determination: `CORRECTION` — "Master Spine" is a lattice tier, not a spine ID.**

Applied rule: Register §5 and `SPINE_TRACEABILITY.yaml` (15 registered spines; no Master).

- "Master Spine" is read as the **lattice tier name** from
  `Spines/— each spine is a separate constitutional subsystem…`, not as a fifteenth-and-a-half
  spine.
- Its claimed supremacy is struck. Article IX §9.2 makes the **Constitution** supreme; a spine
  cannot be.
- Its claimed function ("registers directive", "authority over all workflows") is **transferred
  to the Governance Spine**, which is already registered — removing the need for a new spine.

### A10. C2 — the Safety Spine is the Big-5 verification pipeline
**Determination: `PROPOSED` — with one problem the Founder must settle.**

The weight of the corpus says the safety function is the **Universal Verification Spine**:
Article X §10.1 defines it as the mandatory pipeline, `UVS/UVS.txt` says *"No subsystem, agent,
or spine may bypass UVS. No output may be returned to the user without UVS approval"*, and
`RULES.yaml` compiles `CONST-BIG5-1/2` with a fixed order.

**But Article X does not name a Safety Spine, and Constitutional Intent §6 refers to one.**
A registered `SPINE-SAFETY` exists with `source: null` and no Article. So the choice is:

- **(a)** Safety Spine = the UVS pipeline. Then `SPINE-SAFETY` is a duplicate of `SPINE-UVS`
  and should be retired, and `SPINE-VERIFICATION` (currently a "secondary reference") becomes a
  duplicate too. **Registry correction only — no amendment required.**
- **(b)** Safety Spine = a distinct spine that the UVS consults. Then it needs its own Article,
  because none exists today. **Requires a constitutional amendment.**

**Recommendation: (a).** No new authority is needed, it matches the code (`rcaos.uvs.*`,
`tests/test_uvs_gates.py`, `tests/constitution/test_big5.py`), and it removes two duplicate
registry entries instead of adding a third.

### A11. C3 — the financial mandate is doctrine
**Determination: `RECLASSIFICATION` — doctrine, precedence rank 6.**

The canonical Constitution contains no revenue target and the Register never admitted one.
The $95B–$500B, 15% growth, 7-stream, 80%-reinvestment figures are **strategic doctrine**, and
they bind executives as objectives, not the system as law.

### A12. C9 — the Directorate model
**Determination: `PROPOSED` — the 14-directorate operational list is the functional model.**

Recorded evidence: `DIRECTORATES.txt` (14) is the only list with routing relationships; `_#1`'s
seven (Prometheus, Code-Weaver, Silicon-Forge, Vox, Aegis, Nexus, Abacus) is an *executive
layer* — and `AM-XXII` already places the CEO office above the directorates.

**Proposed resolution:** the seven are the **Executive layer** (CEO, CFO, Legal, HR, CGO, plus
the Board and Founder), and the fourteen are the **Directorates**. They are two tiers, not two
competing lists. This needs the Founder's signature because it re-reads `_#1` §4.

---

## Part B — Corrections that are pure errors

### B1. Rule provenance: 27 compiled rules cite non-existent canonical invariants
**`CORRECTION`.** `RULES.yaml` compiles 27 rules whose IDs imply canonical invariants that do not
exist in the canonical text: `A-3`, `E-3`, `EVO-1/2`, `EX-1..5`, `HIER-1..3`, `ID-1..4`,
`TCO-1..5`, `UVS-3..6`, `BIG5-1/2`.

Verified by enumeration: the canonical text states exactly **20 invariant sets** —
`I-1/2, E-1/2, G-1/2, N-1/2, R-1/2, S-1/2, A-1/2, AU-1/2, SG-1/2, UVS-1/2, H-1/2, D-1/2,
RRP-1/2, RE-1/2, CL-1/2, RCA-1/2/3, F-1..6, FC-1..6, CEO-1..5`. Anything outside that list is
not a canonical invariant.

Their sources are real but **lower precedence**: `AM-XX` (TCO), `UVS/UVS.txt` (Big-5),
`STRUCTURE OF THE CONSTITUTION` (HIER), the Execution Spine (EX).

**Action:** each such rule's `source:` field must name the instrument that actually authorises
it. A rule whose provenance names an invariant that does not exist cannot be audited, and
`CONST-HIER-1` requires every rule to trace to a superior instrument.

### B2. The reverse gap: 10 canonical invariants have no compiled rule
**`CORRECTION`.** `F-1`, `F-2`, `F-3`, `FC-2`, `FC-3`, `FC-6`, `CEO-2`, `CEO-3`, `CEO-4`,
`CEO-5` are stated in the canonical Constitution (including in the **active** `AM-XIX` and
`AM-XXII`) and are absent from `RULES.yaml`.

**Action:** compile them. An invariant stated in an active amendment but absent from the rule set
is unenforceable by construction.

### B3. `AM-XXII` invariants were added outside the amendment register
**`CORRECTION`.** `CEO-1..5` appear in the canonical text (lines 1042–1046) but the Register §3
table records `AM-XXII` only by title — its invariant set is not enumerated anywhere traceable.
The same is true of the `F-1..6` and `FC-1..6` sets from `AM-XIX` and `AM-XXI`.

**Action:** the Register carries an **invariant index** enumerating every invariant set with its
owning Article or amendment, so each can be traced like the Article-level sets already are.
Without it, an invariant stated in an active amendment has no address.

### B4. `SPINE-UVS` digest mismatch
**`CORRECTION` — pending one confirmation.** Registry says `cdc9b950…`; the worktree file hashes
to `4ec9fc7b…`; both the file and the manifest carry uncommitted edits.

**Action:** the Founder confirms which content is intended; the registry is updated to that
content's digest in a single signed change. **The digest must never be updated to match the file
without that confirmation** — that would ratify an unreviewed edit.

### B5. `CONST-UVS-1` is marked `enforce: false` while being the system's central invariant
**`CORRECTION`.** The rule "every operation must be verified along the full spine" is the
load-bearing invariant of the whole design, and `CONST-UVS-2` ("nothing bypasses UVS") is
enforced while `UVS-1` is recorded only.

**Action:** either promote `CONST-UVS-1` to `enforce: true` in Phase 2 as scheduled, or record
explicitly that the pipeline order is enforced by `CONST-BIG5-1` and `UVS-1` is its declarative
twin. Silent partial enforcement of the central invariant is the worst of the three options.

---

## Part C — Residual defects that survive resolution

Three defects are **not contradictions** and are not closed by this register. They are recorded
because they will otherwise be rediscovered as contradictions later:

| # | Defect | Note |
|---|---|---|
| R1 | **Three expansions of HALLCO** | Article XI: "Hallucination and **Legality** Compliance". UVS: "Hallucination & **Consistency** Office". Both are canonical-adjacent. One expansion must be chosen. |
| R2 | **The invariant namespace is 3–4 characters wide** | `I-1`, `E-1`, `S-1`, `R-1`, `F-1`, `FC-1`, `AU-1`, `SG-1`, `RE-1`, `RRP-1`, `CL-1`, `D-1`, `A-1`, `G-1`, `N-1`, `UVS-1`, `CEO-1`, `RCA-1`. Two future instruments that both want `A-1` cannot both have it. This is a design defect, not a document error, and it will recur. |
| R3 | **`CONST-HIER-1` does not list Regulations** | Article IX §9.2 and `AM-XIX §4` omit Regulations; `STRUCTURE OF THE CONSTITUTION §1` and `AM-XIX §7` include them. A chain that skips a level cannot rank the level it skipped. |

---

## Part D — What closes when this is signed

| Contradiction | Determination | Closes on |
|---|---|---|
| C1 ACT tiers | CORRECTION — three tiers | signature |
| C2 Safety Spine | **PROPOSED** — (a) recommended | **decision** |
| C3 financial mandate | RECLASSIFICATION — doctrine | signature |
| C4 Document #1 authority | RECLASSIFICATION — rank 6 | signature |
| C5 seven principles | RECLASSIFICATION — policy | signature |
| C6 A2A vs Supervisor | CORRECTION — scope split | signature |
| C7 Volume vs Article | CORRECTION — Articles only | signature |
| C8 spine inventory | **PROPOSED** — see below | **decision** |
| C9 directorate model | **PROPOSED** — two tiers | **decision** |
| C10 pillar set | CORRECTION — seven | signature |
| C11 HallCo/HALLCO | PROPOSED — one entity | **decision** |
| C12 Governance Pillar | CORRECTION — no such pillar | signature |
| C13 Integrity/Master spines | CORRECTION — see A9 + below | signature |
| C14 self-validating issuer | CORRECTION — separation mandatory | signature |
| C15 Master Spine | CORRECTION — lattice tier | signature |

**Tally:** 11 close on signature, 4 need a decision. Of the four, three (C2, C8/C13, C9) are
recommended above and one (C11) is a terminology choice.

### C8 and C13 — the one determination that closes both

**`PROPOSED`:** *Data*, *Enforcement* and *Memory* are **not** spines. They are the substantive
subject matter of registered spines:

| Claimed as a spine | Actually |
|---|---|
| **Data** | the Storage/State subject matter of Article VI, governed by the Audit and World-State spines |
| **Enforcement** | the function of the **Execution Spine** (Article XV/execution) and the UVS gates |
| **Memory** | a subsystem specification with no Article — **unregistered, and therefore not a spine** |

And for C13:

| Lifecycle stage owner | Actually |
|---|---|
| **Integrity Spine** (validation) | the **Verification Spine / UVS** (Article X) — validation is what UVS does |
| **Master Spine** (registration) | the **Governance Spine** (per A9) |

If the Founder signs this, **C8 and C13 both close, the registry's 15 spines stand, and no new
spine is created.** That is the smallest correction that makes the corpus self-consistent, which
is why it is the recommended determination.

---

## Signature block

This register is **PROPOSED**. It becomes effective only when the Founder records a decision
against each row in Part D. Publication does not ratify it, and no part of it may be cited as
authority before then.

```
Determination applied by:  ______________________   Date: ____________
C2  resolved as:  (a) Safety Spine = UVS   /   (b) separate spine (requires amendment)
C8/C13 resolved as:  (  ) recommended   /   (  ) alternative: ______________________
C9  resolved as:  (  ) two tiers        /   (  ) alternative: ______________________
C11 resolved as:  (  ) one entity       /   (  ) separate entities
```

---

**Publication control notice.** Proposed determinations only. This document resolves nothing by
itself, creates no authority, and may not be cited as a decision.
