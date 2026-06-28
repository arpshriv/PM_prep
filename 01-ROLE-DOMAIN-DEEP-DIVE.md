# Area A: Role & Domain Understanding

## What the HM is Testing

"Does this person understand the world they'd be walking into on Day 1?"

The HM will assess:
- Do you understand what GCBP/UDL does and why it matters?
- Do you know who the users are and what their pain points look like?
- Can you connect your experience to THIS specific problem space?
- Do you have an informed perspective, not just generic data platform knowledge?

---

## 1. What is GCBP?

**GCBP = Google Cloud Business Platform**

GCBP is Google Cloud's internal business operations platform. It supports:
- How Google Cloud tracks its business (revenue, deals, customers)
- How sales teams manage their pipeline (leads → opportunities → closed deals)
- How finance reports Cloud revenue
- How marketing measures campaign effectiveness
- How support tracks customer health

Think of it as the "business data backbone" for Google Cloud — the equivalent of Salesforce + data warehouse + BI layer, but built internally for Google Cloud's scale.

**Why it matters:** Google Cloud is a $40B+ revenue business growing 25%+ YoY. Every inefficiency in business data = wrong decisions at scale.

## 2. What is UDL?

**UDL = Unified Data Layer**

UDL is a team WITHIN GCBP whose mission is:

> "Create a GCBP-supported, consolidated, and connected source of truth that is of high quality, accurate and reliable, for all of Cloud's business data and metrics."

**Translation:** UDL builds the single source of truth (SOT) for Cloud business data. Before UDL, different teams had different numbers for the same metrics (Sales says revenue is X, Finance says Y, Product says Z). UDL fixes that.

**Key concepts:**
- **SOT (Source of Truth)** — one canonical dataset per business metric
- **CUJ (Critical User Journey)** — the workflows internal Googlers follow (e.g., "sales rep checks pipeline health")
- **Operational vs Analytics** — UDL serves both real-time operational needs AND retrospective analytics

## 3. Who Are the Users?

The JD explicitly names them. Each has different pain points:

| User Group | What They Need | Pain Point |
|-----------|---------------|------------|
| **Sales** | Pipeline data, deal status, account health, quota tracking | "I can't trust the numbers — my dashboard says one thing, my manager's says another" |
| **Marketing** | Campaign performance, lead attribution, funnel metrics | "I can't connect marketing spend to closed deals" |
| **Finance** | Revenue reporting, forecasting, billing reconciliation | "We spend 2 weeks every quarter reconciling numbers across systems" |
| **Product** | Product usage metrics, adoption data, churn signals | "I need to know which features drive retention but the data is scattered" |
| **Support** | Customer health scores, escalation patterns, SLA tracking | "I can't see a unified view of customer health" |
| **Product Management** | Cross-functional metrics, roadmap impact data | "I can't measure whether my launches actually moved business metrics" |

## 4. The "Lead to Cash" Flow

The JD mentions "Enterprise Lead to Cash flow." This is the business lifecycle:

```
Lead → MQL → SQL → Opportunity → Proposal → Negotiation → Closed Won → Billing → Revenue
```

| Stage | Data Needed | UDL's Role |
|-------|------------|------------|
| Lead | Marketing attribution, source tracking | SOT for lead source |
| MQL/SQL | Qualification criteria, scoring | SOT for lead quality metrics |
| Opportunity | Pipeline value, probability, stage | SOT for pipeline reporting |
| Closed Won | Deal terms, contract value | SOT for bookings |
| Billing | Usage, invoicing, payments | SOT for billing data |
| Revenue | Revenue recognition, forecasting | SOT for revenue reporting |

**Why this matters for the interview:** If asked "what do you know about this domain?", walk through Lead-to-Cash and explain how data quality issues at each stage cascade downstream. E.g., "If the lead source attribution is wrong, marketing can't optimize spend, sales gets bad leads, and the pipeline forecast is off."

## 5. The Product Landscape

### What UDL likely builds:

- **Data pipelines** — ETL/ELT from source systems (CRM, billing, usage) into a unified warehouse
- **Data models** — Canonical schemas that define "what is a customer?", "what is revenue?", "what is an opportunity?"
- **Data quality frameworks** — Monitoring, validation, alerting on data freshness and accuracy
- **Self-service analytics** — Dashboards, query interfaces, APIs for internal users
- **Data catalog/discovery** — How do users FIND the right dataset?
- **Access control** — Who can see what data (PII, revenue, deal terms)

### Google's internal data stack (likely):

| Layer | Technology |
|-------|-----------|
| Warehouse | BigQuery (or internal equivalent like Mesa/Dremel) |
| Orchestration | Internal pipelines (similar to Airflow) |
| BI/Dashboards | Looker (Google-owned) |
| Data catalog | Dataplex or internal equivalent |
| Data quality | Custom frameworks |

## 6. Competitive Context

Even though this is an internal product, understanding the external landscape helps show domain depth:

| Competitor | What They Solve | Relevant to UDL |
|-----------|----------------|-----------------|
| Salesforce Data Cloud | Customer 360, unified customer data | Similar SOT ambition |
| Snowflake | Cloud data warehouse, data sharing | Warehouse layer comparison |
| dbt | Data transformation, modeling | How data models are built |
| Atlan / Alation | Data catalog, discovery, governance | Data discovery CUJ |
| Fivetran | Data ingestion, pipeline management | ETL/pipeline layer |
| Segment / mParticle | Customer data platform, event tracking | CDP comparison |

## 7. Questions YOU Should Ask the HM

Show you've done homework. Ask:

1. "What's the biggest data trust gap the team is trying to close right now — is it more about data freshness, accuracy, or discoverability?"
2. "How do you currently handle the tension between operational data needs (real-time) and analytics needs (retrospective)?"
3. "What does 'democratizing access' look like practically — is the bottleneck access controls, data literacy, tooling, or data quality?"
4. "Which user group (Sales, Finance, Marketing, Product) has the most urgent unmet data needs right now?"
5. "How does UDL's roadmap intersect with broader Google Cloud data products like BigQuery and Looker?"

---

## Prep Exercise

**Practice saying this out loud (2 minutes max):**

"The UDL team builds the single source of truth for Google Cloud's business data. The core problem is that different teams — Sales, Finance, Marketing, Product — need the same underlying data but currently get inconsistent numbers because it comes from different systems with different definitions. This erodes trust and wastes time on reconciliation instead of decision-making.

The product challenge is building a data platform that serves both operational workflows — like a sales rep checking pipeline status in real-time — and analytics workflows — like Finance doing quarterly revenue forecasting. These have different latency, accuracy, and access requirements, but they need to draw from the same source of truth.

What excites me about this is [connect to Roopali's specific experience with a similar problem she solved]."
