# Ewing-Family-Guide — PLAN.md

> Status: Draft · Version: 0.1.0 · Last updated: 2026-06-28 · Owner: TBD (maintainer) ·
> Lane: donated · Risk tier: **HIGH** (patient-facing health content)

A free, plain-language, **carefully sourced** guide for families, caregivers, and patients
facing a diagnosis of **Ewing sarcoma** — a rare bone/soft-tissue cancer that most often
strikes children, adolescents, and young adults (AYA). The guide explains, in clear and humane
language, what the diagnosis means, what the journey of tests and treatment typically looks
like, what questions to ask the care team, and where to find trusted support — so that a family
in one of the most frightening moments of their lives can understand and participate in their
child's (or their own) care.

**This guide is education, not medical advice.** Every page carries the standing label
*"Informational, not medical advice — always consult your care team,"* every assertion is
traced to a vetted authority, and **nothing patient-facing ships until it has passed a blocking
review by both a credentialed pediatric/sarcoma oncologist and a patient/caregiver advocate.**
We treat the families who will read this as people in crisis who deserve accuracy, dignity, and
honesty — not approximate information.

---

## Executive summary

A family hears the words "Ewing sarcoma" and the ground disappears. It is rare (roughly 1 in a
million per year; ~200 new cases/year in the US, ~similar in the EU), it is aggressive, the
treatment is long and brutal (months of multi-agent chemotherapy plus surgery and/or radiation),
and almost no one outside pediatric oncology has ever heard of it. The reputable information that
exists — from the National Cancer Institute (NCI), the Children's Oncology Group (COG), the
European Society for Medical Oncology (ESMO), and the Children's Cancer and Leukaemia Group
(CCLG) — is accurate but fragmented, written at a reading level far above where a frightened
parent can absorb it, and scattered across institutional PDFs. Families fall back on web search
and forums, where they meet a mix of outdated statistics, miracle-cure misinformation, and
well-meaning but wrong advice. **The harm of bad information here is not abstract: it can drive
families toward unproven treatments, away from specialist sarcoma centers, or into avoidable
panic and despair.**

Ewing-Family-Guide closes that gap with a single, coherent, plain-language guide that *only*
restates and organizes what vetted authorities already say, with a citation on every claim, at a
reading level a stressed non-expert can actually use, reviewed for clinical accuracy by an
oncologist and for humanity, tone, and lived-experience usefulness by a patient/caregiver
advocate. It does **not** generate new medical claims, does **not** give advice, and does **not**
substitute for the care team — it is a map and a translator, not a doctor.

The single most important design fact is the **review gate**. This is a HIGH risk-tier project
under `docs/good-deed-definition.md` (health domain → credentialed expert sign-off before
merge). For this project the gate is *two* credentialed roles, both blocking, and it is the
spine of the whole pipeline, not a final rubber stamp:

> **No patient-facing page ships, in any channel, until (1) a credentialed pediatric/sarcoma
> oncologist has signed off on clinical accuracy and currency, AND (2) a patient/caregiver
> advocate has signed off on tone, dignity, plain-language clarity, and lived-experience
> usefulness. Either reviewer can block. Sign-off is version-scoped and expires when the
> content or its sources change. A page that has not cleared both gates is not "done," is not
> published, and is not handed to any family.**

The **cancer data guardrails are binding and lead both the data and the quality sections**: we
use **only open-access, aggregate, or de-identified information** sourced from vetted public
bodies; **controlled-access data (dbGaP, EGA, individual-level biobanks) and any identifiable
patient data are strictly out of scope**; we verify the reuse license of every source before a
word of it is used; and we attach provenance to every assertion. This guide does not touch
patient-level data at all — it is a curation and plain-language-translation deed over already-
public, authoritative educational material.

Honesty note: **no partner organization, no oncologist reviewer, and no patient-advocate
reviewer is yet secured.** Every delivery- and review-dependent task is marked `TO BE SECURED`
with `verifiedNeed: false`. The project is not "shipped" when a document is merged; it is
shipped only when a real family-facing channel (a sarcoma foundation, a treating center's family
resource desk, or an equivalent steward) puts the reviewed guide in front of real families and
we can see it being used. Until the two reviewers and a delivery partner are secured, the
project builds the editorial framework, the source-vetting protocol, and *draft, unpublished*
content held behind the review gate.

**Partner & reviewer acquisition plan (dated) + build-vs-hold decision rule.** Outreach is
time-boxed against the build, not open-ended: by **2026-08-31**, ≥ 3 candidate delivery partners
(a pediatric-sarcoma foundation, a COG/CCLG-affiliated family-support program, or a treating
center's patient-education office) are in active conversation and the editorial framework is
drafted; by **2026-10-31**, a credentialed oncologist reviewer and a patient/caregiver advocate
reviewer are both secured (this gates all content drafting that is meant to ship). **Decision
rule:** if *both* reviewers are not secured by the M2 entry date, content drafting intended for
publication does **not** start — the project holds at M1 (framework + source vetting), because
unreviewed patient-facing health content must never be the thing that ships. If no delivery
partner is secured by **2027-02-28**, the project does **not** self-publish to an unknown
audience: it either (a) **pivots** the last-mile beneficiary (e.g., contribute the reviewed,
cited content to an existing trusted sarcoma-org library under their editorial governance), or
(b) **holds** as a reviewed-but-unpublished reference, recorded in governance — rather than
pushing unvetted-channel content at vulnerable families.

---

## Problem & beneficiaries

**Who is helped (directly):** families and caregivers of a child, adolescent, or young adult
newly diagnosed with Ewing sarcoma — and AYA patients themselves — in the first weeks and months
after diagnosis, when the need to understand is highest and capacity to absorb dense clinical
material is lowest. Secondary direct beneficiaries: extended family (grandparents, the patient's
siblings' caregivers) and non-specialist front-line clinicians (a community pediatrician or ER
nurse) who want a trustworthy plain-language reference to share.

**Who is helped (ultimately):** the patient, through a more informed, more engaged, calmer
family that can participate in shared decision-making, ask better questions, get to a specialist
sarcoma center faster, and avoid misinformation-driven harm.

**The need.** Ewing sarcoma is rare enough that most families have never heard of it and most
local clinicians rarely see it. Authoritative information exists but is (a) **fragmented** across
NCI, COG, ESMO, CCLG and individual cancer-center sites; (b) **written above the reading level**
a person in acute distress can use (much patient material sits at a 11th–14th-grade reading
level; health-literacy guidance targets ~6th–8th grade); (c) **uneven on the hard topics**
families most need plain talk about (what staging means, what "metastatic" changes, fertility
preservation before treatment, relapse, and palliative/end-of-life care); and (d) surrounded, in
ordinary web search, by **outdated survival statistics and active misinformation** (unproven
"natural cures," supplement claims, clinics selling false hope). The downside of bad information
in this disease is severe and concrete — delayed specialist referral, refused or interrupted
standard treatment, financial exploitation, and compounded trauma.

**Verified need / partner:** **TO BE SECURED.** No sarcoma foundation, treating center,
oncologist reviewer, or patient-advocate reviewer has yet agreed to co-develop, review, or
distribute this guide. Target partner profiles to pursue: a pediatric/AYA **sarcoma foundation**
or patient-advocacy organization; a **COG-** or **CCLG-affiliated** family-support or
patient-education program; a treating **children's cancer center's** patient-education office;
and, for review, a board-certified **pediatric or medical oncologist with sarcoma experience**
plus an experienced **patient/caregiver advocate** (ideally someone with lived Ewing or
pediatric-cancer experience). Until they are secured, all delivery/review-dependent work is
`TO BE SECURED` with `verifiedNeed: false`, and the dated acquisition plan above governs what
happens if the dates slip (hold at M1 without reviewers; pivot or hold-unpublished without a
delivery partner) — we do not ship unreviewed health content to families to hit a date.

---

## Goals and non-goals

**Goals**

- Produce a free, openly-licensed, plain-language Ewing sarcoma guide for families/caregivers/AYA
  patients that **only restates and organizes vetted-authority information**, with a citation on
  every assertion.
- Hit a real **health-literacy bar** (target reading level ~grade 6–8; tested, not assumed) so a
  frightened non-expert can actually use it.
- Make **oncologist + patient-advocate dual review a hard, blocking gate** before any page ships,
  with version-scoped sign-off and a re-review trigger when sources change.
- Cover the hard, often-neglected topics families need plain talk about — staging, what
  metastatic disease means, **fertility preservation before treatment** (time-critical),
  clinical-trial participation (informational), relapse, and palliative/end-of-life care —
  honestly and humanely.
- Build a **source-provenance system** so every claim is traceable to a named vetted body, a
  citation, a retrieval date, and a verified reuse license.
- Make the content **accessible and translation-ready** (WCAG-aligned, plain structure) so it can
  later feed `ewing-info-translations` without re-architecting.
- Deliver the reviewed guide through a real family-facing channel and confirm it reaches families.

**Non-goals**

- **Not medical advice, diagnosis, prognosis-for-an-individual, or treatment recommendation.** It
  never tells a specific family what to do, never estimates *their* child's odds, never suggests
  choosing or refusing a treatment.
- **Not a source of new medical claims.** It does not synthesize, infer, or extrapolate beyond
  what vetted authorities state; it does not "fill gaps" with the model's own knowledge.
- Not a clinical decision tool, symptom checker, triage tool, or anything that simulates a
  clinician.
- Not a research/data project: **no patient-level data, no controlled-access datasets, no
  re-analysis of biology.** (Those live in sibling Ewing projects; this guide may *link* to their
  published, family-appropriate outputs but does not produce them.)
- Not a fundraising vehicle, and not a promotion for any particular hospital, clinic, product,
  supplement, or commercial therapy.
- Not a forum, a community, or a place that collects family stories or PII at launch.
- Not a substitute for the treating care team, the social worker, or qualified counsel — it
  routes families *to* those people, repeatedly and explicitly.

---

## Success metrics (outcomes)

Outcome-centric and beneficiary-first. Pageviews and "engagement" are explicitly **not** success;
a guide that is accurate, trusted, and actually used by families in crisis is.

| Metric | Baseline | Target | How measured |
|---|---|---|---|
| Patient-facing pages with recorded **dual sign-off** (oncologist + advocate) before publish | none | **100%** of shipped pages | Governance/reviewer ledger; pre-publish gate check |
| Assertions carrying a **vetted-source citation + provenance** | none | **100%** of shipped assertions | Citation-coverage check in the build; reviewer audit |
| Source license verified before use | none | **100%** of sources | Source-vetting ledger; license field required |
| **Readability** of shipped pages (plain-language bar) | typical patient material ~grade 11–14 | **≤ grade 8** (target 6–8) on each shipped page, with hard medical terms defined on first use | Automated readability score (e.g. Flesch–Kincaid/SMOG) + advocate plain-language review |
| **Currency**: no page served past its `validUntil` without re-review | n/a | **0** stale pages served as current | Staleness check against `lastVerified`/`validUntil`; auto-flag/withhold |
| Misinformation-correction coverage on high-risk topics (unproven cures, outdated survival stats) | n/a | each high-risk topic page **explicitly addresses** the common misinformation and points to vetted sources | Editorial checklist + oncologist review |
| **"Not medical advice / consult your care team"** labeling present and clear | n/a | **100%** of pages; verified legible (not buried) | Template lint + advocate review |
| Time-critical topics surfaced early (esp. **fertility preservation before treatment**) | n/a | flagged prominently, with "ask *before* treatment starts" framing | Oncologist + advocate review |
| Reading-ease confirmed with **real readers** before broad release | n/a | ≥ 5 family/caregiver readers (or advocate-proxy) review comprehension in a pilot | Pilot comprehension check |
| Delivered through a **real family-facing channel** | not delivered | guide live in ≥ 1 vetted partner channel reaching families | Steward confirmation |
| Families/caregivers reached + finding it useful | 0 | partner-attested usefulness from ≥ a small cohort (qualitative) | Partner/steward feedback (no PII collected) |

The **defining success outcome** (Definition of Shipped): the dual-reviewed, fully-cited,
plain-language guide is delivered through a trusted family-facing channel and real families use it
to better understand the diagnosis and engage with their care team — with clinical accuracy
signed off by an oncologist, tone/dignity/usefulness signed off by a patient advocate, the "not
medical advice" framing intact, and provenance on every claim.

---

## Scope

**In scope**

- A structured set of plain-language guide pages/sections (the topic map is co-designed with the
  patient advocate and oncologist — see *Architecture*), each restating vetted-authority
  information with citations.
- An **editorial & safety policy** (the project's "guardrail spec"): what may be stated, the hard
  refusals (no advice/prognosis/diagnosis), the standing "not medical advice" labeling, the
  source-tiering rules, and the dual-review gate.
- A **source-vetting + provenance system**: an allow-list of vetted bodies, per-source license
  verification, and a provenance record (source, citation, retrieval date, URL, license,
  `lastVerified`/`validUntil`) attached to every assertion.
- A **readability/plain-language process** (target grade 6–8, glossary, terms defined on first
  use) and a **dignity/tone standard** for sensitive topics.
- **Accessibility & translation-readiness** (WCAG 2.2 AA-aligned structure, alt text, clear
  headings, reading order) so the content can later feed `ewing-info-translations`.
- Honest coverage of the **hard topics**: staging and what metastatic means; fertility
  preservation *before* treatment; clinical-trial participation (informational, links to
  `ewing-trial-finder`); relapse; and palliative/end-of-life care, handled with care.
- A **misinformation-correction** approach on high-risk topics, sourced to vetted bodies.
- Delivery of the reviewed guide through a vetted family-facing channel and outcome tracking.

**Out of scope (explicitly will NOT do)**

- **Any medical advice, diagnosis, individual prognosis, or treatment recommendation** — including
  "what would you do," dosing, choosing/refusing therapy, or estimating a specific patient's
  odds. The guide gives general, population-level, source-cited education only.
- **Any patient-level, identifiable, or controlled-access data** — dbGaP, EGA, individual-level
  biobanks, medical records, or any identifiable patient information. This project does not
  request, store, or process such data at all. (Binding cancer guardrail.)
- **New medical/biological claims, synthesis, or extrapolation** beyond what vetted authorities
  publish; no model-generated "facts" without a citable vetted source.
- Non-vetted sources: random web pages, forums, blogs, vendor/clinic marketing, social media,
  preprints used as patient-facing fact, or AI-generated medical content from elsewhere.
- Collecting family stories, testimonials, PII, or any health information from readers at launch.
- Promoting, ranking, or steering toward any specific hospital, clinic, doctor, product,
  supplement, or commercial therapy.
- Auto-translation shipped without per-language qualified review (that is `ewing-info-
  translations`' scope and its own HIGH-tier gate).
- Self-publishing reviewed-but-undelivered content to an unknown audience to "hit a date" — see
  the build-vs-hold rule.

When a contributor or AI session is tempted toward an out-of-scope item (e.g., a drafting prompt
that would have the model state a survival figure from memory, or soften a refusal into soft
advice), the editorial policy requires it to **stop and flag** rather than proceed (mirrors the
Elyos refusal guardrails in `CLAUDE.md`).

---

## Solution approach & architecture

This is a **content/writing deed**, not a software product, so the "architecture" is an editorial
pipeline, a content schema, and a provenance system — engineered with the same rigor a codebase
would get. AI sessions draft and structure; humans (and especially the two credentialed
reviewers) are the load-bearing quality layer.

**Content model (the unit of work).** The atomic unit is a **guide page** (a topic), composed of
**assertions**. Each assertion is a plain-language statement plus a structured **provenance
record**:

```
Assertion {
  text:          plain-language statement (grade 6-8)
  sources:       [ Source ]            # >= 1 vetted source required ("no source, no claim")
  reviewStatus:  draft | onco-reviewed | advocate-reviewed | dual-approved
}
Source {
  body:          NCI | COG | ESMO | CCLG | <vetted body on the allow-list>
  citation:      human-readable citation
  url:           canonical URL
  retrievedOn:   date
  license:       verified reuse terms (see Data section)
  lastVerified:  date
  validUntil:    date (per review interval)
}
Page {
  topic, audience (caregiver | AYA-patient | both),
  readingLevel:  measured score,
  assertions:    [ Assertion ],
  notMedicalAdvice: true (template-enforced),
  signoff:       { oncologist: {who, version, date}, advocate: {who, version, date} }
}
```

A page may not publish unless **every** assertion has ≥ 1 vetted source and the page has both
sign-offs for its current version. This is the content equivalent of "no source, no claim" + a
two-key release gate.

**Editorial pipeline (the stages every page passes through):**

1. **Topic map & need-ranking** — co-designed with the advocate + oncologist; orders pages by
   family need (diagnosis-shock topics and time-critical items like fertility preservation
   first).
2. **Source vetting** — for each topic, gather candidate material *only* from the vetted-body
   allow-list; verify each source's reuse license; record provenance. Non-vetted material is
   rejected at this stage.
3. **Drafting** — an AI session drafts the page **strictly from the vetted sources provided**, at
   the target reading level, defining terms on first use, with the "not medical advice" framing
   and citations inline. The drafting prompt forbids unsourced claims, advice, prognosis, and
   reaching beyond the provided sources.
4. **Citation & readability checks** — automated: every assertion has a source; readability score
   ≤ grade 8; required labels present; glossary terms linked.
5. **Oncologist review (blocking)** — clinical accuracy, currency, correct framing, no advice
   creep, time-critical items correctly surfaced. Can require changes or block.
6. **Patient-advocate review (blocking)** — tone, dignity, plain-language clarity, lived-
   experience usefulness, sensitivity on hard topics, that it answers what families actually ask.
   Can require changes or block.
7. **Dual sign-off recorded** — version-scoped; only now may the page publish.
8. **Accessibility & translation-readiness pass** — WCAG structure, alt text, clean reading
   order; tagged ready for `ewing-info-translations`.
9. **Delivery** through the vetted partner channel; **review-cadence clock** starts
   (`validUntil`).

**Formats & tooling.** Source content authored in **Markdown** with structured front-matter
(topic, audience, sources, reading-level, sign-off) in a Git repo so every change is reviewable
and provenance is diffable. Build tooling (lightweight, TypeScript/ESM per Elyos conventions):
a **citation-coverage check** (fail if any assertion lacks a vetted source), a **readability
check** (fail if a page exceeds the grade bar), a **label lint** (fail if "not medical advice"
framing is missing), and a **staleness check** (flag/withhold pages past `validUntil`). Output
rendered to accessible HTML and a print-friendly PDF (families value printable material at the
bedside). No reader data is collected; static delivery (no accounts, no tracking).

**Key decisions.**

- **Dual human review is the architecture**, not a checkpoint — the pipeline is built around two
  blocking gates.
- **Curate-and-translate, never generate** — the AI restates vetted sources in plain language; it
  is forbidden from being the source of a medical fact.
- **Provenance is structural** — "no source, no claim" is enforced by tooling, not goodwill.
- **Plain language is measured**, not assumed (readability scoring + real-reader comprehension).
- **Agent-neutral / Elyos-aligned** — Markdown + simple TS checks; no vendor lock-in; the CLI
  never runs an agent headless (donated lane).
- **Translation-ready by construction** so the high-value multilingual follow-on
  (`ewing-info-translations`) is cheap and safe.

---

## Data, licensing & compliance

> **CANCER GUARDRAILS LEAD HERE (binding).** This project uses **only open-access, aggregate, or
> de-identified educational information from vetted authorities.** **Controlled-access datasets
> (dbGaP, EGA, individual-level biobanks) and ANY identifiable patient data are OUT OF SCOPE** —
> not requested, not stored, not processed. This is a curation-and-plain-language deed over
> already-public, authoritative *educational* material; it does **not** touch patient-level data,
> genomics under access control, or medical records. Every source's **reuse license is verified
> before any of its content is used**, and **provenance is attached to every assertion.**

**Source allow-list (vetted bodies only).** Patient-facing assertions may be sourced **only**
from an explicit allow-list of vetted authorities, primarily:

- **NCI** (National Cancer Institute) — PDQ® and patient/caregiver education.
- **COG** (Children's Oncology Group) — family handbook / patient-education materials.
- **ESMO** (European Society for Medical Oncology) — patient guides.
- **CCLG** (Children's Cancer and Leukaemia Group, UK) — family information.
- Additional vetted bodies may be added **only** by editorial decision with the oncologist's
  concurrence (e.g., a major specialist sarcoma center's patient-education office, a national
  cancer institute's patient material) — each still license-verified and provenance-recorded.

Forums, blogs, vendor/clinic marketing, social media, general web pages, and AI-generated medical
content from elsewhere are **not** acceptable sources for any assertion.

**Licensing is verified per source (conservative).** Vetted bodies have **different and specific
reuse terms**, and we do **not** assume reuse is permitted:

- **NCI / PDQ®** content is generally a U.S. Government work and **not under copyright** in the
  US, but **the PDQ® name and trademark are protected** and **must not** imply NCI endorsement;
  attribution and non-endorsement framing are required.
- **COG, ESMO, CCLG** materials are typically **copyrighted by those organizations**; reuse
  beyond fair quotation/linking generally **requires permission**. We therefore **prefer to
  restate facts in our own plain language with citation + link**, and we **do not copy
  substantial verbatim text** without explicit permission recorded in the source ledger.
- The safe default is **link + cite + restate-in-plain-language**, never wholesale copying; where
  an organization's permission is needed (e.g., to adapt a handbook), it is **secured and
  recorded before use**, or that source is not used.

A per-source **license-verification ledger** is a build artifact and a gate: a source with
unverified or incompatible terms cannot back a shipped assertion.

**Provenance model.** Every assertion carries ≥ 1 `Source` (body, citation, URL, retrieval date,
verified license, `lastVerified`, `validUntil`). A citation-coverage check fails the build if any
assertion lacks a vetted source. Reviewers can trace any statement on the page back to the exact
authority it came from.

**Currency / staleness is fail-safe, not best-effort.** Cancer information changes (survival
figures, standard-of-care, trial landscape). Each `Source` has a `validUntil` derived from a
per-topic review interval (e.g., survival statistics and treatment-overview pages on a shorter
cadence; glossary/structural pages longer). At serve time, a page whose backing sources are past
`validUntil` is **auto-flagged or withheld** ("this page is past its review window — please
verify with your care team") and routed to re-review; it cannot return to normal service until
re-verified and **re-signed-off by the oncologist** (and advocate if wording changed). This makes
the worst failure mode — *the guide silently goes out of date and misleads a family* — a visible,
gated event.

**Output licensing.** Content/text: **CC-BY-4.0** (free reuse with attribution; preserves
attribution to primary vetted sources). Any small build tooling: **MIT**. Docs: CC-BY-4.0.
NCI/PDQ® citations preserve the non-endorsement notice; copyrighted-source facts are
restated-and-cited, not relicensed.

**Privacy / PII stance (conservative).** The guide **collects no reader data** — no accounts, no
analytics that identify readers, no health information, no family stories at launch. Because it
touches **no patient-level data**, the patient-data attack surface is essentially eliminated by
design. No secrets, tokens, or any PII are written into the repo, build artifacts, or logs (Elyos
rule). If a future phase ever introduces feedback collection, it goes through a fresh privacy
review and is out of scope here.

**Attribution.** Each page cites and links its vetted sources; redistribution preserves
attribution per CC-BY. Reviewers (oncologist, advocate) are credited, **with consent**, in a
reviewers ledger, scoped to the versions they approved, with **no implication of endorsement**
beyond what they reviewed.

---

## Quality, review & risk gates

> **CANCER GUARDRAILS + THE BLOCKING DUAL-REVIEW GATE LEAD HERE.** This is a **HIGH risk-tier**
> project (`docs/good-deed-definition.md`: health content requires credentialed expert sign-off
> before merge). For patient-facing Ewing content the gate is **two** credentialed roles, **both
> blocking**, and review is woven through the pipeline — it is not a final formality.

**THE BLOCKING GATE (binding, non-negotiable):**

> **No patient-facing page ships — in the repo's published output, in any partner channel, or to
> any family — until BOTH of the following are recorded for the page's current version:**
> 1. **A credentialed pediatric/sarcoma oncologist** has signed off on **clinical accuracy,
>    currency, correct (non-advice) framing, and that time-critical items (e.g., fertility
>    preservation before treatment) are correctly surfaced.**
> 2. **A patient/caregiver advocate** has signed off on **tone, dignity, plain-language clarity,
>    sensitivity on hard topics, and lived-experience usefulness.**
>
> **Either reviewer can block.** Sign-off is **version-scoped**: it attaches to a specific
> content version and source set and does **not** carry forward to edits or to sources that have
> gone stale — those require **re-review**. A page that has not cleared **both** gates is not
> "done," is **not published**, and is **not handed to any family.**

**Required reviews before a deed is "done":**

- **Maintainer / editorial review** on every change (structure, citation coverage, readability,
  label presence, no scope/advice creep, provenance complete).
- **Oncologist sign-off (blocking, HIGH-tier)** — recorded before any clinical content ships.
  **No oncologist, no ship.**
- **Patient-advocate sign-off (blocking, HIGH-tier)** — recorded before any patient-facing page
  ships. **No advocate, no ship.**
- **Sensitive-topic extra care** — relapse, palliative/end-of-life, and prognosis-adjacent pages
  require explicit advocate tone review and oncologist framing review, and must avoid individual
  prognosis entirely.
- **Real-reader comprehension check** (pilot) before broad release — ≥ 5 family/caregiver readers
  (or advocate-proxied) confirm the content is understandable and not distressing in avoidable
  ways.

**Standing labels (template-enforced on every page):** *"Informational, not medical advice —
always consult your care team,"* plus, where relevant, *"Survival statistics describe groups, not
your child/you — your care team can explain what they mean for your situation,"* and a clear
"when to call your care team / seek urgent help" pointer where appropriate (sourced).

**Definition of Shipped (project):** the dual-reviewed (oncologist + advocate), fully-cited,
plain-language, accessibility-ready guide is **delivered through a vetted family-facing channel**
and used by real families — with every assertion provenance-backed, the "not medical advice"
framing intact, currency in force (nothing served past `validUntil`), and the misinformation-
correction coverage on high-risk topics verified. Merge ≠ shipped.

---

## Roadmap & milestones

Phased: editorial/safety framework and source vetting first; drafting only behind the dual-review
gate; delivery to families last and gated on a secured partner and both reviewers.

- **M0 — Editorial & safety framework (cold-start).**
  *Goal:* the rules, the source allow-list, and the content/provenance system exist before a
  single patient-facing word is drafted.
  *Exit:* editorial & safety policy (the "guardrail spec": refusals, no-advice rule, standing
  labels, source-tiering, the dual-review gate) drafted; vetted-source **allow-list + license-
  verification protocol** defined; content schema + provenance model + the citation/readability/
  label/staleness **checks** scaffolded; Markdown repo + CI green; reviewer-acquisition outreach
  begun. **No patient-facing content ships in M0.**

- **M1 — Topic map + source corpus vetting.**
  *Goal:* know exactly what to write and from which verified sources, ranked by family need.
  *Exit:* topic map co-designed with the advocate + oncologist (or, until secured, drafted for
  their review) and need-ranked (diagnosis-shock + time-critical topics first); the vetted-source
  corpus assembled with **every source license-verified** and provenance recorded; misinformation
  hot-spots per topic identified. **Gate:** content drafting intended to ship does **not** begin
  until **both** reviewers are secured (decision rule in the exec summary).

- **M2 — Core content drafting (highest-need topics), held behind the gate.**
  *Goal:* draft the most-needed pages, fully cited and at the reading-level bar — *unpublished*
  until reviewed.
  *Exit:* draft pages for the top-priority topics (what Ewing sarcoma is; understanding the
  diagnosis/tests/staging; the care team & specialist centers; treatment overview & what to
  expect; **fertility preservation before treatment**; questions to ask the care team) — each
  passing citation-coverage + readability + label checks; misinformation-correction included.
  All marked `draft`, **none published**.

- **M3 — Dual expert review + sensitive topics + accessibility.**
  *Goal:* clear the blocking gate; add the hard topics with extra care; make it accessible and
  translation-ready.
  *Exit:* oncologist **and** advocate sign-off recorded for each page slated to ship; sensitive
  pages (clinical trials [informational], relapse, palliative/end-of-life, survivorship pointer)
  drafted and dual-reviewed with explicit tone/framing review; WCAG 2.2 AA structure + alt text +
  print-friendly output; glossary complete. Real-reader comprehension check passed.

- **M4 — Delivery to families (the deed).**
  *Goal:* a real family-facing channel puts the reviewed guide in front of real families.
  *Exit (Definition of Shipped):* a secured partner/steward publishes/distributes the dual-
  reviewed, cited guide; families reach and use it; outcomes (qualitative usefulness, no PII)
  recorded; currency in force. *(Gated on a secured partner + both reviewers — TO BE SECURED.)*

- **M5 — Sustain, review cadence & translation hand-off (post-delivery).**
  *Goal:* keep it accurate over time and enable the multilingual follow-on.
  *Exit:* maintenance rotation + review-cadence clock running (re-verify sources; re-sign-off on
  changes); staleness fail-safe verified live; content handed, translation-ready, to
  `ewing-info-translations` (which carries its own per-language HIGH-tier review).

Dependencies flow M0 → M1 → M2 → M3 → M4 → M5. The **two reviewers gate M2's ship-intent and all
of M3–M4**; the **delivery partner gates M4**. M2 may *draft* before reviewers are secured only
as explicitly-unpublished work; if reviewers are not secured by the M2 entry date, the project
**holds at M1** rather than producing ship-intended unreviewed health content.

---

## Work breakdown

The itemized, schema-mapped backlog lives in **`TASKS.md`**: ~16 tasks across milestones M0–M5
plus a future backlog, each mapped to the Elyos Task JSON schema, with per-task acceptance
criteria for the most important items, milestone Definitions of Done, and a complete, schema-valid
example Task JSON for the first M0 task (the editorial & safety policy / guardrail spec). The
first build item is the **editorial & safety policy + the dual-review gate**, reflecting its
status as the project's spine; the **source allow-list + license-verification protocol** and the
**citation/readability/staleness checks** are sequenced next so all drafting is gated on verified
sources and measurable plain language. Every patient-facing writing task is `riskTier: high` with
`verifiedNeed: false` until the reviewers and partner are secured.

---

## Governance, roles & stakeholders

- **Maintainer (Owner): TBD.** Owns the editorial framework, the repo/CI, citation/readability/
  staleness checks, agent-neutral tooling, and merge quality. Cannot override a reviewer's "do not
  ship" on substance.
- **Editorial reviewers / rotation:** at least one editorial reviewer for structure, plain
  language, citation coverage, and scope/advice-creep policing, independent of the drafter.
- **Credentialed oncologist reviewer (HIGH tier, blocking): TO BE SECURED** — a board-certified
  pediatric or medical oncologist with **sarcoma/Ewing experience**; signs off clinical accuracy,
  currency, and non-advice framing before any clinical content ships. Tracked in a reviewers
  ledger with credentials and consent. **Holds a veto** on whether content is clinically safe and
  accurate to publish.
- **Patient/caregiver advocate reviewer (HIGH tier, blocking): TO BE SECURED** — an experienced
  patient/caregiver advocate (ideally lived pediatric-cancer/Ewing experience); signs off tone,
  dignity, clarity, sensitivity, and usefulness. **Holds a veto** on whether content is humane and
  usable for families.
  - **Independence / COI:** reviewers disclose material conflicts (e.g., affiliation with a
    specific clinic/product the content might appear to favor) and recuse where relevant. Sign-off
    is **version-scoped** and **does not imply endorsement** of the product as a whole.
  - **Disagreement fallback:** either reviewer's "do not ship" on substance is binding — the
    maintainer cannot override it. A reviewer-vs-reviewer or reviewer-vs-maintainer dispute is
    logged and escalated to **Elyos governance / a second credentialed reviewer** for a tie-break;
    contested clinical content does not ship until resolved. Where a single reviewer is a single
    point of failure, the project prefers securing a **backup reviewer** before relying on
    contested or high-sensitivity content.
- **Steward (last-mile owner): TO BE SECURED** — owns the partner relationship and the delivery
  that constitutes shipping, plus post-delivery family feedback (no PII).
- **Partner / requestor: TO BE SECURED** — the sarcoma foundation, COG/CCLG-affiliated program,
  or treating-center patient-education office that distributes the guide to families.
- **Community / board:** source allow-list additions, license edge-cases, and the CC-BY decision
  go through Elyos governance + the oncologist's concurrence.

---

## Dependencies & integrations

- **Vetted sources (data):** NCI/PDQ®, COG, ESMO, CCLG patient/family educational materials — each
  license-verified and provenance-recorded; copyrighted-source facts restated-and-cited (or used
  only with recorded permission).
- **Human/decision dependencies (critical path):** the **oncologist reviewer** and the **patient-
  advocate reviewer** (both block M2 ship-intent and M3–M4); the **delivery partner/steward**
  (blocks M4). These are the project's true bottlenecks, hence the dated acquisition plan.
- **Tooling:** a Markdown content repo; small TypeScript/ESM build checks (citation coverage,
  readability scoring, label lint, staleness); static accessible HTML + print-friendly PDF
  output. No reader-data services, no analytics, no accounts.
- **Sibling Elyos projects:** `ewing-trial-finder` (HIGH — link to its family-appropriate trial
  finder for the trials topic, do not duplicate); `ewing-survivorship-late-effects` (survivorship
  pointer); `ewing-info-translations` (HIGH — downstream consumer of this content,
  translation-ready hand-off); other Ewing data/KG projects only as *linked, published, family-
  appropriate* references, never as patient-data inputs.
- **Elyos pieces:** `packages/schema` (Task JSON), `CLAUDE.md` (work rules + refusal guardrails +
  cancer guardrails), `docs/good-deed-definition.md` (risk tiers), Elyos governance for
  license/allow-list/edge-case decisions; donated-lane CLI (workspace prep + PRs, never headless).

---

## Risks & mitigations

| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| Inaccurate or outdated medical claim reaches a family | Medium | **Critical** | "No source, no claim" + vetted allow-list; **blocking oncologist sign-off**; runtime **staleness fail-safe** (`validUntil` auto-flag/withhold + re-sign-off); citation-coverage check | Oncologist / Maintainer |
| Content drifts into **advice / individual prognosis** | Medium | **Critical** | Editorial policy hard-refuses advice/prognosis/diagnosis; drafting prompt forbids it; standing "not medical advice" labels; oncologist + advocate review specifically check for advice creep | Maintainer / Oncologist |
| AI session invents a "fact" from model memory (no vetted source) | Medium | High | Drafting restricted to provided vetted sources only; citation-coverage build check fails unsourced assertions; reviewer audit | Maintainer |
| Families harmed by **misinformation** the guide fails to counter (unproven cures, stale survival stats) | Medium | High | Misinformation-correction coverage required on high-risk topics; survival-stats framing ("groups, not your child"); route to care team + vetted orgs | Oncologist / Advocate |
| Source **license/copyright** violated (esp. COG/ESMO/CCLG copyrighted material) | Medium | High | Per-source license verification before use; default to **restate-in-plain-language + cite + link**, no verbatim copying without recorded permission; NCI/PDQ® non-endorsement notice | Maintainer / Governance |
| **No oncologist and/or advocate reviewer secured** → cannot clear the gate | High | High | Dated acquisition plan (both by 2026-10-31); **hold at M1** if not secured — never ship unreviewed health content; recruit via sarcoma foundations, COG/CCLG, academic centers | Maintainer / Steward |
| **No delivery partner secured** → can't reach families | High | High | Dated plan (≥3 in conversation by 2026-08-31); **build-vs-hold rule** at 2027-02-28 — pivot to an existing trusted org's library or hold reviewed-unpublished, rather than self-publish to an unknown audience | Steward / Maintainer |
| Sensitive topics (relapse, end-of-life) cause avoidable distress | Medium | High | Advocate tone review + oncologist framing review on every sensitive page; honest-but-humane standard; clear support-resource pointers | Advocate |
| Reading level too high for families in crisis | Medium | Medium | Measured readability gate (≤ grade 8); terms defined on first use; real-reader comprehension pilot | Advocate / Maintainer |
| Reviewer is a **single point of failure** / version sign-off goes stale | Medium | Medium | Version-scoped sign-off + re-review triggers; secure a backup reviewer for high-sensitivity content; staleness fail-safe | Maintainer |
| Accidental collection of reader PII / health info | Low | High | No accounts/analytics/story-collection at launch; static delivery; any future feedback gated by fresh privacy review; no PII in repo/logs | Maintainer / Steward |
| Scope creep into patient-level data / research | Low | Critical | Binding cancer guardrail in policy + plan; explicit out-of-scope list; controlled-access data never requested | Maintainer / Governance |

---

## Security & privacy

**Threat surface (small by design).** Because the project collects **no reader data** and touches
**no patient-level or controlled-access data**, the classic health-data breach surface is largely
designed away. The remaining surfaces are: (a) **content integrity** (an inaccurate, stale, or
advice-creeping claim reaching a vulnerable family — the top risk, treated as a safety, not just a
quality, concern); (b) **source/license integrity** (using non-vetted or improperly-licensed
material); (c) **supply-chain/repo integrity** (a malicious or careless edit slipping past
review); and (d) **secrets hygiene** in the (small) tooling.

**Controls.**
- **Content as safety-critical:** dual blocking review, "no source, no claim," staleness
  fail-safe, and standing "not medical advice" labels are the primary controls; a citation or
  readability regression fails the build.
- **Source integrity:** vetted allow-list + per-source license verification ledger; non-vetted
  sources cannot back an assertion.
- **Repo integrity:** every change reviewed; no patient-facing publish without recorded dual
  sign-off for the current version; provenance is diffable and auditable.
- **No PII anywhere:** no reader accounts, no identifying analytics, no health-info or story
  collection at launch; no secrets/tokens/PII in repo, build artifacts, or logs (Elyos rule).
- **Tooling hygiene:** minimal dependencies; dependency + secret scanning in CI for the build
  scripts; static output (no server-side reader data path to attack).

**Abuse/misuse prevention.** The editorial policy's refusal set (no advice, no individual
prognosis, no diagnosis, no promotion of unproven/commercial therapies, no non-vetted sources, no
patient-level data) is enforced through drafting constraints and the two review gates — and a
contributor or AI session that hits one of these must **stop and flag**, not work around it.

---

## Sustainability & maintenance

After delivery, a named **maintenance rotation** owns the content and tooling; the **steward**
owns the partner relationship and (PII-free) family feedback. Medical content carries a
**review cadence**: each source's `lastVerified`/`validUntil` drives the runtime **staleness
fail-safe**, so a page past its review window is **auto-flagged or withheld** until a reviewer
re-verifies the source and the **oncologist re-signs-off** (advocate too if wording changed) —
stale cancer information can never silently keep serving as current. Outcomes are tracked
qualitatively (partner-attested usefulness, reach), **not** engagement metrics, with **no PII
collected**. The reviewed, translation-ready content is handed to **`ewing-info-translations`**,
which carries its **own per-language HIGH-tier review** (auto-translation never ships unreviewed).
Adding a new vetted source or topic follows a documented, oncologist-concurred process.

---

## Open questions

- **Which delivery partner first?** A pediatric-sarcoma foundation, a COG/CCLG-affiliated family
  program, or a treating center's patient-education office — decision drives audience, channel,
  and possibly co-branding/governance. (Dated: ≥3 in conversation by 2026-08-31.)
- **Securing the two reviewers** — recruiting a sarcoma-experienced oncologist and a lived-
  experience advocate, their **compensation/credit model** (volunteer vs. a future funded lane for
  review hours with a hard budget cap) **without compromising independence**, and a **backup
  reviewer** for continuity. (Dated: both by 2026-10-31.)
- **Geography/standard-of-care variation** — US (NCI/COG) vs. Europe (ESMO/CCLG) guidance differ
  in detail; ship a single carefully-framed "general + see your care team" guide first, or
  region-tagged variants? Affects sourcing and reviewer profile.
- **Copyrighted-source adaptation** — do we seek explicit permission to adapt specific COG/ESMO/
  CCLG handbook material, or stay strictly restate-and-cite? Permission could improve fidelity but
  adds dependency.
- **Audience split** — one guide for caregivers with AYA-patient call-outs, or separate
  caregiver vs. AYA-patient tracks (different reading needs)?
- **Misinformation-correction tone** — how directly to name and counter specific unproven "cures"
  without amplifying them; advocate + oncologist to set the standard.
- **Lane** — donated by default; is there a future funded lane (hard budget cap) for reviewer
  hours or professional medical illustration, without compromising independence?

---

## References

- Proposal: `governance/proposals/ewing-family-guide.md` *(TO BE WRITTEN — referenced in
  `planning/ROADMAP.md` Track 8a)*
- Elyos work rules, refusal guardrails & cancer guardrails: `CLAUDE.md`
- Good-deed definition & risk tiers: `docs/good-deed-definition.md`
- Task JSON schema: `packages/schema/src/schemas.ts`
- Portfolio + Track 8 cancer guardrails: `planning/ROADMAP.md`
- House style (HIGH-tier sibling plan): `planning/projects/public-official-guide/{PLAN,TASKS}.md`
- Sibling Ewing projects: `ewing-trial-finder` (HIGH), `ewing-survivorship-late-effects`,
  `ewing-info-translations` (HIGH, downstream consumer)
- Vetted source bodies: NCI (PDQ®), Children's Oncology Group (COG), ESMO, Children's Cancer and
  Leukaemia Group (CCLG)

---

## Appendix A — Improvements applied

The 25 specific, concrete improvements below were identified during planning and have each been
**applied** in the body of this PLAN (and the companion TASKS.md). They are recorded here for
traceability and review.

1. **Dual blocking review elevated to "the architecture."** Made the oncologist + patient-advocate
   sign-off an explicit, non-negotiable blocking gate (boxed in both the Executive summary and
   Quality sections), not a final checkpoint — *applied* in Exec summary, Quality gates, Roadmap.
2. **Version-scoped sign-off with expiry + re-review trigger.** Sign-off attaches to a content
   version + source set and does not carry forward to edits or stale sources — *applied* in
   Quality gates, Governance, Sustainability.
3. **Either-reviewer veto + disagreement fallback.** Specified that either reviewer can block,
   the maintainer cannot override "do not ship," and disputes escalate to governance / a second
   reviewer — *applied* in Governance.
4. **Backup reviewer to remove single-point-of-failure** for high-sensitivity content — *applied*
   in Governance, Risks.
5. **Cancer guardrails lead the Data and Quality sections** (boxed callouts) — open-access/
   aggregate/de-identified only; dbGaP/EGA/individual biobanks + identifiable data out of scope —
   *applied* per the binding instruction.
6. **Per-source license verification, conservatively differentiated** (NCI/PDQ® government-work
   but trademark/non-endorsement; COG/ESMO/CCLG copyrighted → restate-and-cite, no verbatim
   without recorded permission) — *applied* in Data section + a dedicated source-vetting task.
7. **"No source, no claim" enforced by tooling** (citation-coverage build check), not goodwill —
   *applied* in Architecture, Data, TASKS checks.
8. **Runtime staleness fail-safe** (`lastVerified`/`validUntil` → auto-flag/withhold + re-sign-off)
   so cancer info can't silently go stale — *applied* in Data, Quality, Sustainability, Risks.
9. **Measured readability bar (≤ grade 8), not assumed**, with terms defined on first use +
   real-reader comprehension pilot — *applied* in Metrics, Architecture, Quality.
10. **Fertility preservation surfaced as time-critical** ("ask *before* treatment starts"),
    prioritized into M2 — *applied* in Metrics, Scope, Roadmap, TASKS.
11. **Explicit no-advice / no-individual-prognosis refusal**, including survival-stats framing
    ("groups, not your child/you") — *applied* in Non-goals, Scope, Quality labels, Risks.
12. **Misinformation-correction coverage required** on high-risk topics (unproven cures, stale
    stats), with tone set by advocate + oncologist — *applied* in Metrics, Scope, Risks, Open Qs.
13. **Sensitive-topic care standard** for relapse + palliative/end-of-life (advocate tone +
    oncologist framing review; no individual prognosis) — *applied* in Quality, Roadmap M3, Risks.
14. **Zero reader-data / no-PII-by-design** (no accounts, analytics, or story collection at
    launch; static delivery) shrinking the threat surface — *applied* in Data, Security, Risks.
15. **Curate-and-translate, never generate** stated as a key decision; AI forbidden from being the
    source of a medical fact — *applied* in Architecture, Non-goals, Risks.
16. **Dated reviewer + partner acquisition plan** with concrete deadlines — *applied* in Exec
    summary, Problem, Open questions.
17. **Build-vs-hold/pivot decision rule** (hold at M1 without reviewers; pivot/hold-unpublished
    without a partner; never ship unreviewed to families to hit a date) — *applied* in Exec
    summary, Roadmap, Risks.
18. **Honest `TO BE SECURED` / `verifiedNeed:false`** throughout for reviewers + partner —
    *applied* in Exec summary, Problem, Governance, TASKS.
19. **Translation-readiness by construction** (WCAG structure + clean reading order) so
    `ewing-info-translations` is cheap and safe — *applied* in Goals, Scope, Architecture,
    Roadmap M5, Dependencies.
20. **Accessibility target (WCAG 2.2 AA) + print-friendly output** for bedside use — *applied* in
    Scope, Architecture, Roadmap M3.
21. **Structured content schema (Page/Assertion/Source)** making provenance diffable and the
    release gate machine-checkable — *applied* in Architecture.
22. **Outcome-based, beneficiary-first metrics** (reviewed-before-publish %, citation %, currency,
    real families reached) — vanity metrics explicitly excluded — *applied* in Metrics,
    Sustainability.
23. **Sibling-project boundaries** (link to `ewing-trial-finder`, hand off to
    `ewing-info-translations`, don't duplicate or ingest patient data) — *applied* in Scope,
    Dependencies, Sustainability.
24. **Geography/standard-of-care variation flagged** (US NCI/COG vs EU ESMO/CCLG) with a "general
    + see your care team" default — *applied* in Open questions, Data allow-list.
25. **Stop-and-flag refusal behavior for AI sessions** (advice creep, unsourced facts, non-vetted
    sources, patient data) mirroring `CLAUDE.md` — *applied* in Scope, Security/abuse-prevention.

---

## Review sign-off

**Reviewer pass (self-review for completeness + correctness), 2026-06-28.** Checked against
`PLAN_SPEC.md` (all 17 H2 sections present and in order), `CLAUDE.md` (cancer guardrails, refusal
guardrails, donated-lane, agent-neutral, no-secrets, CC-BY content), `docs/good-deed-definition.md`
(HIGH tier → credentialed sign-off before merge; 5 good-deed criteria), and the binding cancer
guardrails in the task.

- **Completeness:** all 17 required sections present and ordered; Appendix A (25 applied
  improvements) and this sign-off added. Metadata header present. TASKS.md companion exists with
  schema mapping, milestone tables, per-task acceptance criteria, milestone DoDs, a backlog, and a
  schema-valid example Task JSON. ✔
- **Cancer guardrails lead Data + Quality:** both sections open with a boxed binding callout
  (open-access/aggregate/de-identified only; controlled-access + identifiable data out of scope;
  per-source license verification; provenance on every assertion). ✔
- **HIGH-risk blocking gate:** oncologist + patient-advocate dual sign-off is an explicit,
  boxed, non-negotiable blocking gate before any deed ships; version-scoped; either-reviewer veto;
  escalation fallback. ✔
- **Honesty:** no partner/reviewers invented — all `TO BE SECURED`, `verifiedNeed:false`; dated
  acquisition plan + build-vs-hold/pivot rule so the project never ships unreviewed health content
  to families to hit a date. ✔
- **Good-deed criteria:** tangible public benefit (families in crisis), freely available
  (CC-BY-4.0), no primary for-profit benefit, no harm/misinformation (actively corrects it),
  AI-executable with HIGH-tier human/expert review. ✔
- **Corrections made during review:** (a) tightened the staleness fail-safe so re-sign-off (not
  just re-verification) is required before stale pages re-serve; (b) made explicit that the
  blocking gate applies to *any* channel and to "handed to a family," not only repo publish;
  (c) added the survival-statistics framing label ("groups, not your child/you") to Quality and
  Risks; (d) ensured `ewing-trial-finder` and `ewing-info-translations` are referenced as HIGH-tier
  siblings with their own gates. ✔
- **Residual human decisions (cannot be resolved in-plan):** secure the two credentialed reviewers
  and a delivery partner; choose US-vs-EU-vs-general framing; decide copyrighted-source
  adaptation-vs-restate; confirm CC-BY + any funded-lane reviewer compensation.

**Status:** Plan is internally consistent and ready for maintainer + (once secured) oncologist and
patient-advocate review. It must not advance past M1 ship-intent until both reviewers are secured.
