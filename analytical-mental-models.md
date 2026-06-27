# Analytical Framework — Mental Models for NSM, Top Metrics & Biases

> Quick-reference cheat sheet for the Analytical round. Use alongside `frameworks-canonical.md`.
> These models work for ANY product — memorize the process, not specific answers.

---

## 1. NSM: The "Value Moment" Method

Don't pick a metric. **Find the value moment first — the metric names itself.**

### 3-Step Process

**Step 1: "When does the user get what they came for?"**

Not when they open the app. The specific moment they'd say "that was worth it."

| Product | Value moment |
|---|---|
| Podcasting app | Listener absorbs enough of an episode to feel informed/entertained |
| DoorDash | Food arrives at the door, on time, correct |
| YouTube | Viewer watches a video that satisfies their curiosity/entertainment need |
| Airbnb | Guest sleeps comfortably in a place that matched expectations |
| Google Search | User finds the answer and stops searching |
| Spotify | Listener discovers a song/playlist that fits their mood |
| Slack | Team member gets an answer without scheduling a meeting |

**Step 2: "What's the repeatable version of that moment?"**

A single value moment = transaction. Repeated value moments = habit. NSM captures **habit-level engagement**.

Your NSM almost always has 3 components:
- **Frequency wrapper** (weekly/monthly — matches natural usage cadence)
- **Depth signal** (hours, completions, $ value — not just "opened the app")
- **Per active user** (so growth doesn't mask engagement decay)

| Product | NSM | Structure |
|---|---|---|
| Podcasting | Weekly listening hours per active user | Weekly + hours + per user |
| DoorDash | GOV per week | Weekly + $ value |
| YouTube | Weekly watch hours per active user | Weekly + hours + per user |
| Airbnb | Nights booked per quarter | Quarterly + nights |
| Slack | Weekly messages sent per active user | Weekly + count + per user |
| Google Maps | Weekly navigation sessions per active user | Weekly + sessions + per user |

**Step 3: Connect to revenue in one sentence**

"This metric drives revenue because: [NSM] × [monetization lever] = [revenue]."

- Podcasting: listening hours × ad load × CPM = ad revenue
- DoorDash: GOV × take rate = revenue
- YouTube: watch hours × ad density × CPM = ad revenue
- Airbnb: nights booked × nightly rate × take rate = revenue
- Slack: active users × seat price = subscription revenue

**If you can't write this sentence, your NSM is wrong.**

### NSM Template Cheat Sheet

| Template | When to use | Examples |
|---|---|---|
| **[Time spent] per [active user] per [period]** | Content/media — attention = revenue | YouTube, Spotify, TikTok, Netflix, Twitch |
| **[Transaction value/volume] per [period]** | Marketplace/commerce — transactions = revenue | DoorDash, Airbnb, Uber, Shopify, Coinbase |
| **[Core action count] per [active user] per [period]** | Utility/tools — usage = value | Slack, Notion, Zoom, Figma, Grammarly |
| **[Active users] at [engagement threshold]** | Growth-stage — activation = survival | Duolingo, Discord, early-stage products |

Pick the template → fill in the blanks → justify why.

### Defining "Active User"

Don't guess the threshold. Say: "I'd define 'active' as [hypothesis], then validate empirically by plotting D7 retention against first-session behavior and finding the inflection point."

Rules of thumb:
- **≥5 min** for content products (filters accidental taps)
- **≥1 core action** for tool products (sent a message, created a doc)
- **≥1 transaction** for marketplace products (placed an order)
- Use **trailing window** (not calendar period) to avoid boundary artifacts

---

## 2. Top Metrics: The "5 Levers" Method

You're not picking random metrics. You're covering **5 levers** that tell the full health story.

### The 5 Levers

| # | Lever | What it answers | Metric templates |
|---|---|---|---|
| 1 | **Growth** | Are we getting bigger? | GOV, order volume, MAU, revenue, bookings |
| 2 | **Profitability** | Are we making money? | Contribution margin/order, EBITDA, unit economics, take rate |
| 3 | **Engagement/Retention** | Are users coming back? | D7/D30 retention, DAU/MAU ratio, subscription penetration, churn |
| 4 | **Quality** | Is the experience good? | On-time rate, NPS, completion rate, refund rate, error rate |
| 5 | **Supply health** | Can we sustain growth? | Active merchants/creators/drivers, content published, inventory |

### How to use

**Exec dashboard** (3-5 metrics): ONE metric per lever. Drop any lever that doesn't apply.

**PM dashboard** (10-15 metrics): 2-3 metrics per lever, organized by user journey stage.

### Which levers matter most?

Ask: **"What would kill this company if it went wrong?"**

| Company | Kill risk | Priority levers |
|---|---|---|
| DoorDash | Dashers leave → delivery times spike → consumers leave | Supply + Quality |
| Netflix | Content quality drops → subscribers churn | Quality + Engagement |
| Duolingo | Users stop opening app → paid conversion drops | Engagement |
| Airbnb | Regulatory bans → supply vanishes | Supply + Growth |
| YouTube | Creator exodus → content quality drops | Supply + Engagement |
| Uber | Driver shortage → wait times increase | Supply + Quality |

The levers that could kill the company get the most dashboard real estate.

### Audience Calibration

| Audience | # of metrics | Altitude | Time to review |
|---|---|---|---|
| CEO/Board | 3-5 | Company health. "Are we on track?" | 60 seconds |
| VP/Director | 5-10 | Product area health. "Where should I dig in?" | 5 minutes |
| PM | 10-20 | Feature-level diagnostics. "What's broken and why?" | 30 minutes |

**If the prompt says "executive dashboard" — you must be at the CEO altitude.** This means ruthless prioritization, not comprehensive coverage.

---

## 3. Biases: The "6 Usual Suspects" Method

There are really only **6 bias patterns**. Memorize them. In any interview, 2-3 will apply.

### The 6 Patterns

#### 1. Power User Skew
- **When**: Any mean/average metric
- **Shape**: Small group of heavy users inflates average. Typical user looks healthier than they are.
- **Example**: Mean listening hours = 4 hrs/wk. Median = 45 min. 10% of users drive 60% of hours.
- **Fix**: Report median alongside mean. Segment by usage cohort (light/medium/heavy).
- **Say**: "A small cohort of power users could inflate the mean — I'd watch the median alongside."

#### 2. Segment/Category Mix Shift
- **When**: Product has multiple categories, tiers, or user types
- **Shape**: Growing category with different economics changes the blended metric without behavior changing.
- **Example**: DoorDash grocery (high AOV, low freq) grows vs food (low AOV, high freq). Blended AOV rises but frequency drops.
- **Fix**: Decompose by category/segment. Never trust a blended metric alone.
- **Say**: "Category mix could shift the blended number — I'd decompose by segment."

#### 3. Duration/Length Normalization
- **When**: Measuring completion or engagement on items of varying length/size
- **Shape**: Short items always show higher completion. Algorithm optimizes for short → kills long-form.
- **Example**: 15-min podcast = 85% completion. 3-hour podcast = 30%. Short content looks artificially healthier.
- **Fix**: Normalize within length/size quartiles. Compare within cohort.
- **Say**: "Completion rate is biased by content length — I'd normalize within length quartiles."

#### 4. Geographic/Market Concentration
- **When**: Product operates in multiple markets/regions
- **Shape**: Top 5 markets mask declining performance in the long tail.
- **Example**: National GOV up 8%, but NYC/LA/SF drive all growth while 200 smaller markets decline.
- **Fix**: Break down by market tier. Track # of markets growing vs declining.
- **Say**: "A few top markets could mask weakness in the tail — I'd split by market tier."

#### 5. Survivorship Bias
- **When**: Measuring health of users who are still around
- **Shape**: You only see users who didn't churn, so metrics look artificially healthy.
- **Example**: NPS of current DashPass subscribers = 72. But you're not surveying the ones who cancelled.
- **Fix**: Include cohort analysis from acquisition. Track churned user behavior pre-churn.
- **Say**: "We're only measuring users who stayed — I'd include churned cohort analysis."

#### 6. Correlation ≠ Causation (Reverse Causality)
- **When**: Claiming one metric is a "leading indicator" of another
- **Shape**: DashPass members order 2-3x more. But did they order more BECAUSE of DashPass, or join BECAUSE they already ordered a lot?
- **Fix**: Use holdout experiments. Compare behavior pre vs post the event.
- **Say**: "Correlation here might be reversed — I'd validate with a holdout test."

### The Interview Checklist

After finishing your metrics, silently run through:

| Check | Bias to name |
|---|---|
| Is there a mean/average? | → Power user skew |
| Multiple categories or segments? | → Mix shift |
| Measuring completion or engagement? | → Length normalization |
| Multiple geographies or markets? | → Concentration |
| Only measuring active/current users? | → Survivorship |
| Claiming X causes Y? | → Reverse causality |

Pick 2-3 most relevant. For each: **name the bias → describe the shape → state the fix.**

---

## The 60-Second Pre-Answer Mental Walkthrough

Before you start talking, take 30-60 seconds of silence to run this:

```
1. VALUE MOMENT
   "When does the user get what they came for?"
   → That seeds my NSM

2. REVENUE FORMULA
   "NSM × [what] = revenue?"
   → Confirms NSM, connects to business

3. FIVE LEVERS
   Growth / Profitability / Engagement / Quality / Supply
   → Which 3-5 apply? One metric per lever.

4. AUDIENCE
   CEO (3-5 metrics) or PM (10-15)?
   → Calibrate depth to the prompt

5. BIAS CHECKLIST
   Mean? Categories? Completion? Geographic? Active-only? Causal?
   → Pick 2-3, name shape + fix
```

This gives you the full skeleton. Then just talk through it.

---

---

## 4. Metric Diagnosis: The "Funnel-First" Method

For "metric X is declining/slowing — diagnose" questions. This is a separate question type from "define metrics" — it tests root-cause thinking, not metric design.

### The 6-Step Process

```
1. CLARIFY    → Magnitude, timeframe, geo, platform, exact metric definition
               "Is growth rate declining, or absolute number? Since when?"

2. HYPOTHESIZE → External causes FIRST, then internal
               External: competition, seasonality, macro, regulation
               Internal: product changes, bugs, algorithm, pricing

3. WALK THE FUNNEL → Find WHERE the drop occurs before theorizing WHY
               Decompose the metric into a multiplicative funnel.
               Check each component — which one moved?

4. ATTRIBUTE  → Assign % of drop to each root cause
               "70% from X, 30% from Y" — quantify, don't just list.
               This is the L6 move most candidates miss.

5. ACTION PLAN → By root cause: escalate / investigate / fix / monitor
               Different causes need different response types.

6. SYSTEMIC SIGNAL → "Is this a blip or a structural trend?" (L6)
               Pull the 8-week trend. If gradual erosion: it's not
               a tactical fix, it's a cross-functional initiative.
```

### Funnel Decomposition Templates

The key move: decompose the metric into a **multiplicative formula** where each component can be checked independently.

| Metric | Funnel decomposition |
|---|---|
| **Daily unique uploaders** | Total users × consideration rate × upload start rate × upload completion rate × retention rate |
| **Trips per driver** | Hours online × trip requests/hour × acceptance rate × completion rate |
| **Ad revenue** | Watch time × fill rate × CPM |
| **DAU** | New users + Returning users − Churned users |
| **Conversion rate** | Impressions × CTR × landing page conversion × checkout completion |
| **ARPU** | Sessions/user × actions/session × revenue/action |

Check each component. The one that moved IS the problem. Then ask WHY that specific component changed.

### The Attribution Move (L6 differentiator)

Most candidates list hypotheses. Strong candidates **quantify**:

> "The funnel shows hours-online dropped 10% and acceptance rate dropped 5%. Since trips = hours × requests × acceptance × completion, and requests and completion are flat, the 10% hours drop accounts for ~67% of the total 15% decline, and the 5% acceptance drop accounts for the remaining ~33%."

This tells the interviewer you can do the math, not just wave at possibilities.

### The Systemic Signal (L6 close)

Always end with: *"But the bigger question is whether this is episodic or structural. If I pull the 8-week trend and this has been gradually eroding, the fix isn't [tactical response] — it's a cross-functional review of [underlying system]. That's a very different conversation."*

This separates "I can debug" (L5) from "I see the strategic implication" (L6).

---

## Common Mistakes to Avoid

| Mistake | Fix |
|---|---|
| Jumping straight to metrics without stating a goal | State the goal in one sentence FIRST |
| Picking DAU/MAU as NSM | These are vanity metrics. Go deeper — what do active users DO? |
| "Revenue" as NSM | Revenue is an output, not a lever. Find what drives revenue. |
| Listing metrics without connecting to business model | End with "this drives revenue because [formula]" |
| Naming biases without shape and fix | "Power user skew" alone is L5. Shape + fix is L6. |
| Over-engineering for the audience | Exec dashboard = 5 metrics. PM dashboard = 15. Read the prompt. |
| Arbitrary thresholds ("3+ orders") | Either justify with logic OR say "I'd validate empirically with retention curves" |
