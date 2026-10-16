# RCA-OS PUBLIC CONSTITUTION — BUILD STATE

**Maintained by:** RCAOS agent (AbacusAI bot)
**Started:** 2026-10-16 (America/Chicago)
**Work dir:** `/RCA`
**Public repo:** `aiaviumtechnology-lab/RCA-OS-PUBLIC` (pending creation)
**Rule of engagement:** publish one constitutional section at a time; nothing is
promoted into authority by publication.

---

## 1. Publisher state (authoritative map)

| Source | Class | In git | Live GitHub |
|---|---|---|---|
| `Constitution/Constitutional Intent — the highest form of authority inside RCA‑OS.txt` | **CANONICAL Constitution** (Intent, Architecture Add. Art. I–XV, Master RCA Framework Add., Amendment Register) | tracked, modified | not on GitHub |
| `Constitution/CONSTITUTIONAL REGISTER.md` | **C0 control document** (precedence, namespace, amendment status, completion criteria) | tracked, clean | not on GitHub |
| `Constitution/_#1 — Governance & Strategic Mandate.txt` | **Draft** Doctrine/Policy-1 (financial mandate, Big-5 principles, ACT tiers, 7 Directorates) | **untracked**, not in `RULES.yaml` sources | not on GitHub |
| `Constitution/Governance and produce … .docx.txt` | **Draft** "Governance Spine v1.0" source prose (409 words, one block, no structure) | tracked, clean | not on GitHub |
| `Constitution/STRUCTURE OF THE CONSTITUTION.docx.txt` | Registered source — hierarchy of norms. **Contradicts drafts** (3-tier ACT vs 5-tier) | tracked | not on GitHub |

Compiled normative layer (private): `src/rcaos/constitution/RULES.yaml`
(70 rules, Articles I–XV; 47 `enforce: true`, 20 `enforce: false`).

Live GitHub (`aiaviumtechnology-lab/rca-os-private`, **private**) holds only pre-2026-07-04
prose exports — a stale generation, not the canonical corpus:
- `main`: 29 root docs + `docs/RCA_OS_CONSTITUTION_VOLUME_VI.md` (Directorates & Org Governance)
- `constitution` branch: Kernel Architecture, ACT, Kyverno/Policy Vault, HR/Legal/KeyManager vaults, ULC, agent fabric map, workload classes/placement

**Conclusion:** no public, authoritative, structured publication exists yet.

---

## 2. Corrected document model (three layers, not three versions)

**Lawyer view**

| # | Document | Class | Status |
|---|---|---|---|
| 1 | **Constitutional Intent** | The Constitution | Canonical (ratification evidence outstanding — Register §4) |
| 2 | **Governance Spine** | Constitutional Spine (subordinate spec under Art. III / XII) | Non-binding draft text |
| 3 | **Governance & Strategic Mandate** | Doctrine / Policy #1 (below regulation) | Unregistered draft |

**Engineer view**

| # | Document | Layer | Authority effect |
|---|---|---|---|
| 1 | Constitutional Intent | normative constitution (text) | controls everything below it |
| 2 | Governance Spine | interpretation + enforcement **engine** (kernel) | binds policy to agent, resolves precedence |
| 3 | Governance & Strategic Mandate | **loadable policy profile** | configuration — cannot amend 1 or 2 |

The mismatch is weight, not just wording: #3 carries OC-2 veto over any owned
network/cloud/agent design, G1–G5 clearance and "full system access", 7 revenue
streams, autonomous external-world action — reading it as a real third branch
contradicts `AM-XIX §8` ("no component may amend the Constitution by
configuration or code"), the Register, and STRUCTURE §1.

---

## 3. Contradiction register (blocks ratification if unresolved)

| ID | Subject | Body #1 / Register | Body #3 | Status |
|---|---|---|---|---|
| C1 | ACT clearance tiers | STRUCTURE §5: G1/G2/G3 (3 tiers) | G1–G5 (5 tiers) | **open** |
| C2 | Safety Spine definition | UVS Big-5: HALLCO, DEEPGUARD, RRPO-SRE, GHM, RE | "Safety Spine (HALCO + DeepGuard)" | **open** |
| C3 | Financial mandate visibility | not in canonical Constitution | 10-yr targets, 15% growth, 80% reinvestment in canonical doctrine slot `_#1` | **open** |
| C4 | Authority of `_#1` | per Register: no authority until registered | asserts it is "the governing charter" | **open** |
| C5 | Supremacy wording | Constitution → Governance Spine → Policies → Directives → Config → Code | 7 "cannot be overridden" sub-policies | **open** |

Publication requirement: every published section carries a `contradictions[]` entry
or an explicit "none". No section may silently resolve one.

---

## 4. Publication sequence (one section per step)

| Step | Section | Status |
|---|---|---|
| P0 | `_META` — metadata schema, contradiction register, build order, spine contract, spine baseline, resolutions, decision + ratification records | **published** |
| P0.9 | **RATIFICATION** — `RCA-DEC-001` Parts 1 and 3 in force; 11 contradictions closed | **done 2026-10-16** |
| P1 | **Governance Spine** → restructured (11 sections, GS-1..8, carries C2/C7) | published 2026-10-16 |
| P2 | **Constitutional Intent** → Part I–IV (flat, exact, canonical vocabulary; zero restructuring) | pending |
| P3 | **Governance & Strategic Mandate** → reclassified doctrine + contradiction flags | pending |
| P4 | **Spine set** — the 4 Article-backed spines first (HALLCO, DEEPGUARD, RRPO-SRE, Reasoning), then Execution + World-State format pass, then the remainder | **unblocked — C8 blocks only *completion*** |
| P5 | **Pillar set** — Identity/Safety/Execution format pass; 4 registered with no source | blocked on C10 |
| P6 | **Directorate set** | blocked on C9 |
| P7+ | Policies, Regulations, then Agents | blocked by design |

## 4a. The four-layer build order (set by the Founder 2026-10-16)

```
1. Constitution  2. Spines  3. Pillars  4. Directorates  → 5. Policies  6. Regulations  → 7. Agents
```

Policies and regulations come only after all four framework layers are complete, so that when
agents are created a full framework already exists to guide them and to govern how RCA-OS
evolves. Criteria and per-layer status: `P0_META/BUILD-ORDER.md`.

**Layer 2 measured state:** 1 of 15 spines has a published specification (Governance, draft);
2 have source text in the wrong format (Execution, World-State); 1 has a source with a digest
mismatch (UVS); **11 have no source at all**. See `2_GOVERNANCE-SPINE/SPINE-BASELINE.md`.

**The working documents claim "100% Spine completion" and "all 11 Pillars fully drafted".
Neither claim survives measurement** — see C8 (spine inventory), C10 (pillar set), C9
(directorate models).

---

## 5. Repository hygiene gate (before any public push)

Measured 2026-10-16: repo 12 GB on disk; **313 MB tracked**; worktree 265 deleted /
212 untracked / 80 modified.

**Never push (sensitive):**
- `api-Keys`, `GOOGLE OAUTH2`, `backup_codes.txt`
- `Library/client_secret_985094422115-*.apps.googleusercontent.com.json`
- `aiaviumtechnology Root CA / Intermediate CA *.cer`, `ghost_*.asc`, `RCAOS_*.asc`
- `constitutional-operating-systemGBS.zip`

**Never push (bulk, not source):** `Anaconda3-*.sh` (2×1.2 GB), `ghidra*.zip` (544 MB),
`GitHub-Copilot*.AppImage` (528 MB), `gradle-*-all.zip` (253 MB), `linux-7.2.3.tar.xz`,
`opencode-desktop*.rpm`, `google-chrome*.rpm`, `*.exe`, `*.deb`, `Photos-*.zip` (85 MB),
`Research Papers -*.zip` (125 MB), `.rustup/ .cargo/ .npm/ .gradle/ .venv/ .vscode/ localperl/`.

**Publication content is text only:** constitutional text, registry, metadata, digests.
No binaries, no keys, no certificates, no personal or financial documents.

**Also know:** `TR` and `"TR` are two tracked directories whose names differ only by a
trailing space — a portability hazard. `TR/Research Papers ` is tracked and distorts the
secret scan. Not touched by this publication.

---

## 6. Open decisions for the Founder

1. Confirm public repo target name: `RCA-OS-PUBLIC` (public) vs an independent public org.
2. Resolve C1–C5 (or instruct publication to carry the flag unmodified).
3. Confirm whether Governance Spine is **subordinate spec** or the **runtime governance mechanism**
   (this changes the HALLCO/DEEPGUARD authority chain, not just wording).
4. Supply or explicitly mark-absent the ratification evidence required by Register §4.
5. Confirm handling of `CONST-A-3` and the 20 `enforce: false` rules (recorded, not enforced).
