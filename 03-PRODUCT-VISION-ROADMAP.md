# Area C: Product Vision & Roadmap Thinking

## What the HM is Testing

"Can this person think beyond the next sprint and articulate where we should be in 2-3 years?"

They want to see:
- You can zoom out from features to strategy
- You understand the difference between vision (north star) and roadmap (how to get there)
- You can balance short-term stakeholder pressure with long-term platform investment
- You have an informed POV on data products, not just generic answers

---

## Framework: Vision → Strategy → Roadmap → Now

```
VISION (3 year)     → "Every Cloud Googler trusts the data and can self-serve"
STRATEGY (1 year)   → "Consolidate SOTs, build discovery, improve freshness"
ROADMAP (quarterly) → "Q3: Sales pipeline SOT, Q4: Marketing attribution SOT"
NOW (this sprint)   → "Ship pipeline data model v2 with freshness SLA"
```

### Practice Exercise: Articulate the UDL Vision

**The problem today (hypothetical but realistic):**
- 15+ data sources across CRM, billing, usage, marketing
- Each team built their own dashboards with their own definitions
- "Revenue" means 3 different things depending on who you ask
- New Googlers spend their first month figuring out which dashboard to trust
- Quarterly reporting takes 2 weeks of reconciliation

**The vision (2-3 years out):**
- ONE canonical definition for every business metric
- Self-service: any Googler can find, understand, and query the right data in <5 minutes
- Real-time: operational data is fresh enough for daily decision-making
- Trusted: data quality is monitored, SLAs are published, issues are caught before users see them

**The strategy (this year):**

| Pillar | Goal | Metric |
|--------|------|--------|
| Consolidation | Migrate top 10 business metrics to UDL SOTs | % of queries hitting SOT vs legacy |
| Discovery | Launch data catalog so users can find the right dataset | Time-to-find (minutes) |
| Quality | Publish freshness + accuracy SLAs per SOT | SLA compliance % |
| Adoption | Deprecate 50% of legacy dashboards | Active legacy dashboard count |

---

## How to Answer "What's Your Product Vision for This Space?"

**Structure (2-3 minutes max):**

1. **Start with the user pain** (30 sec)
   "The core problem is data fragmentation — different teams have different numbers for the same metric, which erodes trust and wastes time on reconciliation."

2. **Paint the north star** (30 sec)
   "In 3 years, I'd want every Cloud Googler to be able to find and trust the right data in under 5 minutes — no Slack messages asking 'which dashboard is the right one?'"

3. **Name the pillars** (60 sec)
   "To get there, I'd focus on three pillars: consolidation (canonical SOTs), discovery (finding the right data), and trust (quality monitoring + SLAs)."

4. **Ground it in a specific first step** (30 sec)
   "I'd start with the highest-pain metric — probably pipeline revenue, since Sales and Finance need alignment most urgently — and build the SOT, the quality framework, and the adoption playbook as a repeatable template for every subsequent metric."

5. **Show you know it's iterative** (15 sec)
   "The roadmap would evolve as we learn which metrics have the most adoption friction and where the data quality gaps are worst."

---

## Common Vision Questions & How to Handle Them

### "How would you prioritize which data products to build first?"

**Framework: Impact × Urgency × Feasibility**

| Data Product | Impact (who benefits, how much) | Urgency (pain today) | Feasibility (data exists, eng effort) | Priority |
|-------------|-------------------------------|---------------------|--------------------------------------|----------|
| Sales Pipeline SOT | Sales + Finance + Exec (high) | Quarterly reconciliation pain (high) | CRM data exists, needs modeling (medium) | P0 |
| Marketing Attribution | Marketing + Sales (medium) | Campaign ROI unknown (medium) | Multi-touch data is messy (hard) | P1 |
| Customer Health Score | Support + CSM (medium) | Churn risk (medium) | Needs usage + support + billing data (hard) | P2 |
| Product Usage Dashboard | Product + Eng (medium) | Feature adoption unknown (low) | Usage data exists in logs (easy) | P1 |

"I'd prioritize by asking: which metric, if wrong, causes the most expensive bad decisions? Pipeline revenue is the answer — a wrong pipeline forecast misallocates Sales resources across all of Cloud."

### "How do you balance platform work vs feature requests?"

**Answer shape:**

"I use a 70/20/10 framework:
- 70% on features that directly serve user CUJs (the SOTs, dashboards, APIs)
- 20% on platform work that makes future features faster (data quality framework, pipeline reliability, self-service tooling)
- 10% on exploratory work (what does AI-powered data discovery look like?)

The key is making platform work VISIBLE. I'd publish 'time to ship a new SOT' as a team metric — if it's 3 months today and platform investment can bring it to 2 weeks, that's a compelling ROI story for stakeholders."

### "What would you do in your first 90 days?"

**30-60-90 for this role:**

| Period | Focus | Output |
|--------|-------|--------|
| Days 1-30 | LISTEN — meet every user group, understand their CUJs and pain points | User pain map + current data landscape diagram |
| Days 31-60 | DIAGNOSE — audit existing SOTs, identify top 3 trust gaps, map data lineage | Gap analysis doc + prioritized problem list |
| Days 61-90 | PROPOSE — draft multi-year roadmap, align with eng on feasibility, present to leadership | Roadmap v1 + first sprint plan |

"I'd resist the urge to propose solutions in the first month. The biggest risk for a new PM in a data platform role is solving the wrong problem because you didn't listen long enough."

---

## Data Product Concepts to Know

| Concept | What It Means | Why It Matters for This Role |
|---------|--------------|------------------------------|
| **SOT (Source of Truth)** | One canonical dataset per metric | The core product UDL builds |
| **Data Mesh** | Decentralized data ownership by domain teams | Counter-argument to UDL's centralized approach — know the trade-offs |
| **Data Contracts** | Formal agreements on schema, freshness, quality between producer and consumer | How UDL enforces data quality |
| **Data Lineage** | Tracking where data comes from and how it transforms | Critical for debugging "why is this number wrong?" |
| **Semantic Layer** | Business-friendly definitions on top of raw data (e.g., Looker's LookML) | How UDL makes data accessible to non-technical users |
| **Data Freshness SLA** | Promise that data will be updated within X hours | Trust-building mechanism |
| **Self-Service Analytics** | Users can answer their own questions without filing a request | The end-state UDL is driving toward |
| **Data Democratization** | Making data accessible to everyone, not just analysts | The JD literally says this is the mission |

---

## Red Flags to Avoid in Vision Answers

| Red Flag | Why It's Bad | What to Say Instead |
|----------|-------------|-------------------|
| "Build a single dashboard" | Too tactical, not a vision | "Build a platform that enables any team to create trusted dashboards from canonical SOTs" |
| "Use AI to solve everything" | Buzzwordy, ungrounded | "Use AI to surface data quality issues before users see them" (specific, grounded) |
| "Migrate everything to BigQuery" | Technology-first, not user-first | "Start with the user CUJ that's most broken, then choose the right technology" |
| "We need better data governance" | Too abstract | "We need data contracts between producer and consumer teams with SLAs on freshness and accuracy" |
