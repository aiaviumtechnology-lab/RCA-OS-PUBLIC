# SPINE CONTRACT — WHAT MAKES A SPINE A SPINE

**Document ID:** `RCA-PUB-META-005`
**Document Class:** Publication Control — Spine Completeness Contract
**Version:** 1.0.0
**Status:** Active (publication control only — creates no authority)
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`
**Derived from:** `2_GOVERNANCE-SPINE/SPINE-BASELINE.md` and the Register's classification rules

---

## Why this exists

Fourteen of the fifteen registered spines have **no source document**. Completing them
consistently cannot be done from inspiration; it has to be done against a fixed contract.
This is that contract. It defines what "done" means for a spine, and it holds every spine to
the same shape so gaps are visible rather than hidden in prose.

## The Spine Lattice (context)

Spines are separate but inseparable. The registry binds them:

```
vertical:   Master Spine → Operational Spines → System Spines → Directorate Spines
lateral:    Audit ↔ Enforcement ↔ Arbitration ↔ Data ↔ Identity ↔ Memory ↔ Execution
supremacy:  no subsystem may bypass a spine
invariants: cross-spine (Audit immutable · Enforcement deterministic · …)
```

A spine is sovereign **in its jurisdiction** and never **outside** it. No spine may
contradict, bypass, weaken or amend another.

> **Baseline note.** The lateral list above names *Enforcement*, *Data* and *Memory*, which are
> **not** in the registry (see **C8**). The lattice as written and the registry as written do
> not describe the same set. The contract below is written against the registry; the lattice
> wording is carried as evidence for C8.

## The eight-part contract

Every spine document must contain all eight. A spine missing any part is **incomplete**, and
incomplete is the default state — a spine is guilty until proven complete.

### 1. Jurisdiction
- **Grants** — what this spine is authorised to decide, grant, deny, and record.
- **Excludes** — what this spine explicitly does **not** govern, named, so that adjacent
  spines cannot drift into each other.
- **Overlap declaration** — where this spine touches another spine's jurisdiction, the
  boundary is stated as a rule, not left to judgement.

### 2. Constitutional basis
- The Article(s) that create it, or an explicit statement that it is a *named concept* with no
  creating Article (the registry distinguishes `canonical_article_spine` from
  `canonical_named_concept` — a concept spine derives authority from the Articles it serves and
  must say which).
- The amendments that constrain it.
- The compiled rule IDs it implements or supports in `RULES.yaml`.

### 3. Duties and prohibitions
- **Must** — the duties, each written so that non-performance is detectable.
- **Must not** — the prohibitions. A spine with no written prohibitions has no boundary.
- **Failure to perform** — what the spine does when it cannot perform a duty (it never
  continues silently).

### 4. Invariants
- Identified (`<SPINE-PREFIX>-1..n`), stated as a single falsifiable sentence each.
- Each invariant states **who enforces it** — invariants with no enforcement point are
  aspirations, and must be labelled as such.
- Each invariant must not contradict an invariant above it in the authority order.

### 5. Enforcement boundary
- The **enforcement points**: the named moments at which this spine can deny.
- The **denial behaviour**: fail closed, always.
- The **escalation**: which authority receives a denial it cannot resolve.
- A spine that can observe but cannot deny is a monitor, not a spine — and must say which.

### 6. Interfaces
- **Consumes** — what it receives from other spines, and in what form.
- **Exposes** — what it provides, and to whom.
- **Ledger obligations** — what it must write, to which ledger, before an action is lawful.
- Interface descriptions are contracts: another spine may rely on them.

### 7. Failure and recovery
- **Failure modes** — enumerated, each with the required response.
- **Containment** — how it stops rather than degrades.
- **Recovery** — how it returns to a deterministic state, and what must be revalidated first.
- **Records** — what the failure writes to the Audit Spine.

### 8. Source and digest
- A registered source path, or explicit `source: null` with a completion plan.
- SHA-256 of the source as published.
- Editing policy applied (`EXACT` / `EDITORIAL` / `RESTRUCTURED`).
- Any contradiction carried, by ID, unresolved.

## Standard spine shape

```
1.  Jurisdiction            (grants / excludes / overlaps)
2.  Constitutional basis
3.  Duties and prohibitions (must / must not / on failure)
4.  Invariants              (<PREFIX>-1..n)
5.  Enforcement boundary    (points / denial / escalation)
6.  Interfaces              (consumes / exposes / ledger)
7.  Failure and recovery
8.  Placement and source    (registry id, source, digest, contradictions)
```

## Classification honesty

The registry uses three classes. A spine must not claim a stronger class than it holds:

| Class | Means | May claim |
|---|---|---|
| `canonical_article_spine` | A canonical Constitution Article creates it (e.g. UVS ← Article X) | Constitutional authority, via that Article |
| `canonical_named_concept_with_registered_source` | Named in the Constitution, with a registered source document | Named authority + a registered specification |
| `canonical_named_concept` | Named in the Constitution, no registered source | Named authority only — **no specification exists yet** |
| `canonical_secondary_reference` | Referenced, not defined | Referenced status only |

## Completion record

When a spine meets all eight parts, this note is added to it and to `SPINE-BASELINE.md`:

```
Completeness: 8/8
Parts:        1 ✓ 2 ✓ 3 ✓ 4 ✓ 5 ✓ 6 ✓ 7 ✓ 8 ✓
Enforcement:  <enforcement points>
Invariants:   <PREFIX>-1..n  (each with an enforcing spine)
Open:         <contradiction ids, or none>
```

A spine is not complete because it reads well. It is complete because all eight parts exist,
each invariant has an enforcer, and the source digest verifies.

---

**Publication control notice.** This contract measures spine completeness. It creates no spine,
grants no jurisdiction, and does not itself enforce anything.
