# SPINE BASELINE — MEASURED STATE OF LAYER 2

**Document ID:** `RCA-PUB-META-006`
**Document Class:** Publication Control — Layer 2 Baseline
**Version:** 1.0.0
**Status:** Active (publication control only — creates no authority)
**Measured:** 2026-10-16 against `src/rcaos/constitution/SPINE_TRACEABILITY.yaml`
**Publication class:** `PUBLIC`

---

## What this is

A measurement, not a plan. Every row below is taken from the registry as it exists in the
worktree, plus the source files that actually exist on disk. Where the working documents claim
completion that the registry does not support, both are shown.

**Headline: of 15 registered spines, 1 has a published specification, 3 have source text that
is not in spine format, and 11 have no source at all.**

## The registry, as measured

| # | Spine ID | Class | Registered source | Source exists? | In spine format? | Complete |
|---|---|---|---|---|---|---|
| 1 | `SPINE-GOVERNANCE` | named concept | *(none registered)* | — | — | **draft** — `RCA-PUB-002` published |
| 2 | `SPINE-UVS` | article spine (Art. X) | `UVS/UVS.txt` | yes | partially | text complete; **digest mismatch** |
| 3 | `SPINE-HALLCO` | article spine (Art. XI) | `null` | — | — | **no** |
| 4 | `SPINE-DEEPGUARD` | article spine (Art. XII) | `null` | — | — | **no** |
| 5 | `SPINE-RRPO-SRE` | article spine (Art. XIII) | `null` | — | — | **no** |
| 6 | `SPINE-REASONING` | article spine (Art. XIV) | `null` | — | — | **no** |
| 7 | `SPINE-EXECUTION` | named concept + source | `Spines/Execution Spine (RCA‑OS) — Finalized1.txt` | yes | **no** — 8 numbered prose blocks | text usable, unregistered |
| 8 | `SPINE-SAFETY` | named concept | `null` | — | — | **no** |
| 9 | `SPINE-AUDIT` | named concept | `null` | — | — | **no** |
| 10 | `SPINE-IDENTITY` | named concept | `null` | — | — | **no** |
| 11 | `SPINE-TEMPORAL` | named concept | `null` | — | — | **no** |
| 12 | `SPINE-EVENT` | named concept | `null` | — | — | **no** |
| 13 | `SPINE-WORLD-STATE` | named concept | *(registered source absent; `Spines/Volume X — Spine World‑State Constitution.txt` exists on disk)* | yes | **no** | text usable, unregistered |
| 14 | `SPINE-ARBITRATION` | named concept | `null` | — | — | **no** |
| 15 | `SPINE-VERIFICATION` | secondary reference | `null` | — | — | **no** |
| — | `COMPONENT-GLOBAL-HEALTH-MONITOR` | UVS child component | *(not a spin)* | — | — | **no** — and **not a spine** |

## Completeness tally

```
Published specification   1   Governance (draft)
Source text, wrong format 2   Execution, World-State
Source text, complete     1   UVS (partial format, digest mismatch)
No source at all         11   HALLCO, DEEPGUARD, RRPO-SRE, Reasoning,
                              Safety, Audit, Identity, Temporal, Event,
                              Arbitration, Verification
```

Against the eight-part contract (`SPINE-CONTRACT.md`):

| Part | Present anywhere | Notes |
|---|---|---|
| 1 Jurisdiction | partially | Execution and World-State declare scope; none declare exclusions |
| 2 Constitutional basis | partially | Article-backed spines yes; named-concept spines cite no Article |
| 3 Duties / prohibitions | partially | Duties common; **prohibitions almost never written** |
| 4 Invariants | no | No spine document states numbered, enforcer-bound invariants except Governance `GS-1..8` (draft) |
| 5 Enforcement boundary | no | No enforcement points named in any spine source |
| 6 Interfaces | partially | Execution lists what it binds to; no consumes/exposes contract |
| 7 Failure and recovery | partially | Execution §6 and World-State §VI give failure protocols |
| 8 Source and digest | 1 of 15 | Only UVS has a registered digest, and it **does not match** |

## Two source-integrity findings

**F1 — `SPINE-UVS` digest mismatch (open).**
Registry records `cdc9b950e9870f40f09234a6c38f7f3726dcc9777788c02a350a7956151df1a0`.
The worktree file `UVS/UVS.txt` hashes to
`4ec9fc7bdfd76a1058aa4231df04bda844fd31e180cd27bad97f59a3f954421`.
Both `UVS/UVS.txt` and the manifest carry uncommitted local edits. **The registry and the
source disagree about what the UVS says, and neither party has confirmed which is intended.**
This is not a formatting problem — it is a provenance problem, and it means the one spine with
a registered source cannot currently be treated as verified.

**F2 — the registered World-State source path does not resolve.**
The registry entry for `SPINE-WORLD-STATE` has `source: null`, while a substantial
`Spines/Volume X — Spine World‑State Constitution.txt` exists on disk. Either the file should
be registered (with a digest) or it is not the intended source. Unregistered text is not a
source.

## C8 — the spine inventory conflict (open)

| Claimant | Set |
|---|---|
| `Spines/spines that need to be done .txt` | Audit, Safety, Identity, **Data**, Arbitration, **Enforcement**, Execution, World-State |
| `Spines/— each spine is a separate constitutional subsystem…` | Audit, **Enforcement**, Arbitration, **Data**, Identity, **Memory**, Execution |
| **Registry (controlling)** | the 15 above — **no Data, no Enforcement, no Memory**; **adds** Governance, Verification, UVS, HALLCO, DEEPGUARD, RRPO-SRE, Reasoning, Temporal, Event |

The working documents claim "100% Spine completion across RCA‑OS". Measured against the
registry, that claim is false in both directions: three named spines are unregistered, and
eleven registered spines have no source. The claim also cannot be validated, because the two
lists do not describe the same system.

**This is the single largest blocker in Layer 2 and it is a Founder decision, not an editorial
one:** either Data / Enforcement / Memory are registered as spines (and their jurisdiction
separated from Storage, the Execution Spine and the Memory subsystem), or they are recorded as
subsystems of a registered spine and the working documents are corrected.

## What completing Layer 2 requires

1. **Founder decisions:** C8 (spine inventory), C2 (Safety Spine composition), B8 (UVS digest
   provenance), and whether Arbitration / Identity / Temporal / Event / World-State are spines
   separate from their Pillars of the same name.
2. **Format pass:** Execution and World-State text brought into the eight-part contract.
3. **Drafting:** 11 spines with no source.
4. **Digest registration:** every completed spine gets a source path and a verified SHA-256.

Items 3 and 4 are mechanical once item 1 is answered — and item 1 is the whole difficulty,
because guessing at the inventory would produce fourteen documents that describe a system
nobody agreed to.

---

**Publication control notice.** Measurements only. This document completes no spine, resolves
no contradiction, and grants no authority.
