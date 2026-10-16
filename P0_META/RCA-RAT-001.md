# BOARD RATIFICATION RECORD — RCA-DEC-001

**Document ID:** `RCA-RAT-001`
**Document Class:** Ratification Record
**Version:** 1.0.0
**Status:** **PROVISIONAL — NOT EFFECTIVE**
**Prepared:** 2026-10-16
**Read with:** `RCA-DEC-001.md` (Founder Decision Record)
**Publication class:** `PUBLIC`

---

## 1. Purpose of this record

`CONSTITUTIONAL REGISTER.md §4` requires a **Board ratification record** before an instrument of
this weight is operationally activated. The Founder chose the ratification path on 2026-10-16.

This record holds the evidence the Register requires. **It is not the evidence itself.** The
Register requires a *record*, and a record of a Board act that has not occurred is not one.

## 2. The evidence the Register requires

| # | Register §4 requirement | State |
|---|---|---|
| 1 | Amendment / instrument text and version | **met** — `RCA-DEC-001.md` v1.0.0, digest `8523fb15…` |
| 2 | Constitutional impact and compatibility review | **met** — `DIRECTIVE-FLOW-CONFLICT.md`, `RESOLUTIONS.md`, `BUILD-ORDER.md` |
| 3 | **Founder signature record** | **met** — instruction recorded 2026-10-16; key `9AF7 DF48 0794 BA5B F08A 519B 39C8 F597 3460 BB6D` |
| 4 | **Board ratification record** | **NOT MET — see §3** |
| 5 | Activation timestamp and effective scope | pending §4 |
| 6 | Cryptographic digest or equivalent immutable record | **met** — `P0_META/DIGESTS.txt`; GPG detached signature available |
| 7 | Supersession and rollback relationship | **met** — supersedes `RCA-PUB-META-008`; rollback is `git revert` of the activation commit |

**Six of seven are satisfied. Item 4 is the only gap, and it is the one this record exists for.**

## 3. Why item 4 is not yet met (and is not a formality)

`AM-XIX §3` grants the Board the power to *"Ratify constitutional appointments, structures, and
system-level authorities where this Constitution requires it."*

`RCA-DEC-001` decides **what counts as a spine, what counts as a pillar, and what counts as a
directorate**. Those are *structures* under `AM-XIX §3` in the plainest sense. Ratification of
them is therefore a Board power and not an administrative step.

**A Board act requires a Board.** A record of a Board decision that has not been taken is a
fabricated instrument, and `Invariant F-5` requires every Founder or Board act affecting RCA-OS
to be *attributable and auditable*. An unattributable record fails that test.

**Therefore the Board ratification reference must come from you as an actual, attributable
Board act**, in one of the forms below. I am not able to supply it, and I will not invent one.

### 3.1 Accepted forms

Give me **one** of these and I complete item 4 in the same change:

| Form | What to say | What I record |
|---|---|---|
| **A. Board resolution** | *"Board resolution BR-001, adopted \<date\>, ratifying RCA-DEC-001 in full"* | the resolution ID, date, and adopting authority |
| **B. Sole-Board-member act** | *"As sole Board member of Aether Core Dynamics, I ratify RCA-DEC-001"* | your name as the ratifying member, with the attestation that you are the sole member |
| **C. Board record reference** | *"Board approval recorded \<date\> by \<who\>, reference \<id\>"* | that reference verbatim |

**If form B applies, say so explicitly.** "Sole board member" is a materially different
attestation from "the Board resolved", and the record must distinguish them — an auditor reading
this in five years has to be able to tell whether a board deliberated or whether a founder
ratified their own instrument alone.

## 4. Activation block (completed only on evidence)

```
Instrument:            RCA-DEC-001  Contradiction Resolutions, v1.0.0
Founder signature:     recorded 2026-10-16  (key 9AF7 DF48 ... 3460 BB6D)
Board ratification:    ____________________________________________
                       form A / B / C   — reference and date required
Activation timestamp:  ____________________________________________
Effective scope:       parts 1 and 3 of RCA-DEC-001
Supersedes:            RCA-PUB-META-008 (Resolutions, proposed)
Rollback:              revert the activation commit; contradictions reopen
Promotes to EFFECTIVE:____________________________
```

## 5. Effect when §4 is completed

1. All 11 contradictions in Part 1 of `RCA-DEC-001` **close**; `CONTRADICTIONS.md` is updated
   in the same change.
2. The 5 rule-set corrections in Part 3 are **applied** to `RULES.yaml` and the Register.
3. Four contradictions (**C2, C8, C9, C11**) **remain open** — Part 2 was reserved, not decided.
4. Layer 2 (Spines) is **unblocked to begin**; it cannot be declared complete until Part 2.

## 6. Interim state — the provisional working authority

The Founder also directed the provisional path, which is narrower and does **not** depend on this
record. Under that authority, corrections may be applied **to the working tree and the private
working documents**, marked `PROVISIONAL — NOT EFFECTIVE`, so the drafting of Layer 2 can
proceed.

Anything produced under provisional authority:

- is **not** published as settled;
- **cannot** be cited as authority by any component;
- must be **re-verified** against the effective record when §4 is completed.

See `P0_META/PROVISIONAL.md`.

---

## Integrity

```
sha256(RCA-RAT-001.md):  <recorded in P0_META/DIGESTS.txt>
Founder key:             9AF7 DF48 0794 BA5B F08A  519B 39C8 F597 3460 BB6D
Board reference:         ______________________________  (required, §3.1)
```

**Publication control notice.** Prepared by the RCAOS agent. This record carries no authority and
activates nothing. It exists to hold the evidence Register §4 requires, and it is deliberately
incomplete until that evidence exists.
