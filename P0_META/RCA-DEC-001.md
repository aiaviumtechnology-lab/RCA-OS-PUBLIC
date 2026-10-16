# RCA-OS FOUNDER DECISION RECORD — CONTRADICTION RESOLUTIONS

**Document ID:** `RCA-DEC-001`
**Document Class:** Founder Decision Record
**Version:** 1.0.0
**Status:** **AWAITING COUNTERSIGNATURE — not in force until the signature block is complete**
**Prepared:** 2026-10-16
**Publication class:** `PUBLIC`

---

## What this record is

The Founder has signed the determinations in `RESOLUTIONS.md`. This record converts that
instruction into the form the Constitution requires for an instrument of this weight.

**Founder's recorded instruction (2026-10-16):** *"let me sign since i am the founder.
Samuel Stevenson"*

## Why a countersignature is required

This is not a procedural formality, and it is not a doubt about who you are. It is the rule the
corpus already sets for itself.

`CONSTITUTIONAL REGISTER.md` **§4 (Ratification Evidence Rule)** requires, for any instrument to
be operationally activated:

> - amendment text and version;
> - constitutional impact and compatibility review;
> - **Founder signature record;**
> - **Board ratification record;**
> - activation timestamp and effective scope;
> - **cryptographic digest or equivalent immutable record;**
> - supersession and rollback relationship, if applicable.

Every one of those items is available. The **Board ratification record is not** — and this
decision resolves fifteen contradictions, three of which (C2, C8/C13, C9) change what RCA-OS
*is* by deciding what counts as a spine, what counts as a pillar, and what counts as a
directorate.

There is also a live reason to hold the line here. `AM-XIX §2` makes the Founder the highest
human authority in RCA-OS, and `AM-XXI §2` gives the Founder comprehensive operational command.
But `AM-XIX §1` and `Invariant F-1` make the **Constitution** supreme over every human
authority, and `Invariant F-6` requires Board ratification before a constitutional change
activates. **If the first formal act under the new framework is the Founder waiving the
framework's own ratification rule, the framework's central claim is falsified on day one.**

`AM-XIX §6` provides the lawful alternative if speed matters: an **emergency Founder
intervention**, which is TCO-bound, signed, time-limited, automatically expiring, and which
*"may not... create permanent authority without amendment ratification."* A founder decision
that needs to bind today can be issued under §6 and converted to permanent authority at
ratification.

## Binding signature (required)

For the record to become effective, countersign this block by replacing the placeholder with the
signature, then commit it. Only the Founder may complete it.

```
I, Samuel Stevenson, Founder and Supreme Constitutional Steward of RCA-OS, adopt the
determinations recorded in RCA-DEC-001 as follows:

  Date (UTC):        ______________________
  Scope:             all 15 determinations recorded below
  Effective:         immediately upon Board ratification, except any item marked
                     EMERGENCY which takes effect under AM-XIX section 6 and expires
                     automatically in 30 days unless ratified.

  GPG signature:     ______________________
  (gpg --armor --detach-sign RCA-DEC-001.md
   using 9AF7 DF48 0794 BA5B F08A  519B 39C8 F597 3460 BB6D
   samuel stevenson <samuelfstevenson@gmail.com>)

  Board ratification:  [ ] PENDING   [ ] RECORDED — reference: ______________________
  Activation timestamp: ______________________
  Cryptographic digest: see "Integrity" below
```

## Binding conditions

1. **No determination takes effect before the block above is complete.**
2. Until then every contradiction remains **open** in `CONTRADICTIONS.md` and no published
   section may cite this record as a decision.
3. This record may not be amended to remove the Board ratification requirement. Doing so is
   itself a constitutional change and requires the amendment process.
4. This record grants no authority to any agent, spine, pillar or directorate. It corrects
   documents and registers.

---

## Part 1 — Determinations adopted (11)

These are errors, corrected by applying authority that already exists. They take effect on
signature and ratification.

| # | Contradiction | Determination |
|---|---|---|
| 1 | **C1** ACT clearance | **Three tiers: G1 / G2 / G3** (`STRUCTURE OF THE CONSTITUTION §5`; active `AM-XX §5`). Document #1 §2.7's five-tier table is non-authoritative. "G1 Executive — full system access" is **not** a clearance: full system access is Founder authority under `AM-XIX §2`. |
| 2 | **C3** Financial mandate | **Doctrine**, precedence rank 6. The $95B–$500B / 15% / 7-stream / 80%-reinvestment figures bind executives as objectives, not the system as law. |
| 3 | **C4** Document #1 authority | **`DOCTRINE`, rank 6.** Its "governing charter" and "all subsequent documents (2–∞) must comply" claims are **struck**. Text preserved. |
| 4 | **C5** The seven principles | **Binding policy, not constitutional invariants.** "Cannot be overridden by any subsystem or agent" is **struck**. Elevation to invariant requires an ID and an enforcement point. |
| 5 | **C6** A2A vs Supervisor | **Both hold, by scope.** A2A is the sole agent-to-agent **transport**; the Supervisor is the sole **orchestration and routing** authority. `_#1 §2.5`'s "no direct peer-to-peer communication" is corrected to **"no unregistered peer-to-peer routing"**. |
| 6 | **C7** Volume vs Article | **Articles I–XV only.** "Volume" is descriptive. Existing volume-numbered documents keep their text and gain a mapping note — **no renumbering**, to preserve traceability. |
| 7 | **C10** Pillar set | **Seven pillars:** Execution, Safety, Audit, Identity, Temporal, Event, World-State. Governance, Operations, Storage and Network are **not** pillars. |
| 8 | **C12** "Governance Pillar" | **No such pillar.** Article III §3.1 creates a **Governance Kernel** (function). The issuer is the **Governance Directorate**, acting through the **Governance Spine**. |
| 9 | **C13** Integrity / Master spines | **Integrity Spine → the Verification Spine / UVS** (Article X). **Master Spine → the Governance Spine.** Neither is a separate spine. No new spine is created. |
| 10 | **C14** Self-validating issuer | **Separation mandatory:** issuer ≠ validator ≠ registrar ≠ auditor; at least two outside the issuing authority. Directives rank **below policies** (Article III §3.2) — "Henceforth law" is **struck**; "binding application of an existing policy" is substituted. |
| 11 | **C15** "Master Spine" | A **lattice tier**, not a spine ID. Its claimed supremacy is **struck**: Article IX §9.2 makes the Constitution supreme. |

## Part 2 — Decisions reserved (4)

Recorded as **OPEN**. The Founder has not yet made these; the recommendations below are the
publication's, not decisions.

| # | Contradiction | Recommendation (not adopted) |
|---|---|---|
| 12 | **C2** Safety Spine | **(a)** Safety Spine = the UVS pipeline. `SPINE-SAFETY` and `SPINE-VERIFICATION` retire as duplicates of `SPINE-UVS`. No amendment needed. |
| 13 | **C8** Spine inventory | **Data, Enforcement, Memory are not spines.** Data = the Article VI Storage/State subject matter; Enforcement = the Execution Spine's function; Memory = an unregistered subsystem specification. |
| 14 | **C9** Directorate model | **Two tiers, not two lists.** The 14 in `DIRECTORATES.txt` are the Directorates; `_#1 §4`'s seven are the **Executive layer** (`AM-XXII` already places the CEO office above them). |
| 15 | **C11** HallCo / HALLCO | **One entity.** The acronym expansion is undecided: Article XI says "Hallucination and **Legality** Compliance"; `UVS/UVS.txt` says "Hallucination & **Consistency** Office". |

## Part 3 — Rule-set corrections directed (5)

Directed by the Founder's instruction to correct the errors. These are repairs to
`src/rcaos/constitution/RULES.yaml` and the Register, not new law.

| # | Correction |
|---|---|
| B1 | **27 compiled rules cite canonical invariants that do not exist** (`A-3`, `E-3`, `EVO-1/2`, `EX-1..5`, `HIER-1..3`, `ID-1..4`, `TCO-1..5`, `UVS-3..6`, `BIG5-1/2`). The canonical text states exactly **20 invariant sets**. Each affected rule's `source:` must name the instrument that actually authorises it (AM-XX, `UVS/UVS.txt`, `STRUCTURE OF THE CONSTITUTION`, the Execution Spine). |
| B2 | **10 canonical invariants have no compiled rule** (`F-1..3`, `FC-2/3/6`, `CEO-2..5`), including invariants from the **active** `AM-XIX` and `AM-XXII`. Compile them. An invariant in an active amendment and absent from the rule set is unenforceable by construction. |
| B3 | **The Register carries an invariant index** enumerating every invariant set with its owning Article or amendment. `AM-XXII`'s `CEO-1..5` currently have no address. |
| B4 | **`SPINE-UVS` digest mismatch.** Registry `cdc9b950…`; worktree `4ec9fc7b…`. Founder confirms the intended content; the registry is updated to that content's digest **in one signed change**. The digest must never be updated to match the file without that confirmation. |
| B5 | **`CONST-UVS-1` is `enforce: false`** while being the system's central invariant, and `CONST-UVS-2` is enforced. Either promote it in Phase 2 as scheduled, or record explicitly that the pipeline order is enforced by `CONST-BIG5-1` and `UVS-1` is its declarative twin. Silent partial enforcement is the worst option. |

## Part 4 — Residual defects recorded (3)

Not contradictions; not closed by this record. Recorded so they are not rediscovered as
contradictions later.

| # | Defect |
|---|---|
| R1 | **Three expansions of HALLCO** — Article XI ("Hallucination and Legality Compliance"), `UVS/UVS.txt` ("Hallucination & Consistency Office"), and the pillar drafts ("HallCo"). One must be chosen. |
| R2 | **The invariant namespace is 3–4 characters wide.** `I-1`, `A-1`, `S-1`, `R-1`, `F-1`, `G-1`, `N-1`… Two future instruments that both want `A-1` cannot both have it. A design defect that will recur. |
| R3 | **`CONST-HIER-1` omits Regulations.** Article IX §9.2 and `AM-XIX §4` skip Regulations; `STRUCTURE OF THE CONSTITUTION §1` and `AM-XIX §7` include them. A chain that skips a level cannot rank the level it skipped. |

## Part 5 — Effect on the build order

Adopting Parts 1 and 3 **unblocks Layer 2 (Spines)**. Specifically:

- 11 spines with no source can be drafted against the eight-part contract.
- The four Article-backed spines — **HALLCO (XI), DEEPGUARD (XII), RRPO-SRE (XIII),
  Reasoning (XIV)** — need no new authority and can be drafted immediately.
- **C2, C8/C13 and C9 remain blockers** for spine-set, pillar-set and directorate-set
  completion respectively. Layer 2 can *begin*; it cannot be *declared complete* until Part 2
  is decided.

---

## Integrity

```
sha256(RCA-DEC-001.md):        <recorded in P0_META/DIGESTS.txt>
Founder signing key:           9AF7 DF48 0794 BA5B F08A  519B 39C8 F597 3460 BB6D
                               samuel stevenson <samuelfstevenson@gmail.com>
                               (rsa4096, created 2026-09-22, expires 2029-09-22)
Board ratification reference:  ______________________
Activation timestamp:          ______________________
```

An equivalent immutable record is the detached GPG signature over this file. Once the
countersignature and the Board reference are recorded, the contradictions named in Part 1 close
and `CONTRADICTIONS.md` is updated in the same change.

---

**Publication control notice.** Prepared by the RCAOS agent for the Founder's signature. It
carries no authority until the binding signature block and Board ratification are complete, and
it may not be cited as a decision before then.
