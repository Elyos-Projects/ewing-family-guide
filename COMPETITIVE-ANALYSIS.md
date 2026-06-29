# Competitive + Improvement Analysis — `ewing-family-guide`

> Analyst review of `PLAN.md` (v0.1.0, 2026-06-28) and `TASKS.md`. Scope: a free, plain-language,
> vetted-source-only guide for families/caregivers/AYA patients facing a **Ewing sarcoma**
> diagnosis. HIGH risk-tier, patient-facing, cancer guardrails binding. All competitor claims below
> are grounded in cited web sources (research date 2026-06-29).

---

## 1. Correctness & completeness review of PLAN.md

The plan is unusually strong for a HIGH-tier patient-facing health deed: the blocking dual-review
gate, "no source, no claim," the runtime staleness fail-safe, version-scoped sign-off, the
honest `TO BE SECURED` posture, and the build-vs-hold rule are all present and well-reasoned.
Appendix A already captures 25 applied improvements. The gaps below are what remains.

**A. Source allow-list + citation enforcement — real but partly fictional gaps in the model.**

- **The allow-list omits several first-tier authorities the plan will obviously need**, and which
  competitors already cover better (see §2): the **American Cancer Society** (has a complete
  Ewing-specific patient section), **Together by St. Jude** (the single best plain-language
  pediatric-cancer resource and explicitly designed for families), **Macmillan**, **Cancer
  Research UK**, **Bone Cancer Research Trust** (UK bone-cancer specialist with Ewing-specific
  info docs), **Sarcoma UK**, and **Nemours KidsHealth** (already at the target reading level).
  Restricting to NCI/COG/ESMO/CCLG is defensible as a *minimum*, but the plan should name the
  full candidate tier-1 set and the inclusion criteria, or it will under-cover and look less
  authoritative than free competitors.
- **COG sourcing is mis-specified.** The plan repeatedly cites a "COG family handbook." The widely
  distributed **Ewing Sarcoma Family Handbook is actually published by APHON** (Association of
  Pediatric Hematology/Oncology Nurses), 2023 copyright — not COG. COG publishes a general
  *Family Handbook* and survivorship guidelines, not a Ewing-specific one. This is a factual
  sourcing error that the license-verification step must catch; the plan should correct the
  attribution now.
- **Citation-coverage check is necessary but not sufficient.** "Every assertion has ≥1 vetted
  source" does not verify the source *actually supports the claim* — the well-documented LLM
  failure mode is a real URL attached to a statement it doesn't substantiate (reference
  hallucination). The plan needs an explicit **claim-source faithfulness check** in the oncologist
  review (spot-check that the cited page says what the assertion says), not just presence of a
  citation. This is the single most important tooling gap.
- **No "allowed claim granularity" rule.** The "curate, never generate" rule is stated, but
  *combining* two sourced facts into a third implied claim, or choosing which of several
  conflicting authority figures to present, is itself an editorial/medical judgment. The policy
  should say how conflicts between vetted sources are resolved (e.g., defer to oncologist; present
  ranges; never average).

**B. Blocking oncologist + advocate gate — concrete enough on policy, thin on operationalization.**

- The gate is well-specified as *policy* but **under-specified as a process**: there is no defined
  **review SLA / turnaround**, no **structured reviewer checklist or rubric** (what exactly the
  oncologist signs against, line by line), no **conflict-of-claim resolution workflow when an
  oncologist edit pushes reading level back above grade 8** (clinical accuracy vs. plain-language
  tension is guaranteed and unaddressed), and no **reviewer onboarding packet**. For a gate that
  *is the architecture*, the absence of a reviewer rubric artifact in M0 is a gap.
- **Single-reviewer-per-role is still a latent single point of failure** despite the "backup
  reviewer" note. With one oncologist and one advocate, the project's entire ship-ability depends
  on two volunteers' availability indefinitely (re-review on every source-staleness event). The
  sustainability section needs a **standing reviewer panel** target, not just a backup.
- **No defined recourse if a secured reviewer later becomes unavailable** mid-life (content
  already shipped, sources go stale, reviewer gone) — the staleness fail-safe would withhold the
  whole guide. Needs a continuity plan.

**C. Prognosis / false-hope avoidance — strong intent, needs sharper mechanics.**

- The "groups, not your child/you" label and the no-individual-prognosis refusal are excellent.
  But the plan does not resolve the hardest concrete question: **does the guide state
  population-level survival statistics at all?** My own research surfaced exactly the hazard:
  reputable-looking figures range wildly and are often stale or from marketing sites —
  localized 5-yr survival quoted as "70–80%," "81%," "84.7%"; metastatic as "15–30%" vs "50.4%";
  adult outcomes far worse than pediatric. ([survival figures vary by
  source](https://pmc.ncbi.nlm.nih.gov/articles/PMC11498927/),
  [marketing-site example](https://int.livhospital.com/ewing-sarcoma-cancer-survival-rate/)).
  The policy must explicitly decide: cite NCI/PDQ aggregate figures *with* the era/caveat and the
  "groups not you" frame, **or** omit raw percentages and route to the care team. Right now this is
  left to reviewers; it should be a written editorial rule because it is the highest-stakes call.
- **"No false hope" cuts both ways and isn't addressed.** Avoiding false hope must not tip into
  fatalism (Ewing outcomes have genuinely improved). The advocate-tone standard should name *both*
  failure modes.

**D. Emotional / psychosocial safety — present but light.**

- Sensitive topics (relapse, palliative/EoL) get tone review, good. But there is **no "safe
  reading" / content-warning or pacing design** (a frightened parent landing on the end-of-life
  page first), **no crisis/mental-health signposting standard** (when a caregiver is in distress —
  e.g., link to bereavement, psych support, helplines), and **no guidance on imagery/illustration
  tone**. Competitors (Together by St. Jude) bake emotional-support navigation into the IA; the
  plan treats it as a backlog item (content-018).

**E. Health literacy + reading level — well-handled, one refinement.**

- Grade ≤8 (target 6–8), measured (Flesch–Kincaid/SMOG), plus real-reader pilot: strong, and
  well-justified — [NIH/AMA recommend ≤6th–7th grade and most cancer materials run grades
  9–14](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9955234/),
  [60% of patients only comprehend 6th-grade materials](https://pmc.ncbi.nlm.nih.gov/articles/PMC11181814/).
  One gap: **automated readability formulas are unreliable for medical text** (penalize
  unavoidable terms like "chemotherapy," miss comprehension). The pilot mitigates this, but the
  policy should note formulas are a floor, not proof, and weight the human comprehension check.

**F. Multilingual — deferred entirely, which is a strategic miss.**

- Multilingual is the project's biggest differentiation opportunity (see §3–4) yet is fully
  punted to `ewing-info-translations`. Meanwhile **NCI/PDQ already ships Spanish**, so for the
  largest US minority-language population the project adds little unless it goes *beyond* Spanish.
  "Translation-ready by construction" is necessary but the plan should name a **priority-language
  hypothesis** (driven by Ewing/AYA epidemiology and LEP disparity data — [LEP linked to delayed
  diagnosis and ~70% lower trial engagement](https://pmc.ncbi.nlm.nih.gov/articles/PMC12606142/))
  rather than leaving language selection unscoped.

**G. Accessibility — good target, missing specifics.**

- WCAG 2.2 AA + print PDF + alt text is right. Missing: **plain-language is itself an
  accessibility/cognitive-load requirement** (WCAG mentions reading level), **screen-reader
  testing** (not just structural conformance), and an explicit stance on the **print PDF's
  readability** (PDFs are notoriously inaccessible; needs tagged-PDF requirement).

**H. Keeping content current — strong design, one runtime risk.**

- The `validUntil`/staleness fail-safe is excellent. Risk: in a *static, no-server* delivery model
  (chosen for privacy), there is **no runtime to "auto-withhold" a page** — staleness can only be
  enforced at build/publish time or via a manual cadence. The plan asserts a runtime gate it may
  not have an engine for. Reconcile: either a build-time gate + scheduled rebuilds, or accept a
  manual review-cadence with prominent "last verified" dates on every page. The mechanism needs
  to match the static architecture.

**I. Medical-accuracy verification — see A above (claim-source faithfulness is the gap).**

**J. Liability / "not advice" — labeling strong; legal posture absent.**

- Standing labels are well-specified and template-enforced. But there is **no jurisdictional
  liability/disclaimer review** (a global CC-BY health guide is read in many legal regimes), **no
  policy on the CC-BY downstream risk** (anyone may reuse/modify the content under CC-BY and strip
  the labels or staleness dates — a real harm vector the plan doesn't address), and **no medical-
  content insurance/indemnity consideration** for the volunteer reviewers. At minimum, flag CC-BY
  modification-stripping as a risk and consider CC-BY-ND for safety-critical pages or a
  "verified copy" canonical-source norm.

**K. Metrics — outcome-first and good; two weak spots.**

- "Families reached + finding it useful" is qualitative and partner-attested — appropriate given
  no-PII, but **unfalsifiable as stated**; define the minimum evidence (e.g., steward confirms ≥N
  distributions and collects structured non-PII feedback). Also, **no metric for "harm avoided"**
  (the actual mission: families not steered to unproven cures) — inherently hard, but a proxy
  (misinformation-correction coverage is there; consider a reviewer-rated "does this page reduce a
  known harm" check).

**L. Smaller items.** Owner is TBD (every dated commitment lacks an accountable human);
no **versioning/changelog norm visible to families** ("what changed since you last read this");
no **feedback/erratum channel** for a family or clinician who spots an error (tension with
no-PII, but an error-report path is a safety need); the **2026-10-31 reviewer deadline** with
zero reviewers secured as of 2026-06-29 is aggressive and is the project's gating risk.

---

## 2. Competitive landscape

Most authoritative Ewing content already exists and is free. The competition is not "no
information" — it is **fragmentation, reading level, region-specificity, and monolingual delivery**.

| Resource | What it does | Strengths | Weaknesses / gaps |
|---|---|---|---|
| **NCI / PDQ® (cancer.gov)** | Authoritative US treatment summary, patient + clinician versions | Gold-standard accuracy; expert editorial board; regularly updated; **free, public-domain, Spanish available** | Reading level high; dense/clinical tone; US-centric; not emotionally designed; not a "journey/what-to-expect" narrative |
| **Together by St. Jude** | Dedicated plain-language Ewing page + whole emotional-support/daily-life IA | **Best-in-class plain language + emotional design**; built for families; covers support networks, school, siblings; trusted brand | Single-institution voice; English (some Spanish); not a synthesis across authorities; St. Jude-centric framing |
| **American Cancer Society** | Full Ewing patient section (symptoms, staging, treatment, key stats) | Comprehensive, well-structured, trusted, free; good navigation | US-centric; adult-oriented house style; reading level moderate-high; not pediatric-family-tailored |
| **CCLG (UK)** | Ewing-in-children info + downloadable family publication | Pediatric-specific, UK family-oriented, charity-trusted | UK standard-of-care framing; smaller scope; English-only |
| **Macmillan (UK)** | Ewing within bone-cancer hub + broader support services | Strong supportive-care/practical/financial info; helpline | UK system-specific; sarcoma is a small slice; not pediatric-focused |
| **Cancer Research UK** | Bone-cancer info + resources/support-orgs signposting | Clear, reputable, good signposting to orgs | UK-centric; Ewing not deeply pediatric-tailored |
| **ESMO patient guide (Bone Sarcomas, w/ Anticancer Fund)** | European patient guide to bone sarcomas | Authoritative EU counterpart to NCI; translation-minded | **Dated (2016)**; bone-sarcoma-general not Ewing-specific; PDF format; currency concern |
| **Bone Cancer Research Trust (UK)** | Ewing-specific info + Support & Information Service | Primary-bone-cancer specialist; Ewing-specific docs; support line | UK-centric; charity scale; English-only |
| **Sarcoma UK** | National sarcoma charity: guides, support line, trials hub | Support line + downloadable guides + trials hub | Sarcoma-general; UK; Ewing is a subset |
| **Sarcoma Foundation of America** | Info/links + free trial-navigation (EmergingMed) | Trial-matching service; US advocacy presence | Thin patient-education depth; adult/general sarcoma; research/fundraising lean |
| **MIB Agents** | Pediatric osteosarcoma nonprofit; family-written handbook, OsteoBites, OSI Connect | **Lived-experience, family-written model**; expert webinars; AYA voice | **Osteosarcoma-focused, not Ewing**; community/program not a structured guide |
| **Nemours KidsHealth** | Parent-facing Ewing explainer | **Already at low reading level**; parent-friendly tone; trusted | Shallow depth; not cited/sourced visibly; US general-pediatric, not sarcoma-deep |
| **Alex's Lemonade Stand / APHON handbook** | "Ewing Sarcoma Family of Tumors" family handbook (APHON-published, 2023) | Family-oriented, nurse-authored, pediatric-specific | PDF; static; distribution-limited; single-document |
| **General web search / forums / marketing sites** | Whatever ranks | — | **The actual enemy**: outdated/conflicting survival stats, hospital-marketing SEO pages, unproven-cure content, no provenance |

Sources: [NCI PDQ patient version](https://www.cancer.gov/types/bone/patient/ewing-treatment-pdq),
[Together by St. Jude — Ewing](https://together.stjude.org/en-us/conditions/cancers/ewing-sarcoma.html),
[ACS — Ewing](https://www.cancer.org/cancer/types/ewing-tumor.html),
[CCLG — Ewing in children](https://www.cclg.org.uk/about-cancer/cancer-children-and-young-people/types-cancer-children-and-young-people/ewing-sarcoma-children),
[Macmillan — Ewing](https://www.macmillan.org.uk/cancer-information-and-support/bone-cancer/ewing-sarcoma),
[Cancer Research UK — bone cancer resources](https://www.cancerresearchuk.org/about-cancer/bone-cancer/living-with/resources-books),
[ESMO bone-sarcoma patient guide (2016)](https://www.esmo.org/for-patients/patient-guides/bone-sarcoma),
[Bone Cancer Research Trust — Ewing](https://www.bcrt.org.uk/information/information-by-type/ewing-sarcoma/),
[Sarcoma UK](https://sarcoma.org.uk/),
[Sarcoma Foundation of America — info/links](https://curesarcoma.org/support-resources/information-links/),
[MIB Agents — education](https://www.mibagents.org/education),
[Nemours KidsHealth — Ewing](https://kidshealth.org/en/parents/ewings.html),
[Alex's Lemonade Stand — Ewing family of tumors](https://www.alexslemonade.org/childhood-cancer/guides/childhood-cancer/chapter-2-bone-sarcomas/ewing-sarcoma-family-tumors),
[APHON Ewing Family Handbook](https://resources.aphon.org/view/210107630).

**Bottom line:** No single competitor is *the* open, synthesized, multilingual, plain-language,
provenance-on-every-claim Ewing family guide. Together by St. Jude is closest on tone/IA but is
single-institution and English-first; NCI is the accuracy gold standard but dense and US-centric;
the UK charities are pediatric-warm but region-locked. The white space the plan targets is real.

---

## 3. Gaps we can fill

1. **Synthesis across vetted authorities.** Every competitor speaks in one institutional/national
   voice. A family must currently triangulate NCI + St. Jude + CCLG + a charity themselves. A
   single guide that *reconciles* US (NCI/COG) and EU (ESMO/CCLG) framing, citing each, with "your
   care team will follow your region's protocol," is genuinely new.
2. **Provenance on every claim.** No consumer competitor shows a citation + retrieval date +
   "last verified" on each statement. In a disease where [survival figures conflict wildly across
   reputable-looking sites](https://pmc.ncbi.nlm.nih.gov/articles/PMC11498927/), visible
   provenance is itself a trust differentiator and a misinformation antidote.
3. **Measured plain-language at scale.** Most authoritative content sits at grades 9–14
   ([cancer-agency materials avg ~grade 9.3](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9955234/));
   a *measured* ≤grade-8 synthesis across all of it is rare.
4. **Multilingual beyond Spanish.** NCI covers Spanish; almost no one covers the next tier of
   languages for a rare AYA cancer, where [LEP families face delayed diagnosis and far lower trial
   engagement](https://pmc.ncbi.nlm.nih.gov/articles/PMC12606142/). This is the highest-leverage gap.
5. **Global accessibility, region-aware.** A free, CC-BY, offline-printable, WCAG-AA guide usable
   in low-resource settings — most competitors are web-bound and region-locked.
6. **The neglected hard topics, in one humane place.** Fertility preservation *before* treatment
   (time-critical), what "metastatic" really means, relapse, palliative care — fragmented or
   buried across competitors; consolidated and gently sequenced here.
7. **Currency as a visible guarantee.** A "last verified / valid until" stamp and a staleness
   fail-safe is a structural trust feature no competitor offers patient-side.
8. **Active misinformation correction.** Naming and countering the unproven-cure/stale-stat
   content that dominates general search — competitors mostly ignore it.

---

## 4. Differentiators to win

1. **Provenance-on-every-claim + visible currency** — the "no source, no claim" + `validUntil`
   stamp is a trust artifact nobody else ships to patients.
2. **Cross-authority synthesis, region-aware** — one reconciled, cited voice over NCI/COG/ESMO/CCLG
   instead of one institution's view.
3. **Measured ≤grade-8 plain language, comprehension-tested with real families** — not assumed.
4. **Dual blocking expert + lived-experience review as the architecture** — clinical accuracy *and*
   humanity gated, version-scoped, either can veto.
5. **Multilingual-by-construction beyond Spanish** — the equity wedge.
6. **Open + free + CC-BY + offline-printable + WCAG-AA** — reusable by any foundation/clinic,
   bedside-usable, globally accessible.
7. **Honest, non-fatalistic, no-false-hope tone** — explicitly avoiding both miracle-cure framing
   and despair, a needle competitors rarely thread deliberately.
8. **Designed to feed siblings** (`ewing-info-translations`, `ewing-trial-finder`,
   survivorship) — a hub, not a leaf.

---

## 5. Claude API leverage

**Where Claude clearly helps (all human-gated, all sourced):**

1. **Plain-language synthesis from supplied vetted sources, with inline citations.** Claude drafts
   a ≤grade-8 page *strictly from the oncologist-approved source set provided in-context*,
   attaching the citation to each assertion. This is retrieval-grounded restatement — the
   documented way to [reduce hallucination via RAG-style grounding](https://cancer.jmir.org/2025/1/e70176) —
   not open-ended generation.
2. **Reading-level adaptation + glossary generation.** Rewrite to target grade, define terms on
   first use, auto-draft the glossary, and flag residual jargon — Claude is strong at controlled
   simplification ([LLMs improve patient-material readability](https://www.jmir.org/2025/1/e69955)).
3. **Translation drafting for `ewing-info-translations`** (then per-language qualified human
   review) — first-draft multilingual at low cost, the equity lever.
4. **Question-prompt generation** — drafting neutral "questions to ask your care team" lists from
   sourced material (not scripting decisions).
5. **Editorial QA assistance** — drafting reviewer checklists, diffing a new source version against
   prior to surface what changed (currency), spotting tone/advice-creep for human confirmation,
   and *flagging* possible claim-source mismatches for the oncologist to verify.
6. **Misinformation-corpus drafting** — summarizing, from vetted sources, the common myths to
   counter (for human approval), without amplifying specifics.

**Where Claude must NOT decide (binding):**

- **Never medical advice, diagnosis, individual prognosis, or "what would you do."** Population-
  level, source-cited education only. Survival figures, if used at all, come from a vetted source
  with the "groups, not your child/you" frame — never Claude's estimate.
- **Every claim traces to a vetted authority.** Claude may not be the source of a medical fact;
  no model-memory "facts," no extrapolation beyond the supplied sources, no averaging conflicting
  figures. Given that [chatbots produced problematic answers in ~half of a 250-question health
  audit](https://academic.oup.com/oncolo/article/30/4/oyaf038/8120372), unsourced model output is
  out of scope by construction.
- **No fabricated citations.** Reference hallucination is the named risk; a citation's *existence*
  is insufficient — the oncologist verifies it supports the claim.
- **Oncologist + patient-advocate review is a blocking gate Claude cannot satisfy or bypass.**
  Tone, dignity, and clinical accuracy are human sign-offs, version-scoped.
- **Translations don't ship on Claude's word** — per-language qualified human review (the sibling
  project's own HIGH-tier gate).
- **Stop-and-flag, never work around** a refusal (advice creep, unsourced fact, non-vetted source,
  patient data).

---

## 6. Ten concrete optimizations

1. **Add a claim-source faithfulness check** to the oncologist rubric (and an automated
   pre-screen that flags assertions whose cited page text doesn't lexically support them) — close
   the biggest verification gap; citation *presence* ≠ citation *support*.
2. **Correct and expand the source allow-list now**: fix the APHON-vs-COG handbook attribution; add
   ACS, Together by St. Jude, BCRT, Macmillan/CRUK, KidsHealth as candidate tier-1 with written
   inclusion criteria and per-source license notes.
3. **Write the explicit survival-statistics editorial rule** (cite-with-caveat vs. omit-and-route)
   into the policy rather than leaving the highest-stakes call to ad hoc reviewer judgment.
4. **Ship a reviewer rubric + SLA + onboarding packet as an M0 artifact**, plus a defined
   accuracy-vs-readability tie-break workflow (the guaranteed tension).
5. **Reconcile the staleness fail-safe with the static no-server architecture**: build-time gate +
   scheduled rebuild + a visible per-page "verified on / valid until" stamp; don't promise a
   runtime withhold you can't execute.
6. **Name a priority-language hypothesis** for the translation hand-off (driven by AYA/Ewing +
   LEP-disparity data), so "translation-ready" has a concrete first target beyond Spanish.
7. **Add a CC-BY downstream-safety control**: mark safety-critical pages so labels/currency can't
   be silently stripped on reuse (canonical-copy norm, or CC-BY-ND for those pages), and flag this
   as a risk.
8. **Add an erratum / error-report path** for a family or clinician who spots an inaccuracy
   (PII-free), with a documented re-review trigger — a safety obligation the no-PII stance omits.
9. **Add psychosocial-safety design**: content-warning/pacing for relapse + EoL pages, a
   distress/crisis-support signposting standard, and an explicit "non-fatalistic AND no-false-hope"
   tone rule covering both failure modes.
10. **Strengthen outcome evidence**: define the minimum partner-attested usefulness evidence
    (≥N distributions + structured non-PII feedback) and add a reviewer-rated "reduces a known
    harm" check so the mission (harm avoided) is measured, not just asserted.

---

## 7. Parallel & perpendicular spin-offs

**Parallel (same playbook, adjacent content):**

- **`ewing-info-translations`** — already named; the equity multiplier. Prioritize languages by
  LEP/AYA epidemiology; each language its own HIGH-tier per-language review.
- **`ewing-survivorship-late-effects`** — late-effects/survivorship plain-language guide (COG
  survivorship guidelines exist as a vetted base); natural pointer from this guide.
- **`ewing-trial-finder`** — family-appropriate, informational trial finder (SFA/EmergingMed and
  Sarcoma UK trials hub show the demand); link, don't duplicate.
- **`question-prompt-lists`** — a standalone, reusable "questions to ask your care team" library
  across cancer types (this guide seeds the Ewing instance).
- **`nutrition-during-treatment`** — vetted-source plain-language nutrition guidance during
  pediatric cancer treatment (high family demand, high misinformation risk — strong guardrail fit).

**Perpendicular (generalize the machinery):**

- **Generalized rare-cancer family-guide template** — the real reusable asset is the *pipeline*:
  allow-list + provenance schema + citation/readability/staleness checks + dual-review gate. Other
  rare cancers (osteosarcoma, rhabdomyosarcoma, DSRCT, neuroblastoma) could be instantiated from
  it — MIB Agents' family-written osteosarcoma handbook shows the appetite.
- **A "provenance + currency" content framework** as open tooling any health-info nonprofit could
  adopt (the claim-source check, the staleness fail-safe, the label lint).
- **Foundation partnership program** — co-publish under existing trusted libraries (St. Jude,
  CCLG, BCRT, Sarcoma UK, SFA, MIB) rather than self-publishing; this is also the build-vs-hold
  pivot target and the most credible last-mile.

---

## 8. Open questions for the maintainer

1. **Will the guide state population-level survival statistics at all?** If yes, from which single
   vetted source, with what caveat framing; if no, how is the inevitable "what are the odds"
   question handled? (Highest-stakes unresolved editorial call.)
2. **Region strategy:** one carefully-framed "general + see your care team" guide first, or
   US/EU-tagged variants? This drives sourcing, reviewer profile, and the allow-list.
3. **Which delivery partner first**, and would co-publishing *under their* editorial governance
   (vs. self-publishing) be acceptable as the primary path rather than the fallback?
4. **Reviewer model:** volunteer vs. funded-lane review hours (hard cap) — and how is independence
   protected? With zero reviewers secured at 2026-06-29 against a 2026-10-31 gate, what is the
   recruitment channel and is the deadline realistic?
5. **First non-Spanish translation language(s)** — what evidence picks them?
6. **CC-BY vs. label-stripping risk** — accept open reuse, or protect safety-critical pages
   (CC-BY-ND / canonical-copy)?
7. **Static-architecture vs. runtime staleness** — how is "auto-withhold" actually enforced
   without a server?
8. **Error-report channel** — can a PII-free erratum path coexist with the no-data stance, and who
   triages it?
9. **Where does this guide stop and a sibling begin** — especially the survivorship and trials
   boundaries, to avoid duplication or gaps families fall through?
