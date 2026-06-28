# TMAY & Behavioral Stories — Roopali's Google Interview

## TMAY (Tell Me About Yourself) — FINAL

> "I'm a product manager who builds data products that give business teams one trusted number to act on.
>
> Right now at Palo Alto Networks, I'm the Senior PM for the global Customer Success data platform — metrics, pipelines, and governance across every product in our portfolio. When a new product launches, I work with stakeholders to define what adoption actually means for that product, get telemetry flowing from the product analytics team into our warehouse, build the dashboards, and govern it all through Atlan with clear metric owners and quality standards. I work across seven-plus teams — Sales for opportunity data, Finance for ARR and ACV, Renewals for contracts, People for org hierarchy, Product Analytics for telemetry — stitching it into one source of truth per product.
>
> Before this, I was at Cisco in CX Product Management — launched Success Track Services across Enterprise Networking, Data Center, and Compute, built the forecasting models and GTM strategy for each. Before that, 5 years at Enquero building analytics for clients like RingCentral and Cisco Enterprise Networking. At RingCentral, I built the subscription analytics platform — MRR, ARR, Churn — for the Global Sales Org. Three competing definitions of Churn when I started; I unified them, built the analytics, and it uncovered upsell opportunities that drove a 5-7% revenue increase. For Cisco, I built pipeline conversion analytics — lead to opportunity to closed deal by product and rep — and the Customer 360 view by integrating licensing data that had always lived in a separate system.
>
> Which brings me to today — I see the same problem of fragmented data, conflicting metrics, and teams who've stopped trusting the numbers. I've been solving that for 10 years. UDL is doing it at Google Cloud's scale, and that's exactly where I want to be."

**Timing:** ~100 seconds

---

## Googleyness Stories — TODO

### 6 Traits to Cover

| # | Story Theme | Googleyness Trait | Status |
|---|------------|-------------------|--------|
| 1 | Made a decision with incomplete data | Comfort with Ambiguity | DONE |
| 2 | Changed direction after receiving feedback | Values Feedback | DONE |
| 3 | Proposed an unconventional approach | Challenges the Status Quo | DONE |
| 4 | Redesigned a feature based on user research | User First | TODO |
| 5 | Raised an ethical concern about a product decision | Does the Right Thing | DONE |
| 6 | Built alignment across a resistant cross-functional team | Collaborative Nature | TODO |

---

## Story 1: Comfort with Ambiguity — PANW/CyberArk Integration

*"Tell me about a time you had to make a decision with incomplete information."*

**Situation:**
Palo Alto Networks acquired CyberArk, and I was tasked with building the integration roadmap for global Customer Success — migrating their data, processes, and dashboards into PANW's systems. This covered everything: Snowflake to GCP, their Salesforce to ours, Gainsight to Gainsight, telemetry, historical data, and 40 dashboards — across three functions: Customer Success, Professional Services, and Support.

**The ambiguity:**
The business leaders had written high-level BRDs and Key Design Decision documents for each workstream, but the data team wasn't included in those discussions. By the time we got involved, the data requirements were unclear — the KDD documents described business outcomes but didn't specify what data needed to move, where it lived, or what the dependencies were. We had 40 dashboards to migrate and no clarity on which to keep, rebuild, or retire. Nobody could tell me where to start.

**Task:**
Turn ambiguous, incomplete business documents into a concrete product requirements document and execution roadmap — without waiting for someone to hand me clear requirements, because they didn't exist.

**Action:**
I broke down each KDD myself and systematically filled the gaps through structured workshops. For every workstream, I drove a series of questions:

1. What's the business outcome this KDD is trying to achieve?
2. What does the actual business process look like — systems, workflows, playbooks?
3. Do we need historical data migrated, or just go-forward? If yes, which specific data objects?
4. For each of the 40 dashboards — do we migrate as-is, build net new on PANW's platform, or retire it?

For dashboards, I met with each stakeholder to get a walkthrough of what they used and why, then met with developers to understand the backend — data sources, metric definitions, refresh schedules. I prioritized into three buckets: migrate immediately (business-critical), rebuild within existing PANW dashboards (consolidation), and retire (redundant/low-usage).

For telemetry, I mapped how CyberArk handled product usage data versus how PANW does it, identified the gaps, and defined what needed to change.

This took dozens of workshops and continuous meetings across multiple teams over several weeks.

**Result:**
Delivered a comprehensive PRD for all three functions — Customer Success, Professional Services, and Support — with clear workstreams, dependencies, risks, and priorities. Went from "everything is ambiguous" to a structured roadmap with sprint planning.

**Learning:**
When you're brought in late and requirements are vague, you can wait for clarity or go create it. I chose to create it — by breaking the big ambiguous problem into small answerable questions and systematically working through each one.

**Why this demonstrates Comfort with Ambiguity:**
- Dropped into massive undefined integration with no clear requirements
- Didn't wait — took ownership and created structure
- Comfortable making prioritization decisions (migrate/rebuild/retire) without perfect information
- Turned chaos into a roadmap through systematic breakdown

---

## Story 2: Values Feedback — Data Governance Deadlock

*"Tell me about a time you changed direction after receiving feedback."*

**Situation:**
I was responsible for implementing the data governance and data quality framework across PANW's global Customer Success organization — covering CS, Professional Services, and Support. The framework had clear steps: establish governance structure (metric owners, domain owners, data stewards), then metadata (definitions, business logic, technical logic, lineage, usage patterns, certification), then data observability (integrity checks, quality rules).

**The problem:**
Work stalled at Step 1. When we brought business stakeholders together to assign ownership, nobody wanted accountability. Each team pushed responsibility to someone else — "that's the data team's job" or "that's the other team's metric." Complete deadlock.

**The feedback that changed my approach:**
I escalated to the Senior Director. His feedback was direct: "Instead of waiting for business owners to volunteer, why don't you draft all of it yourself — the definitions, business logic, technical logic, lineage — and bring it to them for review?"

That shifted my thinking. I had been approaching it as "the business defines, I facilitate." He was saying: "You draft, the business validates."

**Action:**
I changed approach completely:
- Drafted metric definitions, business logic, and technical logic myself based on my understanding of each product area and existing dashboards
- Documented lineage and usage patterns by working with IT technical leads
- Instead of asking leaders to "define your metrics," I set up workshops where I walked them through my draft and asked: "Is this right? What would you change?"

This changed the dynamic entirely. People are much more willing to react to a draft than create from scratch. The blank-page problem was the real blocker.

**Result:**
Work is now materially progressing with each workshop. Getting sign-offs on definitions, logic, and ownership from leaders across each function. The framework that was stuck for weeks is moving through all steps.

**Learning:**
Facilitation isn't always the right approach. Sometimes you lead with a strong draft and let people react. People engage more deeply when they're editing than when they're authoring. I've applied this to every cross-functional alignment problem since.

---

## Story 3: Challenges the Status Quo — Two Flavors of Adoption

*"Tell me about a time you proposed an unconventional approach."*

**Situation:**
At PANW, my team is the source of truth for product telemetry. For most products, the flow is straightforward: usage data flows from the product through pub/sub into our data lake, we transform it, and publish into Gainsight where CSMs see customer usage.

But for one product, the CS team was modifying our telemetry data in Gainsight — manually adjusting adoption numbers based on their direct knowledge. For example, some licenses were sold by Sales but the customer never intended to deploy them. Those unused licenses dragged down the usage percentage, making it look like the customer wasn't adopting when they were fully using everything they planned to.

**The problem:**
This modified data was flowing back into our data lake and showing up in dashboards. Product management dashboard showed one adoption number, CS dashboard showed another, Customer 360 showed a third. Same customer, same product, three different numbers. Nobody trusted any of them.

**The established approach:**
The conventional fix: stop the manual intervention, enforce one standard number, tell CS they can't modify the data. That's what "single source of truth" typically means.

**My unconventional approach:**
Before jumping to a solution, I sat with CS stakeholders and asked: "Is this adjusted metric actually important? Do you report it to executives? How much do you care?" They said yes — the influenced number reflected customer engagement reality that raw telemetry couldn't capture.

So instead of killing the adjustment or forcing one number, I proposed two official flavors of adoption:

1. **Standard Adoption** — raw telemetry-based, consistent across all functions (Sales, Finance, Product Management). No manual intervention.
2. **Influenced Adoption** — CS-specific view accounting for CSM engagement, no-intent-to-deploy licenses, and customer context only CS has. Clearly labeled as the CS lens.

Both documented, both governed, both with clear definitions. The difference is transparent, not hidden.

**Result:**
Cross-functional teams stopped arguing about which number was right. CS got the metric they needed for executive reporting. Product, Sales, and Finance kept their standard metric. Inconsistency disappeared — not by forcing one number, but by making two legitimate views explicit.

**Learning:**
Sometimes the right answer is two well-defined numbers rather than one wrong one. The key is both are governed, documented, and labeled. The enemy isn't having two metrics; it's having two metrics that nobody knows are different.

---

## Story 5: Does the Right Thing — Rejecting Manual Adoption Numbers

*"Tell me about a time you raised an ethical concern about a product decision."*

**Situation:**
At PANW, we have a hardware product — Product B — where the CS motion hadn't been fully set up. The customer journey wasn't captured through Gainsight, but we needed consistent adoption metrics for executive reporting. We worked with stakeholders to define adoption: registered devices over total devices sold. Additional lenses included hardened versions, versions >=10.2, etc.

**The problem:**
When the numbers came back, some CS managers weren't happy. Adoption was low — it showed how far they were from targets. They felt the numbers didn't reflect the real customer sentiment from their conversations.

So CSMs started manually entering customer-stated adoption numbers from engagement calls directly into Gainsight. Then they asked my D&A team to use those manually-entered numbers as the official adoption metric — replacing the telemetry-based numbers.

**The ethical concern:**
The manually-entered numbers were:
- Not verifiable — came from conversations, not telemetry
- Not consistent — customer wasn't sharing telemetry, so no way to validate
- Not maintained — no guarantee CSMs would update as things changed
- Potentially inflated — replacing low telemetry with higher self-reported numbers makes CS look better than data supports

We were being asked to build a source of truth on unverified self-reported data.

**Action:**
I asked the hard question directly: "Using manually-entered numbers from customer conversations as our adoption metric is not something I can support as the source of truth. These numbers aren't verifiable, aren't consistently maintained, and replacing telemetry with manual input undermines trust in every other metric we report."

I put my foot down: the source of truth must come from trusted, system-generated data. If telemetry isn't capturing the right signal, we fix the telemetry — we don't replace it with unverifiable inputs.

I offered an alternative: a separate "CSM Sentiment" field in Gainsight for qualitative customer feedback — clearly labeled as CSM input, not mixed into the adoption metric.

**Result:**
The team accepted. Telemetry-based adoption remained the official metric. CSM sentiment was added as supplementary context. The integrity of the source of truth was maintained.

**Learning:**
Doing the right thing sometimes means telling a stakeholder what they don't want to hear. A source of truth built on unverified data isn't a source of truth. As a data PM, my job is to protect metric integrity even when it's uncomfortable.
