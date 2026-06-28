# Area D: Hypothetical Product Questions

## What the HM is Testing

"Can this person think through a product problem they haven't seen before?"

The recruiter said: "We'll explore your product insights skills with some hypothetical questions — this is your chance to demonstrate your product skills, even if the questions aren't directly tied to the role."

These are PRODUCT SENSE questions — not behavioral. You're designing or improving a product in real-time.

---

## Framework for Any Product Question

Use this structure every time (memorize it):

```
1. CLARIFY (30 sec) — Ask 1-2 questions to scope the problem
2. USERS (30 sec)   — Who are the users? Pick 1-2 to focus on
3. PAIN (60 sec)    — What are their biggest pain points? List 3-4
4. SOLUTIONS (90 sec) — Brainstorm 3-4 solutions, then prioritize
5. PRIORITIZE (30 sec) — Pick the top solution and explain WHY
6. METRICS (30 sec) — How would you measure success?
```

**Total: 4-5 minutes per question**

---

## Practice Question 1: Role-Adjacent

**"Imagine you're building a data catalog for a large enterprise. How would you approach it?"**

### Model Answer:

**Clarify:** "Is this for technical users (data engineers, analysts) or also for business users (marketing managers, sales reps)? And is this greenfield or replacing an existing solution?"

*Assume: both technical and business users, greenfield*

**Users:**
- Data engineers (need to find tables, understand schemas, check freshness)
- Business analysts (need to find the right dashboard or dataset for a question)
- Business users (need to answer "where is the data for X?" without asking a data team)

**I'll focus on business analysts — they're the highest-leverage user because they bridge technical and business.**

**Pain points:**
1. "I don't know what datasets exist" — discovery problem
2. "I found a dataset but I don't know if it's trustworthy" — trust problem
3. "I found two datasets that seem like the same thing — which is canonical?" — duplication problem
4. "I need to understand how this metric is calculated" — lineage/definition problem

**Solutions:**
1. **Search-first catalog** — natural language search ("how many customers churned last quarter?") that returns the RIGHT dataset with context
2. **Trust badges** — every dataset has a freshness indicator, quality score, and owner badge (like a verified checkmark)
3. **Usage signals** — "this dataset is used by 47 dashboards and queried 2000 times/week" (social proof for trust)
4. **Lineage view** — click any metric to see where the data comes from and how it transforms

**Prioritize:** I'd start with #1 (search) + #2 (trust badges) together. Discovery without trust is useless — you find the data but don't know if you can use it. Trust without discovery means nobody finds the trusted data.

**Metrics:**
- Time-to-find (from "I have a question" to "I found the right dataset"): target <5 min
- Trust: % of queries hitting certified/SOT datasets vs uncertified
- Adoption: monthly active users of the catalog
- Reduction in "where is the data for X?" Slack messages

---

## Practice Question 2: Generic Product Sense

**"How would you improve Google Sheets for enterprise users?"**

### Model Answer:

**Clarify:** "When you say enterprise, do you mean large companies using Sheets for business operations? And by improve, do you mean adoption or engagement for existing users?"

*Assume: large companies, improve adoption for business workflows*

**Users:**
- Finance teams (budgeting, forecasting, reporting)
- Operations teams (project tracking, inventory)
- HR teams (headcount planning, org charts)

**Focus on Finance — highest-value enterprise CUJ.**

**Pain points:**
1. "Sheets can't handle our data volume" — performance degrades at 100K+ rows
2. "No audit trail" — who changed this cell and when? Critical for SOX compliance
3. "Connecting to live data is painful" — they want Sheets connected to their database, not copy-paste
4. "No approval workflows" — budget changes need sign-off but Sheets has no built-in process

**Solutions:**
1. **Connected Sheets (BigQuery integration)** — already exists, but enterprise onboarding is painful. Simplify the setup.
2. **Cell-level audit log** — who changed what, when, with ability to revert. Table stakes for finance.
3. **Approval workflows** — "Submit this budget for manager approval" built into the sheet.
4. **Row-level permissions** — different teams see different rows (budget by department).

**Prioritize:** #2 (audit log) — it's the #1 blocker for regulated industries adopting Sheets for real business processes. Without it, Finance can't use Sheets for anything SOX-relevant.

**Metrics:**
- Enterprise adoption: # of companies using Sheets for finance workflows
- Trust: % of enterprise users who cite "lack of audit trail" as a blocker (should decrease)
- Engagement: sheets per enterprise user per month

---

## Practice Question 3: Analytical/Estimation

**"A key metric for your data product dropped 20% week over week. How would you investigate?"**

### Model Answer:

**Structure: Segment → Validate → Hypothesize → Test**

**Step 1: Validate the drop is real**
- Is the data correct? (Pipeline delay, logging bug, definition change)
- Is it a calendar effect? (Holiday, end-of-quarter, fewer business days)
- Is the denominator stable? (If total users grew 25% but metric users grew only 5%, the ratio drops even if absolute numbers are up)

**Step 2: Segment the drop**
- By user type: Did all user groups drop or just one? (Maybe Sales dropped but Finance didn't)
- By geography: Is this global or one region?
- By platform: Web vs mobile vs API?
- By new vs existing users: Did we lose existing users or fail to onboard new ones?

**Step 3: Hypothesize root causes (ranked by likelihood)**
1. Product change: Did we ship anything last week? (Feature change, UI update, deprecation)
2. Data quality issue: Did a source pipeline break, causing missing or stale data?
3. External factor: Did a competitor launch something? Did a partner integration break?
4. Seasonality: Is this a known pattern?

**Step 4: Test each hypothesis**
- Check release notes for last week's deploys
- Check data pipeline health dashboards
- Compare drop timing to specific events
- Look at cohort behavior (do users who dropped also share another characteristic?)

**Step 5: Recommend action**
- If product change: revert or fix
- If data quality: fix pipeline + communicate SLA breach to users
- If external: monitor and adapt roadmap
- If seasonal: document the pattern for future reference

---

## Practice Question 4: Data-Specific

**"How would you measure the success of a data quality initiative?"**

### Model Answer:

**Three layers of metrics:**

**Layer 1: Data Quality Metrics (leading indicators)**
- Freshness: % of datasets meeting their SLA (e.g., "updated within 4 hours")
- Accuracy: % of automated data validation checks passing
- Completeness: % of records with all required fields populated
- Consistency: # of metrics with conflicting values across systems (should decrease to zero)

**Layer 2: User Impact Metrics (lagging indicators)**
- Trust: "Do you trust the data?" survey score (quarterly)
- Time saved: hours/week spent on data reconciliation (should decrease)
- Self-service rate: % of data questions answered without filing a ticket
- Incident rate: # of "the data is wrong" escalations per month

**Layer 3: Business Impact Metrics (outcome indicators)**
- Decision speed: time from "I need data" to "I made a decision"
- Forecast accuracy: did better data lead to better predictions?
- Adoption: % of teams using the SOT vs their own spreadsheet

"I'd report Layer 1 weekly to the data team, Layer 2 monthly to stakeholders, and Layer 3 quarterly to leadership. The north star is Layer 3, but you can't wait a quarter to know if you're on track — Layer 1 gives you weekly signal."

---

## Tips for Hypothetical Questions

| Do | Don't |
|----|-------|
| Always start by clarifying scope | Jump straight into solutions |
| Name specific users with specific pain points | Say "users want better experience" |
| Propose 3-4 solutions THEN prioritize | Only offer one solution |
| End with metrics | Forget to mention how you'd measure success |
| Think out loud — the process matters more than the answer | Go silent while thinking |
| Say "I'd want to validate this with user research" | Present your idea as the definitive answer |
| Acknowledge trade-offs in your chosen solution | Pretend there are no downsides |
