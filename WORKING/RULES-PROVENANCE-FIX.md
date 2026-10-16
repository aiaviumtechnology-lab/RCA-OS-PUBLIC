# RULES PROVENANCE FIX — B1 (RATIFIED 2026-10-16)

**Document ID:** `RCA-FIX-001`
**Status:** EFFECTIVE — ratified by `RCA-RAT-001` (form B, 2026-10-16)
**Standing debt:** `BOARD_REVIEW_DEBT`
**Corrects:** `src/rcaos/constitution/RULES.yaml` — 27 rules citing invariants that do not exist

---

## The defect

`RULES.yaml` compiles 27 rules whose IDs imply canonical constitutional invariants. Those
invariants **do not exist in the canonical text**.

Verified by enumeration of `Constitution/Constitutional Intent — the highest form of authority
inside RCA‑OS.txt`: it states exactly **20 invariant sets** —

```
I-1/2  E-1/2  G-1/2  N-1/2  R-1/2  S-1/2  A-1/2  AU-1/2  SG-1/2  UVS-1/2
H-1/2  D-1/2  RRP-1/2  RE-1/2  CL-1/2  RCA-1/2/3  F-1..6  FC-1..6  CEO-1..5
```

Anything outside that list is not a canonical invariant. Each affected rule's source is real but
**lower precedence**, and `CONST-HIER-1` requires every rule to trace to a superior instrument.
A rule whose provenance names an invariant that does not exist **cannot be audited**.

## The 27 rules and their correct authorising instrument

| Rule ID | Implied invariant (does not exist) | Actual authorising instrument |
|---|---|---|
| `CONST-A-3` | `A-3` | `AM-XXI §3` — Agent Construction and Registration (identity bundle, role, registration record, ACT clearance, TCO lineage, retirement path) |
| `CONST-E-3` | `E-3` | `AM-XX §3` — TCO propagation across every hop |
| `CONST-EVO-1` | `EVO-1` | `Article V §5.3` — Schema Evolution (governed, compatibility-guaranteed) |
| `CONST-EVO-2` | `EVO-2` | `Article V §5.3` + `AM-XIX §8` — no amendment by code or learned behaviour |
| `CONST-EX-1` | `EX-1` | `Spines/Execution Spine (RCA‑OS) — Finalized1.txt` §2 — intent qualification |
| `CONST-EX-2` | `EX-2` | Execution Spine §3 — plan validation |
| `CONST-EX-3` | `EX-3` | Execution Spine §4 — authorisation chain and multi-spine checks |
| `CONST-EX-4` | `EX-4` | Execution Spine §4.3 — Execution Token (single-use, revocable) |
| `CONST-EX-5` | `EX-5` | Execution Spine §5–§6 — rollback, compensation, observability |
| `CONST-HIER-1` | `HIER-1` | `Article IX §9.2` + `AM-XIX §4` — hierarchy of norms |
| `CONST-HIER-2` | `HIER-2` | `STRUCTURE OF THE CONSTITUTION §1` — no policy contradicts the Constitution |
| `CONST-HIER-3` | `HIER-3` | `AM-XIX §1`, §7 — conflict fails closed and escalates |
| `CONST-ID-1` | `ID-1` | `AM-XXI §5` — Identity Pillar mandate |
| `CONST-ID-2` | `ID-2` | `AM-XXI §5` — deterministic identity lifecycle |
| `CONST-ID-3` | `ID-3` | `AM-XXI §5` — no implicit or self-authorised identity |
| `CONST-ID-4` | `ID-4` | `Pillars/Identity Pillar…` Art. IV — delegation bounds |
| `CONST-TCO-1` | `TCO-1` | `AM-XX §1–§2` — every task encapsulated in a TCO |
| `CONST-TCO-2` | `TCO-2` | `AM-XX §2` — required TCO fields |
| `CONST-TCO-3` | `TCO-3` | `AM-XX §3` — route history is append-only and sealed |
| `CONST-TCO-4` | `TCO-4` | `AM-XX §6` — missing/malformed/out-of-clearance → halt |
| `CONST-TCO-5` | `TCO-5` | `AM-XX §4` — Directorate responsibilities for the Contract Layer |
| `CONST-UVS-3` | `UVS-3` | `UVS/UVS.txt` Article III — subsystem mandates |
| `CONST-UVS-4` | `UVS-4` | `UVS/UVS.txt` Article IV — mandatory operational flow |
| `CONST-UVS-5` | `UVS-5` | `UVS/UVS.txt` Article V — logging requirements |
| `CONST-UVS-6` | `UVS-6` | `UVS/UVS.txt` Article VI — failure handling and escalation |
| `CONST-BIG5-1` | `BIG5-1` | `T Big 5.txt` + `BIG-5-MANDATE.md` — the mandatory five-stage sequence |
| `CONST-BIG5-2` | `BIG5-2` | `T Big 5.txt` — complete logging at every stage |

## Correction applied to each rule

The `source:` field is rewritten to name the instrument above, and a `canonical_invariant:`
field is set to `null` where the rule does not derive from a canonical invariant. Rules that
*do* derive from one keep it.

```yaml
# before
- id: CONST-TCO-1
  source: "AM-XX §1 (TCO-1)"          # names an invariant that does not exist

# after
- id: CONST-TCO-1
  source: "AM-XX §1–§2 — Contract Layer and Task Contract Object"
  canonical_invariant: null            # not a canonical invariant; derives from an amendment
  authorising_instrument: AM-XX
```

## Effect

- Every rule traces to an instrument that exists → `CONST-HIER-1` becomes satisfiable.
- The rule set's audit surface becomes complete: no rule cites an address that has no referent.
- **No rule text, severity, phase or `enforce` flag changes.** This is provenance only.

## Not done here

The inverse gap — **10 canonical invariants with no compiled rule** (`F-1..3`, `FC-2/3/6`,
`CEO-2..5`) — is `B2` and is recorded in `INVARIANT-INDEX.md`. Compiling new rules is not a
provenance fix and is not applied under provisional authority.

---

**Notice.** Ratified 2026-10-16. Carries `BOARD_REVIEW_DEBT` — the first constituted Board must review it.
