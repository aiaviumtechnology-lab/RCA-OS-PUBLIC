# AGENT INVENTORY AND REGISTRATION READINESS REPORT

**Document ID:** `RCA-PUB-005`
**Document Class:** Publication Control — Inventory Reconciliation
**Version:** 1.0.0
**Status:** Active (analysis only — registers nothing)
**Date of Issue:** 2026-10-16
**Measured against:** `Agents/Agents_list`, `Agents/agent_catalog.yaml`, `Agents/README.md`,
`tools/agents/build_agents.py`, `src/rcaos/constitution/RULES.yaml`,
`docs/phase0/AGENT_CONSTITUTION_INTEGRATION_PLAN.md`
**Publication class:** `PUBLIC`

---

## 1. Why this report exists, and its one conclusion

The Founder has supplied **45 agents to be created and coded**. This report measures whether they
can lawfully be created today.

**Conclusion, stated first: they cannot — and not because of a defect in any of the 45 profiles.**

Every blocker is upstream of the catalog. Under the Founder's own build order, agents are Layer 7,
built last, against a completed framework. The framework is at Layer 2. **Creating these agents now
would build Layer 7 on a foundation whose own completion state is unresolved** — and every agent
would inherit the C2/C8/C9 ambiguity as an unanswerable authority question.

This is a sequencing finding, not a criticism of the catalog. The catalog is, in places, better than
the corpus above it, and §7 says where.

---

## 2. What is actually here (measured)

| Artifact | Count | Status |
|---|---|---|
| `Agents_list` numbered inventory | 45 entries, numbers 0–5 + 7–45 (gap at 6) | working tree has **39 changed lines** vs committed |
| `agent_catalog.yaml` profiles | 45 | `status: development-profiles-unregistered` |
| Generated profiles `.opencode/agents/rca/*.md` | 45 | **4 stale** — `ceo`, `legal`, `research`, `coding` |
| Catalog self-description (`README.md`) | says **41** | **stale — the catalog now holds 45** |

### 2.1 The reconciliation the README warns about is now complete

`Agents/README.md` states: *"The current working-tree `Agents_list` has diverged from the catalog;
reconcile its new and renumbered entries before claiming complete inventory coverage."*

**Measured: every one of the 45 inventory labels matches its catalog `source_label` exactly.**

```
0 Founder(F)            16 Hallco System         31 Provider Agent (PA)
1 CEO                   17 RRPO-SE System        32 Key Manager Agent (KMA)
2 CFO                   18 Boot Agent(BA)        33 Library System(LS)
3 CTO                   19 DEEPGAURD System      34 Procurement Agent(PA)
4 Legal                 20 Sales Agent(SA)       35 Spine Sub-System
5 HR                    21 cidi System           36 Pillar Sub-System
7 Research Agent(RA)    22 Cloud System          37 Directorate Sub-System
8 Audit Agent(AGA)      23 Cluster System        38 Architect Agent(AA)
9 Supervisor Agent(SA)  24 Network Agent(NA)     39 Orchestrator Agent(OA)
10 build Agent(BA)      25 System Monitor        40 DataOps Agent(DA)
11 context Agent(CA)    26 System Health Monitor 41 Reasoning Agent(RA)
12 prompt Agent(PA)     27 UVS Sub-SWystem       42 Token Agent(TA)
13 Installer Agent(IA)  28 ULC Sub-System        43 Coding Agent(CA)
14 Security Agent(SA)   29 Telemtry Agent(TA)    44 Global Build System(GBS)
15 Database Agent(DA)   30 Git System(GS)        45 Global Debug System(GDS)
```

**The blocking note in `README.md` and in the integration plan is out of date.** The catalog and
the inventory now agree. That is a real, verified improvement — and it removes one of the three
inventory blockers the integration plan recorded.

### 2.2 Two inconsistencies that remain

| # | Finding | Detail |
|---|---|---|
| **I1** | Number **6 is skipped** | The inventory runs `0-5, 7-45`. `agent_catalog.yaml` declares `skipped_numbers: [6]`. The old list had `6. coding`; the renumbering moved Coding to 43 and left the gap. The skip is *declared*, so the generator accepts it — but nothing records **why 6 is empty**. An unexplained gap in a constitutional inventory is where a future agent gets inserted without ratification. |
| **I2** | Staleness is real | `tools/agents/build_agents.py --check` reports **FAILED** on four profiles: `ceo.md`, `legal.md`, `research.md`, `coding.md`. The tracked generated files do not match the catalog. Either regenerate, or the catalog is not the source of truth. |

## 3. The 45 profiles, grouped by catalogue class

### 3.1 Executive / human-authority (6) — numbering matches the Board charter §3.2

`0 Founder` · `1 CEO` · `2 CFO` · `3 CTO` · `4 Legal` · `5 HR`

**Note the absence: no `CGO` (Chief Governance Officer) and no `CHRO` (Chief Human Officer)
distinct from `HR`.** The Board charter §3.2 names **CGO** as a seat. The Board cannot reach its
stated composition from this inventory. `AM-XIX §3` makes ratifying appointments a Board power, so
this gap is a Board-composition defect, not a catalog oversight.

### 3.2 The five Big-5 gates (5) — all present, all named canonically

| Big-5 role | Catalog id | Canonical name |
|---|---|---|
| 1st gate | `hallco` | HALLCO |
| 2nd gate | `deepguard` | DEEPGUARD |
| 3rd gate | `rrpo-sre` | RRPO-SRE |
| 4th gate | `system-monitor` | Global Health Monitor |
| 5th gate | `reasoning` | Reasoning Engine |

**This is the strongest part of the catalog.** The five gates map one-to-one onto the canonical
Big-5 sequence in `UVS/UVS.txt` and `T Big 5.txt`, with `big5_role` set on each. Four of the five
are guardrails against false claims (`"Do not claim runtime HALLCO execution when only this
repository prompt profile ran."`).

### 3.3 Sub-system profiles (8)

`27 UVS` · `28 ULC` · `30 Git` · `33 Library` · `35 Spine` · `36 Pillar` · `37 Directorate` ·
`44 Global Build` · `45 Global Debug`

These are the ones with the deepest authority problem — see §4.2.

### 3.4 By category

| Category | Count |
|---|---|
| engineering | 15 |
| assurance | 12 |
| governance | 6 |
| operations | 6 |
| domain | 5 |
| human-authority | 1 |

### 3.5 By declared permission profile

| Profile | Count | Note |
|---|---|---|
| `read-only` | 26 | cannot mutate |
| `guarded` | 14 | mutation with approval |
| `implement` | 4 | `supervisor`, `build`, `uvs`, `coding` |
| `orchestrator` | 1 | `orchestrator` |

**`implement` on four profiles is the highest-risk declaration in the catalog.** `uvs` holds
`implement` — the profile that builds the verification gate can also write code. `C14`
(closed 2026-10-16) requires issuer ≠ validator; the same separation question applies here.

## 4. The blockers, in dependency order

### 4.1 B1 — C1 ACT clearance is closed, but `default_act_clearance: G3` was set before it was

The catalog sets `default_act_clearance: G3` for all 45 profiles. `C1` closed on 2026-10-16 with
**three tiers G1/G2/G3**, so `G3` is now a valid tier — **by accident of the closure, not by
design.** The value was written when two incompatible tier systems were live.

**Action:** re-derive each profile's clearance against the closed three-tier model, and record that
"full system access" is Founder authority (`AM-XIX §2`), **not** a clearance. Six executive profiles
cannot all be `G3` if `G3` means "operational and execution authority".

### 4.2 B2 — 14 profiles carry `unresolved:` blocks, and 4 of them are authority-bearing

| Profile | Unresolved issue recorded | Severity |
|---|---|---|
| `cidi` | *"The inventory label CIDI is not defined in a registered artifact... Confirm the canonical subsystem name and authority before activation."* | **blocks activation** |
| `global-build` | *"The Global Build System inventory entry does not establish a registered runtime Agent or permission to execute its design."* | **blocks activation** |
| `global-debug` | *"Global Debug System documents are design hints, not a registered runtime debugger or authority to mutate state."* | **blocks activation** |
| `reasoning` | `canonical_name: Reasoning Engine` — but `Article XIV` is the authority and `src/rcaos/uvs/reasoning.py` is the runtime gate | **authority binding** |
| `orchestrator` | `canonical_name: Orchestrator Agent` — the canonical instrument names the **Supervisor** as sole orchestration authority (`C6`, closed) | **C6 collision** |
| `founder` | the Founder's own authority transition (Board charter `BD-3`/`BD-4`) | **state-dependent** |
| `token`, `telemetry`, `key-manager`, `ulc`, `cloud`, `cluster`, `network`, `cfo` | phase/registration caveats | pending |

**`orchestrator` versus `supervisor` is a live contradiction inside the catalog.** `C6` closed with
*"the Supervisor Agent is the sole orchestration and routing authority."* A second profile named
`orchestrator` with `permission_profile: orchestrator` contradicts that closure. Either the
Orchestrator Agent is the Supervisor under a second name, or `C6` needs revisiting.

### 4.3 B3 — C8 blocks the sub-system profiles

`spine`, `pillar`, `directorate`, `uvs`, `library` and `git` are profiles **about the framework
layers**. They cannot be built while the framework layers' own inventory is undecided:

- `spine` — cannot be built against an unresolved spine set (**C8**)
- `pillar` — cannot be built against an unresolved pillar set (**C10** closed at 7, so this one is
  now buildable)
- `directorate` — cannot be built against an unresolved directorate model (**C9**)

### 4.4 B4 — C2 blocks the safety-adjacent profiles

`hallco`, `deepguard`, `system-monitor`, `system-health`, `security`, `uvs` all route through the
safety/verification layer whose definition is open (**C2**).

### 4.5 B5 — Registration prerequisites are recorded but not enforced

- `CONST-A-3` (agent-registration prerequisites) is **`enforce: false`, phase 2**.
- `CONST-A-1/2`, `CONST-I-1`, `CONST-TCO-1/4`, `CONST-UVS-2`, `CONST-AU-1`, `CONST-BIG5-1/2` are
  enforced and bind every agent.
- **`CONST-A-3` is the rule that would make registration mandatory, and it does not deny.**
- The 45 profiles are declared `status: development-profiles-unregistered` — correctly, and the
  declaration must survive activation.

### 4.6 B6 — the identity layer is declared but not verified

From the integration plan, unchanged: `IdentityBundle.validate()` currently checks that issuer and
signature fields are **nonempty** — not that a signing chain verifies. `AM-XXI §3` requires a
*"uniquely versioned, time-valid, scoped, cryptographically verified Identity Bundle"*. **Nothing
in the repository can currently produce one.** Agent registration therefore has no working
mechanism even where the rules exist.

## 5. Layer mapping — what each profile's layer actually requires

| Layer | Profiles | Gate |
|---|---|---|
| **Executive (Board)** | `founder`, `ceo`, `cfo`, `cto`, `legal`, `hr` | Board charter adoption + `C9` |
| **Big-5 gates** | `hallco`, `deepguard`, `rrpo-sre`, `system-monitor`, `reasoning` | the four Article-backed spine drafts |
| **Assurance / ops** | `audit`, `security`, `system-health`, `telemetry`, `boot`, `installation` | Layers 2–3 complete |
| **Engineering** | `coding`, `build`, `global-build`, `global-debug`, `git`, `database`, `cidi`, `dataops`, `architect` | Layers 2–3 complete |
| **Domain** | `sales`, `procurement`, `library`, `provider`, `key-manager`, `token` | policy layer |
| **Framework sub-systems** | `uvs`, `ulc`, `spine`, `pillar`, `directorate`, `supervisor`, `orchestrator`, `cloud`, `cluster`, `network`, `context`, `prompt`, `research` | `C2`, `C8`, `C9` |

## 6. What can be done now, and what cannot

**Can be done now, with no new authority:**

1. **Register the reconciliation** achieved in §2.1 and correct `README.md` from 41 to 45.
2. **Record the reason for the number-6 gap** (`I1`).
3. **Regenerate the four stale profiles** so the catalog is again the source of truth (`I2`).
4. **Resolve `orchestrator` vs `supervisor`** — this is a `C6` follow-up, not a new contradiction.
5. **Draft the four Article-backed spines** (HALLCO, DEEPGUARD, RRPO-SRE, Reasoning), which is the
   precondition for five of the 45 profiles.

**Cannot be done until C2, C8, C9 close:**

6. Agent registration, activation, or the grant of a single ACT clearance.
7. Building `spine`, `directorate`, `uvs`, `security` and the safety-adjacent profiles.

## 7. Where the catalog is better than the corpus above it

Recorded because it calibrates how much to trust each layer:

- **Honest guardrails.** Almost every profile forbids claiming runtime execution when only a prompt
  profile ran. That is the fail-closed culture the Constitution asks for, written into the agents
  themselves.
- **Correct source hints.** Profiles cite real files (`src/rcaos/uvs/gates.py`, `src/rcaos/health.py`,
  `docs/phase0/THREAT_MODEL.md`) rather than aspirations.
- **`unresolved:` blocks.** Fourteen profiles openly declare what is not settled. No other layer in
  the corpus does this.
- **Correct non-claim.** `status: development-profiles-unregistered` — it does not pretend to be
  registered.

**The catalog is a better-governed artifact than several documents that outrank it.** That is worth
saying, and it is also why it must not be used as a substitute for the framework it depends on.

## 8. Recommendation

**Do not build the agents yet.** Build in this order:

```
1. Adopt the Board charter  ->  gives ratification an authority   (acts 1-3, charter §10)
2. Draft the 4 Article-backed spines                            (Layer 2)
3. Close C2, C8, C9                                             (Board's first substantive act)
4. Finish Layers 2-4
5. Then register agents, against CONST-A-3 made real
```

If speed matters more than sequencing, the **five Big-5 gate profiles** are the only ones with a
complete authority basis today (`Article X–XIV`), and they are also the five the framework needs
first. That is the one place where building an agent now is not building on sand.

---

**Publication control notice.** Analysis only. Registers no agent, grants no clearance, activates
nothing, and resolves no contradiction.
