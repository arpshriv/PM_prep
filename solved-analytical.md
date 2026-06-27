# Solved Analytical Questions — Model Answers

> L6/L7 model answers following the canonical Analytical framework from `frameworks-canonical.md`.
> Use these as reference for structure, depth, and altitude — not as scripts to memorize.

---

## Q1: "What 3-5 metrics would you use to measure the success of a podcasting app?"

**Company**: Spotify (recently launched podcasting in US)
**Framework**: Canonical Analytical

---

### What is the product designed to do?

A podcasting app is an **audio content discovery and consumption platform** connecting three stakeholders: **listeners** (demand), **creators** (supply), and **advertisers** (monetization). It captures a uniquely valuable slice of attention — the "eyes-busy, ears-free" moments (commuting, cooking, exercising) that video platforms like YouTube and TikTok fundamentally cannot reach.

The deeper purpose: podcasting apps are fighting to become the **default audio companion** — the thing you open when your hands and eyes are occupied. Whoever wins that habit owns 2+ hours/day of attention that's complementary to, not competitive with, visual media.

### Competitors

- **Spotify** (~30% of podcast listening): Integrated with music. Bet $1B+ on exclusives, pivoted to open ecosystem + ad tech.
- **YouTube** (~25-30%): Now the #1 podcast platform by consumption time. Video podcasts are the format shift. Killer advantage: VOD discovery algorithm.
- **Apple Podcasts** (~15-20%): Default on iOS. Distribution moat but minimal product innovation.
- **The real competitor is silence and radio** — 60%+ of audio time is still FM radio or no audio at all. This reframes the TAM.

### Why is the company investing?

- **Mission**: "To unlock the potential of human creativity — by giving a million creative artists the opportunity to live off their art and billions of fans the opportunity to enjoy and be inspired by it." Podcasts extend this to a new creator class.
- **Ecosystem impact**: Podcasts drive platform stickiness and session duration, increasing the value of the broader music product. If podcast listeners also stream more music, podcasts are a flywheel, not a silo.
- **Revenue**: Podcast advertising is a ~$4B+ US market growing 15-20% annually. Dynamic ad insertion enables programmatic buying — far higher margin than music royalties (~70% to labels).

### Goal (stated explicitly — the spine everything ladders to)

**Grow Spotify's share of audio attention by making podcasts a daily habit for listeners, while building a creator ecosystem that's self-sustaining through advertising revenue.**

### When do users derive value?

Users derive value at **two distinct moments**:
1. **Discovery**: Finding a podcast worth listening to (browsing, recommendation, search, social referral)
2. **Consumption**: Actually listening — specifically, reaching the point where they feel informed, entertained, or connected to the host

The value moment is NOT pressing play. It's reaching ~60-70% completion of an episode, when the listener has absorbed enough content to feel the session was worthwhile. This shapes the north star.

### North Star Metric

**Weekly listening hours per active podcast listener (W-LHAU)**

Definition:
- **Numerator**: Total podcast listening hours in trailing 7 days
- **Denominator**: Users who listened to ≥5 minutes of podcast content in trailing 7 days
- **Why ≥5 min**: Filters accidental taps and immediate bounces. 5 minutes signals intentional listening.
- **Why trailing 7 days** (not calendar week): Avoids artifact where a Sunday listener looks "inactive" on Monday.

Why this metric:
- **Weekly** not daily because podcast consumption is naturally episodic — most listeners don't listen every day, and a daily metric would penalize a healthy Tuesday/Thursday listener
- **Listening hours** not "episodes started" because a user who starts 10 episodes and abandons each at 2 minutes is failing; a user who deeply listens to 3 episodes is succeeding
- **Per active user** not total hours because total hours can grow by adding low-engagement users who inflate the denominator without real product health

Revenue connection: advertising revenue = f(listening hours × ad load per hour × CPM). Growing W-LHAU directly grows the revenue opportunity.

Validation note: I'd validate the ≥5 min threshold empirically — plot the D7 retention curve by first-session listen duration and find the inflection point where retention jumps. That's where "active" starts.

### Ecosystem Impact Metric

**Cross-format retention lift** — what percentage of podcast listeners also use Spotify's music product at a higher rate than non-podcast listeners?

This captures the ecosystem flywheel: podcasts → longer sessions → discovery of music → stickier platform → harder to churn. If this number is high, it justifies podcast investment even if podcast-specific revenue is thin. If it's flat, podcasts are a silo, not a flywheel.

### Secondary Metrics (User Journey)

| Journey Stage | Metric | Why |
|---|---|---|
| **Awareness → Try** | New listener activation rate (% of Spotify users who listen to ≥1 podcast episode within 7 days of first exposure to podcast content) | Top-of-funnel conversion from "has the app" to "tried podcasts" |
| **Discovery → Play** | Browse-to-play rate (% of podcast browse sessions that result in pressing play) | Is discovery surfacing the right content? If users browse but don't play, recommendations are failing |
| **Play → Completion** | Episode completion rate, normalized by length quartile (% of started episodes listened to ≥70%, reported separately for <20 min, 20-60 min, 60+ min episodes) | Content-listener fit. Normalization prevents short-form bias |
| **Completion → Return** | D7 listener retention (% of new podcast listeners who listen again within 7 days) | The habit formation gate. The product either earns a recurring user or loses them here |
| **Return → Subscribe** | Shows followed per listener | Subscription (following a show) is the commitment signal that predicts long-term retention |

**Volume-based lagging indicator**: **Total weekly listening hours (platform-wide)**. This is the lagging aggregate — it only moves after per-user engagement improves AND the user base grows. It's the revenue-correlated metric for the executive dashboard, while using per-user metrics above for diagnosis.

### Creator-Side Metrics

| Stage | Metric |
|---|---|
| **Supply health** | Monthly active shows (published ≥1 episode in last 30 days) |
| **Creator engagement** | Average episodes published per active show per month |
| **Creator retention** | MoM creator retention (% of shows that published last month that also publish this month) |
| **Creator growth** | Average followers per show (growing = platform is distributing well) |

### Guardrail Metrics

**Quality guardrail — Creator publishing health**: Monthly active creators (shows that published ≥1 episode in last 30 days). If listening hours grow but creator supply contracts, we're concentrating attention on fewer shows, making the platform fragile.

**Cannibalization guardrail — Music session time**: If podcast listening hours grow but music hours decline 1:1, we're cannibalizing our own product rather than capturing net-new audio attention. Watch the ratio: Δ podcast hours / Δ total audio hours. If >1, we're cannibalizing. Goal is to grow total platform time, not redistribute.

**Long-tail health — % of listening hours going to shows outside the top 100**: If 95% of listens go to top 50 shows, the ecosystem is fragile and algorithm is over-indexing on popularity.

### Does Bias Exist?

Yes, in three ways:

1. **Episode length bias on completion rate**: A 20-minute news podcast naturally has higher completion than a 3-hour interview. Optimizing for completion naively biases the algorithm toward short-form, which may not drive the deepest listener relationships. **Fix**: Normalize completion rate by episode length quartile, or use "listened minutes" alongside completion rate.

2. **Power-user skew in W-LHAU**: A small number of heavy listeners (commuters, truck drivers) can dramatically inflate the average. If the median listener does 1 hr/week but the mean is 4 hrs because of power users, the metric looks healthy while the typical user is barely engaged. **Fix**: Report median W-LHAU alongside mean, and segment by listening frequency cohort (light/medium/heavy).

3. **New show discovery bias**: Recommendation algorithms tend to push proven, popular shows (safe clicks) over new/niche shows. This looks good on browse-to-play rate (popular shows convert well) but slowly kills creator diversity and makes the platform dependent on a small number of shows. **Fix**: Track % of listening hours going to shows outside the top 100, and set a floor.

### Summary — The 5 Metrics

1. **Weekly listening hours per active listener** (north star — engagement depth + habit)
2. **Episode completion rate, normalized by length** (content-listener fit)
3. **D7 listener retention** (habit formation gate)
4. **Total weekly listening hours** (lagging volume indicator, revenue-correlated)
5. **Monthly active creators** (supply-side health guardrail)

Everything ladders to the goal: build a podcasting platform that captures net-new audio attention, creates habitual listeners, and grows the revenue surface area (listening hours × ad load × CPM).

### L6 Altitude Moves in This Answer

- **Anchored on a goal before any metric** (capture eyes-busy/ears-free attention)
- **Named the flywheel** (podcasts → sessions → cross-format stickiness → retention)
- **Connected metrics to the business model** (W-LHAU → ad revenue formula)
- **Explicitly called out cannibalization** as a guardrail (not just quality)
- **Named where the metrics lie** (3 biases — length, power-user, discovery) proactively
- **Defined the NSM denominator precisely** with an empirical validation approach

---

## Q2: "Say you're creating the executive dashboard to show to DoorDash leadership about the health of the company. Name 3-5 metrics you'd put on the dashboard."

**Company**: DoorDash (mature, recently profitable)
**Framework**: Canonical Analytical
**Key framing**: This is an EXEC dashboard (3-5 metrics a CEO reads in 60 seconds), not a PM analytics dashboard.

---

### What is the product designed to do?

DoorDash is a **three-sided marketplace** connecting consumers, merchants (restaurants + retailers), and Dashers (drivers). It's the dominant US food delivery platform (~67% market share) that has expanded into grocery, convenience, and retail delivery. The company just achieved its first full-year profitability (2024) after years of losses, making the shift from "growth at all costs" to "profitable growth" the defining executive narrative.

### Competitors

- **Uber Eats** (~23% US share): Strong driver network from ride-sharing. Dominant in urban hubs.
- **Grubhub** (distant 3rd): Sold for $650M after $7.3B acquisition — a cautionary tale about marketplace fragility.
- **Instacart**: The emerging threat for grocery delivery specifically.
- **Amazon**: The long-term threat for convenience/retail delivery.

### Why is the company investing?

- **Mission**: "To grow and empower local economies" — connecting local businesses to consumers through delivery infrastructure.
- **Revenue model**: Three streams — (1) commission fees from merchants (15-30%), delivery/service fees from consumers, (2) DashPass subscriptions ($9.99/mo), and (3) **advertising** (promoted listings — the highest-margin revenue stream, approaching $1B+ with 70%+ margins).
- **Ecosystem impact**: DoorDash is evolving from "food delivery" to "delivery of everything" — the infrastructure layer for local commerce.

### Goal

**Ensure DoorDash is growing profitably while maintaining marketplace health across all three sides — consumers, merchants, and Dashers — and expanding high-margin revenue streams (advertising, DashPass).**

### When do users derive value?

- **Consumer**: When the item arrives on time, correct, at a price they consider fair for the convenience.
- **Merchant**: When DoorDash drives incremental orders they wouldn't have gotten through their own channels.
- **Dasher**: When they earn enough per hour to justify choosing DoorDash over alternative gig work.

The value exchange completes when an order is placed, prepared correctly, delivered on time, and all three parties are satisfied enough to repeat.

### Executive Dashboard — 5 Metrics

**1. GOV growth rate (WoW, with trailing 4-week trend)**

Gross Order Value = total dollar value of all orders processed. This is the top-line marketplace health indicator.

Why GOV not order count: GOV captures both volume AND basket size. As DoorDash expands into grocery (AOV $80+) and retail, order counts may grow slower but basket sizes are 2-3x larger. GOV reflects total throughput regardless of category mix.

Why not revenue directly: Revenue depends on take rate (a business decision DoorDash controls). GOV measures organic marketplace health independent of pricing decisions.

**2. Contribution margin per order**

Revenue per order minus delivery costs, payment processing, refunds, and support. This is the unit economics health check.

Why this matters now: DoorDash just turned profitable. The board watches this obsessively. If it's declining, growth is unprofitable. If stable/growing, the flywheel is working.

L6 insight: This metric reveals the **advertising margin boost**. As ad revenue grows (near-100% margin), contribution margin per order should rise even if delivery economics stay flat. If it's NOT rising, the ad business isn't scaling.

Revenue connection: Profit = orders × contribution margin per order. This metric times GOV-implied order volume gives you the P&L trajectory.

**3. DashPass subscriber penetration (% of total orders from DashPass members)**

DashPass members order 2-3x more frequently and churn at ~50% lower rates. This is DoorDash's Amazon Prime equivalent — the loyalty flywheel.

Why penetration not subscriber count: Subscriber count can grow while penetration falls (if non-DashPass orders grow faster). Penetration tells you whether the most engaged users are driving the business or whether you're dependent on one-time orderers.

**4. On-time & correct delivery rate**

The quality guardrail. If this drops, everything else eventually follows — consumers churn, merchants lose trust, NPS tanks.

Why combined: A delivery that's on time but missing items is still a failure. One number gives the CEO a single quality read.

**5. Active merchants + active Dashers (supply-side health)**

- Active merchants: accepted ≥1 order in trailing 30 days
- Active Dashers: completed ≥1 delivery in trailing 7 days

A marketplace dies from the supply side first. If merchant count declines, selection shrinks, consumers leave. If Dasher count drops, delivery times increase, consumers leave.

Why different time windows: Merchants operate on monthly cycles (seasonal closures, menu changes). Dashers operate weekly (gig workers decide week-to-week which platforms to drive for).

### Ecosystem Impact Metric

**Cross-category adoption rate**: % of food delivery customers who also place ≥1 grocery or convenience order per month. Measures whether DoorDash is becoming "delivery of everything" or staying a food-only platform. Rising rate = expansion strategy working, customers view DoorDash as a utility.

### Guardrail Metrics

- **Dasher earnings per active hour**: If this drops below ~$15-20/hr including tips, Dashers leave for Uber, Amazon Flex, or Instacart. Supply-side retention lever.
- **Customer refund/credit rate**: % of orders resulting in refunds. Catches quality problems the on-time metric alone won't surface.

### Bias

1. **Geographic concentration**: Top 5 metros (NYC, LA, SF, Chicago, Houston) can mask weakness in expansion markets. Aggregate GOV looks healthy while growth markets quietly fail. **Shape**: National trend looks stable, suburban/rural markets are dying silently. **Fix**: Break down all top-line metrics by market tier (top 10 cities vs. mid-tier vs. emerging).

2. **DashPass skew**: DashPass members order 2-3x more frequently. If DashPass penetration is 40% of orders, those members dominate GOV and retention metrics, masking softness in non-subscribers who are price-sensitive and may be churning. **Shape**: Retention looks healthy because DashPass is sticky, while one-time users silently leave. **Fix**: Split all metrics into DashPass vs. non-DashPass cohorts.

3. **Category mix shift**: As grocery (higher AOV, lower frequency) grows relative to food (lower AOV, higher frequency), blended metrics become misleading. GOV rises because grocery AOV is $80+ vs. food $30, but order frequency drops — is that healthy growth or behavioral decline? **Shape**: GOV looks great but frequency drops. **Fix**: Report GOV and order frequency by category separately.

### Summary — The 5 Metrics

1. **GOV growth rate** (marketplace throughput, category-agnostic)
2. **Contribution margin per order** (unit economics, profitability trajectory)
3. **DashPass penetration** (loyalty flywheel, retention predictor)
4. **On-time & correct delivery rate** (quality guardrail)
5. **Active merchants + active Dashers** (supply-side health)

Everything ladders to the goal: profitable growth through marketplace density and high-margin revenue streams. GOV × take rate = revenue. Revenue − delivery costs = contribution margin. DashPass drives frequency. Quality drives retention. Supply health sustains the flywheel.

### L6 Altitude Moves in This Answer

- **Right altitude for the audience**: 5 metrics a CEO reads in 60 seconds, not a 15-metric PM dashboard
- **Profitability front and center**: Contribution margin per order reflects DoorDash's current strategic narrative (just turned profitable)
- **DashPass as the flywheel metric**: Shows understanding of DoorDash's most important strategic lever
- **Connected metrics to business model**: GOV × take rate = revenue; ad margin boosting contribution margin
- **Three biases with shape and fix**: Geographic concentration, DashPass skew, category mix shift
- **Supply-side health with justified time windows**: Different windows for merchants (monthly) vs Dashers (weekly)

---

## Q3: "Define some success metrics for YouTube's search result page."

**Product**: YouTube Search Results Page
**Framework**: Canonical Analytical
**Key framing**: This is about a specific PAGE (the screen after you type a query), not YouTube search in general. The page must convert search intent into satisfying content consumption.

---

### What is the product designed to do?

YouTube's search results page is the **high-intent gateway** to YouTube's content library. Unlike the home feed (which serves lean-back browsing), search captures users who KNOW what they want — "how to tie a tie," "Taylor Swift live," "iPhone 16 review." This makes search the highest-intent surface on YouTube, and therefore the most valuable per-impression for both users and advertisers.

**Strategic insight**: Most YouTube consumption (~80%) starts from the home feed or recommendations, not search. Search drives only ~15-20% of video starts. But search sessions are disproportionately valuable because (1) they signal explicit intent (higher-CPM ad targeting), (2) they drive new creator discovery (users find creators they wouldn't have seen in their feed), and (3) they're Google's unique competitive advantage — no other video platform has YouTube's search infrastructure.

### Competitors

- **YouTube's own home feed** — the internal competitor. If the recommendation algorithm is good enough, users stop searching and just browse. Search must prove it delivers value the home feed can't.
- **Google Search** — some video-intent queries get answered by Google Search with YouTube embeds, bypassing the YouTube search page entirely.
- **TikTok search** — Gen Z increasingly starts product/how-to searches on TikTok. YouTube search is losing the youngest cohort for discovery queries.
- **ChatGPT / AI search** — for informational queries ("how does X work"), AI answers may satisfy the intent without a video. YouTube search competes with the AI answer, not just other video platforms.

### Why is the company investing?

**Mission**: "Give everyone a voice and show them the world." Search is the most direct expression — a user asks, YouTube shows.

**5-way ecosystem**:
- **Creators**: Search is their discovery engine. A creator's video being findable via search = long-tail views for years (unlike feed, which is ephemeral).
- **Consumers**: Come to find specific knowledge, entertainment, or content they've heard about.
- **Platform**: Facilitates the match between intent and content. Search quality = platform trust.
- **Advertisers**: Search intent signals are the highest-CPM targeting data YouTube has. A user searching "best running shoes 2026" is more valuable to Nike than a random feed impression.
- **Music rights holders**: Music video searches drive licensing revenue.

**Revenue connection**: Search queries → video views → ad impressions → ad revenue. Each search that converts to a satisfying video view generates ad revenue at a higher CPM than feed-driven views (because the intent signal enables better ad targeting).

### Goal

**Maximize the rate at which search intent converts into satisfying content consumption — because high-intent search sessions generate the highest-CPM ad impressions and drive the creator discovery that sustains YouTube's long-tail content flywheel.**

### When do users derive value?

The search results page serves **three distinct query intents**, each with a different value moment:

| Query type | Example | Value moment | Success looks like |
|---|---|---|---|
| **Navigational** | "MrBeast" "Marques Brownlee" | Finding the specific creator/video instantly | First result is correct; CTR on result #1 >80% |
| **Informational** | "How to fix a leaky faucet" "Python tutorial" | Finding a video that answers the question AND watching enough to learn | Video completion ≥60% with no return-to-search |
| **Exploratory** | "Funny cat videos" "Lo-fi hip hop" | Entering a satisfying viewing session (multiple videos) | Session depth ≥3 videos, extended watch time |

### North Star Metric

**Search-attributed watch time per active searcher per week**

- **Search-attributed**: Only counts watch time that originated from a search query (not home feed, not recommendations). This isolates search's contribution.
- **Watch time** (not clicks, not CTR): A click that leads to a 5-second bounce is a failure. Watch time captures whether the user found what they wanted AND it was good.
- **Per active searcher**: Denominator = users who performed ≥1 search in trailing 7 days. This prevents the metric from being inflated by feed-driven watch time growth.
- **Per week**: Weekly cadence matches YouTube's natural usage rhythm.

**Revenue formula**: Search-attributed watch time × ad load per hour × search-intent CPM premium = search ad revenue. Growing this NSM directly grows the highest-CPM revenue stream.

### Ecosystem Impact Metric

**Search-to-subscribe rate**: % of search sessions where the user subscribes to a new creator they discovered through search results. This measures whether search is feeding the creator discovery flywheel — users who discover creators via search then see those creators in their home feed, creating a self-reinforcing loop. If search only surfaces creators users already follow, it's not adding ecosystem value.

### Secondary Metrics (User Journey)

| Journey Stage | Metric | Why |
|---|---|---|
| **Query → Results** | Query-to-result latency (p50 and p95 in ms) | Search must feel instant. >500ms = perceivable delay. |
| **Results → Click** | CTR on top 3 results (by query type: navigational / informational / exploratory) | Measures relevance. Must be segmented by query type because baselines differ dramatically. |
| **Click → Watch** | Bounce rate (% of clicks where user watches <30s and returns to results) | Measures thumbnail/title accuracy. High bounce = misleading results. |
| **Watch → Satisfy** | Search-originated completion rate (normalized by video length quartile) | Measures content-intent fit. Normalized to avoid short-video bias. |
| **Satisfy → Return** | D7 search retention (% of searchers who search again within 7 days) | Measures habit formation for search specifically. |

**Volume-based lagging indicator**: Total weekly search-attributed watch hours (platform-wide). This is the exec dashboard number; per-user metrics above are for diagnosis.

### Guardrail Metrics

- **Repeat search rate in same session**: % of sessions where a user searches, clicks a result, returns, and searches the SAME or similar query again. This is a frustration signal — the first set of results failed. Target: <15%.
- **Null result rate**: % of searches that return zero or irrelevant results. Should be <1% for top-100K queries.
- **Shorts vs long-form cannibalization**: If search increasingly surfaces Shorts, track whether search-attributed watch TIME grows or shrinks. Shorts may increase click count but decrease watch time per click. Watch the ratio: Δ search watch time / Δ search clicks.
- **Ad load guardrail**: Number of ads shown on the search results page before first organic result. If this exceeds 1-2, user trust in search results degrades (the "Google Search becoming ads" problem).

### Bias

**1. Video length normalization (duration bias)**: The completion rate metric (≥70%) systematically favors short videos. A 2-minute music video hits 70% easily; a 2-hour lecture won't. If we optimize for raw completion rate, the algorithm pushes short content — which may not satisfy informational queries that need depth. **Shape**: Short content looks artificially healthier. **Fix**: Normalize completion within length quartiles (<5 min, 5-20 min, 20-60 min, 60+ min). Compare within cohort, not across.

**2. Popular creator bias (popularity skew)**: YouTube's ranking naturally favors high-subscriber creators (more watch history data, higher CTR baselines, more engagement signals). This inflates CTR on search results (popular videos get clicked) but may suppress relevant content from mid-tier or new creators. **Shape**: Search results become a "top 100 creators" surface. CTR looks healthy but creator diversity dies. **Fix**: Track % of search-attributed views going to creators outside the top 1000. Set a diversity floor. Monitor whether new creators' videos ever appear in top-3 results for non-navigational queries.

**3. Recency bias (freshness over relevance)**: YouTube's search algorithm uses freshness as a ranking signal — newer videos rank higher. For trending queries ("election results") this is correct. For evergreen queries ("how to tie a tie") it's actively harmful — the best tutorial might be from 2019, but it gets buried under inferior 2026 versions. **Shape**: Evergreen content loses traffic over time despite being the best answer. **Fix**: Segment metrics by query type (trending vs evergreen); for evergreen queries, track whether the highest-rated result (by completion + satisfaction) is also the highest-ranked. If not, freshness is overweighted.

### Summary — The 5 Metrics

1. **Search-attributed watch time per active searcher per week** (NSM — captures intent-to-satisfaction conversion)
2. **CTR on top 3 results, segmented by query type** (relevance signal — navigational vs informational vs exploratory baselines differ)
3. **Repeat search rate in same session** (frustration guardrail — the search results page FAILED if users re-search)
4. **Search-to-subscribe rate** (ecosystem impact — is search feeding the creator discovery flywheel?)
5. **Bounce rate** (thumbnail/title accuracy — are results misleading users?)

Everything ladders to the goal: maximize intent-to-satisfaction conversion on the highest-CPM surface YouTube has. Search-attributed watch time × ad load × CPM premium = the revenue this page drives.

### L6 Altitude Moves in This Answer

- **Goal stated explicitly before metrics**: "Maximize the rate at which search intent converts into satisfying content consumption"
- **Named the strategic position of search**: ~15-20% of video starts but disproportionately valuable (high CPM, creator discovery, Google's moat)
- **Segmented by query type**: Navigational vs informational vs exploratory — each has different success metrics and baselines
- **Revenue formula connected**: Search-attributed watch time × ad load × search CPM premium
- **Three biases with shape + fix**: Duration, popularity, recency — each with specific mechanism and fix
- **"Repeat search" guardrail**: Frustration signal most candidates wouldn't think of
- **Named the real competitor**: YouTube's own home feed, not just external platforms
