# Ewing-Family-Guide — TASKS.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) ·
> Lane: donated · Risk tier: **HIGH** (patient-facing health content)

Backlog for **Ewing-Family-Guide** (slug: `ewing-family-guide`), a free, plain-language,
carefully-sourced guide for families/caregivers/AYA patients facing a Ewing sarcoma diagnosis.
It **only restates and organizes vetted-authority information** (NCI/PDQ®, COG, ESMO, CCLG), with
a citation on every assertion, at a health-literacy reading level — and **nothing patient-facing
ships until both a credentialed oncologist and a patient/caregiver advocate sign off.** See
`PLAN.md` for full context.

**Binding cancer guardrails (apply to every task):** open-access / aggregate / de-identified
educational sources **only**; controlled-access data (dbGaP, EGA, individual-level biobanks) and
any identifiable patient data are **out of scope**; verify each source's reuse license before use;
provenance on every assertion; no medical advice, diagnosis, or individual prognosis; standing
"Informational, not medical advice — consult your care team" labeling.

This is a **HIGH risk-tier** project: every **patient-facing writing task is `riskTier: high`**
and requires **dual blocking sign-off** (oncologist + patient-advocate) before it is "done." No
delivery partner, oncologist reviewer, or advocate reviewer is yet secured, so delivery/review-
dependent tasks carry `requestor: TO BE SECURED` and `verifiedNeed: false`.

## How these tasks map to Elyos

Each task below becomes an Elyos **Task JSON** validated against
`packages/schema/src/schemas.ts`. Field mapping:

- **id** — stable slug `ewing-family-guide-<area>-NNN` (e.g. `ewing-family-guide-policy-001`).
- **title** — the task title in the milestone table.
- **project** — `ewing-family-guide`.
- **type** — one of `code | research | writing | data | design-spec | maintenance`. (Content pages
  are `writing`; source vetting is `data`; checks/tooling are `code`; policy/schema are
  `design-spec`; delivery/ops are `maintenance`/`research`.)
- **lane** — `donated` (default; no funded tasks planned. Any `funded` task must add
  `fundedBudgetUsd` with a hard cap).
- **priority** — `high | medium | low`.
- **domain** — array, e.g. `["health","oncology","ewing-sarcoma","patient-education","plain-language"]`.
- **riskTier** — `low | medium | high`. **Any patient-facing content is `high`**; source/data and
  schema/tooling are `low`–`medium`.
- **urgent** — boolean (no urgent tasks at cold-start; the *fertility-preservation* topic is
  content-prioritized as time-critical *for families*, but the task itself is not `urgent` in the
  ops sense).
- **deliverable** — `pr | dataset | document | translation`.
- **tokenEstimate** — `small | medium | large` (maps to the Size column).
- **status** — `open | in-progress | review | delivered | done` (all start `open`).
- **context / objective / acceptanceCriteria[] / resources[] / output** — per task.
- **requestor** — partner/steward/reviewer; `TO BE SECURED` where unknown.
- **verifiedNeed** — `true` only once a specific partner/need is confirmed; otherwise `false`
  (currently `false` everywhere — no partner/reviewers secured).
- **outputLicense** — content/docs/datasets: `CC-BY-4.0`; any build tooling: `MIT`.

Size legend: small ≈ tokenEstimate `small`, med ≈ `medium`, large ≈ `large`.
Reviewer roles: **Oncologist** = board-certified pediatric/medical oncologist with sarcoma
experience (HIGH-tier clinical sign-off, **TO BE SECURED**); **Advocate** = patient/caregiver
advocate (HIGH-tier tone/usefulness sign-off, **TO BE SECURED**); **Maintainer** = editorial +
engineering owner. **Dual sign-off (Oncologist + Advocate)** is required on every patient-facing
page before it is "done."

---

## Milestone M0 — Editorial & safety framework (cold-start)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-policy-001 | Editorial & safety policy + dual-review gate spec (refusals, no-advice, standing labels, source-tiering) | design-spec | medium | high | document | — | Oncologist + Advocate + Maintainer |
| ewing-family-guide-sources-002 | Vetted-source allow-list + per-source license-verification protocol | data | small | medium | document | — | Maintainer + Oncologist |
| ewing-family-guide-schema-003 | Content schema + provenance model (Page/Assertion/Source) + Markdown repo | design-spec | small | low | document | 001 | Maintainer |
| ewing-family-guide-checks-004 | Build checks: citation-coverage + readability + "not medical advice" label lint + staleness | code | medium | low | pr | 003 | Maintainer |

**Acceptance criteria — key tasks**

- **ewing-family-guide-policy-001** (editorial & safety policy / guardrail spec)
  - Enumerates the **hard refusals** in concrete, testable terms: no medical advice, no diagnosis,
    no individual prognosis or "what would you do," no dosing, no choosing/refusing treatment, no
    promotion of unproven/commercial therapies, no non-vetted sources, **no patient-level or
    controlled-access data**.
  - Defines allowed content (general, population-level, source-cited education) and the
    **curate-and-translate, never generate** rule (AI may not be the source of a medical fact).
  - Specifies the **standing labels** (every page: "Informational, not medical advice — consult
    your care team"; survival-stats framing: "groups, not your child/you"; urgent-care pointer
    where relevant) and that they are template-enforced and legible (not buried).
  - Specifies the **blocking dual-review gate**: oncologist (accuracy/currency/non-advice framing/
    time-critical surfacing) **and** advocate (tone/dignity/clarity/usefulness), either can block,
    **version-scoped** sign-off, re-review on edits/stale sources, applies to **any** channel and
    to content "handed to a family," not just repo publish.
  - States the source-tiering rule (vetted allow-list only) and the **stop-and-flag** behavior for
    AI sessions that hit a refusal.
  - Reviewed and signed off by the oncologist + advocate (recorded in the reviewers ledger).

- **ewing-family-guide-sources-002** (allow-list + license protocol)
  - Establishes the vetted-body allow-list (NCI/PDQ®, COG, ESMO, CCLG; additions only by editorial
    decision with oncologist concurrence).
  - Defines the **per-source license-verification** steps and ledger fields (body, citation, URL,
    retrieval date, **verified license/reuse terms**, `lastVerified`, `validUntil`), with the
    conservative defaults: NCI/PDQ® government-work-but-non-endorsement/trademark; COG/ESMO/CCLG
    copyrighted → **restate-and-cite, no verbatim copying without recorded permission**.
  - A source with unverified or incompatible terms **cannot** back a shipped assertion.

- **ewing-family-guide-checks-004** (build checks)
  - **Citation-coverage** check fails the build if any assertion lacks ≥ 1 vetted `Source`.
  - **Readability** check fails a page that exceeds the grade bar (target ≤ grade 8).
  - **Label lint** fails a page missing the standing "not medical advice" framing.
  - **Staleness** check flags/withholds any page whose sources are past `validUntil`.

**M0 Definition of Done:** editorial & safety policy (with the dual-review gate) drafted and
slated for reviewer sign-off; vetted-source allow-list + license-verification protocol defined;
content/provenance schema + Markdown repo + CI green; the four build checks scaffolded. **No
patient-facing content drafted or shipped in M0.**

---

## Milestone M1 — Topic map + source corpus vetting

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-topicmap-005 | Family-need-ranked topic map (diagnosis-shock + time-critical first), co-designed with reviewers | research | small | medium | document | 001 | Oncologist + Advocate + Maintainer |
| ewing-family-guide-corpus-006 | Vetted source corpus assembly + per-source license verification + provenance records | data | medium | medium | dataset | 002, 003, 005 | Oncologist + Maintainer |
| ewing-family-guide-misinfo-007 | Per-topic misinformation hot-spot map (unproven cures, outdated survival stats) from vetted sources | research | small | medium | document | 005, 006 | Oncologist + Advocate |

**Acceptance criteria — key tasks**

- **ewing-family-guide-topicmap-005** (topic map)
  - Produces a need-ranked topic list ordering diagnosis-shock topics (what Ewing sarcoma is;
    understanding the diagnosis/tests/staging) and **time-critical items (fertility preservation
    *before* treatment)** first.
  - Co-designed with the oncologist + advocate (or drafted for their review until secured);
    distinguishes audience (caregiver / AYA-patient / both) per topic.
  - Defines sensitive topics (relapse, palliative/end-of-life, prognosis-adjacent) requiring extra
    review care.

- **ewing-family-guide-corpus-006** (source corpus + provenance)
  - Every candidate source is on the allow-list and has its **reuse license verified and recorded**
    (with the restate-vs-permission decision noted per source).
  - Provenance records complete (body, citation, URL, retrieval date, license, `lastVerified`,
    `validUntil`) — these become the `Source` records every assertion will cite.
  - No controlled-access or patient-level data present; verified and noted.

**M1 Definition of Done:** need-ranked topic map (reviewer-co-designed or review-ready); vetted
corpus assembled with **every source license-verified** and provenance recorded; per-topic
misinformation map done. **Gate:** ship-intended content drafting (M2) does **not** begin until
**both** reviewers are secured; otherwise the project **holds here**.

---

## Milestone M2 — Core content drafting (highest-need), held behind the gate

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-content-008 | "What is Ewing sarcoma?" + "Understanding your diagnosis: tests & staging" (plain-language, cited) | writing | medium | high | document | 004, 006, 007 | Oncologist + Advocate (dual sign-off) |
| ewing-family-guide-content-009 | "Your care team & specialist sarcoma centers" + "Treatment overview: what to expect" | writing | medium | high | document | 004, 006, 007 | Oncologist + Advocate (dual sign-off) |
| ewing-family-guide-content-010 | "Fertility preservation before treatment" (time-critical) + "Questions to ask your care team" | writing | medium | high | document | 004, 006, 007 | Oncologist + Advocate (dual sign-off) |
| ewing-family-guide-glossary-011 | Plain-language glossary (terms defined on first use, cited) | writing | small | high | document | 004, 006 | Oncologist + Advocate (dual sign-off) |

**Acceptance criteria — key tasks**

- **ewing-family-guide-content-008** ("What is Ewing sarcoma?" + diagnosis/staging)
  - Every assertion restates a **vetted source** and carries provenance (passes citation-coverage).
  - Reading level **≤ grade 8**; hard terms defined on first use; standing "not medical advice" +
    survival-stats framing ("groups, not your child/you") present.
  - Explains localized vs. metastatic and what staging means **without** giving individual
    prognosis or advice; routes to the care team.
  - Drafted **strictly from provided vetted sources** (no model-generated facts); marked `draft`,
    **not published**, until dual sign-off.

- **ewing-family-guide-content-010** (fertility preservation + questions to ask)
  - Surfaces fertility preservation as **time-critical** ("ask *before* treatment starts"),
    framed as general education sourced to vetted bodies, not advice.
  - "Questions to ask" lists vetted, neutral questions; does not script medical decisions.
  - Citation-coverage + readability + labels pass; `draft`, unpublished pending dual sign-off.

- **ewing-family-guide-glossary-011** (glossary)
  - Plain-language definitions of key terms (biopsy, staging, metastatic, chemotherapy, radiation,
    EWSR1, remission, relapse, etc.), each cited; ≤ grade 8.

**M2 Definition of Done:** top-priority pages drafted, each passing citation-coverage +
readability + label checks, with misinformation-correction included where relevant — **all marked
`draft` and none published** (publication requires M3 dual sign-off). Reached only if both
reviewers are secured.

---

## Milestone M3 — Dual expert review + sensitive topics + accessibility

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-content-012 | Sensitive topics: clinical trials (informational), relapse, palliative/end-of-life, survivorship pointer | writing | medium | high | document | 008, 009, 010 | Oncologist + Advocate (dual sign-off) |
| ewing-family-guide-review-013 | Dual sign-off pass: oncologist accuracy/currency + advocate tone/usefulness on all ship-slated pages | maintenance | medium | high | document | 008, 009, 010, 011, 012 | Oncologist + Advocate (blocking) |
| ewing-family-guide-a11y-014 | Accessibility (WCAG 2.2 AA) + print-friendly output + translation-readiness tagging | code | small | medium | pr | 008, 009, 010, 011, 012 | Maintainer + Advocate |
| ewing-family-guide-pilot-015 | Real-reader comprehension pilot (≥5 family/caregiver or advocate-proxy readers) | research | small | high | document | 013, 014 | Advocate + Maintainer |

**Acceptance criteria — key tasks**

- **ewing-family-guide-content-012** (sensitive topics)
  - Clinical-trials page is **informational only**, links to `ewing-trial-finder` (HIGH sibling),
    does not recommend or rank trials.
  - Relapse and palliative/end-of-life pages are honest **and humane**, give **no individual
    prognosis**, carry clear support-resource pointers, and get explicit advocate tone review +
    oncologist framing review.
  - Survivorship/late-effects handled as a pointer to `ewing-survivorship-late-effects`.

- **ewing-family-guide-review-013** (dual sign-off — the blocking gate)
  - **Oncologist** sign-off recorded per page for clinical accuracy, currency, non-advice framing,
    and correct surfacing of time-critical items.
  - **Advocate** sign-off recorded per page for tone, dignity, clarity, sensitivity, usefulness.
  - Sign-off is **version-scoped**; either reviewer may block; unresolved disputes escalate per
    Governance; **no page publishes without both sign-offs for its current version**.

- **ewing-family-guide-a11y-014** (accessibility + translation-ready)
  - Pages meet WCAG 2.2 AA structure (headings, reading order, alt text, contrast); print-friendly
    PDF output; tagged translation-ready for `ewing-info-translations`.

**M3 Definition of Done:** all ship-slated pages (including sensitive topics) carry recorded
**dual sign-off** for their current version; accessibility + print + translation-readiness done;
real-reader comprehension pilot passed. Content is now **eligible to ship** — pending a delivery
partner.

---

## Milestone M4 — Delivery to families (the deed)

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-partner-016 | Secure delivery partner/steward + publish dual-reviewed guide through a vetted family-facing channel | maintenance | medium | high | document | 013, 014, 015 | Steward + Oncologist + Advocate |

**Acceptance criteria — ewing-family-guide-partner-016**
- A real family-facing channel (sarcoma foundation, COG/CCLG-affiliated program, or treating-center
  patient-education office) is secured; steward assigned; `verifiedNeed` flips to `true`.
- Only **dual-signed-off, cited, accessible** pages are published/distributed; standing labels and
  currency (`validUntil`) in force.
- Driven by the **dated acquisition plan** (≥3 partners in conversation by 2026-08-31; reviewers
  by 2026-10-31). If no partner is secured by **2027-02-28**, apply the **build-vs-hold rule**
  (PLAN exec summary): pivot the last-mile beneficiary (contribute reviewed content to an existing
  trusted org's library under their governance) or hold reviewed-unpublished — **never** self-
  publish unreviewed-channel content to vulnerable families to hit a date.
- Outcomes (qualitative usefulness, reach) recorded with **no PII collected**.

**M4 Definition of Done:** project-level **Definition of Shipped** met — the dual-reviewed,
fully-cited, plain-language guide is delivered through a vetted family-facing channel and used by
real families, with "not medical advice" framing intact, provenance on every claim, and currency
in force. *(Gated on a secured partner + both reviewers — TO BE SECURED.)*

---

## Milestone M5 — Sustain, review cadence & translation hand-off

| ID | Title | Type | Size | Risk | Deliverable | Depends on | Reviewer |
|---|---|---|---|---|---|---|---|
| ewing-family-guide-ops-017 | Maintenance rotation + review-cadence/staleness live + translation-ready hand-off to ewing-info-translations | maintenance | small | medium | document | 016 | Maintainer + Oncologist + Steward |

**Acceptance criteria — ewing-family-guide-ops-017**
- Named maintenance rotation; review cadence running (sources re-verified; **oncologist re-sign-off**
  on changes, advocate too if wording changed); staleness fail-safe verified live (no page served
  past `validUntil`).
- Outcomes tracked qualitatively (usefulness, reach), **not** engagement metrics; no PII.
- Reviewed, translation-ready content handed to **`ewing-info-translations`** (which carries its
  own per-language HIGH-tier review).

**M5 Definition of Done:** project sustainably maintained, currency enforced at runtime, outcomes
tracked PII-free, and content handed off translation-ready.

---

## Backlog / future

| ID | Title | Type | Size | Risk | Deliverable | Notes |
|---|---|---|---|---|---|---|
| ewing-family-guide-content-018 | "Supporting your child & family" (siblings, school, emotional) — cited, vetted | writing | medium | high | document | Dual sign-off; advocate-led tone |
| ewing-family-guide-content-019 | "Practical & logistical" (treatment travel, what to bring, talking to your team) — non-financial-advice | writing | small | high | document | Dual sign-off; no financial advice |
| ewing-family-guide-region-020 | Region-tagged variants (US NCI/COG vs EU ESMO/CCLG) | writing | large | high | document | Only after M5; per-region reviewer + sourcing |
| ewing-family-guide-trials-link-021 | Deepen integration with ewing-trial-finder (informational) | writing | small | high | document | Link, don't duplicate; HIGH sibling gate |
| ewing-family-guide-feedback-022 | Optional PII-free family feedback mechanism | design-spec | small | medium | document | Requires fresh privacy review before any data path |

---

## Example task JSON

Complete, schema-valid Task JSON for the first M0 task (`ewing-family-guide-policy-001`):

```json
{
  "id": "ewing-family-guide-policy-001",
  "title": "Editorial & safety policy + dual-review gate spec (refusals, no-advice, standing labels, source-tiering)",
  "project": "ewing-family-guide",
  "type": "design-spec",
  "lane": "donated",
  "priority": "high",
  "domain": ["health", "oncology", "ewing-sarcoma", "patient-education", "plain-language"],
  "riskTier": "high",
  "urgent": false,
  "deliverable": "document",
  "tokenEstimate": "medium",
  "status": "open",
  "context": "Ewing-Family-Guide is a free, plain-language guide for families, caregivers, and AYA patients facing a Ewing sarcoma diagnosis. It ONLY restates and organizes vetted-authority information (NCI/PDQ, COG, ESMO, CCLG), with a citation on every assertion, at a health-literacy reading level. It is HIGH risk-tier patient-facing health content: nothing ships until both a credentialed pediatric/sarcoma oncologist AND a patient/caregiver advocate sign off (either can block). Binding cancer guardrails apply: open-access/aggregate/de-identified educational sources only; controlled-access (dbGaP, EGA, individual-level biobanks) and any identifiable patient data are out of scope; verify each source license; provenance on every assertion; no medical advice, diagnosis, or individual prognosis. This cold-start task writes the editorial & safety policy that all later sourcing, drafting, and review must implement. No delivery partner, oncologist reviewer, or patient-advocate reviewer is yet secured.",
  "objective": "Write the authoritative editorial & safety policy (the project's guardrail spec) that all later source-vetting, content drafting, and review must implement and be tested against: the hard refusals (no advice/diagnosis/individual prognosis/unproven-therapy promotion/non-vetted sources/patient-level data), the curate-and-translate-never-generate rule, the standing 'not medical advice' and survival-statistics framing labels, the vetted-source tiering rule, and the blocking dual-review gate (oncologist + patient-advocate, version-scoped, either can block, applies to any channel).",
  "acceptanceCriteria": [
    "Enumerates the hard refusals in concrete, testable terms: no medical advice, no diagnosis, no individual prognosis or 'what would you do', no dosing, no choosing/refusing treatment, no promotion of unproven/commercial therapies, no non-vetted sources, and no patient-level or controlled-access data",
    "Defines allowed content as general, population-level, source-cited education and states the curate-and-translate, never generate rule (AI may not be the source of a medical fact)",
    "Specifies the standing, template-enforced labels on every page: 'Informational, not medical advice - consult your care team', the survival-statistics framing ('groups, not your child/you'), and an urgent-care pointer where relevant - and requires they be legible, not buried",
    "Specifies the blocking dual-review gate: oncologist (accuracy/currency/non-advice framing/time-critical surfacing) AND patient-advocate (tone/dignity/clarity/usefulness) sign-off, either may block, version-scoped sign-off that expires on edits or stale sources, applying to any channel and to content handed to a family - not only repo publish",
    "States the source-tiering rule (vetted allow-list only: NCI/PDQ, COG, ESMO, CCLG; additions only by editorial decision with oncologist concurrence) and the per-source license-verification requirement",
    "Defines the stop-and-flag behavior for AI sessions or contributors that hit a refusal (advice creep, unsourced fact, non-vetted source, patient data) rather than working around it",
    "Reviewed and signed off by a credentialed pediatric/sarcoma oncologist and a patient/caregiver advocate, recorded in the reviewers ledger (version-scoped, with consent and no implied endorsement)"
  ],
  "resources": [
    "planning/projects/ewing-family-guide/PLAN.md",
    "governance/proposals/ewing-family-guide.md",
    "CLAUDE.md",
    "docs/good-deed-definition.md",
    "packages/schema/src/schemas.ts",
    "planning/ROADMAP.md",
    "planning/projects/public-official-guide/PLAN.md"
  ],
  "output": "A reviewed editorial & safety policy document (the guardrail spec) defining the hard refusals, allowed content, curate-and-translate rule, standing labels, vetted-source tiering + license-verification requirement, stop-and-flag behavior, and the blocking dual-review gate - the contract that ewing-family-guide-sources-002 (allow-list/license protocol), ewing-family-guide-checks-004 (build checks), and every patient-facing writing task implement and are verified against.",
  "requestor": "TO BE SECURED",
  "verifiedNeed": false,
  "outputLicense": "CC-BY-4.0"
}
```

---

## Generated task index

Every backlog row above is now materialized as a schema-valid `tasks/<id>.json`
(validated against `packages/schema/src/schemas.ts`; all start `status: open`,
`lane: donated`, `urgent: false`, `verifiedNeed: false`, `requestor: TO BE SECURED`).
All 22 tasks pass the Elyos task validator (filenames == ids, no duplicates, no extra keys).

**Fan-out:** none. Each `TASKS.md` row maps 1:1 to a single task JSON — there is no
plan-enumerated dimension (no fixed language/dataset/document set) to expand. Pages that
bundle two topics (008, 009, 010) are kept as one task per the row, with both outputs named.
Region variants (020) are intentionally **not** pre-split per region until M5 secures
per-region reviewers and sourcing.

**Guardrails preserved verbatim in the JSON:** HIGH risk-tier on every patient-facing
writing task; the binding cancer guardrails (open-access/aggregate/de-identified sources only;
controlled-access and patient-level data out of scope; license-verify each source; provenance
on every assertion; no advice/diagnosis/individual prognosis); the curate-and-translate,
never-generate rule; standing "not medical advice" + survival-stats framing labels; and the
blocking dual sign-off (oncologist + patient-advocate, version-scoped, either can block).
No task authors refused content (no advice, eligibility, trial ranking, or prognosis): the
clinical-trials work (012, 021) is informational-only and links to `ewing-trial-finder`.

- **M0** — `ewing-family-guide-policy-001` (seed), `-sources-002`, `-schema-003`, `-checks-004`
- **M1** — `ewing-family-guide-topicmap-005`, `-corpus-006`, `-misinfo-007`
- **M2** — `ewing-family-guide-content-008`, `-content-009`, `-content-010`, `-glossary-011`
- **M3** — `ewing-family-guide-content-012`, `-review-013`, `-a11y-014`, `-pilot-015`
- **M4** — `ewing-family-guide-partner-016`
- **M5** — `ewing-family-guide-ops-017`
- **Backlog/future** — `ewing-family-guide-content-018`, `-content-019`, `-region-020`,
  `-trials-link-021`, `-feedback-022`

Build-tooling tasks (`-checks-004`, `-a11y-014`) carry `deliverable: pr` and
`outputLicense: MIT`; all content/spec/dataset tasks carry `outputLicense: CC-BY-4.0`.
