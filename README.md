# RCA-OS — Public Constitutional Corpus

**RCA-OS** is a constitutional operating system: a system in which no agent, task, or
operator may act outside a constitution, and where every action is identity-bound,
verified, and auditable.

This repository publishes the **constitutional corpus** of RCA-OS — the text that governs
the system — in a form that can be read, cited, diffed, and cryptographically verified.

> **This repository is a publication, not a ratification.** Publishing a document does not
> grant it authority. `DRAFT` and `PROPOSED` text is not law and must never be cited as such.

---

## Read in this order

| # | Document | What it is |
|---|---|---|
| 1 | [`P0_META/00-METADATA-SCHEMA.md`](P0_META/00-METADATA-SCHEMA.md) | What every document header means, and why the old 8-line header was not enough |
| 2 | [`P0_META/CONTRADICTIONS.md`](P0_META/CONTRADICTIONS.md) | What is currently in dispute inside the corpus |
| 3 | [`P0_META/REGISTER.md`](P0_META/REGISTER.md) | Index of every published section and its status |
| 4 | `RCA-PUB-001` — **Constitutional Intent** | The Constitution: supreme authority, Articles I–XV, amendments |
| 5 | `RCA-PUB-002` — **Governance Spine** | How governance is meant to be interpreted and enforced |
| 6 | `RCA-PUB-003` — **Governance & Strategic Mandate** | The operational doctrine (financial mandate, directorates) — doctrine, not law |
| + | [`P0_META/BUILD-ORDER.md`](P0_META/BUILD-ORDER.md) · [`2_GOVERNANCE-SPINE/SPINE-CONTRACT.md`](2_GOVERNANCE-SPINE/SPINE-CONTRACT.md) · [`2_GOVERNANCE-SPINE/SPINE-BASELINE.md`](2_GOVERNANCE-SPINE/SPINE-BASELINE.md) | Build order, spine contract, and the measured spine baseline |

Sections 4–6 are published one at a time; see [`_BUILD-STATE.md`](_BUILD-STATE.md) for the
sequence and what is pending.

---

## The structure of the corpus

```
Constitution            (supreme)
  └── Governance Spine  (interpretation + enforcement)
        └── Policies
              └── Regulations
                    └── Directives
                          └── Configurations
                                └── Code
```

A lower level may never create authority its superior does not grant. Where a lower-level
artifact conflicts with the Constitution, the artifact is void to the extent of the conflict.

## Three ideas that make this a constitutional system, not a policy document

1. **Constitutional Intent is the origin of all lawful action.** Every spine, pillar,
   directorate, agent, and execution pathway derives its authority from it and is bound by it.
2. **Nothing bypasses verification.** Every operation passes a fixed pipeline —
   HALLCO → DEEPGUARD → RRPO-SRE → Global Health Monitor → Reasoning Engine — and no
   subsystem may be skipped.
3. **Everything is reconstructable.** Every identity, event, task, and decision is bound to
   an immutable audit lineage, and any constitutional state must be reproducible from it.

## Every published section declares

- its **class and placement** in the hierarchy of norms;
- whether it is **binding** and, separately, whether it is **enforced**;
- the **digest** of both its source and the published file;
- its **ratification evidence** state (`AVAILABLE` / `OUTSTANDING` / `NOT_REQUIRED`);
- its **open contradictions**, which are never silently cleared;
- its **trust** marking (`TRUSTED` / `UNVERIFIED` / `UNTRUSTED`).

See [`P0_META/00-METADATA-SCHEMA.md`](P0_META/00-METADATA-SCHEMA.md).

## Verify what you are reading

```bash
sha256sum <file>          # compare against P0_META/DIGESTS.txt
```

The digest ledger is written at publication time and re-checked before any republication.

## Status

The corpus is under active consolidation. Known open issues — including a clearance-tier
conflict (three tiers vs five), a conflict over what the Safety Spine is, and the
authority status of Document #1 — are recorded in full in
[`P0_META/CONTRADICTIONS.md`](P0_META/CONTRADICTIONS.md). They are published rather than
hidden, because a governance system that conceals its conflicts is not one.

## How the framework is being completed

The Founder set the construction order: **Constitution → Spines → Pillars → Directorates**,
then Policies and Regulations, then Agents — so that an agent is built against a finished
framework rather than an aspiration.

Measured progress and per-layer completion criteria: [`P0_META/BUILD-ORDER.md`](P0_META/BUILD-ORDER.md).
What makes a spine complete: [`2_GOVERNANCE-SPINE/SPINE-CONTRACT.md`](2_GOVERNANCE-SPINE/SPINE-CONTRACT.md).
Where Layer 2 actually stands: [`2_GOVERNANCE-SPINE/SPINE-BASELINE.md`](2_GOVERNANCE-SPINE/SPINE-BASELINE.md).

## Rights

© 2025–2026 Aether Core Dynamics / AI.Avium Technology. All rights reserved.
Published by the Founder's authority as a public record of the constitutional corpus.
