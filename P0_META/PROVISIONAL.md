# PROVISIONAL WORKING AUTHORITY — SCOPE AND RULES

**Document ID:** `RCA-PROV-001`
**Document Class:** Publication Control — Provisional Working Authority
**Version:** 1.0.0
**Status:** **PROVISIONAL — NOT EFFECTIVE**
**Date of Issue:** 2026-10-16
**Granted by:** Samuel Stevenson, Founder — instruction of 2026-10-16 (option 3)
**Publication class:** `PUBLIC`

---

## 1. What was granted

The Founder authorized the 11 corrections in `RCA-DEC-001` Part 1, and the 5 rule-set repairs in
Part 3, to be **applied to the working tree now**, while Board ratification is pending.

This document defines the exact boundary of that authority. It is deliberately narrow.

## 2. What provisional authority permits

1. **Editing working documents** to reflect the 11 corrections — registers, traceability
   manifests, rule provenance, and internal reference documents.
2. **Applying Part 3 repairs** to `src/rcaos/constitution/RULES.yaml` and the Register's
   invariant index.
3. **Drafting new sections** (the Spine set, and later the Pillar and Directorate sets) against
   the corrected baseline.
4. **Testing** against the corrected baseline in the working tree.

## 3. What provisional authority does not permit

1. **It does not close a contradiction.** All 15 remain open in `CONTRADICTIONS.md` until
   `RCA-RAT-001 §4` is complete. A provisional correction is a *draft correction*.
2. **It does not publish corrected content as settled.** Anything produced under it is published
   — if at all — marked `PROVISIONAL — NOT EFFECTIVE`.
3. **It does not create authority.** No agent, spine, pillar, directorate, clearance, permission
   or enforcement point is created, activated or extended.
4. **It does not decide the four reserved contradictions** (C2, C8, C9, C11). Those remain
   Founder decisions and no provisional draft may assume an answer to them.
5. **It does not touch canonical text.** `Constitutional Intent …txt` is not edited under
   provisional authority. Corrections are recorded *about* it, never *in* it.

## 4. Marking requirement

Every file produced or corrected under provisional authority carries, in its header:

```
**Status:** PROVISIONAL — NOT EFFECTIVE
**Provisional basis:** RCA-PROV-001 (Founder instruction 2026-10-16)
**Ratification:** pending — RCA-RAT-001 §4
```

Every line item in a corrected register carries a trailing `[PROVISIONAL]` marker so that a
reader — or a program — can separate drafted corrections from effective ones at a glance.

## 5. The re-verification obligation

Provisional corrections are **not** self-validating. When `RCA-RAT-001 §4` is completed:

1. every `[PROVISIONAL]` item is re-verified against the effective record;
2. items the Board ratified are promoted to effective and lose the marker;
3. items the Board did not ratify are **reverted**, not left in place;
4. the digests in `P0_META/DIGESTS.txt` are recomputed and the promotion is committed as one
   change, so the effective baseline is a single auditable step.

**A provisional change that is never ratified must be reverted, not quietly retained.** An
unratified correction left in place is exactly the drift the corpus is built to prevent.

## 6. Rollback

Provisional work is confined to the working tree and to the `provisional` branch. Rollback is
`git revert` of the provisional commits, or discarding the branch. No provisional change reaches
`main` unmarked.

## 7. Why this is written down rather than just done

Because "the Founder said it's fine" is not a mechanism. A governance system that allows
authorized-but-unratified change to enter silently has no way to tell, later, which of its rules
were actually ratified. The marker and the re-verification obligation are what make the
provisional path safe to use. Without them, option 3 would have been a slower version of simply
ignoring Register §4.

---

**Publication control notice.** Provisional working authority only. Creates no authority, closes
no contradiction, and activates nothing.
