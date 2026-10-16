# CANONICAL INVARIANT INDEX (RATIFIED 2026-10-16)

**Document ID:** `RCA-FIX-002`
**Status:** EFFECTIVE — ratified by `RCA-RAT-001` (form B, 2026-10-16)
**Standing debt:** `BOARD_REVIEW_DEBT`
**Addresses:** B2 (invariants with no compiled rule) and B3 (AM-XXII outside the amendment register)

---

## Why this exists

`CONSTITUTIONAL REGISTER.md §6` requires that *"every constitutional article has a title, scope,
invariants, enforcement authority, and cross-reference."* No index currently enumerates the
invariants, so an invariant stated inside an **active amendment** has no address and cannot be
traced to a rule.

Enumeration of the canonical text gives **exactly 20 invariant sets, 62 invariants**:

## The index

| Set | Owner | Invariants | Compiled rules | Gap |
|---|---|---|---|---|
| `I-` | Article I — Sovereign Identity and Root CA | I-1, I-2 | `CONST-I-1`, `CONST-I-2` | — |
| `E-` | Article II — Event Legality and Universal Event Substrate | E-1, E-2 | `CONST-E-1`, `CONST-E-2` | — |
| `G-` | Article III — Governance Authority and Enforcement Kernel | G-1, G-2 | `CONST-G-1`, `CONST-G-2` | — |
| `N-` | Article IV — Network Sovereignty, Fabric, Cluster Constitution | N-1, N-2 | `CONST-N-1`, `CONST-N-2` | — |
| `R-` | Article V — Replication, Evolution, Schema Safety | R-1, R-2 | `CONST-R-1`, `CONST-R-2` | — |
| `S-` | Article VI — Storage, State, Immutable Snapshots | S-1, S-2 | `CONST-S-1`, `CONST-S-2` | — |
| `A-` | Article VII — Agents, Capabilities, Constitutional Behavior | A-1, A-2 | `CONST-A-1`, `CONST-A-2` | `CONST-A-3` exists with **no** `A-3` |
| `AU-` | Article VIII — Auditability, Lineage, State Reconstruction | AU-1, AU-2 | `CONST-AU-1`, `CONST-AU-2` | — |
| `SG-` | Article IX — Sovereign Governance and Constitutional Supremacy | SG-1, SG-2 | `CONST-SG-1`, `CONST-SG-2` | — |
| `UVS-` | Article X — Universal Verification Spine | UVS-1, UVS-2 | `CONST-UVS-1`…`UVS-6` | `UVS-3..6` cite invariants that **do not exist** |
| `H-` | Article XI — HALLCO | H-1, H-2 | `CONST-H-1`, `CONST-H-2` | — |
| `D-` | Article XII — DEEPGUARD | D-1, D-2 | `CONST-D-1`, `CONST-D-2` | — |
| `RRP-` | Article XIII — RRPO-SRE | RRP-1, RRP-2 | `CONST-RRP-1`, `CONST-RRP-2` | — |
| `RE-` | Article XIV — Reasoning Engine | RE-1, RE-2 | `CONST-RE-1`, `CONST-RE-2` | — |
| `CL-` | Article XV — Cloud, Cluster, Deployment Sovereignty | CL-1, CL-2 | `CONST-CL-1`, `CONST-CL-2` | — |
| `RCA-` | Master RCA Framework Addendum | RCA-1, RCA-2, RCA-3 | `CONST-RCA-1`…`RCA-3` | — |
| `F-` | **AM-XIX** — Constitutional Supremacy, Founder Stewardship, Board Ratification | F-1 … F-6 | `CONST-F-4`, `CONST-F-5`, `CONST-F-6` | **F-1, F-2, F-3 ungoverned** |
| `FC-` | **AM-XXI** — Executive Directorate, Founder Command, Identity-Bound Control | FC-1 … FC-6 | `CONST-FC-1`, `CONST-FC-4`, `CONST-FC-5` | **FC-2, FC-3, FC-6 ungoverned** |
| `CEO-` | **AM-XXII** — Chief Executive Officer and Operational Execution | CEO-1 … CEO-5 | `CONST-CEO-1` | **CEO-2, CEO-3, CEO-4, CEO-5 ungoverned** |
| `HIER-` | *(no canonical invariant — see B1)* | — | `CONST-HIER-1/2/3` | rules exist, invariant does not |

**Totals:** 62 canonical invariants · 10 with no compiled rule · 27 rules citing non-existent
invariants.

## B2 — the 10 invariants that have no compiled rule

| Invariant | Statement (abbreviated) | Why it matters |
|---|---|---|
| **F-1** | The Constitution is supreme over every human, machine, and autonomous authority | The system's central claim, unenforced by any rule |
| **F-2** | Samuel Stevenson is the highest human authority and Supreme Constitutional Steward | Founder authority basis |
| **F-3** | The Board is the constitutional ratification and oversight authority | **This is the rule that makes Board ratification mandatory** — it is unenforced |
| **FC-2** | The Founder may authorise agent construction; every component remains subordinate to the Constitution | Bounds agent creation |
| **FC-3** | Every freeze must preserve evidence and produce an auditable release or recovery path | Freeze-evidence obligation |
| **FC-6** | Founder operational authority cannot silently amend or repeal the Constitution | Prevents the exact failure `AM-XIX §8` targets |
| **CEO-2** | The CEO may not amend or override the Constitution | Delegation bound |
| **CEO-3** | Material CEO decisions must be identity-bound, TCO-logged, verified, auditable | TCO coverage |
| **CEO-4** | The CEO must escalate beyond delegated authority rather than infer permission | Fail-closed at the executive level |
| **CEO-5** | The CEO may not conceal material risk or failure | Reporting integrity |

**Observation that needs the Founder's attention:** `F-3` — the invariant that makes Board
ratification a constitutional requirement — is itself stated in an active amendment and has no
enforcement point. The rule that requires ratification is not enforced. That is why
`RCA-RAT-001` matters beyond this record.

## B3 — the amendment register gap

`AM-XIX`, `AM-XXI` and `AM-XXII` are recorded as **active** in `CONSTITUTIONAL REGISTER.md §3`,
but their invariant sets (`F-*`, `FC-*`, `CEO-*`) are enumerated nowhere in the Register. The
Register's table lists amendments by title and status only.

**Correction:** the Register carries this index, so every invariant has an address —
`<set> ← <amendment> ← <status> ← <compiled rule | none>`.

## B5 — the partial-enforcement anomaly

`CONST-UVS-1` ("every operation must be verified along the full spine") is the load-bearing
invariant of the entire design, and it is marked **`enforce: false`**, while `CONST-UVS-2`
("nothing bypasses UVS") is `enforce: true`.

Three lawful options, for the Founder to choose:

1. Promote `CONST-UVS-1` in Phase 2 as the phase table already schedules.
2. Record explicitly that the pipeline order is enforced by `CONST-BIG5-1` and `UVS-1` is its
   declarative twin.
3. Leave it — **not recommended.** Silent partial enforcement of the central invariant is the
   one state a fail-closed system cannot justify.

## Residual defect R2 — namespace collision risk

The invariant namespace is **3–4 characters wide**: `I-`, `E-`, `G-`, `N-`, `R-`, `S-`, `A-`,
`AU-`, `SG-`, `UVS-`, `H-`, `D-`, `RRP-`, `RE-`, `CL-`, `RCA-`, `F-`, `FC-`, `CEO-`.

Two future instruments that both want `A-1` cannot both have it. `A-`, `E-`, `R-`, `S-`, `N-`,
`F-` and `H-` are all single letters already taken. Recorded as a **design defect that will
recur**, not as a document error. A future amendment should reserve a namespace prefix scheme
(e.g. `AM<roman>-N` for amendment-borne invariants) before the next one is written.

---

**Notice.** Ratified 2026-10-16. Index only — it compiles no rule and enforces nothing.
