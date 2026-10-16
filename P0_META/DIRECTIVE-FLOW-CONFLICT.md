# DIRECTIVE-FLOW CONFLICT — ONE NAME, FOUR LAYERS

**Document ID:** `RCA-PUB-META-007`
**Document Class:** Publication Control — Layer Reconciliation Analysis
**Version:** 1.0.0
**Status:** Active (publication control only — creates no authority)
**Date of Issue:** 2026-10-16
**Publication class:** `PUBLIC`
**Triggered by:** `Constitution/Governance Directives — the constitutional instructionern itself.txt`
  (Added to the working set at 02:03 on 2026-10-16, after the C8–C11 measurement.)

---

## What this document is and is not

This document was added to give a "better understanding" of how governance is done. It does.
It carries the most concrete governance mechanism in the corpus — a four-class directive
taxonomy and an eight-stage issuance lifecycle that matches what the code actually implements.
For that, it is the most useful governance document I have read in this repository.

It also, read as written, **forbids the build order you gave me.** That is not a reading I
chose; it is what the text says when its nouns are taken in their registered sense. Below is
the exact chain, then the reconciliation, then the decision you actually have to make.

**Reconciliation is proposed here and nowhere claimed as resolved.** Nothing below is written
back into the Governance Spine; the four new contradictions (C12–C15) are carried open.

---

## 1. The conflict, in four steps

| Step | Source | Statement |
|---|---|---|
| 1 | This document §4 | The mandated lifecycle is: *Drafting (Governance Pillar) → Validation (**Integrity Spine**) → Authorization (Governance Spine) → Registration (**Master Spine**) → Propagation → Enforcement → Audit → Arbitration* |
| 2 | This document §1, §4–5 | Directives are **"binding"**, **"Henceforth law"**; **"This chain is non-bypassable"**; **"No subsystem can drift. No executor can interpret intent."** |
| 3 | Structural logic | For any directorate to *be* or *be fixed*, a directive must first pass Validation and Registration — which requires the **Integrity Spine** and the **Master Spine** |
| 4 | `SPINE_TRACEABILITY.yaml` | Neither **Integrity Spine** nor **Master Spine** is registered. Of the four spines the lifecycle depends on, two do not exist in the registry |

**Therefore, as written:** no directorate can be constitutionally formed until the directive
lifecycle runs, and the directive lifecycle cannot run until the spines exist. Layer 4 depends
on a mechanism that depends on a spine that is not in the registry. **And this document names
Governance a *Pillar*, which a literal reading makes source-of-law rather than rank-4.**

## 2. What the build order requires

```
1. Constitution  2. Spines  3. Pillars  4. Directorates  → Policies  → Regulations → Agents
```

Under this order, a **Directorate is the thing that operationalizes** a directive. It cannot be
the prerequisite for one. And the directive-lifecycle chain, read literally, makes
**Enforcement / Execution / Safety / Identity / Audit / Arbitration** — six spines — the things
that *enforce* directives, hence earlier and, in that mechanic, superior.

That is the whole conflict: **who exists first, the framework or the instrument?** The corpus
asserts both.

## 3. The reconciliation — two orders, correctly separated

This document contains **two distinct chains** and the source runs them together. Separated,
both are true and the conflict dissolves:

### 3a. Authority order — which instrument outranks which

```
Constitution → Governance Spine → Policies → Regulations → Directives → Config → Code
                                             └────────────┬────────────┘
                                          Directives rank HERE — below policies
```

Canonical basis: Article IX §9.2, `AM-XIX §4`, `CONST-HIER-1`. Article III §3.2 states it
exactly: *"Policies define enduring rules. Directives define concrete actions."*

**So a Directive is not "Henceforth law" in the sense of overriding the framework. It is the
concrete application of an existing policy.** Its bindingness is real, and it is *derived*.

### 3b. Flow order — how a decided instrument reaches the thing it governs

```
Governance (issuer) → Validation → Registration → Enforcement → Execution/Operation → Audit → Arbitration
```

This is a **lifecycle**, not a hierarchy. A spine being *downstream* in a flow does not make it
*subordinate* in authority: the Audit Spine is the last step, and is also the authority that
makes every earlier step lawful (`CONST-AU-1`). Flow position and rank are orthogonal.

### 3c. Where the issuer sits

The issuer of directives is the **Governance Directorate**, operating as the constitutional
function of the **Governance Spine**, executing the **Governance Kernel** (Article III §3.1 —
the only one of the four "Governance" senses the canonical text actually creates).

The canonical text already says this and the draft missed it: the Governance Kernel interprets
*"policies, directives, and invariants"* and enforces them *"across all substrates"*. It is a
**function**, not a fourth power. There is no **Governance Pillar** in the Constitution, and a
Pillar cannot be created by naming one.

## 4. Defence in depth — where the issuer must not be

The lifecycle has a genuine structural defect, independent of the naming:

> **The Governance Spine both *issues* the directive and *signs* it.** And the Governance
> Directorate and the Governance Spine are the same word.

An instrument validated and signed only by the party that produced it is self-validating. The
lifecycle's own stage 2 (Validation by the **Integrity Spine**) is the fix — a validator that is
*not* the issuer — but that fix is unusable while the Integrity Spine is unregistered, and it is
undermined anyway by stage 3 being the issuer's own signature.

**Minimum repair, for the Founder's consideration:** the issuer of a directive must not be its
validator, its registrar, or its auditor. Four distinct authorities, at least two of them
outside Governance. This is the same separation the corpus already requires of Founder freezes
(`AM-XXI §4`: notify *Executive, Governance, Safety, Integrity and RRPO-SRE* — five parties,
none of them the actor).

## 5. The code already agrees with the reconciled reading

Worth noting, because it settles which reading is the intended one.

`SPINE_TRACEABILITY.yaml` maps `SPINE-GOVERNANCE` with:

```yaml
implementation:
  modules: [rcaos.constitution.loader, rcaos.policy.engine]
  tests:   [tests/test_constitution_loader.py, tests/constitution/test_pillar_traceability.py]
```

The implementation binds Governance to the **constitution loader** and the **policy engine** —
it implements authority resolution, precedence and policy binding. It does **not** implement
four lower-level flows. The engineering layer already treats Governance as the **meta/framework
function**, and the "operationalizes" position belongs to the Directorates, exactly as the
build order says.

**The code and the build order agree. The draft does not. One of the two must be corrected, and
it should not be the code.**

## 6. The four new contradictions, stated plainly

| ID | In one line |
|---|---|
| **C12** | "Governance Pillar" is a fourth layer for a name that already belongs to a Directorate, a Spine, and the canonical Kernel. The Constitution creates no Governance Pillar. |
| **C13** | The mandated directive lifecycle runs through the **Integrity Spine** and the **Master Spine**. Neither is registered. The lifecycle is non-executable as written. |
| **C14** | The issuer signs the instrument it later interprets → self-validation, against `AM-XIX §8` and `GS-4`; and §1 calls directives "binding" while Article III §3.2 ranks them below policies. |
| **C15** | "Master Spine" acts as a supreme authority over workflows and a registrar of law, with no registry entry — and its claimed supremacy collides with Article IX §9.2. |

## 7. What is genuinely new and worth keeping from this document

Stated so the useful half is not lost in the defect:

1. **The four-class taxonomy** — Interpretive, Operational, Structural, Prohibitive — with
   worked examples (`Interpret Constitutional Clause`, `Define Safety Thresholds`,
   `Prohibit Identity Drift`). Reusable as-is.
2. **The principle that directives are not suggestions, policies, preferences or heuristics.**
   Consistent with Constitutional Intent's "It is law, not advice."
3. **A Directive acts as a structured update to four spines at once** — constraints and
   preconditions to Execution, risk thresholds and kill-switch conditions to Safety, logging
   and replayability mandates to Audit, escalation pathways to Arbitration (§6–§9). This is the
   most concrete governance-to-spine interface in the corpus, and it maps directly onto the
   `Interfaces` part of the spine contract in `2_GOVERNANCE-SPINE/SPINE-CONTRACT.md`.
4. **The lifecycle's shape** (draft → validate → authorise → register → propagate → enforce →
   audit → arbitrate) is correct as a *shape*. It is only the owners of stages 2 and 4 that
   don't exist.

## 8. The decision

The single decision that unblocks both this conflict and C8:

> **Is a Directorate an *output* of the governance mechanism (built at Layer 4, operationalizing
> directives), or is it a *prerequisite* of it (its Validation/Registration pathway)?**

If **output** — the build order stands, this document's §5 chain is describing *post-framework*
operation, and only the stage owners (Integrity, Master) need registering.
If **prerequisite** — the build order cannot be executed as given, and Layers 2–4 must be
reordered.

Everything else in C8–C15 becomes easier once that sentence is answered, because the answer
tells you whether Integrity and Master are spines that must exist before anything else.

---

**Publication control notice.** Analysis only. This document resolves nothing, amends nothing,
completes no layer, and creates no authority. All four contradictions it raises remain open and
must be closed by the Founder.
