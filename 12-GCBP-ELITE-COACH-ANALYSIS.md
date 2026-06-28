# GCBP / UDL — Elite Coach Analysis (PM II, Data Products)

> Role: Product Manager II, Data Products | GCBP / UDL (Google Cloud). L5. Bay Area / Seattle / Kirkland. ~$156–229K + bonus + equity.
> Candidate grounding: **Roopali** (RingCentral subscription SOT, Palo Alto customer-health KPIs, Cisco revenue forecasting, Brocade warehouse).
> Companion to `01-ROLE-DOMAIN-DEEP-DIVE-EXPANDED.md` and `08-GCBP-UDL-COMPLETE-QUESTION-BANK.md`.
> Altitude: L5 — own a product area well, land a clear V1, sound judgment throughout (not L6/L7 portfolio altitude).
> No interviewer profile provided — Section 3 re-tailorable once a LinkedIn is shared.

---

## SECTION 1 — Core requirements & assumptions

### A. The Hiring Manager's Blindspots (the real gaps behind the hire)

1. **The real problem is trust & adoption, not building the warehouse.** Eng can build the SOT; the unsolved problem is getting Sales/Finance/Marketing/Product/Support to abandon their own dashboards and trust ONE number. "Trusted advisor… managing expectations" + "adoption of data products" admit this. Need a PM who treats **adoption + change management as the product**.

2. **Definitional governance across orgs with legitimately different incentives.** "What is a customer/churn/pipeline" has 3–4 reasonable answers. The hard part is facilitating canonical agreement + a governance model — political/product, not schema. Distinct from #1 (consensus vs adoption).

3. **Justifying unglamorous platform/warehouse infra vs loud product demand.** Bullet 2 + "balance short/long-term" = infra with indirect, long-horizon ROI competing with visible dashboards. Need a PM who can sequence foundations vs shiny deliverables and defend the unsexy work.

4. **Ruthless prioritization & saying "no" with no market forcing function.** Internal users can't churn; six orgs all want their metric first → infinite demand. "Manage expectations" = prioritize hard, disappoint gracefully.

5. **Operational + analytics CUJs from one source (freshness vs accuracy).** Real-time pipeline for Sales AND penny-reconciled revenue for Finance from the same SOT is a real architecture/product tension. Need someone who designs tiered SLAs / a semantic layer, not one pipeline pretending to serve both.

### B. Assumption-busting (beliefs to reframe)

1. **"Goal = a single canonical number."** → A single number is wrong for half the use cases. Better: a **governed semantic layer with explicitly-labeled, context-aware definitions** — a *system* of truth, not a single number. Serve Sales' real-time pipeline and Finance's reconciled revenue from one governed metrics layer with the definition visible on hover.

2. **"Build quality/accuracy and adoption follows."** → Trust is earned via **transparency + migration choreography** (parallel runs, lineage/quality scores), not accuracy alone. Adoption is a first-class product; decommissioning legacy dashboards is the success event.

3. **"Internal = lower bar (captive users, no competition)."** → Captive users are *harder* — entrenched shadow spreadsheets, zero switching incentive. Real competitor is Excel; you must out-compete workarounds on trust + ease.

4. **"Data quality is a backend/monitoring concern."** → DQ is a **user-facing product surface** — quality/freshness score + lineage on every dashboard turns trust into a feature with a feedback loop.

5. **"AI / NL query is a future layer."** → With Gemini, **NL access + AI-assisted definition reconciliation** is plausibly *the* democratization unlock — but only if the semantic/governance layer is clean. Governance is the moat that makes Google's AI-on-data trustworthy where Snowflake/Salesforce can't.

---

## SECTION 2 — Expected questions & winning answers

### Q1 — "Sales, Finance, Marketing each define 'churn'/'pipeline' differently. How do you land a single definition?"
*(Definitional governance)*
Lived it at RingCentral (3 conflicting churn definitions across GSO/Finance/Product). Don't "win" the fight — **govern** it: (1) interview each org for *why* their definition exists; (2) separate metric from use case → canonical metric with explicitly-labeled variants (gross revenue churn vs logo churn); (3) ratify in a lightweight governance forum with named owners; (4) encode once in the semantic layer (LookML on BigQuery) so every dashboard inherits it with the label on hover. Output = a definition *enforced in the data*, not a memo.

### Q2 — "Your SOT changes a number a VP has reported for years. How do you drive adoption?"
*(Trust / migration / adoption-as-product)*
Treat adoption as the product. **Parallel run** old vs new and explain the delta ("$495M not $500M — excludes double-counted partner deals") — reconciliation builds trust faster than asserting correctness. **Transparency as a feature** (freshness, lineage, quality score). **Migration with a decommission date + white-glove for top stakeholders + exec sponsorship.** RingCentral GSO rollout was 20% data, 80% trust-building.

### Q3 — "Five orgs want their product first, Eng wants platform investment. How do you build the multi-year roadmap?"
*(Prioritization + platform-vs-product sequencing)*
Anchor on UDL's mission, prioritize against it not loudness. **Impact × reach × strategic/foundational value × confidence**, scored transparently. Two role-specific principles: (1) **sequence platform before proliferation** — land canonical models + DQ framework for the highest-leverage domain (Lead-to-Cash revenue/pipeline, touches Sales *and* Finance) first, then expand; (2) **tie infra to a user-visible win** ("this pipeline upgrade lets Finance close two days faster"). Publish roadmap with explicit short-term wins + long-term foundations to manage expectations up front.

### Q4 — "Sales needs real-time pipeline; Finance needs penny-accurate revenue — same source. How do you design for both?"
*(Freshness vs accuracy / operational + analytics CUJ)*
Two SLAs on the same data, one governed source — not two divergent pipelines. Operational layer: near-real-time, "directionally right, hourly," labeled. Finance layer: reconciled post-close, ties to the bank, labeled "audited." Both derive from the **same canonical entities** so they never contradict — they differ only in latency/reconciliation state, transparently. Architecture: BigQuery warehouse, semantic layer for consistent definitions, DQ checks (freshness/completeness/reconciliation) gating the audited tier. Product decision = make the trade-off visible and intentional.

### Q5 — "Internal product, no direct revenue. How do you measure UDL's success?"
*(Metric design)*
Three things laddering to the mission. **Adoption** — MAU of the SOT + share of decisions/reviews run off it vs shadow dashboards, with *# legacy dashboards decommissioned* as hard proof. **Trust** — DQ SLA attainment (freshness, completeness, reconciliation rate to Finance's books). **Productivity** — reconciliation hours eliminated before close, decision latency reduced. Guardrails: DQ incidents, stakeholder trust survey. Mirrors the Palo Alto customer-health KPI framework; here the "customer" is the Cloud Googler and the north star is *decisions made confidently on the SOT*.

---

## SECTION 3 — Strategic reverse questions

1. **(System-of-truth vs single number)** "When two orgs have legitimately different definitions of the same metric, does UDL force one canonical number or expose a governed semantic layer with labeled variants? Where does that tension bite most today?"
2. **(Trust-gap diagnosis)** "What's the biggest trust gap right now — freshness, accuracy, or discoverability — and how do you measure 'trust' in the SOT today?"
3. **(Adoption & decommissioning)** "How do you measure adoption, and is there a forcing function to migrate teams off legacy/shadow dashboards, or is it opt-in? What's the hardest org to move?"
4. **(Platform vs product investment)** "How does the team arbitrate unglamorous warehouse/platform infra vs the data products stakeholders loudly request — and who breaks the tie?"
5. **(AI / democratization)** "Given 'democratize access' is core to the mission, how are you thinking about Gemini / NL query as the access layer — and is the semantic/governance foundation mature enough to make AI answers trustworthy yet?"
