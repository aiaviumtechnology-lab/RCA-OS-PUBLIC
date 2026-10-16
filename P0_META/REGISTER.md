# RCA-OS PUBLIC REGISTER (PUBLICATION INDEX)

**Document ID:** `RCA-PUB-META-003`
**Document Class:** Publication Control — Index
**Version:** 1.0.0
**Status:** Active (publication control only — grants no authority)
**Digests:** pinned in `P0_META/DIGESTS.txt` (written after the digest pass completes)
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`

---

## Published sections

| ID | Section | Class | Status | Placement | Trust | Editing | Contradictions | Enforceable |
|---|---|---|---|---|---|---|---|---|
| `RCA-PUB-META-001` | Publication Metadata Schema | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-META-002` | Contradiction Register | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-META-003` | Public Register (this file) | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-META-004` | Constitutional Build Order | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-META-005` | Spine Contract | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-META-006` | Spine Baseline (layer 2 measurement) | Publication Control | Active | outside the hierarchy of norms | TRUSTED | RESTRUCTURED | none | n/a |
| `RCA-PUB-001` | Constitutional Intent (Part I–IV) | Constitution | Canonical text, ratification evidence outstanding | rank 1 (supreme) | TRUSTED | EXACT | none | partial (47/70 compiled rules enforced) |
| `RCA-PUB-002` | Governance Spine | Spine | Draft | rank 4 (subordinate specification) | UNVERIFIED | RESTRUCTURED | C2, C7 | no |

## The four-layer build order

The Founder set the construction order on 2026-10-16:

```
1. Constitution  2. Spines  3. Pillars  4. Directorates  → 5. Policies  6. Regulations  → 7. Agents
```

Layers 5–7 are gated on 1–4. Full criteria, per-layer status and the blocker list are in
`P0_META/BUILD-ORDER.md`. Layer 2 (Spines) is measured in
`2_GOVERNANCE-SPINE/SPINE-BASELINE.md` and defined by `2_GOVERNANCE-SPINE/SPINE-CONTRACT.md`.

> The build order is **not** the authority order. Authority runs
> `Constitution → Governance Spine → Policies → Regulations → Directives → Config → Code`.
> The Governance Spine is *rank 4* in authority and a *Spine* in the build order. The two
> orderings coexist and must not be read as one.

### `RCA-PUB-002` — Governance Spine, detail

- **Path:** `2_GOVERNANCE-SPINE/GOVERNANCE-SPINE.md`
- **Source:** `Constitution/Governance and produce the fully formal constitutional document using the new metadata header you requested.docx.txt` (421 words, one unbroken block)
- **Source digest:** `a90b1dca2ef437fb02ecc1b13c7c3fe3af838a32e06d412326f452be7f4ec40c`
- **Treatment:** `RESTRUCTURED` on the Founder's instruction of 2026-10-16 ("reconstruct the governance spine to make sense"). Structure, scope boundaries, and eight invariant identities were added. No claim in the source was reversed or strengthened; the source's two unbounded claims ("no bypass" and "immutable authority") are reconciled explicitly in §1.2 and §8.
- **What is new:** the document itself (11 sections), invariants `GS-1`–`GS-8`, defined components, a bounded interpretation scope (§7), a failure-mode table, and a placement table that substitutes subject areas for the source's Volume numbers (**C7**).
- **What is *not* claimed:** authority, enforcement, ratification. `status: DRAFT`, `enforceable: false`.
- **Before this can leave `DRAFT`:** Founder sign-off on the eight invariants and on the interpretation limits in §7.
| `RCA-PUB-003` | Governance & Strategic Mandate (Document #1) | Doctrine / Policy-1 | Draft, unregistered | rank 6 until registered | UNTRUSTED | EDITORIAL | C1, C3, C4, C5, C6 | no |

## Not yet published

Articles I–XV as individual sections, the Spines, the Pillars, the TCO Contract Layer (AM-XX),
the Appendices (A–J), the Constitutional Invariant Matrix, the Glossary, and the ratified
amendment series. Sequence is set by the Founder; see `_BUILD-STATE.md` §4.

## Reading order for a newcomer

1. `P0_META/00-METADATA-SCHEMA.md` — what every document header means.
2. `P0_META/CONTRADICTIONS.md` — what is currently in dispute.
3. `RCA-PUB-001` — the Constitution itself.
4. `RCA-PUB-002` — how governance is meant to be interpreted and enforced.
5. `RCA-PUB-003` — the operational mandate, to be read as doctrine, not law.

## Standing notices printed in every section

- Publication is a presentation act, not a ratification act.
- `status: PROPOSED` or `DRAFT` text is not authority and must never be cited as such.
- "Mandatory" is not the same as "enforced"; sections state which applies.
- A contradiction is resolved by the Founder (and Board where required), never by publication.
- Cryptographic digests cover the text as published; re-verify before reuse.
