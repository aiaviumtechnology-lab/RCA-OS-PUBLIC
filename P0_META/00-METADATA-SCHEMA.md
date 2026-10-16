# RCA-OS CONSTITUTIONAL PUBLICATION — METADATA SCHEMA (P0)

**Document ID:** `RCA-PUB-META-001`
**Document Class:** Publication Control Schema
**Version:** 1.0.0
**Digests:** pinned in `P0_META/DIGESTS.txt` (written after the digest pass completes)
**Status:** Active (publication control only — **creates no constitutional authority**)
**Date of Issue:** 2026-10-16
**Author:** RCAOS agent, for Samuel Stevenson, Founder
**Authority basis:** `Constitution/CONSTITUTIONAL REGISTER.md` §1 (precedence) and §6 (completion criteria)
**Supersedes:** the informal 8-line header ("Document Title / Class / Version / Date of Issue /
Copyright / Author / Document Status / Constitutional Binding") used in the July 2026 drafts.
**Publication class:** `PUBLIC` — safe to publish

---

## 1. Why a new header

The informal header carried no document identity, no placement in the hierarchy of norms, no
digest, no context binding and no contradiction record. A constitutional corpus cannot be
audited, diffed or mechanically verified with that header. This schema replaces it and is
**backward compatible**: the eight informal fields are preserved in `legacy_header`.

## 2. Normative field set

Every published section MUST carry these fields. A missing REQUIRED field fails the
publication gate; a section with a failed gate is not published.

| # | Field | Req | Type | Meaning / allowed values |
|---|---|---|---|---|
| 1 | `document_id` | yes | string | Stable identity, `RCA-<CLASS>-<NNN>`. Never reused. |
| 2 | `title` | yes | string | Human title of the section. |
| 3 | `document_class` | yes | enum | `CONSTITUTION` \| `CONTROL` \| `SPINE` \| `PILLAR` \| `DOCTRINE` \| `POLICY` \| `REGULATION` \| `APPENDIX` \| `PUBLICATION_CONTROL` |
| 4 | `version` | yes | semver | Content version of this section. |
| 5 | `status` | yes | enum | `ACTIVE` \| `PROPOSED` \| `DRAFT` \| `RESERVED` \| `SUPERSEDED` |
| 6 | `authority_basis` | yes | string[] | The instrument that authorises this document (Article, amendment, Register section). |
| 7 | `placement` | yes | string | Position in the hierarchy of norms — `Constitution → Governance Spine → Policy → Regulation → Directive → Config → Code`. |
| 8 | `precedence_rank` | yes | int | 1 = canonical Constitution … 6 = drafts/unregistered (Register §1). |
| 9 | `binds` | yes | enum | `ALL` \| `DIRECTORATES` \| `AGENTS` \| `SPINES` \| `SUBSTRATES` \| `NONE` |
| 10 | `mandatory` | yes | bool | Whether the document's rules are binding on its `binds` scope. |
| 11 | `enforceable` | yes | bool | Whether any mechanism currently enforces it (a binding rule may be unenforced — see §5). |
| 12 | `invariants` | yes | string[] | Invariant IDs the section states (empty array if none). |
| 13 | `cross_references` | yes | string[] | Articles, amendments, spines, pillars, rules referenced. |
| 14 | `compiled_rules` | yes | string[] | `RULES.yaml` IDs compiled from this section (empty array if none). |
| 15 | `source_path` | yes | string | Repository path of the canonical source text. |
| 16 | `source_digest` | yes | sha256 | `sha256:<hex>` of the source file **as published**. |
| 17 | `published_digest` | yes | sha256 | `sha256:<hex>` of the published Markdown file itself. |
| 18 | `supersedes` | no | string[] | Document IDs this replaces. |
| 19 | `superseded_by` | no | string | Filled only when a later version activates. |
| 20 | `ratification` | yes | object | `{evidence: "AVAILABLE"\|"OUTSTANDING"\|"NOT_REQUIRED", ledger_ref: string\|null}` — Register §4. |
| 21 | `contradictions` | yes | string[] | Open contradiction IDs (see `CONTRADICTIONS.md`); `[]` if none. **Never silently cleared.** |
| 22 | `trust` | yes | enum | `TRUSTED` \| `UNVERIFIED` \| `UNTRUSTED` — see §4. |
| 23 | `editing_policy` | yes | enum | `EXACT` \| `EDITORIAL` \| `RESTRUCTURED` — see §6. |
| 24 | `publication_class` | yes | enum | `PUBLIC` \| `INTERNAL` \| `PROHIBITED` |
| 25 | `copyright` | yes | string | Rights statement. |
| 26 | `date_of_issue` | yes | date | `YYYY-MM-DD`. |
| 27 | `legacy_header` | no | object | Original informal header, verbatim, when one existed. |

## 3. Forbidden claims

A published section MUST NOT:
1. claim ratification when `ratification.evidence != "AVAILABLE"`;
2. describe a document with `status: PROPOSED` as adopted, active or enforceable;
3. claim enforcement when `enforceable: false`;
4. cite an authority that does not exist in the Register;
5. present a publication-control document as constitutional authority.

## 4. Trust marking

Publication is a **presentation act, not a ratification act**. Because the publication
pipeline itself carries no constitutional authority, every section states how it was handled:

- `TRUSTED` — text verifies against its recorded `source_digest`, no transformation, and the
  source is a registered or canonical document.
- `UNVERIFIED` — content is transcribed or reconstructed from a source whose provenance,
  digest or authority is not confirmed.
- `UNTRUSTED` — content reaches the pipeline from an unregistered, duplicated or
  conversational source, or fails an integrity check. Publishable only with the flag intact.

**Default for every source in this corpus has not yet been asserted by the Founder; sections are
marked per their actual treating, never optimistically.**

## 5. Enforceability vs bindingness

Two different properties, previously conflated:

- **Binding** — the rule constrains behaviour (`mandatory: true`).
- **Enforced** — a mechanism currently denies non-compliance (`enforceable: true`).

`RULES.yaml` records 70 constitutional rules, of which 47 are `enforce: true` and 20 are
`enforce: false` (recorded but not yet activated). A published section whose rules are
recorded-but-not-enforced MUST say so. "Mandatory" alone is not evidence enforcement exists.

## 6. Editing policy (how faithfully the source was handled)

| Value | Meaning |
|---|---|
| `EXACT` | Reproduced without change other than mechanical reformatting; source digest recorded. |
| `EDITORIAL` | Wording preserved; formatting, headings, numbering applied. No claim reworded. |
| `RESTRUCTURED` | Text reorganised or rewritten. **Requires an explicit Founder decision**, because restructuring a run-on draft is drafting, not transcription. |

## 7. Published file shape

```
--- YAML metadata block (§2 fields) ---
# Title
> One-line status banner: class · status · placement · trust · editing policy

## Body
…verbatim or edited text, per editing_policy…

## Invariants stated in this section
## Cross-references
## Contradictions carried (or: none)
## Verification
- source_digest, published_digest, verification command
```

## 8. Verification procedure

```
sha256sum "<source_path>"      -> must equal metadata.source_digest
sha256sum "<published_path>"   -> must equal metadata.published_digest
```

Digests are recorded at publication time and re-checked before any later republication.

## 9. Legacy header mapping

| Old field | New field |
|---|---|
| Document Title | `title` |
| Document Class | `document_class` |
| Version | `version` |
| Date of Issue | `date_of_issue` |
| Copyright | `copyright` |
| Author | `author` (in `legacy_header`, plus publication `Author:` line) |
| Document Status | `status` |
| Constitutional Binding | `mandatory` + `binds` + `authority_basis` |

`Document ID`, `placement`, `precedence_rank`, `source_digest`, `published_digest`,
`ratification`, `contradictions`, `trust` and `editing_policy` have **no** counterpart in the
old header and are the reason it was insufficient.

---

**Publication control notice.** This schema governs how text is presented. It does not
interpret, amend, ratify, repeal or activate any constitutional provision.
