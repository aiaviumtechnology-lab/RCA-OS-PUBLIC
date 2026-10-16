# RCA-OS CONTRADICTION REGISTER (PUBLICATION)

**Document ID:** `RCA-PUB-META-002`
**Document Class:** Publication Control — Contradiction Register
**Version:** 1.0.0
**Status:** Active (publication control only)
**Digests:** pinned in `P0_META/DIGESTS.txt` (written after the digest pass completes)
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`

---

## Purpose

Every published constitutional section declares its open contradictions in its metadata
`contradictions[]` field. This register defines them. **A contradiction is never closed by
publication, editorial preference, or inference — only by a recorded decision of the Founder
and, where the Register requires it, Board ratification.**

Publication's job is to make a conflict visible, not to resolve it. Where two sources disagree,
both are published with the conflict flagged.

## Severity scale

| Level | Meaning |
|---|---|
| `S1 — Blocking` | Contradicts the hierarchy of norms or would create unauthorised authority. Must be resolved before the affected document can be called settled. |
| `S2 — Material` | Changes operational behaviour or scope if read literally. |
| `S3 — Editorial` | Wording/terminology only; no authority change. |

---

## Open contradictions

**Open contradictions: 4** — **C2, C8, C9, C11**. The other eleven **closed on 2026-10-16** by
`RCA-DEC-001` Part 1 under `RCA-RAT-001` (form B — sole-member ratification; see the standing
`BOARD_REVIEW_DEBT` below).

### CLOSED 2026-10-16 (11)

Closed by `RCA-RAT-001`. Each closure is a recorded Founder determination applying authority that
existed before it — none created new authority.

| ID | Determination | Instrument |
|---|---|---|
| C1 | ACT clearance is **three tiers: G1/G2/G3**; Document #1's five-tier table is non-authoritative; "G1 Executive — full system access" is Founder authority, not a clearance | `STRUCTURE OF THE CONSTITUTION §5`; `AM-XX §5` |
| C3 | Financial mandate is **doctrine**, rank 6 | Register §1 |
| C4 | Document #1 is **doctrine, rank 6**; its supremacy claims are struck | `AM-XIX §8`; Register §1 |
| C5 | The seven principles are **binding policy**, not invariants; "cannot be overridden" struck | Register §5 |
| C6 | A2A is the sole agent-to-agent **transport**; the Supervisor is the sole **orchestration/routing** authority; "no peer-to-peer" corrected to "no unregistered routing" | `CONST-HIER-2` |
| C7 | **Articles I–XV only**; volumes kept with a mapping note, never renumbered | Register §2, §5 |
| C10 | **Seven pillars**; Governance, Operations, Storage and Network are not pillars | `PILLAR_TRACEABILITY.yaml` |
| C12 | **No Governance Pillar exists.** Article III §3.1 creates a Governance **Kernel** (function); the issuer is the Governance Directorate through the Governance Spine | Article III §3.1 |
| C13 | Integrity Spine → **Verification Spine / UVS**; Master Spine → **Governance Spine**. No new spine | Article X; Register §5 |
| C14 | Separation mandatory: **issuer ≠ validator ≠ registrar ≠ auditor**; directives rank **below policies** ("Henceforth law" struck) | `AM-XIX §5`; `AM-XXI §4`; Article III §3.2 |
| C15 | "Master Spine" is a **lattice tier**, not a spine ID; supremacy struck | Article IX §9.2 |

**Standing debt:** every closure above, and every instrument activated under `RCA-RAT-001`, carries
`BOARD_REVIEW_DEBT` — the first constituted Board must review the sole-member ratification. The
Founder's attestation of 2026-10-16: the Board does not yet exist because the Executive
Directorate has not been built, so the Founder is the only member able to ratify.

---

## Closed contradiction records (C1, C3–C7, C10, C12–C15)

> The four open contradictions are C2, C8, C9 and C11 — they appear immediately below.

Closed 2026-10-16 by `RCA-DEC-001` Part 1 / `RCA-RAT-001`. Evidence retained as the audit trail.


### C2 — What is the "Safety Spine"?
- **Severity:** S2 — Material
- **A:** `UVS/UVS.txt` and `Constitutional Intent…txt` Art. X — the verification layer is the
  **Universal Verification Spine**, composed of five mandatory subsystems in fixed order:
  HALLCO → DEEPGUARD → RRPO-SRE → Global Health Monitor → Reasoning Engine.
- **B:** `Governance and produce… .docx.txt` §7 — "Governance is enforced by … **Safety Spine
  (HALCO + DeepGuard)**"; `_#1 — Governance & Strategic Mandate.txt` §2.3 — "Secure-by-Default
  Architecture" as a foundational principle.
- **Consequence:** A says safety is two gates inside a five-gate pipeline with a defined order;
  B says safety is a spine composed of those two. Enforcement points, escalation paths and
  audit obligations differ.
- **Owner decision required:** yes.

### C3 — Financial mandate: constitutional or doctrine?
- **Severity:** S1 — Blocking
- **A:** The canonical Constitution contains no revenue target. `CONSTITUTIONAL REGISTER.md` §5
  treats unregistered documents as subsystem specifications or drafts.
- **B:** `_#1 — Governance & Strategic Mandate.txt` §1 sets a 10-year mandate: $95B–$500B total
  revenue, 15% compounded annual growth, 7+ diversified income streams, 80% profit reinvestment.
- **Consequence:** if B is doctrine, these are targets an executive may be held to; if B is
  constitutional, they constrain the whole system and require the amendment process to change.
  B is currently **untracked and absent from `RULES.yaml` sources** — it has no authority at all.
- **Owner decision required:** yes.

### C4 — Authority of Document #1
- **Severity:** S1 — Blocking
- **A:** Register §1 precedence puts unregistered documents at rank 6; `RULES.yaml` does not list
  `_#1 — Governance & Strategic Mandate.txt` among its sources. It creates no authority.
- **B:** The document states it is "the governing charter of the RCA OS" and that "all subsequent
  documents (2–∞) must comply with this governance layer".
- **Consequence:** B's self-description would make it superior to registered policy and to the
  Governance Spine. That conflicts with `AM-XIX §8` ("No Agent, Spine, Pillar, Directorate,
  provider, subsystem, or autonomous process may amend the Constitution by configuration, code,
  learned behavior, policy, regulation, or model output") and with Register §1.
- **Resolution path:** either register the document (with a recorded amendment/consolidation
  decision) or publish it reclassified as `DOCTRINE` with no supremacy claim. Publication takes
  the second path and flags the conflict.
- **Owner decision required:** yes.

### C5 — Number and status of "non-overridable" principles
- **Severity:** S3 — Editorial, rising to S2 if enforced
- **A:** Hierarchy of norms is a chain: Constitution → Governance Spine → Policies → Directives →
  Configurations → Code (`Constitutional Intent…txt` §9.2, `AM-XIX §4`).
- **B:** `_#1` §2 declares seven principles that "cannot be overridden by any subsystem or agent"
  and one (§2.2 Open Standards) that "cannot be changed or overridden".
- **Consequence:** "cannot be overridden" is the language of an invariant. If the seven principles
  are invariants they must be registered with IDs, an owning Article, and enforcement; if they are
  policy, they may be superseded by a higher policy. Currently they are neither.
- **Owner decision required:** yes.

### C6 — Supervisor as sole orchestration authority
- **Severity:** S2 — Material
- **A:** `_#1` §2.5 — "The Supervisor Agent is the sole orchestration authority. No direct
  peer-to-peer communication."
- **B:** `A2A/` and `Constitution/a2a-message_protocol.py.txt` — agent-to-agent messaging is a
  first-class constitutional substrate, with the Supervisor monitoring A2A traffic rather than
  replacing it.
- **Consequence:** "no direct peer-to-peer communication" and "all agents MUST use A2A" cannot
  both be read literally.
- **Owner decision required:** yes.

### C7 — Canonical title/namespace: "Volume" vs "Article"
- **Severity:** S3 — Editorial
- **A:** Register §2 fixes Articles **I–XV** as the canonical namespace; Register §5 states the
  word "Volume" is descriptive unless a volume index is ratified.
- **B:** The July 2026 drafts (`Governance Spine` §10, `Vol 1.txt`, live `rca-os-private`
  `docs/RCA_OS_CONSTITUTION_VOLUME_VI.md`) use Volumes I–IX for different, overlapping subject
  matter (e.g. "Volume VI — Directorates" vs the Governance Spine's "Volume VI — Arbitration
  Procedures").
- **Consequence:** the same number names different bodies of law. Any citation by volume number
  is ambiguous today.
- **Owner decision required:** yes — ratify a volume index (Register §7 decision 5) or drop
  volume numbering in public documents.

### C8 — Spine inventory: which concepts are spines?
- **Severity:** S1 — Blocking
- **A (controlling):** `SPINE_TRACEABILITY.yaml` registers 15 spines: UVS, HALLCO, DEEPGUARD,
  RRPO-SRE, Reasoning, Execution, Safety, Audit, Identity, Temporal, Event, World-State,
  Arbitration, Governance, Verification. Global Health Monitor is registered as a **UVS child
  component, not a sixteenth spine**.
- **B:** `Spines/spines that need to be done .txt` and `Spines/— each spine is a separate
  constitutional subsystem…` name **Audit, Safety, Identity, Data, Arbitration, Enforcement,
  Execution, World-State** — and in one version also **Memory**. The same file concludes
  "100% Spine completion across RCA‑OS".
- **Consequence:** **Data, Enforcement and Memory** are claimed as spines and are absent from
  the registry. Eleven registered spines have no source document at all. Two lists describing
  different systems means no completion claim about either can be validated.
- **Blocks:** all of Layer 2 (Spines). See `2_GOVERNANCE-SPINE/SPINE-BASELINE.md`.
- **Owner decision required:** yes — register Data/Enforcement/Memory as spines, or record them
  as subsystems of a registered spine and correct the working documents.

### C9 — Directorate models: fourteen or seven?
- **Severity:** S1 — Blocking
- **A:** `Directorates/DIRECTORATES.txt` — 14 directorates: Intelligence, Security, Memory,
  Integrity, R&D, Observability, Executive, Network, CI/DI, Board, Coding, Research, Cloud,
  Arbitration.
- **B:** `Constitution/_#1 — Governance & Strategic Mandate.txt` §4 — seven AI Directorates:
  Prometheus (CEO), Code-Weaver (R&D software), Silicon-Forge (R&D hardware), Vox (product &
  sentiment), Aegis (compliance & legal), Nexus (operations & supply chain), Abacus (finance).
- **C:** `docs/RCA_OS_CONSTITUTION_VOLUME_VI.md` (live private repo) — a third arrangement,
  placing Founder, CEO, CFO, General Counsel, Chief Human Officer, Chief Governance Officer
  and the Board inside an *Executive Directorate*.
- **Consequence:** Directorate authority, escalation paths and agent ownership differ under
  each arrangement. Layer 4 cannot be completed against three models.
- **Owner decision required:** yes.

### C10 — Pillar set: seven or eleven?
- **Severity:** S1 — Blocking
- **A (controlling):** `PILLAR_TRACEABILITY.yaml` and the canonical Constitution name **seven**:
  Execution, Safety, Audit, Identity, Temporal, Event, World-State.
- **B:** `Pillars/📘 RCA‑OS PILLAR COMPLETION SET…` states "all 11 Pillars fully drafted:
  Constitution, Governance, Operations, Audit, Safety, Storage, Network, Identity, Temporal,
  Event, World-State" — and in one passage replaces Operations with Execution.
- **Consequence:** **Governance, Operations, Storage and Network** are unregistered pillars.
  Governance is *also* a Directorate and a registered Spine — one name across three layers.
  "Operations" collides with the Execution Pillar's declared scope ("Execution, Runtime, and
  System-Level Operations"). Storage/Network overlap the unregistered Data/Enforcement spines
  in C8.
- **Owner decision required:** yes.

### C11 — HallCo has no registered layer
- **Severity:** S2 — Material
- **A:** Every pillar draft in `Pillars/` ends with a "HallCo Overlay" article.
- **B:** HallCo appears in the corpus as an execution context, an agent, and a constrained
  jurisdiction, and appears in the UVS pipeline ("HALLCO") as the first verification gate.
- **Consequence:** an overlay is being applied by a concept with no registered pillar, spine,
  or directorate. Whether "HallCo" and "HALLCO" are the same entity is unrecorded, and
  C2 (Safety Spine composition) turns on part of that question.
- **Owner decision required:** yes.

### C12 — "Governance Pillar": a fourth layer for one name
- **Severity:** S1 — Blocking
- **Source:** `Constitution/Governance Directives — the constitutional instructionern itself.txt` — "Governance Directives are the formal, binding outputs of the **Governance Pillar**" and "**Governance Pillar issues directive**".
- **A (controlling):** the canonical Constitution names exactly seven Pillars — Execution, Safety,
  Audit, Identity, Temporal, Event, World-State — and `PILLAR_TRACEABILITY.yaml` registers those
  seven. There is **no Governance Pillar**. The canonical text creates a **Governance Kernel**
  (Article III §3.1) within a Governance **Spine** and a Governance **Directorate**.
- **B:** the working documents call Governance a **Pillar** and make it the *issuer* of binding
  instruments.
- **Consequence:** "Governance" now names a **Directorate** (`DIRECTORATES.txt`), a registered
  **Spine** (`SPINE-GOVERNANCE`), a claimed **Pillar**, and the canonical **Kernel** — four
  layers, one word. The Layer-4 consequence is specific and material: if Governance issues the
  binding instrument *and* is a Directorate that must itself be governed by one, the independent
  check is gone.
- **Owner decision required:** yes.

### C13 — The Governance Directive lifecycle assumes four spine concepts that are not registered
- **Severity:** S1 — Blocking
- **Source:** `Governance Directives … §4–§5` — the mandated lifecycle is
  *Drafting (Governance Pillar) → Validation (**Integrity Spine**) → Authorization (Governance
  Spine) → Registration (**Master Spine**) → Propagation → Enforcement → Audit → Arbitration*.
- **A (controlling):** of the four spines in that chain, only **Governance** and **Audit** are
  registered (and both are `source: null`). **Integrity Spine** and **Master Spine** are not
  registered at all. `docs/phase0/CONTRADICTIONS.md` already records `Master Spine`,
  `Verification Spine`, `Memory Spine` and `eBPF Spine` as competing names with no settled
  relation to the registry.
- **Consequence:** the lifecycle is **non-executable as written**. A directive cannot complete
  step 2 (no Integrity Spine to validate) or step 4 (no Master Spine to register). Since
  Article III §3.2 requires directives to be "signed, versioned, and traceable to sovereign
  authority", an unregisterable directive cannot be shown to be lawful.
- **Owner decision required:** yes.

### C14 — The Directive lifecycle creates a circular authority
- **Severity:** S1 — Blocking
- **Source:** `Governance Directives … §4–§5` — the Governance Pillar *issues* the directive; the
  Governance Spine then *interprets and signs* that directive; the same instrument is then what
  binds the Spine.
- **Consequence:** an interpreter that signs the instrument it later interprets is
  self-validating. It contradicts:
  - `AM-XIX §8` — no component may amend the Constitution by policy, regulation or output;
  - `GS-4` (no self-authorisation) in `RCA-PUB-002` §5.3;
  - the defence-in-depth the corpus relies on elsewhere (Validation by a *different* spine than
    Authorization; Audit by a spine that did not produce the act).
- **Also note:** §1 says directives are **"binding rules"** while the canonical Article III §3.2
  places directives **below policies and regulations** in the hierarchy of norms. Either the
  lifecycle is wrong about the rank, or the instrument is misnamed.
- **Owner decision required:** yes.

### C15 — "Master Spine" is a fifteenth-and-a-half spine
- **Severity:** S2 — Material
- **Source:** `Master Spine Supremacy Clause`, `Master Spine registers directive`, "Master Spine
  Authority Over Workflows: the supreme constitutional authority over all workflows",
  "System Spines directly bound to the Master Spine".
- **A (controlling):** the registry has **no** `SPINE-MASTER`. The lattice in
  `Spines/— each spine is a separate constitutional subsystem…` describes a four-rung vertical
  binding *"Master Spine → Operational Spines → System Spines → Directorate Spines"* — a tier,
  not a spine ID.
- **Consequence:** a "supreme constitutional authority over all workflows" with no registry
  entry, no jurisdiction, no invariants and no digest. Its claimed supremacy also collides with
  Article IX §9.2, where the Constitution — not any spine — is supreme.
- **Owner decision required:** yes.

---

### C1 — ACT clearance tiers: three or five?
- **Severity:** S2 — Material
- **A:** `Constitution/STRUCTURE OF THE CONSTITUTION.docx.txt` §5 — ACT defines **G1** Supreme
  constitutional authority, **G2** Schema and structural authority, **G3** Operational and
  execution authority (three tiers). Registered source; feeds `RULES.yaml`.
- **B:** `Constitution/_#1 — Governance & Strategic Mandate.txt` §2.7 — five tiers:
  G1 Executive (full system access, ethics controls, kill switches), G2 Strategic Oversight,
  G3 Directorate Lead, G4 Specialist, G5 Sub-Agent.
- **Consequence:** every clearance check, agent registration, and rule that names a tier resolves
  differently under A and B. A component granted "G1 Executive / full system access" under B
  has no equivalent under A.
- **Blocks:** agent registration prerequisites (`CONST-A-3`), TCO clearance rules
  (`AM-XX §5` uses G1/G2/G3 and matches A).
- **Note:** `AM-XX §5` (active amendment) uses **three** tiers. That is evidence for A, not a
  resolution.
- **Owner decision required:** yes.


## How to close a contradiction

### Status (2026-10-16)

**11 closed, 4 open.** `RCA-DEC-001` Part 1 closed the eleven as errors, applying authority that
existed before it; `RCA-RAT-001` records the ratification. The four that remain open are
**decisions about what RCA-OS is**, not errors:

| ID | Open question | Blocks |
|---|---|---|
| **C2** | Is the Safety Spine the UVS pipeline, or a distinct spine needing its own Article? | Safety pillar; UVS enforcement; spine-set completion |
| **C8** | Are Data / Enforcement / Memory spines? | Spine-set completion (Layer 2) |
| **C9** | Are the 14 directorates and the 7 executive roles two tiers or two competing lists? | Directorate-set completion (Layer 4) |
| **C11** | HallCo and HALLCO are one entity — which acronym expansion? | Terminology; pillar overlays |

Recommendations for all four are in `RESOLUTIONS.md` Part 2 (recorded, **not adopted**).

1. Founder records a decision (and Board ratification where the Register requires it).
2. The affected source text is amended through the lawful process, or the losing document is
   reclassified with `status: SUPERSEDED`.
3. This register records the closing decision, date, and instrument.
4. The `contradictions[]` field of every affected published section is updated in the same change.

No step may be skipped, and no contradiction is closed by publishing a document that reads
better than its predecessor.
