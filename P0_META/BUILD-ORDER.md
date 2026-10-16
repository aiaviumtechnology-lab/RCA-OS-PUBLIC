# RCA-OS CONSTITUTIONAL BUILD ORDER — AUTHORITY LAYERS AND COMPLETION CRITERIA

**Document ID:** `RCA-PUB-META-004`
**Document Class:** Publication Control — Build Order
**Version:** 1.0.0
**Status:** Active (publication control only — creates no authority)
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`
**Records:** the Founder's governance construction order of 2026-10-16

---

## 1. The order, as instructed

Governance in RCA-OS is constructed in four layers, in this order, and policies and
regulations come only after all four are complete:

```
1. The Constitution
2. Spines
3. Pillars
4. Directorates
   ──────────────── complete ────────────────
5. Policies
6. Regulations
   ──────────────── then ────────────────
7. Agents (built against the completed framework)
```

The purpose of completing 1–4 before 5–6 is that when agents are created, a full framework
already exists to guide them, and the same framework governs how RCA-OS evolves over time.

## 2. Two orders that must not be conflated

**Order of authority** (who overrides whom — Register §1, `AM-XIX §4`):

```
Constitution → Governance Spine → Policies → Regulations → Directives → Configurations → Code
```

**Order of construction** (what must be finished before what — §1 above).

They are different orderings and they coexist. The Governance Spine is *rank 4* in authority —
below the Constitution, above policy — but it is a **Spine**, and Spines are built at step 2.
Pillars sit below Spines in the build order but are not a rank in the precedence chain: a
Pillar is a constitutional authority class that operates **through** Spines, and is registered
by its own traceability manifest.

Reading the two orders as one is a source of drift. A Pillar completed before a Spine does not
outrank it; a Spine built before a Pillar does not authorise over it.

## 3. Layer 1 — The Constitution

**Source of truth:** `Constitution/Constitutional Intent — the highest form of authority inside RCA‑OS.txt`
**Control document:** `Constitution/CONSTITUTIONAL REGISTER.md`

| Completion criterion | State |
|---|---|
| Canonical text exists, single consolidated instrument | yes |
| Article namespace fixed (I–XV) | yes — Register §2 |
| Amendment status recorded per amendment (active/proposed/reserved) | yes — Register §3 |
| Ratification evidence present per amendment | **no** — Register §4 records it outstanding |
| Open contradictions recorded | yes — `P0_META/CONTRADICTIONS.md` (C1–C7) |
| Contradictions resolved by Founder/Board | **no** |

**Layer 1 status: TEXT COMPLETE · RATIFICATION EVIDENCE OUTSTANDING.**

Per Register §4 the corpus may be treated as the governing **design baseline**, but no
implementation may claim independently verified legal activation until the evidence exists.

## 4. Layer 2 — Spines

**Registry:** `src/rcaos/constitution/SPINE_TRACEABILITY.yaml` — 15 spines + 1 component.
**Contract:** `2_GOVERNANCE-SPINE/SPINE-CONTRACT.md`
**Verified baseline:** `2_GOVERNANCE-SPINE/SPINE-BASELINE.md`

A Spine is complete when it has all eight of:

1. **Jurisdiction** — what it governs, and what it explicitly does not.
2. **Constitutional basis** — the Article(s) and amendment(s) that authorise it.
3. **Duties and prohibitions** — what it must do and must never do.
4. **Invariants** — identified, registered, and traceable to an authority.
5. **Enforcement boundary** — the enforcement points at which it denies.
6. **Interfaces** — what it exposes to other spines (per the Spine Lattice).
7. **Failure and recovery posture** — what happens when it fails, and how it returns to a
   deterministic state.
8. **Source and digest** — a registered source document, or an explicit `source: null`.

| # | Spine | Class | Source | Complete |
|---|---|---|---|---|
| 1 | Governance | canonical_named_concept | `2_GOVERNANCE-SPINE/GOVERNANCE-SPINE.md` (restructured draft) | **draft** |
| 2 | UVS | canonical_article_spine | `UVS/UVS.txt` | text complete, digest mismatch |
| 3 | HALLCO | canonical_article_spine | — | **no** |
| 4 | DEEPGUARD | canonical_article_spine | — | **no** |
| 5 | RRPO-SRE | canonical_article_spine | — | **no** |
| 6 | Reasoning | canonical_article_spine | — | **no** |
| 7 | Execution | canonical_named_concept_with_registered_source | `Spines/Execution Spine (RCA‑OS) — Finalized1.txt` | text exists, unregistered format |
| 8 | Safety | canonical_named_concept | — | **no** |
| 9 | Audit | canonical_named_concept | — | **no** |
| 10 | Identity | canonical_named_concept | — | **no** |
| 11 | Temporal | canonical_named_concept | — | **no** |
| 12 | Event | canonical_named_concept | — | **no** |
| 13 | World-State | canonical_named_concept | `Spines/Volume X — Spine World‑State Constitution.txt` | text exists, unregistered format |
| 14 | Arbitration | canonical_named_concept | — | **no** |
| 15 | Verification | canonical_secondary_reference | — | **no** |
| — | *Global Health Monitor* | UVS child component, **not a sixteenth spine** | — | **no** |

### 4.1 Contradiction C8 — the spine inventory

The working documents disagree with the registry:

| Source | Claims |
|---|---|
| `Spines/spines that need to be done .txt` | 8 spines: Audit, Safety, Identity, Data, Arbitration, Enforcement, Execution, World-State |
| The same file's summary | All complete, including **Data** and **Enforcement** |
| `Spines/— each spine is a separate constitutional subsystem…` | names Audit, Enforcement, Arbitration, Data, Identity, Memory, Execution |
| **Registry (controlling)** | 15 spines; **no** Data, **no** Enforcement, **no** Memory; **adds** Governance, Verification, UVS, HALLCO, DEEPGUARD, RRPO-SRE, Reasoning, Temporal, Event |

`Data`, `Enforcement` and `Memory` appear as spines in the working documents and are **absent
from the registry**. Either they are spines that must be registered, or they are subsystems of
a registered spine. Until that is decided, a "100% spine completion" claim in the working
documents is not evidence of registry coverage. **Open — C8.**

## 5. Layer 3 — Pillars

**Registry:** `src/rcaos/constitution/PILLAR_TRACEABILITY.yaml` — 7 pillars.

The canonical Constitution names exactly seven Pillars: **Execution, Safety, Audit, Identity,
Temporal, Event, World-State.**

The working documents name **eleven**: the seven above plus **Governance, Operations, Storage,
Network** — and, in one file, Governance, Operations, Audit, Safety, Storage, Network, Identity,
Temporal, Event, World-State.

Three of the extra four are the ones that also appear as unregistered spines: **Governance,
Storage (Data), Network (Enforcement)**. The same four concepts are being described sometimes
as spines and sometimes as pillars.

| Pillar | Registry | Source document | Complete |
|---|---|---|---|
| Identity | registered | `Pillars/Identity Pillar — Founder Authority and Identity Governance.txt` (7 articles, 6 invariants) | text strong, unregistered format |
| Safety | registered | `Pillars/safety pillar.txt` | text exists |
| Execution | registered | `Pillars/the Operational Pillar — …` | text exists, naming conflict (see below) |
| Temporal | registered | `Pillars/📘 RCA‑OS PILLAR COMPLETION SET…` | outline only (5 articles, no invariants) |
| Event | registered | same | outline only |
| World-State | registered | same | outline only |
| Audit | registered | — | **no source** |
| Governance | **not registered** | `Constitution/Governance Directives — the constitutional instructionern itself.txt` | **open** |
| Operations | **not registered** | — | **open** |
| Storage | **not registered** | — | **open** |
| Network | **not registered** | — | **open** |

### 5.1 Naming conflicts to resolve in Layer 3

- **"Operational Pillar" vs "Execution Pillar."** The source file titles itself *"Pillar III,
  OPERATIONAL PILLAR — Pillar of Execution, Runtime, and System-Level Operations"*, while the
  registry says `PILLAR-EXECUTION`. Same pillar, two names.
- **"Operations" as an eleventh pillar** would collide with the Execution Pillar's declared
  scope (execution, runtime, system-level operations). Either Execution absorbs Operations, or
  Operations is a new pillar with a scope that excludes what Execution already holds.
- **`HallCo` overlays.** Every pillar draft ends with a "HallCo Overlay" article. HallCo is
  named in the corpus as an execution context and as an agent, and the registry has no HallCo
  pillar or spine. Its constitutional position is unrecorded.

**Layer 3 status: 3 of 7 registered pillars have usable text; 4 have none; 4 unregistered
pillars await a decision.**

## 5.1 The Governance Directives mechanism (source added 2026-10-16 02:03)

`Constitution/Governance Directives — the constitutional instructionern itself.txt` carries the
corpus's most concrete governance mechanism — a four-class directive taxonomy (Interpretive,
Operational, Structural, Prohibitive) and an eight-stage issuance lifecycle — and its §6–§9
spine interfaces map directly onto the `Interfaces` part of `SPINE-CONTRACT.md`.

It also, read literally, **forbids the build order in §1**, because the mandated lifecycle runs
through an **Integrity Spine** and a **Master Spine**, neither of which is registered, and it
names **Governance a Pillar** (the Constitution creates no such Pillar — it creates a Governance
*Kernel* at Article III §3.1, within the Governance Spine).

Full analysis, the two-order reconciliation, and the single decision it turns on:
`P0_META/DIRECTIVE-FLOW-CONFLICT.md`.

## 6. Layer 4 — Directorates

**Source:** `Directorates/DIRECTORATES.txt` (14 directorates, each with a routing list) and
`docs/RCA_OS_CONSTITUTION_VOLUME_VI.md` (directorate authority and organisational governance).

**A Directorate is complete when it has:**

1. A constitutional basis for its existence.
2. A defined jurisdiction and its explicit limits.
3. The Pillars and Spines it operates through.
4. Its authority class, and the ACT clearance bound to its leadership.
5. Its escalation and conflict path (which authority it escalates to, and when).
6. Its audit and reporting obligations.
7. Its cross-directorate routing rules, and who authorises a cross-directorate route.
8. A named accountable authority (a role, not an agent instance).

### 6.1 Unresolved in Layer 4

- **Governance is both a Directorate and a Spine and (proposed) a Pillar.** The Directorate
  list contains *Governance*; the spine registry contains *SPINE-GOVERNANCE*; the working
  documents call it a Pillar. Three layers, one name. This must be separated before
  Directorate completion, because a Directorate that is also the spine enforcing it has no
  independent check.
- **Directorates appear in the list that have no constitutional basis recorded**: `Coding`,
  `Research`, `Cloud`, `Reliability`, `Provenance` are referenced as routing targets; the
  source document `_#1` names a different, seven-directorate model (Prometheus, Code-Weaver,
  Silicon-Forge, Vox, Aegis, Nexus, Abacus). **Two directorate models exist.** Which is
  canonical is a Founder decision — **C9**.
- The live repository's `Volume VI` places the Founder, CEO, CFO, General Counsel, Chief Human
  Officer, Chief Governance Officer and the Board inside an *Executive Directorate*. That is a
  third arrangement of the same material.

## 7. Layers 5–6 — Policies and Regulations (not started)

Not begun, by instruction. Their completion criteria will be derived from the canonical
lifecycle requirements already recorded:

- **Policies** cite their constitutional basis, define scope and authority, specify required
  controls, bind all agents and directorates, are approved by Governance, and are ratified by
  the appropriate ACT authority (`STRUCTURE OF THE CONSTITUTION §6`).
- **Regulations** specify step-by-step procedures, define required metadata/lineage/security
  controls, are enforceable by Directorates, and are auditable through TCO and the Audit Spine
  (`STRUCTURE OF THE CONSTITUTION §7`).

Both are blocked on **C1** (clearance tiers), because a policy that binds a clearance cannot be
written against two incompatible tier systems.

## 8. Layer 7 — Agents (blocked by design)

Agent construction is gated on Layers 1–4 and on the removal of the blockers below. Agent
completeness criteria already exist in the corpus (`AM-XXI §3`, `Pillars/Identity Pillar…`
Article III §2, `docs/phase0/AGENT_CONSTITUTION_INTEGRATION_PLAN.md`): unique versioned
identity bundle, declared role/capabilities/scopes/red lines, valid registration and activation
record, applicable ACT clearance, TCO and audit lineage per task, and a defined suspension,
retirement and recovery path.

## 9. Blockers, in dependency order

| # | Blocker | Blocks | Owner |
|---|---|---|---|
| B1 | **C1** — ACT clearance is 3 tiers (G1/G2/G3) vs 5 tiers (G1–G5) | every policy, every agent registration, every clearance check | Founder |
| B2 | **C8** — Data / Enforcement / Memory claimed as spines but absent from the registry | Spine completion (Layer 2) | Founder |
| B3 | **Pillar set** — 7 registered vs 11 claimed; Governance/Operations/Storage/Network unregistered | Pillar completion (Layer 3) | Founder |
| B4 | **C9** — two directorate models (`DIRECTORATES.txt` 14 vs `_#1` 7) | Directorate completion (Layer 4) | Founder |
| B5 | **Governance naming collision** — Directorate + Spine + proposed Pillar, one name | Layers 2, 3, 4 | Founder |
| B6 | **C2** — what the Safety Spine is | Safety spine + Safety pillar + UVS enforcement | Founder |
| B7 | **Ratification evidence absent** (Register §4) | any claim of activated authority | Founder/Board |
| B8 | **`SPINE-UVS` source digest mismatch** (`4ec9fc7b…` worktree vs `cdc9b950…` registered) | UVS source integrity; spine baseline | Founder |
| B9 | **HallCo has no registered layer** | pillar overlays, execution context | Founder |
| B10 | **`CONST-A-3` and 19 other rules recorded but not enforced** | agent registration enforcement | Founder |
| B11 | **C12–C15** — "Governance Pillar", the unregistered directive-lifecycle spines (Integrity, Master), a self-validating issuer, and Master Spine supremacy | Layers 2, 3, 4; the directive mechanism itself | Founder |
| B12 | **Does a Directorate precede or follow the directive mechanism?** | the entire build order | Founder |

## 10. What this order buys

Once Layers 1–4 are complete, the framework answers — before any agent exists — the questions
an agent would otherwise have to guess at: what authority it holds, which spine denies its
action, which pillar constrains it, which directorate owns it, how it escalates, and what
happens when it is wrong. That is the difference between a governed system and a collection of
agents with a document attached.

It also makes evolution tractable: a change is proposed against a layer, reviewed against the
layers above it, and recorded in the layer that owns it — instead of being argued from scratch
each time.

---

**Publication control notice.** This document records a construction order and measures
progress against it. It grants no authority, completes no layer, and resolves no contradiction.
