# Roopali's Profile → Google Role Mapping

## Strength Analysis

| JD Requirement | Roopali's Match | Strength Level | Source |
|---------------|----------------|----------------|--------|
| 5 yrs product management | 10+ years (Palo Alto, Cisco, RingCentral) | STRONG | Direct |
| 2 yrs databases/analytics/big data | 10+ years — entire career is data & analytics | STRONG | Direct |
| Customer Data Platforms / Data Products | KPI dashboards, analytics engines, data frameworks at 3 companies | STRONG | Direct |
| Enterprise Lead-to-Cash flow | Subscription analytics (MRR, ARR, Churn), pipeline analytics, bookings | STRONG | RingCentral + Cisco |
| Cross-functional (Sales, Marketing, Finance, CS) | Led across all 4 at every company | STRONG | All roles |
| Multi-year roadmap | Success Track portfolio at Cisco, analytics platform at RingCentral | STRONG | Map to specific story |
| Data platform/warehouse infra | Oracle DW at Brocade, Snowflake/SFDC at Cisco, ETL/Informatica | MODERATE | Need to elevate in stories |
| MS Business Analytics (SCU) | ✅ | STRONG | Preferred qual |
| Internal product for Googlers | Gap — her products serve external customers/sales teams | GAP | Reframe: internal Sales/CS users are similar |

## Her Superpowers for This Interview

1. **Lead-to-Cash is her ENTIRE career** — MRR, ARR, Churn, pipeline, bookings, subscription analytics. She doesn't need to learn this; she's lived it for 10 years.

2. **She's built exactly what UDL builds** — at RingCentral she built "advanced subscription and revenue analytics" that was the SOT for the Global Sales Organization. That IS UDL's mission.

3. **Cross-functional is her natural mode** — every role involved Sales, Marketing, CS, Finance, Engineering. Not aspirational — proven.

4. **She quantifies impact** — 5-7% revenue increase, 20% ROI boost, 60% time reduction, 15% bookings increase. Google loves numbers.

## Gaps to Bridge

| Gap | How to Bridge in the Interview |
|-----|-------------------------------|
| Internal product (for Googlers, not external customers) | Frame: "At RingCentral, my users were internal Sales teams — they consumed analytics I built. Same dynamic as UDL serving internal Cloud Googlers." |
| Data platform/infra (JD says "data warehouse infra features") | Elevate the Oracle DW implementation at Brocade and Snowflake work at Cisco. Say: "I've been on both sides — building the analytics layer AND driving the underlying data infrastructure decisions." |
| Google Cloud specific | Show you've done homework: mention BigQuery, Looker, Dataplex. Say: "The tools are different but the problem — consolidating business data into a trusted SOT — is the same problem I solved at RingCentral." |
| "Democratize access" language | Frame RingCentral's mobile KPI app as democratization: "We put revenue analytics in every sales leader's pocket — that's democratization." |

---

## 6 STAR Stories From Roopali's Experience

### Story 1: "Define product requirements for data products"
**USE: RingCentral — Subscription & Revenue Analytics**

**S:** RingCentral's Global Sales Organization had no unified view of subscription health — MRR, ARR, and Churn were calculated differently by Sales, Finance, and CS teams, leading to conflicting reports and missed upsell opportunities.

**T:** I was the PM responsible for defining requirements for a unified subscription and revenue analytics platform that would serve as the single source of truth for all revenue metrics.

**A:**
- Interviewed 15+ stakeholders across Sales, Finance, and CS to map how each team defined and used MRR/ARR/Churn
- Discovered 3 conflicting definitions of "Churn" alone — one excluded downgrades, one included them, one only counted full cancellations
- Wrote product requirements that established ONE canonical definition per metric, validated by Finance (the ultimate owner of revenue numbers)
- Worked with engineering to build the analytics engine on [their data stack], with automated pipelines feeding the unified model
- Prioritized upsell/cross-sell opportunity detection as the first feature — this was the highest-value use case for Sales leadership

**R:** The platform uncovered upsell and cross-sell opportunities that contributed to a 5-7% revenue increase. Became the SOT for the Global Sales Organization — replaced 4 competing dashboards.

**LEARNING:** "The hardest part wasn't building the product — it was getting Finance and Sales to agree on one definition of Churn. I learned that data product requirements are 70% alignment, 30% technology."

**WHY THIS MAPS TO GOOGLE:** UDL's mission is literally "consolidated source of truth for business data." Roopali did this at RingCentral. Same problem, same stakeholders, same challenge.

---

### Story 2: "Drive data platform improvements"
**USE: Brocade/Cisco — Data Warehouse Implementation**

**S:** At Brocade (later Cisco acquisition), customer support data was siloed across Salesforce, Adobe web analytics, and Oracle — making it impossible to get a unified view of customer technical issues and their impact on satisfaction.

**T:** I was responsible for implementing an Oracle data warehouse that consolidated data from all three sources, enabling cross-source analytics for the first time.

**A:**
- Mapped the data landscape — identified all source systems, their schemas, update frequencies, and data quality issues
- Designed the ETL pipeline using Informatica to extract, transform, and load data from Salesforce, Adobe, and Oracle into the unified warehouse
- Made a key architectural decision: normalize customer IDs across all three systems (each used a different identifier) — this was the hardest technical problem
- Built Tableau dashboards on top of the warehouse for the sales enablement team to track content consumption from the Flight Deck portal

**R:** Enabled the first-ever cross-source view of customer journey from web engagement → support tickets → resolution. Sales enablement team could now see which content correlated with fewer support tickets.

**WHY THIS MAPS TO GOOGLE:** The JD says "drive data platform/data warehouse infra improvements." This story shows she's done exactly that — designed a warehouse, built ETL, unified data from multiple sources.

---

### Story 3: "Multi-year roadmap"
**USE: Palo Alto Networks — Customer Success Analytics**

**S:** Palo Alto Networks had a massive product portfolio but no unified way to measure Customer Success across it. Each product team tracked their own metrics, making it impossible for executives to compare customer health across products or identify at-risk accounts holistically.

**T:** I led the strategic definition and multi-year implementation of KPIs for evaluating Customer Success across the entire product portfolio.

**A:**
- Year 1: Defined the KPI framework — customer sentiment, churn risk, product utilization, ARR, MRR, deployment efficiency, adoption rates, time-to-value. Got executive sign-off on standard definitions.
- Year 1-2: Built advanced analytical dashboards for each KPI, starting with churn risk (highest business impact) and adoption rates (leading indicator)
- Year 2-3: Extended to cross-portfolio views — executives could now compare customer health across firewall, cloud security, and endpoint products on one dashboard
- Ongoing: Iterated based on executive feedback — added deployment efficiency metrics when a new product launch revealed slow onboarding was driving early churn

**R:** The initiative directly contributed to significant enhancements in customer satisfaction and retention (quantify with specific numbers if available — e.g., "X% reduction in churn" or "identified Y at-risk accounts worth $Z in ARR").

**WHY THIS MAPS TO GOOGLE:** Multi-year roadmap for analytics across a complex portfolio. Google Cloud has the same challenge — many products, many customer segments, need unified measurement.

---

### Story 4: "Cross-functional product development"
**USE: Cisco — Success Track Services Launch**

**S:** Cisco was launching Success Track Services — a new packaged service offering for Enterprise Networking, Data Center Networking, and Compute. It required coordinating across Product Management, Technical Architects, Engineering, Sales, Marketing, and Support to define, build, and go to market.

**T:** I led the product requirements and cross-functional coordination for the launch, bridging technical architecture decisions with go-to-market strategy.

**A:**
- Collaborated with Technical Architects to define new use cases for Success Track Services — translated customer needs into technical requirements
- Partnered with GTM teams to identify target customer segments for each Success Track offering
- Built revenue and customer forecasting models for three product lines (Enterprise Networking, Data Center Networking, Compute) — these became the basis for business planning
- Resolved a key conflict: Marketing wanted to launch all three tracks simultaneously for "bigger splash"; Engineering said the Data Center track needed 2 more months. I proposed a phased launch (Enterprise first, Data Center 2 months later) that satisfied both.

**R:** Successfully launched all three Success Track offerings. The forecasting models I built became the standard for future service launches at Cisco.

**WHY THIS MAPS TO GOOGLE:** Cross-functional launch across multiple product lines with competing timelines. Exactly what Google PM II does.

---

### Story 5: "Trusted advisor to stakeholders"
**USE: Palo Alto Networks — Executive Advisory**

**S:** As a Senior PM, I was asked to deliver data-driven insights to the executive team during a period of significant business challenges — the company was navigating a transition from hardware to software/subscription revenue, and executives needed analytics they could trust to make strategic decisions.

**T:** I acted as the primary analytics advisor to executives, responsible for ensuring data-driven decision-making during the transition.

**A:**
- Built a regular cadence of executive briefings — not just dashboards but interpreted insights with recommendations
- Said "no" when asked to rush a customer health score that I knew had data quality issues — "I'd rather give you the right answer in 2 weeks than the wrong answer today"
- When executives questioned a churn metric that showed an unexpected spike, I dug into the data and discovered it was a definitional issue (product upgrades were being counted as churn). Fixed the definition and rebuilt trust.
- Created a "data confidence" rating for each metric I presented — green (validated), yellow (directionally correct, validating), red (preliminary, use with caution)

**R:** Became the go-to person for data-driven strategic decisions. The "data confidence" rating was adopted by other analytics teams across the company.

**WHY THIS MAPS TO GOOGLE:** JD says "engage regularly as a trusted advisor with internal stakeholders." This is exactly that — advising executives, managing expectations, building trust through transparency.

---

### Story 6: "Partner with Engineering and UX"
**USE: RingCentral — Automated Sales Compensation Engine**

**S:** RingCentral's sales compensation tracking was a manual process — executives spent hours comparing quota attainment against goals for primary and secondary sellers using spreadsheets. The data was error-prone and delayed.

**T:** I designed an automated Sales & Compensation analytics engine to replace the manual process.

**A:**
- Partnered closely with Engineering to design the data pipeline — compensation data had to flow from HR systems, CRM, and finance with daily freshness
- Key technical partnership moment: The engineer proposed a batch-processing approach (updated nightly). I pushed back with user research showing that sales managers checked comp data in real-time during deal negotiations. We compromised: near-real-time for quota attainment (hourly), batch for historical trend analytics (nightly).
- Worked with UX to design the executive dashboard — the original design had 15 metrics on one screen. Through iterative user testing with 3 VP-level users, we narrowed to 5 key metrics with drill-down capability.

**R:** Achieved a 60% reduction in time spent on performance tracking. Replaced a manual spreadsheet process that took 2+ days with an automated dashboard that updated hourly.

**WHY THIS MAPS TO GOOGLE:** Deep Eng + UX partnership with specific examples of technical trade-offs and design iteration. Not just "we worked together" — shows how the partnership changed the outcome.

---

## Narrative Thread: "I've Built UDL Before"

Across her career, Roopali has solved the SAME problem UDL solves, multiple times:

| Company | What She Built | UDL Equivalent |
|---------|---------------|----------------|
| RingCentral | Unified subscription/revenue analytics (MRR, ARR, Churn) for Global Sales | SOT for revenue metrics |
| Cisco | Revenue forecasting models across 3 product lines | Cross-product business data |
| Brocade | Oracle DW consolidating Salesforce + Adobe + Oracle | Data warehouse infra |
| Palo Alto | Cross-portfolio KPI framework for Customer Success | Unified metrics across products |

**Interview pitch:** "I've spent the last 10 years solving the exact problem UDL is solving — building trusted, unified data products for business teams. At RingCentral, I built the SOT for subscription analytics that the entire Global Sales Organization relied on. At Palo Alto, I built the KPI framework that executives used to make strategic decisions about customer retention across their entire product portfolio. The users are different — Googlers instead of sales reps — but the challenge is identical: consolidate, trust, and democratize business data."
