# Mock HM Interview Script

## Format: 45 minutes

| Block | Time | What Happens |
|-------|------|-------------|
| Intro + warm-up | 5 min | HM introduces self, asks Roopali to walk through background |
| Behavioral deep-dive | 15 min | 2-3 STAR questions tied to JD |
| Product vision / problem space | 15 min | Hypothetical questions + domain understanding |
| Roopali's questions | 5 min | Show homework |
| Wrap | 5 min | Next steps |

---

## Block 1: Walk Me Through Your Background (5 min)

### The Question:
"Tell me about yourself and why you're interested in this role."

### Model Answer (2 minutes, practiced):

"I'm a data and analytics PM with 10 years of experience building data products for enterprise business teams — the internal Sales, Finance, and Customer Success teams that need trusted data to make decisions.

Most recently at Palo Alto Networks, I led the strategic definition of Customer Success KPIs across their entire product portfolio — building the unified analytics layer that executives used to track churn risk, adoption, and revenue health across firewall, cloud security, and endpoint products.

Before that at Cisco, I launched Success Track Services across three product lines, building the revenue forecasting models and cross-functional coordination between Product, Engineering, Sales, and Marketing.

And at RingCentral, I built what I'd call a 'source of truth' for subscription analytics — MRR, ARR, Churn — for the Global Sales Organization. That platform uncovered upsell opportunities that contributed to a 5-7% revenue increase.

What draws me to this role is that UDL is solving the same problem I've been solving for a decade — consolidating fragmented business data into a trusted source of truth — but at Google Cloud's scale. The Lead-to-Cash data challenge, the cross-functional user base across Sales, Finance, Marketing, and Product — I've lived that at three companies. I want to do it at the scale that matters most."

### Expected Follow-up:
"What's the most complex data challenge you've faced?"

→ Use Story 1 (RingCentral — 3 conflicting Churn definitions)

---

## Block 2: Behavioral Deep-Dive (15 min)

### Question 1: "Tell me about a time you built a data product from scratch. What was the hardest part?"

→ **Use Story 1: RingCentral Subscription Analytics**

Expected follow-ups:
- "How did you get Finance and Sales to agree on one Churn definition?" → Talk about the specific workshop you ran, the criteria you used, who had final say
- "How did you prioritize which metric to build first?" → "Upsell/cross-sell detection — highest revenue impact, directly measurable"
- "What would you do differently?" → "I'd invest more in data quality monitoring upfront — we found data issues in production that we could have caught in staging"

### Question 2: "Tell me about a time you had to influence stakeholders without direct authority."

→ **Use Story 5: Palo Alto Networks Executive Advisory**

Expected follow-ups:
- "Give me an example of when you said 'no' to an executive." → The churn metric data quality issue — "I'd rather give you the right answer in 2 weeks than the wrong answer today"
- "How did you build the 'data confidence' rating system?" → Explain: green/yellow/red, what criteria determined each level, how executives responded
- "What happened when you found the upgrade-counted-as-churn bug?" → Walk through the investigation, the fix, and the trust recovery

### Question 3: "Tell me about a time you balanced short-term requests with long-term platform investment."

→ **Use Story 3: Palo Alto Multi-Year KPI Roadmap**

Expected follow-ups:
- "How did you decide what to build in Year 1 vs Year 2?" → "Started with churn risk — highest business impact and most demand from CS leaders"
- "Did you ever have to cut something from the roadmap?" → Show you can make hard trade-offs
- "How did you measure whether the KPI framework was successful?" → Tie to customer satisfaction and retention improvements

---

## Block 3: Product Vision / Problem Space (15 min)

### Question 4: "You're the PM for UDL. What would you do in your first 90 days?"

→ **Use the 30-60-90 from the roadmap prep:**

"Days 1-30: Listen and learn. I'd meet every user group — Sales, Finance, Marketing, Product, Support — and understand their CUJs and pain points. I'd also audit the existing data landscape — what SOTs exist, what's the data quality, where are the trust gaps. Output: a user pain map and data landscape diagram.

Days 31-60: Diagnose. I'd prioritize the top 3 trust gaps — probably where the most time is spent reconciling conflicting numbers. I'd map data lineage for those metrics to understand where the discrepancies originate. Output: a gap analysis doc with prioritized problem list.

Days 61-90: Propose. I'd draft the roadmap — starting with the highest-pain metric as a proof point. I'd align with Engineering on feasibility and present to leadership. Output: roadmap v1 with the first sprint plan.

I'd resist jumping to solutions in Month 1. In data products, the biggest risk is solving the wrong problem because you didn't understand the data landscape well enough."

### Question 5: "How would you measure success for a data platform like UDL?"

→ **Use the three-layer metrics framework:**

"Three layers:
- Layer 1 — Data quality metrics (weekly, for the team): freshness SLA compliance, accuracy check pass rate, completeness
- Layer 2 — User impact metrics (monthly, for stakeholders): trust survey scores, time saved on reconciliation, self-service rate, 'data is wrong' escalation count
- Layer 3 — Business impact metrics (quarterly, for leadership): decision speed, forecast accuracy, SOT adoption vs legacy dashboards

The north star is Layer 3, but Layer 1 gives weekly signal on whether we're on track."

### Question 6 (hypothetical): "A Sales VP comes to you and says 'I don't trust the pipeline numbers in your dashboard.' How do you handle this?"

→ **Structure your answer:**

1. "First I'd ask: what specifically doesn't match? Is it the total pipeline value, the stage distribution, or the close rate forecast?"

2. "Then I'd investigate: compare the dashboard numbers against the VP's source (probably their own spreadsheet or SFDC report). Find the specific discrepancy."

3. "Common root causes in my experience:
   - Definition mismatch: the dashboard includes partner pipeline, their spreadsheet doesn't
   - Timing mismatch: dashboard refreshes nightly, their SFDC view is real-time
   - Scope mismatch: dashboard shows all opportunities, they're filtering to their team only"

4. "Once I find the root cause, I'd fix it AND add transparency — show the dashboard's last-updated timestamp, data source, and definition of 'pipeline' right on the dashboard. Trust comes from transparency."

5. "I'd also turn this into a systemic fix — if one VP doesn't trust the numbers, others probably don't either. I'd add a 'data confidence' indicator and schedule a pipeline data review with Sales leadership."

"At RingCentral, I had exactly this scenario with Churn metrics — the VP of Sales and CFO had different numbers. The root cause was three different definitions of Churn. We resolved it by establishing one canonical definition validated by Finance."

---

## Block 4: Questions for the HM (5 min)

Pick 3 from this list:

1. "What's the biggest data trust gap the team is trying to close right now?"
2. "How do you currently handle the tension between operational needs (real-time) and analytics needs (retrospective)?"
3. "Which user group has the most urgent unmet data needs — Sales, Finance, Marketing, or Product?"
4. "How does UDL's roadmap intersect with BigQuery and Looker?"
5. "What does success look like for this role in the first 6 months?"
6. "What's the team's current approach to data quality monitoring?"

---

## Common Traps to Avoid

| Trap | How to Avoid |
|------|-------------|
| Talking about "data" generically | Always tie to a specific user and their specific pain |
| Over-indexing on technology | Lead with user need, end with technology |
| Describing team accomplishments | Say "I" — "I defined," "I built," "I decided" |
| Giving 5-minute answers | Practice: STAR stories should be 3 min MAX |
| Not asking questions | Prepare 3 questions that show you've researched the team |
| Being too humble | Google wants confident PMs — own your impact |
| Memorized answers that sound rehearsed | Practice until it sounds natural, not scripted |

---

## Practice Plan

| Day | Activity | Time |
|-----|----------|------|
| Day 1 | Read domain deep-dive (01). Read JD aloud. | 1 hr |
| Day 2 | Write 6 STAR stories using templates. Read aloud. | 2 hrs |
| Day 3 | Practice "walk me through your background" pitch (2 min, timed). | 30 min |
| Day 4 | Practice 3 behavioral questions with a partner (Arpit!). Time each answer. | 1.5 hrs |
| Day 5 | Practice product vision answers: 90-day plan, metrics, VP trust scenario. | 1.5 hrs |
| Day 6 | Full mock interview (45 min, all blocks). Record and review. | 1.5 hrs |
| Day 7 | Review weak spots. Polish 1-2 stories. Rest before interview. | 1 hr |
