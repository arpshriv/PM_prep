# Product Sense Framework — Mental Models for Segmentation, Needs & Solutions

> Quick-reference cheat sheet for the Product Sense (Comprehend) round.
> Use alongside `frameworks-canonical.md` and `google/analytical-mental-models.md`.
> These models work for ANY product — memorize the process, not specific answers.

---

## The Canonical Comprehend Framework (Full Reference)

```
1. COMPREHEND — Clarify goals & assumptions
   - Understand the prompt, break it down
   - Why should we care?
     • Mission
     • Strengths and weaknesses
     • Latent behaviors
     • Anything in the press?
     • Will it meet business goals?
   - Macro trends: RTO, rising interest rates, tariffs/inflation,
     AI boom, drone delivery, AR/VR

2. IDENTIFY USERS — Who are the key personas?
   - Prioritize top persona and say why. Select one.
   - Marketplace/Ecosystem → focus on one side and why
   - Demographic / psychographic / behavioral segmentation

3. REPORT NEEDS — What are their needs and challenges?
   - Marketplace/Ecosystem → focus on one
   - User journey and pain points
   - Prioritize top 2-3 challenges — why these?
   - TIP: Prioritization matrix → pick pain points with most
     potential vs goals

4. PRODUCT PRINCIPLES
   - Lean into strengths, minimize weaknesses
   - Meet users where they are
   - Focus on the crux of the problem (e.g., address anxiety,
     build discipline)

5. BRAINSTORM SOLUTIONS
   - TIP if stuck — the R's: reversing relationships,
     repurposing resources, recombining elements

6. SELECT MVP + SUCCESS METRICS
   - Why this MVP? Why these metrics?
   - TIP 1: Prioritization matrix / ROI estimate → pick
     highest-potential solution
   - TIP 2: Metrics ← goals (key metrics); secondary metrics ←
     user journey (for troubleshooting)

7. SUMMARIZE — End with "Imagine..."
```

---

## Segmentation: The "Job-to-be-Done" Method

### The Core Rule

**Segment by what users DO, not who they ARE.**

| Bad (demographic) | Good (behavioral) | Why it's better |
|---|---|---|
| "Millennials" | "Binge-watchers who watch 3+ episodes in one sitting" | Tells you what to build |
| "Students" | "Self-directed learners who study in 15-min bursts" | Reveals design constraints |
| "Working professionals" | "Hands-busy commuters who consume audio during transit" | Names the modality |
| "Gamers" | "Social escapists who game to hang out, not compete" | Changes what you build |

Demographics tell you nothing about what to build. Behaviors tell you everything.

### 3-Step Segmentation Process

**Step 1: Name the "Job" the product does**

Every product is hired to do a job. State it in one sentence:

| Product | The job it's hired to do |
|---|---|
| YouTube | "Help me fill time with content that matches my mood/intent" |
| DoorDash | "Get me food I want without leaving where I am" |
| Spotify | "Give me audio that fits this moment" |
| Google Maps | "Get me from here to there without thinking" |
| AR glasses | "Show me info about the world without pulling out a device" |
| Airbnb | "Give me a place to stay that feels like I belong" |
| Slack | "Get me an answer without scheduling a meeting" |

**Step 2: Ask "Who hires this product for DIFFERENT reasons?"**

The same product gets hired for different jobs by different people. Each distinct reason = a segment.

**YouTube example:**

| Segment | The job | Behavior signal |
|---|---|---|
| **Lean-back relaxers** | "Entertain me, I don't want to think" | Long sessions, autoplay on, high recommended-feed usage |
| **Intentional learners** | "Teach me this specific thing" | Search-driven, short sessions, high completion |
| **Background listeners** | "Give me audio while I do something else" | Music/podcasts/ASMR, screen off, long duration |
| **Social participators** | "Watch what my community is talking about" | Trending, comments, shares, Shorts |
| **Appointment viewers** | "Here for MY creator's new upload" | Subscription-driven, notification-clickers |

Each implies different product decisions:
- Lean-back → optimize autoplay, reduce decision fatigue
- Intentional learners → optimize search, chapter markers, skip-to-answer
- Background listeners → audio-only mode, lock-screen playback

**Step 3: Pick ONE and justify with the goal**

Template: *"I'm focusing on [segment] because they have the highest [frequency / willingness to pay / growth potential / strategic alignment] relative to our goal of [goal]. I'm deprioritizing [other segment] because [specific reason]."*

### The 4 Segmentation Lenses

Pick the lens that creates the most useful cuts for the question:

#### Lens 1: By Usage Behavior (DEFAULT — most common)

Segment by HOW people use the product differently.

| Product | Segments |
|---|---|
| **Netflix** | Binge-watchers vs. Nightly-wind-downers vs. Background-noise users |
| **Slack** | Power communicators vs. Lurker-readers vs. Channel-hoppers |
| **Spotify** | Playlist curators vs. Algorithm trusters vs. Podcast-first listeners |

**When to use**: "How would you improve X?" questions.

#### Lens 2: By Use Case / Job (best for 0-to-1 products)

Segment by WHAT they're trying to accomplish.

| Product | Segments |
|---|---|
| **AR glasses** | Navigators vs. Translators vs. Information seekers |
| **Google Photos** | Memory preservers vs. Content creators vs. Storage offloaders |
| **Notion** | Personal organizers vs. Team wiki builders vs. Project trackers |

**When to use**: "Design X" or "Build X for Y" questions.

#### Lens 3: By Lifecycle Stage (best for growth questions)

| Stage | Behavior | What they need |
|---|---|---|
| **Curious** | Heard about it, hasn't tried | Activation — reduce friction to first value |
| **Casual** | Uses occasionally, no habit | Engagement — build habit loop |
| **Core** | Uses regularly, part of routine | Retention — deepen, prevent churn |
| **Champion** | Advocates, high LTV | Expansion — upsell, referral |

**When to use**: "How would you grow X?" or "Get first million users" questions.

#### Lens 4: By Value Derived (best for marketplace questions)

Segment BOTH sides of the marketplace.

| Product | Supply side | Demand side |
|---|---|---|
| **Airbnb** | Income-supplementers (spare room) vs. Professional operators (multiple properties) | Budget explorers vs. Convenience seekers vs. Experience hunters |
| **YouTube** | Hobbyist creators vs. Mid-class professionals (100K-1M) vs. Media companies | Lean-back vs. Intentional learners vs. Appointment viewers |
| **DoorDash** | Small local restaurants vs. Chain restaurants vs. Ghost kitchens | Convenience orderers vs. Discovery/exploration orderers vs. Bulk/family orderers |

**When to use**: Marketplace questions — always segment BOTH sides.

### Quick Reference: Lens by Question Type

| Question type | Default lens |
|---|---|
| "Improve X" | Usage behavior |
| "Design X" / "Build X for Y" | Use case / Job |
| "Grow X" / "First million users" | Lifecycle stage |
| "Improve marketplace X" | Value derived (both sides) |
| "X for [specific audience]" | Don't sub-segment — go to needs |

### The Nancy Chu Rule: Do You Even Need to Segment?

*"Why do we segment? Because the space is too big. If it's contained, maybe you don't need to segment."*

**Don't segment when:**
- The prompt is already narrow ("Design for truck drivers" — they ARE the segment)
- One use case covers 80%+ of users
- Sub-segmenting would feel forced

**The test**: If removing the segmentation doesn't change your solution, you didn't need it.

### Common Segmentation Mistakes

| Mistake | Fix |
|---|---|
| Mixing dimensions ("Tech enthusiasts, tourists, visually challenged, gamers") | Pick ONE dimension and be consistent |
| Segments that don't change the product ("Young vs. old") | Each segment should imply a DIFFERENT product decision |
| Too many segments (6-8 listed) | 3-4 max. Name, pick, move on. Brevity = confidence. |
| Picking without justifying | Tie to goal: "Highest [X] relative to our goal of [Y]" |
| Not deprioritizing | Say: "I'm NOT focusing on [X] because [reason]" — shows judgment |

---

## Needs & Pain Points: The "Journey Gate" Method

### The Process

**Step 1: Map the user journey for your CHOSEN segment (not generic)**

Bad: "Wake up, check phone, commute, work, come home" (this is everyone)
Good: Map the journey specific to how your segment USES or WOULD USE the product.

**Step 2: At each step, ask: "What's frustrating, slow, or missing here?"**

| Journey step | Current behavior | Friction / Pain |
|---|---|---|
| Discover → | How do they find out about it? | Hard to discover? Don't know it exists? |
| Evaluate → | How do they decide to try? | Confusing value prop? Too expensive to try? |
| First use → | What's their first experience? | Too complex? Doesn't deliver value fast enough? |
| Core use → | The main thing they do | Slow? Unreliable? Missing key feature? |
| Return → | What brings them back? | Nothing triggers return? Forgot about it? |
| Share → | Do they tell others? | No shareable moment? Embarrassing to recommend? |

**Step 3: Prioritize 2-3 pain points**

Use this 2×2 mentally:

```
            HIGH frequency
                │
    ┌───────────┼───────────┐
    │  NOISY    │  PRIORITY │
    │  BUT LOW  │  #1 & #2  │
HIGH├───────────┼───────────┤
pain│  IGNORE   │  NICHE    │
    │           │  (maybe   │
    │           │   #3)     │
    └───────────┼───────────┘
                │
            LOW frequency
```

Pick pain points that are BOTH high-frequency AND high-pain. A pain that happens once a year isn't worth solving. A pain that happens daily but is mild may not be worth solving either. The intersection is where product-market fit lives.

### Pain Point Quality Check

Each pain point should pass this test:

- **Specific to your segment** (not "everyone has this problem")
- **Observable** (you could see someone struggling with this)
- **Connected to the product's job** (not a tangential life problem)
- **Solvable** (you can imagine a product feature addressing it)

Bad: "Users are busy" (universal, not actionable)
Good: "Tourists stop walking 15+ times per hour to check phone for directions, losing immersion and feeling unsafe in unfamiliar areas" (specific, observable, solvable)

---

## Solutions: The "Strength-Anchored" Method

### The Rule

Every solution should use at least one of the company's **unique strengths**. If a competitor could build the same solution equally well, it's not differentiated enough.

| Company | Unique strengths to anchor solutions on |
|---|---|
| **Google** | Maps data, Search/Gemini AI, Translate, Android distribution, ad demand pool |
| **Meta** | Social graph, Reels algorithm, WhatsApp reach, Advantage+ ad AI |
| **Apple** | Hardware-software integration, privacy brand, installed base, App Store |
| **Spotify** | Audio personalization algorithm, mood/activity data, cross-platform |
| **Netflix** | Content investment scale, recommendation algorithm, global distribution |
| **Amazon** | Logistics infrastructure, Prime membership, product catalog, Alexa |

### Solution Generation: The "3 R's" (when stuck)

From your canonical framework — when you can't think of solutions:

1. **Reverse relationships**: Flip who does what. Instead of users searching for restaurants, restaurants push offers to nearby users. Instead of patients finding doctors, doctors find patients who match their specialty.

2. **Repurpose resources**: Use an existing asset for a new purpose. Google already has Street View imagery → use it for AR navigation overlay. Spotify already knows your workout playlist → suggest workout routines timed to your music.

3. **Recombine elements**: Mash two existing features together. Google Maps + Google Translate = real-time translated walking directions. YouTube Shorts + Shopping = swipeable product demos.

### Solution Presentation: The "Why This MVP" Structure

For each solution, give 1 sentence on each:

1. **What it is** (the feature, concretely)
2. **Which pain point it solves** (from your prioritized list)
3. **Which strength it leverages** (why Google/Meta/etc. is uniquely positioned)
4. **What you're explicitly excluding from V1** (shows product judgment)

Then pick your MVP and justify: "I'm choosing this because it has the highest [impact/feasibility ratio] and directly addresses [pain point #1] using our unique advantage in [strength]."

---

## The "Imagine" Close: How to Land It

### Structure

One paragraph. 3-4 sentences. Paint a **specific, visceral scene** of one person using your product in one moment.

### The Formula

> "Imagine [specific person] in [specific situation]. [Current frustration in one sentence]. Now with [your product], [describe the new experience — sensory, emotional, concrete]. [One sentence about how their life/moment is different]."

### Examples

**AR glasses**: "Imagine walking through Rome for the first time. The ancient inscriptions on the Colosseum translate themselves as you look at them. A floating arrow on the cobblestone guides you to the trattoria your friend recommended. You never once reached into your pocket."

**Podcasting app**: "Imagine a nurse finishing a 12-hour night shift, too tired to read, too wired to sleep. She puts in her earbuds and her daily briefing starts — 15 minutes of the three stories that matter to her, in a voice she trusts. By the time she's home, she feels informed, not overwhelmed."

**DoorDash improvement**: "Imagine a single mom on a Tuesday night, kids hungry, fridge empty, and she's still on a work call. Three taps, and 25 minutes later, the doorbell rings with exactly what her kids wanted. She didn't have to hang up, drive anywhere, or feel guilty about not cooking."

### What makes it work

- **Specific person** (not "users" — one human)
- **Specific moment** (not "in general" — one scene)
- **Sensory detail** (what they see, hear, feel)
- **Emotional payoff** (relief, delight, connection — not features)
- **No jargon** (no "leveraging AI" or "cross-platform synergy" — human language)

### What to avoid

- "Imagine a world where..." (too abstract, no person)
- Technical features disguised as imagination ("Imagine the ML model recommending...")
- Too long (more than 4-5 sentences loses impact)
- Repeating your solution list (the close should FEEL different from the analytical body)

---

## The 90-Second Pre-Answer Mental Walkthrough

Before you start talking, run this silently:

```
1. COMPREHEND (15 sec)
   "Why should [company] care? What's the strategic stake?"
   → State the goal in 1 sentence

2. SEGMENT (15 sec)
   "What's the job? Who hires it for different reasons?"
   → Name 3-4 segments, pick 1, justify

3. NEEDS (15 sec)
   "What's the journey for THIS segment? Where's the friction?"
   → 2-3 pain points, ranked by frequency × severity

4. PRODUCT PRINCIPLES (10 sec)
   "Lean into what strength? Meet users where?"
   → 1-2 principles that constrain solutions

5. SOLUTIONS (20 sec)
   "3 options anchored on company strengths"
   → Pick MVP, name what's excluded

6. METRICS (10 sec)
   "Value moment → NSM → 2-3 secondary"
   → Use the Analytical mental model

7. IMAGINE CLOSE (5 sec)
   "One person, one moment, one feeling"
   → Have the scene ready before you start talking
```

Total: 90 seconds of silent thinking → 20-25 minutes of structured delivery.

---

## Cross-Framework Reminders (from canonical)

- Everything ladders to the goal you set upfront
- Segment by behavior, not demographics; only segment if the space needs cutting
- Pain points must be segment-specific — if they apply to all users, you haven't proven empathy
- Lean into strengths, minimize weaknesses — every solution should use a company advantage
- Close with "Imagine..." — visceral, human, emotional
