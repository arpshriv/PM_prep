# Google PM Interview Frameworks — L6 / L7 (Non-Behavioral Rounds)

> Covers **Product Vision**, **Strategic Insights (Strategy)**, **Product Analysis**, and **Execute with Judgment**.
> Behavioral / Googleyness intentionally excluded (see `behavioral/ai-era-behavioral.md` when ready).
> For Vision, Strategy, and Analysis, each section includes **how to think**, **dimensions to reason across**, **best practices**, and **pitfalls**.
> Companion to `google/traditional-loop.md` (round structure) and `examples/model-answers.md` (10/10 reasoning principles).

---

## 0. The L6/L7 Altitude Shift (read this first)

The same questions are asked at L5, L6, and L7 — what changes is the **altitude of the answer**. The interviewer is calibrating: *does this person operate at the level we're hiring for?* Show the wrong altitude and you get downleveled even with a "correct" answer.

| Lens | L5 (PM II) answer | **L6 (Senior PM)** answer | **L7 (Group PM)** answer |
|------|-------------------|---------------------------|--------------------------|
| **Scope** | One product / feature area | A portfolio or product area; org-level influence | A multi-product domain; business-level P&L thinking |
| **Vision** | Solve a clear user problem well, land a V1 | Connect the product to a 2–3 year strategy and an ecosystem flywheel | Define a *category* or platform bet; reshape how the org allocates |
| **Strategy** | "Where to play / how to win" for one product | Sequencing of bets, build/buy/partner, second-order effects | Capital allocation across bets; what the company sacrifices and why |
| **Analysis** | Define good metrics, do clean math | Tie metrics to a business model; spot where the metric lies | Design the measurement *system* and the org incentives it creates |
| **Execution** | Make a hard prioritization call with trade-offs | Resolve org-level conflict; set the decision *principle*, not just the decision | Change the operating mechanism so the class of problem stops recurring |
| **Risk** | Name failure modes | Name *strategic* risks + the leading indicator you'd watch | Name the existential risk and the reversible-vs-irreversible framing |

**Three altitude tells the HC reads for at L6/L7:**
1. **You set the goal explicitly and everything ladders to it** (Nancy Chu's #1 correction). Juniors jump from "company strengths" to "user segments" without stating the objective. Seniors state it in the first 2 minutes and refer back to it at every fork.
2. **You think in systems, not silos.** Your product strengthens (or cannibalizes) an ecosystem. You name the flywheel.
3. **You make the call and own the trade-off.** No fence-sitting. "Here's my recommendation, here's what I'm explicitly giving up, here's the one signal that would change my mind."

> Google-specific warning: *"All Leaning Hire" = rejection.* Five lukewarm positives don't clear the bar — you need 1–2 **Strong Hire** spikes. The altitude moves above are how you generate a spike instead of a polite pass.

---

## 1. PRODUCT VISION

> Round goal: user empathy, 0-to-1 thinking, first-principles reasoning, and *landing a V1* that ladders to a strategy. At L6/L7 the V1 must also imply a 2–3 year arc.

### The arc (8 moves)
Clarify → **Anchor on a goal/strategy** → Segment users → Pick segment(s) → Identify & prioritize problems → Design the solution/vision → Prioritize to a V1 → Metrics → Risks → "Imagine" close.

You don't recite this. You use it as scaffolding and *narrate your decisions* at each fork. (Google explicitly notes "excessive reliance on frameworks may hinder performance.")

---

### 1.1 Clarify & Scope
**How to think:** Spend 60–90 seconds bounding the problem, then commit. You're testing the prompt for hidden constraints, not stalling. Restate the prompt in your own words, name your assumptions out loud, and state your game plan.

**Dimensions to clarify:**
- *Business context* — whose product is this, what's the company's goal here? (Drives everything.)
- *Constraint* — geography, platform, regulatory, time horizon, B2B vs B2C.
- *Definition of "improve"/"design"* — growth? revenue? a new segment? retention?
- *Success bar* — what would "great" look like to the company in 2 years?

**Best practices:**
- Convert the open prompt into a *decision* ("So the goal is to grow X for company Y among users Z — is that the right framing?").
- Ask 2–4 high-leverage questions, then proceed even if unanswered (comfort with ambiguity is scored).

**Pitfalls:**
- Death by clarification — asking 10 questions signals you can't operate in ambiguity.
- Designing for "everyone." Unbounded scope = no V1.
- Skipping straight to features (most common L5-altitude failure).

---

### 1.2 Anchor on a Goal / Strategy  ← the L6/L7 differentiator
**How to think:** Before any user or feature, state the **goal** and the **strategy it serves**. This is the spine everything ladders to. If you can't tie a later choice back to this goal, cut it.

Use Nancy Chu's **"Zoom Out"** when the prompt is unanchored: zoom all the way out ("what does this company / this generation care about right now?"), then step down one level at a time until you reach the prompt. The decision then feels *grounded in truth*, not random.

**Dimensions:**
- *Goal type* — reach/users, engagement, revenue, strategic moat, ecosystem pull.
- *Strategic role* — is this a growth bet, a defensive moat, a margin play, a platform/flywheel?
- *Time horizon* — V1 now vs the 2–3 year arc (L6/L7 must articulate both).

**Best practices:**
- State the goal in one sentence: *"My goal is to grow [metric] for [company] by serving [segment] — because it strengthens [strategic flywheel]."*
- Name the **flywheel** explicitly (e.g., more X → better data → better model → more X).

**Pitfalls:**
- Goal-setting too fast / implicitly (jumping strengths → segments). Be explicit.
- Ungrounded macro claims ("given the macro environment…") that don't survive scrutiny — every claim must hold logically.
- A goal that doesn't connect to the company's actual position.

---

### 1.3 User Segments  ← (your example — fullest treatment)
**How to think:** Segmentation is a *tool to make the space tractable*, not a ritual. Nancy Chu: **"Why do we segment? Because the space is too big. If it's contained, maybe you don't need to segment."** First decide whether the space even needs cutting. If it does, segment along a dimension that **creates genuinely different needs**, then prioritize *with conviction* — name 3, kill 2, target 1, and explain *why each was killed*.

**Dimensions to segment across** (pick the one that best separates needs for *this* prompt — don't list all):
| Dimension | When it's the right cut | Example |
|-----------|------------------------|---------|
| **Behavioral / JTBD** *(usually strongest)* | Same demographic behaves differently; intent varies | "Plan-ahead commuters" vs "spontaneous explorers" in Maps |
| **Motivation / mindset** | Emotional driver differs | Learners chasing a credential vs curiosity |
| **Lifecycle stage** | Needs change over the journey | New vs power vs churning user; new-to-category vs switcher |
| **Frequency / intensity** | Heavy vs light users need different things | Daily-active vs occasional |
| **Context of use** | Environment changes the need | Public space vs private; mobile vs desktop; high-stakes vs casual |
| **Sophistication / ability** | Expertise gates the experience | Novice vs expert; technical vs non-technical |
| **Economic value / WTP** | Monetization-led prompts | Free rider vs prosumer vs enterprise buyer |
| **Supply vs demand side** | Marketplaces/platforms | Riders vs drivers; creators vs viewers; buyers vs sellers |
| **Demographic / firmographic** *(use last)* | Only when it *proxies* a real need difference | Age only if it changes the job-to-be-done |

**Best practices:**
- **Segment by behavior/motivation, not demographics.** Demographics are a lazy proxy; only use them when they map to a real need difference.
- Pick **one segmenting dimension** and cut cleanly (MECE-ish). Don't blend three axes into mush.
- **Prioritize explicitly** using criteria — pain intensity × frequency × reachability × willingness-to-pay × *strategic leverage for the goal*. Make the criteria visible.
- **Kill with reasons.** "I'm deprioritizing enterprise (long sales cycle, not our V1 motion) and casual users (low intent), and targeting the [X] because [pain is acute + strategically leveraged]."
- For marketplaces, decide **which side you're solving for first** and why (usually the constrained side).
- L6/L7: connect the chosen segment to the **flywheel** — winning this segment should compound (data, network, distribution).

**Pitfalls:**
- **Segmenting when the space is contained** — wastes time, signals ritualistic framework use.
- **Pain points that aren't segment-specific** — the cardinal sin. If your pains apply to *all* users, you haven't proven empathy for *your* segment (Nancy Chu: "you have not proved you have user empathy").
- **No conviction** — listing 4 segments and waffling, or secretly serving all of them.
- **Demographic-only cuts** ("women 25–34") with no need-based rationale.
- **Choosing the easy segment, not the strategic one.** At L6/L7, justify against the goal, not against convenience.

---

### 1.4 Identify & Prioritize Problems
**How to think:** Go deep on the *target segment's* world before solutioning. Nancy Chu's depth move: don't start from persona → pain list. Start from **"What does living the dream look like for this human? What blocks it? What can/should tech do about it?"** Find the *crux* — the non-obvious insight that reframes the problem.

**Dimensions:**
- *Severity* (how much it hurts) × *Frequency* (how often) × *Reach* (how many in-segment) × *Strategic fit* (does solving it serve the goal).
- *Functional vs emotional vs social* job (often the emotional one is the crux).
- *Latent vs stated* needs — evidence of latent demand (workarounds people already hack together) is gold.

**Best practices:**
- Name 3–5 problems, then **select the one "must-solve"** and justify the cut.
- Surface a crux/insight, not a generic pain ("the problem isn't lack of communication — it's that the same behavior means different things, so you're constantly guessing").
- Tie each prioritized problem back to the goal (laddering).

**Pitfalls:**
- Generic pains anyone could list (slow, expensive, confusing) with no segment specificity.
- Solutioning before the problem is sharp.
- Solving a real pain that doesn't serve the stated goal.

---

### 1.5 Design the Solution / Vision
**How to think:** Derive solutions from **principles**, not the other way around. State 2–3 design principles that resolve your prioritized problems, then propose capabilities that follow. A 10/10 proposes a *vision with principles* and derives features; a 7/10 proposes a feature list.

**Dimensions:**
- *Core user journey* — the end-to-end loop, where value is created and "closed."
- *Key UX moments* — the 2–3 moments that make or break it.
- *Systemic fit* — how it strengthens the ecosystem/flywheel (L6/L7 essential).
- *0-to-1 ambition vs feasibility* — ambitious but shippable.

**Best practices:**
- Coin terms for your key concepts (gives the interviewer vocabulary to retell your answer in the debrief — a known spike-generator).
- Build into **existing workflows/rituals**, not new ones you force on users.
- For AI prompts, treat **safety/guardrails as "Feature Zero"** — woven through from sentence one, not bolted on.
- Show 2–3 solution options, then **choose** with rationale.

**Pitfalls:**
- Feature laundry list with no through-line.
- A solution only its creator would use ("designs for users like themselves").
- Ambition with no V1, or a V1 so timid it proves nothing.

---

### 1.6 Prioritize to a V1
**How to think:** Land a **shippable V1** that proves the riskiest assumption. Be ruthless — what is the smallest thing that validates the vision and serves the goal?

**Best practices:** Use impact × confidence × effort (or RICE), but make the *reasoning* visible. State explicitly what's **in V1 vs the roadmap** (V2/V3 shows the arc — important at L6/L7).

**Pitfalls:** Boiling the ocean; or a V1 that doesn't test the core hypothesis; no sequencing story.

---

### 1.7 Metrics (vision context)
**How to think:** Metrics must measure the **promise**, not vanity. One **North Star** that captures the core value exchange, plus a **safety/counter-metric**. (Full metric craft in §3.2.)

**Best practices:** NSM measures *value delivered* ("Independent Solve Rate," "Real-World Transfer Rate," "Weekly Successful Intent Fulfillments"), not DAU. Add a guardrail that protects the other side (quality, trust, the free experience).

**Pitfalls:** DAU/engagement as the headline; metrics that don't ladder to the goal; no counter-metric.

---

### 1.8 Risks & "Imagine" Close
**How to think:** Name the top 1–2 risks and how you'd detect/mitigate them (the leading indicator). Then **close with a visceral "Imagine…" statement** that makes the interviewer *feel* the product. The summary is forgettable; the image is what they retell.

> Example close: *"Imagine a first-time manager who doesn't have to learn leadership by accidentally damaging three relationships."*

---

## 2. STRATEGIC INSIGHTS (PRODUCT STRATEGY)

> Round goal: a **defensible thesis** with explicit trade-offs and sizing. Weight **grows at L6+** — this is often where the L6/L7 spike is won or lost. Fence-sitting is an automatic fail.

### The arc (7 moves)
**Thesis upfront** → Landscape/market map → Where to play → How to win (moat) → Size it → Monetize → Trade-offs & recommendation.

---

### 2.1 Lead with a Thesis
**How to think:** State your **position in the first 60 seconds**, then defend it. The structure exists to support the thesis, not replace it. ("My recommendation is X; here's the reasoning and what I'm trading off.")

**Best practices:** A real thesis is falsifiable and specific ("Google should *not* enter X; instead double down on Y because Z"). Signal you'll size and stress-test it.

**Pitfalls:** Saving the answer for the end; hedging ("it depends on many factors…"); generic frameworks with no opinion.

---

### 2.2 Map the Landscape
**How to think:** Establish the board before moving pieces. Who plays, where they sit, what's *changing in the next 12–24 months*. Use a lens, not a data dump.

**Dimensions to reason across:**
- *Players & positions* — incumbents, challengers, adjacent entrants, open-source.
- *Value chain* — who captures value at each layer; where margin pools sit.
- *Trends/inflections* — tech shifts, regulation, behavior change, cost curves.
- *Forces* — a quick Porter cut (suppliers, buyers, substitutes, entrants, rivalry) when useful.
- *Company position* — your unique assets (distribution, data, talent, brand) **and** vulnerabilities.

**Best practices:** Be *current and opinionated* (especially for AI prompts — name real competitors, products, recent moves, pricing). Identify the **one or two dynamics that actually matter**, don't list ten.

**Pitfalls:** "AI is changing everything" hand-waving; textbook recitation with no point of view; ignoring the company's real strengths/weaknesses.

---

### 2.3 Where to Play
**How to think:** Choose the battlefield — segment, market, geography, or layer of the stack. This is segmentation at the *market* level (reuse §1.3 dimensions, applied to markets/segments-of-the-economy).

**Dimensions:** market size & growth, intensity of competition, your right-to-win, strategic adjacency to core, regulatory exposure, time-to-defensibility.

**Best practices:** Pick deliberately and say what you're *not* doing. Favor markets where your unique assets compound.

**Pitfalls:** Trying to win everywhere; entering a market with no right-to-win; choosing on size alone (ignoring defensibility).

---

### 2.4 How to Win (Moat / Differentiation)
**How to think:** A position is only good if it's **defensible**. What's the moat, and does it *compound*?

**Dimensions / moat types:** network effects, economies of scale, data/learning flywheel, switching costs/lock-in, brand/trust, distribution advantage, ecosystem/platform pull, cost structure.

**Best practices:** Name the **flywheel** and how today's win makes tomorrow's easier. For AI/cloud, reason about the **data moat** and ecosystem conversion (a product can succeed standalone yet be a *strategic underperformer* if it doesn't feed the flywheel).

**Pitfalls:** Differentiation that's easily copied; "better UX" as the whole moat; ignoring how incumbents retaliate.

---

### 2.5 Size It (Sizing & Sequencing)
**How to think:** Put a number on the prize — TAM/SAM/SOM or revenue/user impact — with transparent assumptions (see estimation craft §3.1). Then **sequence**: beachhead → expand. At L6/L7, also weigh **build vs buy vs partner**.

**Best practices:** Sanity-check the number against a known anchor. Show the beachhead → adjacency path. Name the build/buy/partner call and why (e.g., "model-first company shouldn't manufacture hardware — partner with an OEM").

**Pitfalls:** No quantification; vanity TAM with no SOM; one giant leap with no sequencing.

---

### 2.6 Monetize / Pricing
**How to think:** Start from **cost structure, not price tag** (critical for AI: inference, training/improvement, reliability, support costs). Then value-based pricing tied to the value delivered, and the motion that fits the buyer.

**Dimensions:** pricing model (sub, usage/consumption, seat, freemium, B2B2C), value metric (what you charge per unit of value), cost-to-serve, the sales motion (PLG vs enterprise POC→pilot→production→expansion), willingness-to-pay by segment.

**Best practices:** Tie price to a value metric the customer recognizes. Account for unit economics and margin, not just headline price.

**Pitfalls:** Pricing AI like classic SaaS (ignoring inference cost variance); price with no cost basis; one price for segments with very different WTP.

---

### 2.7 Trade-offs & Recommendation
**How to think:** Restate the thesis, make the **call**, and be explicit about what you sacrifice, the risks you accept, and the **one signal that would change your mind.**

**Best practices:** "Recommend X. I'm accepting [risk] and forgoing [option]. The leading indicator I'd watch is [metric]; if it does [Y], I'd revisit." Connect to the company's actual position.

**Pitfalls:** Ending without a decision; pretending there are no downsides; ignoring second-order effects (competitor response, cannibalization, org cost).

---

## 3. PRODUCT ANALYSIS

> Three modes: **Estimation (Fermi)**, **Metrics definition**, **Root-cause diagnosis**. *Estimation is the most common at Google* (a key difference from other companies). At L6/L7, all three must connect to a business decision, not stay academic.

---

### 3.1 Estimation (Fermi)
**How to think:** Make your reasoning **auditable**. Pick a clear path (top-down from population, or bottom-up from a unit), state assumptions out loud, compute in round numbers, then sanity-check.

**Structure:**
1. Clarify what's being estimated and the unit (per year? per day? QPS?).
2. Choose top-down vs bottom-up and say why.
3. Lay out the equation *before* plugging numbers.
4. Use round, defensible anchors (population, %, frequency).
5. Compute stepwise; keep units consistent.
6. **Sanity-check** against a known reference; state confidence and the biggest swing factor.

**Best practices:** Segment the population when behavior differs (e.g., split heavy vs light users). Round aggressively. Narrate ("I'll assume ~330M US population, ~80% smartphone…"). End with "the number is most sensitive to [assumption]."

**Pitfalls:** Wild single-guess with no structure; messy arithmetic; inconsistent units; no sanity check; false precision (quoting 7 significant figures off guessed inputs).

---

### 3.2 Metrics Definition
**How to think:** Metrics flow from the **goal and the moment of value**. Define when the user *actually* derives value, then measure that. Distinguish the three layers (Nancy Chu):
- **Goal** = what you're trying to achieve (e.g., revenue).
- **Metric** = how you measure achievement (revenue $, conversion rate).
- **Operating metric** = table-stakes you watch regardless (uptime, latency) — *not* a success metric.

**The metric stack:**
| Layer | Question it answers | Example |
|-------|--------------------|---------|
| **North Star** | Is the core value being delivered? | "Weekly Successful Intent Fulfillments," "Independent Solve Rate" |
| **Input / lever metrics** | What drives the NSM? (acquisition, activation, engagement, retention) | First-interaction completion, multi-turn rate |
| **Guardrail metrics** | What must NOT break? | quality/hallucination, latency (TTFT), safety, abuse, cost |
| **Counter-metric** | Am I winning by harming the other side? | free-tier experience when optimizing ads/upgrades |
| **Ecosystem metric** (L6/L7) | Does this strengthen the whole system? | cross-platform conversion, net usage lift |

**How to think about choosing the NSM:**
- It should measure the **promise/value exchange**, be **sensitive** to product changes, **hard to game**, and **ladder to the goal**.
- Defend **every word** of it (cadence, "successful," the value unit, the competitive bar). Daily can be too volatile; monthly too lagging — pick the cadence the product's rhythm justifies.

**Best practices:** Everything ladders to the goal — if the goal is ad revenue, the metric is revenue, not installs. Add a counter-metric that protects the side you might harm. For AI, segment quality metrics by **context severity** (near-zero hallucination tolerance for medical/financial/travel-logistics).

**Pitfalls:**
- Listing DAU/retention/NPS reflexively (the 6/10 answer).
- A flat list instead of a *framework* (NSM → inputs → guardrails).
- Metric that doesn't ladder to the goal, or that's trivially gameable.
- Confusing operating metrics (latency/uptime) with success metrics.
- Ignoring **bias in the metric** (see below) — a known L6/L7 spike.

**Where metrics lie (bias — name this proactively):**
- *Measurement/selection bias* — launching in luxury hotels first skews metrics to affluent English-speakers ("testing in Manhattan, assuming it works in Montana").
- *Model/instrument bias* — ASR works worse for non-native accents → a metric understates PMF abroad.
- *When it bites* — at expansion/scaling decisions, where a biased sample gives overconfident signals (false positives in existing markets, false negatives in new ones).
- *The fix* — segment every metric by language/geo/deployment/demographic from day one; build the infra before you scale.

---

### 3.3 Root-Cause Diagnosis
**How to think:** Resist the first hypothesis. **Structure the space**, then triage by likelihood and ease-of-check. Frameworks: *internal vs external*, then *the funnel* (acquisition → activation → engagement → retention → resurrection), broken down by segment/platform/geo/time.

**Structure:**
1. Clarify the metric, magnitude, and window (5% over a week vs 40% overnight are different animals).
2. **Is it real or measurement?** Logging change, instrumentation bug, definition change, seasonality. (Always rule this out first — cheap and common.)
3. **Internal vs external** — did *we* change something (release, pricing, algo) vs did the *world* change (competitor, season, macro, platform/OS update)?
4. **Segment the drop** — by geo, platform, cohort, new-vs-existing, device. A localized drop points to a specific cause.
5. **Funnel-localize** — which stage moved?
6. Form 2–3 ranked hypotheses; state how you'd confirm each (data pull, A/B, log check).
7. Recommend the fix + how you'd prevent recurrence (L6/L7).

**Best practices:** Ask for the magnitude and shape (sudden cliff vs slow bleed) early — it discriminates causes fast. Sudden cliff → release/outage/logging; slow bleed → competition/saturation/seasonality. Quantify each hypothesis's plausible contribution.

**Pitfalls:** Anchoring on one cause; not checking instrumentation; ignoring segmentation; jumping to fixes before isolating; treating correlation as cause.

---

## 4. EXECUTE WITH JUDGMENT

> Round goal: make the **hard call** under conflicting constraints, own the trade-off, and (at L6/L7) set the **principle/mechanism**, not just the one-off decision. May be run by an engineering manager. Trying to satisfy everyone = fail.

### The arc (6 moves)
Clarify goal & constraints → State the decision criteria/principle → Lay out options → Make the call → Mitigate the downside → (L6/L7) fix the recurring mechanism.

**How to think:**
1. **Anchor on the goal & the real constraint** (time, capacity, quality, strategic relationship). Name what's actually scarce.
2. **State your decision principle before deciding** — e.g., "I optimize for the bet with highest strategic leverage × confidence, protecting the launch-quality bar." The principle is what scores at senior level; it generalizes beyond the scenario.
3. **Lay out 2–3 options with explicit trade-offs** — quantify where you can (impact, effort, risk, # customers, $).
4. **Decide.** Commit to one path with conviction.
5. **Mitigate** — how you protect the losing side (the deprioritized customer, the slipped feature), communicate, and de-risk.
6. **L6/L7 — change the system** so this class of conflict stops recurring (e.g., a prioritization rubric, an intake process, an escalation path). Reversible vs irreversible (one-way-door) framing for big calls.

**Best practices:**
- Make the decision *early* and spend the time defending it (don't bury it).
- Use numbers ("I'd serve the 1 customer representing 60% of pipeline and strategic logo value, and give the other 9 a templated path + timeline").
- For "launch or slip?" — separate *quality bar / user harm* (especially safety, irreversible) from *schedule pressure*; decide on the bar, then manage the schedule.
- Treat XFN partners as collaborators with shared goals, not blockers.

**Pitfalls:**
- Trying to satisfy all stakeholders / no decision.
- **Escalating to leadership as the answer** (signals you can't make the call).
- No criteria (deciding by gut with no generalizable principle).
- Framing partners as obstacles; hero narratives.
- Ignoring the second-order/precedent effects of the call.

---

## 5. Cross-Round Operating Principles (the spikes)

These show up across all four rounds and are what turn a Leaning Hire into a Strong Hire:

1. **State the goal early; everything ladders to it.** Refer back at every fork.
2. **Think in systems, not silos.** Name the flywheel / ecosystem effect.
3. **Segment by behavior, prioritize with conviction, kill with reasons.**
4. **Make the call. Own the trade-off. Name the one signal that flips you.**
5. **Quantify** — sizing, metrics, prioritization. Transparent math, sanity checks.
6. **Name where you could be wrong** — bias in metrics, strategic risk, failure modes + the leading indicator.
7. **Be current and opinionated** (especially AI landscape).
8. **Coin terms and close with an image** — give the interviewer something to retell in the debrief.
9. **Right altitude for the level** — portfolio/business thinking at L6/L7, mechanism over one-off.
10. **Frameworks are scaffolding, not script** — narrate decisions, don't recite steps.
