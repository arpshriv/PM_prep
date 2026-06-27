# Segmentation Cheat Sheet — Reusable Segments by Product Category

> Multi-dimensional segments for the product categories most common in Google PM interviews.
> When a question names a product, look up its category and pick the DIMENSION that creates
> the most useful cut for that specific question.
> Companion to `product-sense-mental-models.md` (the HOW) — this file is the WHAT.

---

## The 6 Segmentation Dimensions

Behavioral is the default, but 5 other dimensions exist. **Pick the one that produces segments
where each segment implies a DIFFERENT product decision.** If the segments don't change what
you'd build, you picked the wrong dimension.

### When to Use Which Dimension

| Dimension | What it cuts by | When to use | Example question |
|---|---|---|---|
| **1. Behavioral** | How they USE the product | DEFAULT — "improve X", general product sense | "Improve YouTube" |
| **2. Use Case / Job** | WHY they hired the product | 0-to-1, new product, GTM | "Design AR glasses" |
| **3. Context / Situation** | WHERE and WHEN they use it | Mobile/location/time-sensitive products | "Design for commuters" |
| **4. Lifecycle Stage** | How MATURE their relationship with the product is | Growth, retention, activation questions | "Grow YouTube's user base" |
| **5. Access / Constraint** | What LIMITATIONS shape their experience | Accessibility, emerging markets, underserved users | "Design for the blind / elderly / low-bandwidth" |
| **6. Value / Willingness to Pay** | How they RELATE to the business model | Pricing, monetization, freemium questions | "Price YouTube Premium" |

---

## Dimension 1: BEHAVIORAL (How they use it)

*Already covered extensively below in the category sections. This is your default.*

---

## Dimension 2: USE CASE / JOB (Why they hired it)

Same product, hired for fundamentally different purposes. Best for 0-to-1 design questions.

### Universal Use-Case Segments (apply to almost any product)

| Use Case | Description | Example across products |
|---|---|---|
| **Utility / Get it done** | Functional task, want efficiency | Maps: navigate. Slack: get answer. DoorDash: eat. |
| **Discovery / Explore** | Open-ended browsing, seeking novelty | YouTube: browse. Airbnb: dream about trips. Spotify: new music. |
| **Social / Connect** | Using product as a bridge to other people | Discord: hang out. Venmo: split bill. Peloton: compete with friends. |
| **Status / Signal** | Using product to project identity | Instagram: curated self. Airbnb: unique stay to post. Tesla: green identity. |
| **Escape / Decompress** | Using product to check out mentally | TikTok: scroll. Netflix: binge. Calm: meditate. |

### Product-Specific Use Cases

**Google Maps:**
- Navigate (A→B, turn-by-turn)
- Discover (find restaurants, gas, parking nearby)
- Research (check reviews, hours, photos before going)
- Share (send location to friends, ETA sharing)

**YouTube:**
- Learn (how-to, tutorials, lectures)
- Be entertained (music videos, comedy, drama)
- Stay informed (news, commentary, analysis)
- Shop/evaluate (product reviews, unboxings, comparisons)
- Background audio (music, podcasts, ASMR)

**Slack:**
- Coordinate (plan who does what, when)
- Decide (async discussion to reach a conclusion)
- Escalate (surface urgent issues)
- Socialize (water-cooler, random channels)
- Search/retrieve (find past decisions, links, files)

---

## Dimension 3: CONTEXT / SITUATION (Where and when they use it)

The SAME person behaves completely differently depending on context. This dimension is powerful
for mobile, location-based, or time-sensitive products.

### Temporal Context

| Context | Behavior shift | Products affected |
|---|---|---|
| **Morning routine** (6-9am) | Quick, habitual, low-decision. Check essentials. | News, email, weather, notifications, smart home |
| **Commute** (transport, 15-60 min) | Hands/eyes constrained. Audio-first. Kill time. | Spotify, podcasts, YouTube (audio), Kindle, news |
| **Work hours** (9-5) | Productivity mode. Low tolerance for distraction. | Slack, Notion, Zoom, Google Docs, Calendar |
| **Lunch/break** (12-1pm) | Reward/escape. Short entertainment burst. | Shorts, Reels, TikTok, DoorDash, social media |
| **Evening wind-down** (8-11pm) | Lean-back, longer sessions, TV screen. | Netflix, YouTube (CTV), Spotify, gaming |
| **Weekend** | Exploration, social, leisure, errands. | Airbnb, Maps, DoorDash, social media, shopping |
| **Late night** (11pm+) | Impulsive, lonely, bored, can't sleep. | TikTok, Reddit, food delivery, dating apps, Calm |

### Spatial Context

| Context | Behavior shift | Products affected |
|---|---|---|
| **At home — couch** | Big screen, lean-back, shared viewing | YouTube CTV, Netflix, gaming, smart home |
| **At home — desk** | Productive, multi-tab, keyboard-first | Notion, Slack, Google Docs, Zoom |
| **In transit** | One-handed, intermittent attention, cellular | Shorts, music, podcasts, Maps, messaging |
| **Walking outdoors** | Hands-free needed, glanceable, audio-primary | Maps navigation, AirPods, AR glasses, podcasts |
| **In store / retail** | Comparison shopping, looking up info about products | Google Search, Google Lens, Amazon price check |
| **At work (non-desk)** | Hands busy, need info overlay | AR glasses, voice assistants, wearables |
| **Foreign country** | Language barriers, unfamiliar navigation, roaming concerns | Translate, Maps offline, Airbnb, currency converter |

### Device Context

| Device | UX implications | Design constraint |
|---|---|---|
| **Phone** | One-handed, small screen, vertical, touch | Thumb-zone design, swipe gestures, short content |
| **Tablet** | Two-handed, medium screen, mixed orientation | Split-view, reading-optimized, richer content |
| **Desktop/laptop** | Keyboard + mouse, multi-window, long sessions | Power features, shortcuts, dense information |
| **TV/CTV** | Remote-controlled, shared screen, lean-back, 10-foot UI | Large text, simple navigation, voice search |
| **Wearable (watch)** | Glanceable, 2-second interactions, no keyboard | Notifications, quick actions, health data |
| **Smart speaker** | Voice-only, no screen, ambient | Audio-first, conversational UI, no visual feedback |
| **AR glasses** | Hands-free, overlaid on world, peripheral vision | Ambient info, minimal UI, voice + gesture input |

**When to use context dimension:** When the question involves a specific situation ("design for commuters"), a specific device ("design for smart TV"), or when you want to show that the same user needs completely different things in different moments.

---

## Dimension 4: LIFECYCLE STAGE (How mature their relationship is)

Best for growth, retention, and activation questions.

| Stage | Behavior | Metric to watch | What they need |
|---|---|---|---|
| **Unaware** | Don't know the product exists | Reach, impressions | Marketing, word-of-mouth, distribution |
| **Curious** | Aware, haven't tried | Landing page visits, app installs | Clear value prop, low-friction trial, social proof |
| **Activated** | Tried once, reached value moment | Activation rate (did core action in first session?) | Onboarding, time-to-value reduction, "aha moment" |
| **Casual** | Uses occasionally, no habit formed | D7/D14 retention, session frequency | Engagement loops, notifications, habit hooks |
| **Core** | Regular user, part of routine | D30 retention, DAU/MAU ratio | Feature depth, power-user tools, personalization |
| **Loyal / Champion** | Advocates, refers others, high LTV | NPS, referral rate, LTV | Loyalty rewards, referral programs, community |
| **At-risk** | Usage declining, approaching churn | Usage trend (declining sessions), re-engagement | Win-back campaigns, "we miss you", feature reminders |
| **Churned** | Left the product | Reactivation rate | "What's new" campaigns, reduced friction to return |

**The "aha moment" framework** (useful for activation questions):

| Product | "Aha moment" (when user gets hooked) |
|---|---|
| Facebook | Add 7 friends in 10 days |
| Slack | 2,000 messages sent (team-level, not individual) |
| Dropbox | Put one file in your Dropbox folder |
| Duolingo | Complete 3 lessons and get a streak going |
| Spotify | Create or save your first playlist |
| YouTube | Watch 3+ videos in first session |
| Airbnb | Complete first booking |

---

## Dimension 5: ACCESS / CONSTRAINT (What limitations shape their experience)

Critical for "design for [underserved population]" questions — these show up frequently in
Google interviews (10+ questions about elderly, blind, kids, low-bandwidth, etc.)

### Physical / Ability Constraints

| Constraint | Affected population | Design implications |
|---|---|---|
| **Visual impairment** | Blind, low-vision users | Screen readers, audio-first, haptic feedback, high-contrast, voice UI |
| **Motor impairment** | Limited hand/finger mobility | Large touch targets, voice control, switch access, reduced gestures |
| **Hearing impairment** | Deaf, hard-of-hearing | Captions, visual alerts, vibration, sign language support |
| **Cognitive load** | Elderly, children, low-literacy, non-native speakers | Simplified UI, fewer choices, visual guidance, larger text |
| **Age — children (<13)** | COPPA compliance, parental controls, safety | Content filtering, no data collection, parental dashboards, no DMs |
| **Age — elderly (65+)** | Lower tech literacy, accessibility needs, trust concerns | Simplified flows, larger UI, fewer steps, human support option |

### Infrastructure / Economic Constraints

| Constraint | Affected population | Design implications |
|---|---|---|
| **Low bandwidth** (2G/3G) | Emerging markets, rural areas | Lite versions, offline mode, compressed media, text-first |
| **Low-end devices** | $50-100 smartphones, limited RAM/storage | Lightweight app, minimal storage, efficient rendering |
| **Limited data plans** | Pay-per-MB users in developing markets | Data usage controls, Wi-Fi-only modes, download management |
| **Low digital literacy** | First-time smartphone users, elderly | Visual onboarding, guided flows, minimal text, demo mode |
| **No credit card** | Unbanked populations, teenagers | Alternative payment (carrier billing, gift cards, crypto, cash) |
| **Language** | Non-English speakers, right-to-left scripts | Localization, RTL support, multi-language UI, auto-detect |

### Regulatory / Privacy Constraints

| Constraint | Context | Design implications |
|---|---|---|
| **COPPA** (children <13) | US, strict data collection rules | Age gate, no behavioral targeting, parental consent |
| **GDPR** (EU users) | Data minimization, consent, right to deletion | Consent flows, data portability, deletion tools |
| **Accessibility law** (ADA/WCAG) | All users in US/EU | WCAG 2.1 AA compliance, screen reader support |
| **Content regulation** | Different by country (hate speech, political, adult) | Geo-specific content policies, moderation systems |

**When to use this dimension:** Any question that says "design for [specific population]" —
blind, elderly, kids, emerging markets, truck drivers, rural users. Also useful when you want
to show empathy by naming constraints most candidates would miss.

---

## Dimension 6: VALUE / WILLINGNESS TO PAY (How they relate to the business model)

Best for pricing, monetization, and freemium strategy questions.

### Universal Value Tiers

| Tier | Relationship to money | Behavior | Implication |
|---|---|---|---|
| **Free riders** | Will never pay. Tolerate ads. | High usage of free features, ignore upgrade prompts | Monetize through ads or make them the product (data) |
| **Convertible free** | Would pay IF the right trigger hits | Hit paywalls, use premium features in trials, compare plans | Trial offers, timed paywalls, feature-gating |
| **Price-sensitive subscribers** | Pay the minimum tier, churn-sensitive to price increases | Basic plan, watch for discounts, may downgrade | Annual discounts, family plans, loyalty rewards |
| **Value subscribers** | Pay willingly, see clear ROI | Mid-tier, use premium features regularly, low churn | Feature expansion, usage-based upsell |
| **Premium/power buyers** | Pay top tier, price-insensitive for this category | Highest tier, heavy usage, may want more | Premium features, early access, concierge support |

### Product-Specific Value Segments

**YouTube:**
- Ad-tolerant viewers (majority — won't pay, accept ads as cost of free)
- Ad-fatigued (annoyed by ads but won't pay — the persuasion target)
- Premium subscribers ($13.99/mo — ad-free, background play, downloads)
- YouTube TV subscribers ($72.99/mo — cord-cutters willing to pay for live TV)

**Spotify:**
- Free tier listeners (60%+ of users — deliberate degraded experience as conversion funnel)
- Individual Premium ($11.99/mo — ad-free, offline, quality)
- Family plan ($19.99/mo — highest LTV, lowest per-user cost, hardest to churn)
- Student ($5.99/mo — acquisition play, converts to full-price post-graduation)

**DoorDash:**
- One-time orderers (no subscription, pay full fees, low loyalty)
- DashPass subscribers ($9.99/mo — 2-3x order frequency, 50% lower churn)
- Corporate/expense account (price-insensitive, high AOV, business delivery)

**When to use this dimension:** "How would you price X?", "Design a subscription model",
"Free vs paid — what's behind the paywall?", "How would you increase revenue for X?"

---

## Combining Dimensions (L6 move)

The best answers often combine 2 dimensions to create a precise segment:

| Combined segment | Dimensions used | Example |
|---|---|---|
| "Mobile commuters who use YouTube for background audio" | Context (commute) + Behavioral (background) | Implies: audio mode, lock-screen play, low bandwidth |
| "Price-sensitive first-time Airbnb users in emerging markets" | Value (price-sensitive) + Lifecycle (new) + Access (emerging market) | Implies: localized pricing, simplified onboarding, mobile-first |
| "Power-user Slack admins in large enterprises" | Behavioral (power user) + Value (enterprise buyer) | Implies: admin tools, compliance, SSO, audit logs |
| "Elderly parents who use Google Maps for the first time when visiting their kids" | Access (elderly) + Context (unfamiliar city) + Lifecycle (new) | Implies: simplified UI, large text, voice-first navigation |

**The rule**: Combine dimensions only when it creates a MORE SPECIFIC segment that implies
a MORE SPECIFIC product decision. If the combination doesn't change what you'd build, one
dimension is enough.

---

## How to Use (Updated)

1. **Read the question** — what type is it? (improve / design / grow / price / design for X)
2. **Pick the right dimension** from the table at the top
3. **Grab 3-4 segments** from the relevant section
4. **Pick one** and justify with your stated goal
5. **Optionally combine** with a second dimension for precision (L6 move)
6. **Adapt the segment names** to the specific product

---

## 1. VIDEO / STREAMING / CONTENT (YouTube, Netflix, TikTok, Twitch)

### Consumer Segments (by viewing behavior)

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Lean-back relaxers** | Want entertainment without decisions. Autoplay, scroll, binge. | Long sessions, high autoplay, low search | Optimize recommendation + reduce decision fatigue |
| **Intentional seekers** | Come for a specific answer or content piece | Search-driven, short sessions, high completion | Optimize search, chapters, skip-to-answer |
| **Background ambienters** | Audio/video as companion while doing something else | Screen off, long duration, music/ASMR/podcasts | Audio mode, low-bandwidth, lock-screen play |
| **Social participators** | Watch what friends/culture is discussing | Trending content, shares, comments, Shorts/Reels | Social features, trending, share mechanics |
| **Appointment subscribers** | Loyal to specific creators, return for new uploads | Sub-driven, notification-click, watch within 24hrs | Notification tuning, creator tools, membership |
| **Snack-scrollers** | Kill 5-10 min between tasks with short content | Short sessions, high frequency, Shorts/Reels heavy | Short-form feed, fast loading, minimal friction |

**Use for**: YouTube, Netflix, TikTok, Twitch, Spotify (podcasts), Disney+

### Creator Segments (supply side — for marketplace questions)

| Segment | Behavior | What they need |
|---|---|---|
| **Hobbyist creators** | Create for fun, no monetization goal, <1K followers | Simple tools, encouragement, small audience growth |
| **Aspiring professionals** | Trying to make content their career, 1K-100K followers | Monetization access, growth analytics, discovery |
| **Mid-class professionals** | Content IS their job, 100K-1M followers, multi-platform | Revenue share, brand deals, audience retention tools |
| **Top-tier creators** | Celebrity-level, 1M+, platform-agnostic | Revenue maximization, exclusivity deals, management tools |
| **Media companies** | Repurposing TV/studio content for platform distribution | Bulk upload, analytics, monetization at scale |

**The strategic battleground** is always the **mid-class (100K-1M)**. Top creators are too expensive to retain exclusively. Small creators don't generate enough value. The mid-class has real switching costs and meaningful but not astronomical earnings.

---

## 2. FOOD DELIVERY / LOCAL COMMERCE (DoorDash, Uber Eats, Instacart)

### Consumer Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Convenience cravers** | Know what they want, optimize for speed | Repeat orders, same restaurants, low browse time | Reorder flow, saved favorites, fast checkout |
| **Discovery explorers** | Browsing for something new, open-minded | High browse time, new restaurants, filter usage | Better discovery, reviews, cuisine filters, "surprise me" |
| **Bulk/family planners** | Ordering for household, higher AOV, weekly patterns | Large orders, family plans, scheduled deliveries | Group ordering, family accounts, meal bundles |
| **Deal hunters** | Price-sensitive, promo-driven, will switch platforms for $2 off | High promo usage, low loyalty, cross-platform | DashPass/subscription lock-in, loyalty rewards |
| **Late-night/impulse** | Ordering outside normal meal times, convenience-driven | Late hours, snacks/drinks, small orders, high frequency | Convenience store integration, fast delivery promise |

### Merchant Segments (supply side)

| Segment | Behavior | What they need |
|---|---|---|
| **Local independents** | Single location, low tech sophistication, delivery is new | Onboarding help, simple dashboard, marketing tools |
| **Chain restaurants** | Multi-location, established delivery ops, negotiate commissions | Bulk analytics, API integration, volume discounts |
| **Ghost/cloud kitchens** | Delivery-only, optimize for throughput, no storefront | Menu optimization, kitchen analytics, multi-platform |
| **Grocery/convenience** | Different operations (pick/pack vs cook), higher AOV | Inventory management, substitution rules, batch picking |

### Driver Segments (supply side)

| Segment | Behavior | What they need |
|---|---|---|
| **Full-time Dashers** | 30+ hrs/week, this is their primary income | Scheduling tools, earnings optimization, benefits |
| **Part-time supplementers** | 5-15 hrs/week, evenings/weekends for extra cash | Flexible scheduling, quick cash-out |
| **Multi-app jugglers** | Run Uber Eats + DoorDash + Instacart simultaneously | Best order-to-time ratio, instant accept/decline |

---

## 3. RIDE-SHARING / MOBILITY (Uber, Lyft, Waymo)

### Rider Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Daily commuters** | Predictable routes, weekday mornings/evenings | Repeat trips, scheduled rides, subscription interest | Ride pass/subscription, scheduled rides, route optimization |
| **Night-out riders** | Late night, social occasions, surge-tolerant | Weekend late-night, destination bars/restaurants | Safety features, group rides, surge communication |
| **Airport travelers** | Infrequent but high-value, price-comparing with taxis | Airport pickups/dropoffs, luggage needs | Premium vehicles, flight tracking, reliable pickup |
| **Errand runners** | Short trips during day, errands/appointments | Short distances, mid-day, medical/retail destinations | Low-cost options, wait-and-return, package delivery |
| **Car-free urbanites** | Ride-sharing replaces car ownership entirely | High frequency across all times, diverse destinations | Loyalty/subscription, multi-modal (bikes, scooters) |

---

## 4. SOCIAL MEDIA / MESSAGING (Instagram, Snapchat, Discord, WhatsApp, Twitter/X)

### Consumer Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Passive scrollers** | Consume but rarely post or engage | High session time, low creation, no comments | Feed algorithm optimization, content quality |
| **Social connectors** | Use platform to maintain relationships | DMs, group chats, stories, tagging friends | Messaging, groups, sharing features |
| **Content creators** | Create and publish content for an audience | Regular posting, analytics checking, follower growth | Creator tools, monetization, analytics |
| **Community builders** | Organize groups around shared interests | Group admins, event creation, moderation | Community tools, moderation, discovery |
| **News/culture consumers** | Come for information and cultural discourse | Following news accounts, trending topics, search | Trending, search, curation, fact-checking |
| **Performative sharers** | Post to project identity/status, selective sharing | Curated posts, Stories over Feed, aesthetic focus | Editing tools, ephemeral content, filters |

---

## 5. MUSIC / AUDIO (Spotify, YouTube Music, Apple Music, Podcasts)

### Listener Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Mood matchers** | Music fits the moment — workout, focus, chill | Playlist by activity/mood, AI DJ, Daylist usage | Mood detection, activity-based playlists, AI DJ |
| **Catalog explorers** | Actively discover new artists and genres | Discover Weekly, Release Radar, genre browsing | Discovery algorithm, new release surfacing |
| **Comfort replayers** | Listen to same songs/playlists repeatedly | Low new-artist rate, high repeat plays, saved library | Library management, offline download, nostalgia playlists |
| **Podcast converts** | Primarily use the platform for spoken word | Long sessions, podcast follows, low music usage | Podcast discovery, episode management, sleep timer |
| **Background players** | Music as ambient noise while working/studying | Very long sessions, lo-fi/ambient, screen off | Background play, low-bandwidth, silence detection |

---

## 6. E-COMMERCE / MARKETPLACE (Amazon, Shopify, Airbnb, eBay)

### Buyer Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Need-driven purchasers** | Know what they want, optimize for speed + price | Search-driven, low browse, high add-to-cart rate | Fast checkout, price comparison, delivery speed |
| **Discovery shoppers** | Browsing for inspiration, open to suggestions | High browse time, wishlist usage, category exploration | Recommendations, curated collections, visual shopping |
| **Deal chasers** | Wait for sales, compare across platforms | Wishlist + price alerts, Prime Day/sale event engagement | Price tracking, deal notifications, flash sales |
| **Repeat replenishers** | Buy same items regularly (household, groceries) | Subscribe & Save, repeat orders, predictable timing | Auto-reorder, subscription, pantry management |
| **Research-heavy buyers** | Extensive comparison before purchasing (electronics, appliances) | Long time-to-purchase, review reading, spec comparison | Reviews, comparison tools, Q&A, detailed specs |

### Airbnb-Specific Guest Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Budget explorers** | Cheapest unique stay, hostel-alternative seekers | Sort by price, shared rooms, long stays | Price filters, long-stay discounts, basic amenities |
| **Convenience seekers** | Hotel-like reliability, business travel | Superhosts, instant book, high-rated, amenity filters | Quality guarantees, business-travel features, clean standards |
| **Experience hunters** | Unique/memorable stays (treehouse, castle, boat) | Category browsing, Wishlists, OMG/unique filters | Curated categories, visual discovery, experience packaging |
| **Group coordinators** | Planning for families, weddings, friend groups | Large-group filters, shared Wishlists, group messaging | Group booking, split payments, shared wishlists |

---

## 7. PRODUCTIVITY / TOOLS (Slack, Notion, Zoom, Figma, Dropbox, Google Workspace)

### User Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Power organizers** | Build complex systems, heavy customization | Many databases/channels, templates, integrations | Advanced features, API, automation, custom workflows |
| **Casual collaborators** | Use the tool because team uses it, minimal personal investment | Low creation, high consumption, follow others' structures | Simple onboarding, templates, reduced complexity |
| **Solo builders** | Individual use, personal projects, not team-driven | Single-player mode, personal workspace, no sharing | Free tier value, personal templates, mobile access |
| **Admin/IT buyers** | Choose and manage the tool for the organization | Admin console, compliance, SSO, billing | Enterprise features, security, deployment tools |
| **Meeting-averse async workers** | Prefer written/async communication over live meetings | Long messages, document comments, recorded videos | Async features, threaded discussions, recording + summary |

---

## 8. FINTECH / PAYMENTS (PayPal, Venmo, Robinhood, Cash App, Stripe)

### Consumer Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Peer-to-peer splitters** | Split bills, pay friends, casual transactions | Small amounts, high frequency, social feed | Easy splitting, social features, request money |
| **Bill payers** | Use for recurring payments, utilities, subscriptions | Scheduled payments, auto-pay, merchant transactions | Autopay, reminders, merchant directory |
| **Micro-investors** | Investing small amounts, learning, experimenting | Small trades, fractional shares, educational content | Low minimums, education, simple UX |
| **Active traders** | High-frequency trading, options, crypto | Many transactions/day, advanced charts, alerts | Advanced tools, real-time data, low fees |
| **Unbanked/underbanked** | Primary financial tool, limited traditional banking | Direct deposit, debit card, ATM usage | Banking features, early deposit, low/no fees |

---

## 9. HEALTH / FITNESS / WELLNESS (Peloton, Calm, Headspace, Fitbit, Apple Health)

### User Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Routine builders** | Trying to establish consistent habits | Streak-focused, calendar views, reminders | Streak mechanics, scheduling, gentle nudges |
| **Goal chasers** | Training for something specific (race, weight, strength) | Program enrollment, progress tracking, metrics | Structured programs, progress visualization, milestones |
| **Social exercisers** | Motivation comes from community/competition | Leaderboards, group classes, challenges, shares | Social features, challenges, group accountability |
| **Recovery/maintenance** | Managing chronic condition, stress, sleep, mental health | Meditation, sleep content, gentle movement | Low-intensity options, medical content, privacy |
| **Novelty seekers** | Try new workouts, get bored easily, variety-driven | Low repeat rate, diverse class types, short retention | Content variety, new releases, cross-training suggestions |

---

## 10. EDUCATION / LEARNING (Duolingo, LinkedIn Learning, Coursera, YouTube edu)

### Learner Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Habit learners** | Daily streaks, short sessions, gamification-driven | High streak counts, predictable time-of-day, streak repairs | Gamification, streaks, daily goals, notifications |
| **Sprint learners** | Intensive bursts before an event (exam, interview, trip) | Sudden high activity, specific topic focus, time-limited | Intensive courses, deadline-driven pacing, assessment |
| **Credential seekers** | Learning for career advancement, certificates matter | Certificate courses, completion focus, LinkedIn sharing | Certificates, employer partnerships, skill badges |
| **Curious browsers** | Learning as entertainment, no specific goal | Wide topic variety, low completion, high starts | Short-form content, topic sampling, recommendation |
| **Forced learners** | Assigned by employer/school, compliance-driven | Uniform enrollment, low engagement, minimum-viable completion | Progress tracking for admins, compliance certificates |

---

## 11. TRAVEL / HOSPITALITY (Airbnb, Google Maps, Airline apps, Booking.com)

### Traveler Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Planners** | Research extensively, book in advance, detailed itineraries | Long lead time, wishlists, comparison shopping | Trip planning tools, price alerts, itinerary builder |
| **Spontaneous travelers** | Book last-minute, flexible, go-with-the-flow | Short lead time, mobile booking, "tonight" searches | Last-minute deals, instant book, location-based |
| **Business travelers** | Predictable patterns, expense compliance, efficiency | Weekday stays, corporate cards, loyalty programs | Receipt/expense tools, corporate booking, loyalty |
| **Family orchestrators** | Complex logistics, child-friendly requirements, group coordination | Family filters, reviews mentioning kids, large-group | Family features, child safety, group coordination |

---

## 12. SMART HOME / HARDWARE (Alexa, Google Home, Nest, Ring, Pixel)

### User Segments

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **Automation enthusiasts** | Build routines, connect devices, optimize home | Many connected devices, complex routines, IFTTT-style | Advanced automation, device ecosystem, API access |
| **Convenience seekers** | Voice commands for basic tasks (timer, weather, music) | Simple commands, few devices, limited exploration | Simplicity, reliability, voice-first UX |
| **Security-focused** | Cameras, locks, alerts, monitoring | Ring/Nest cameras, alert frequency, remote monitoring | Security features, reliable alerts, privacy controls |
| **Entertainment hub users** | Smart display/speaker as media device | Music, video, smart TV control, casting | Media integration, display quality, multi-room audio |

---

## 13. ADVERTISING PRODUCTS (Google Ads, Meta Ads, YouTube Ads, TikTok Ads)

### Advertiser Segments (YOU NEED THIS FOR YOUR YOUTUBE ADS ROLE)

| Segment | Behavior | Signal | Implication |
|---|---|---|---|
| **SMB self-serve** | Small business, low budget (<$5K/mo), no agency | Self-serve tools, automated campaigns, simple UI | Easy setup, PMax/Advantage+, AI creative generation |
| **Mid-market performance** | Medium business, $5K-100K/mo, agency or in-house team | ROAS-focused, conversion tracking, A/B testing | Performance tools, attribution, measurement |
| **Enterprise brand** | Large brand, $100K+/mo, multiple agencies, multi-channel | Brand lift, reach/frequency, premium inventory | YouTube Select, Brand Lift studies, cross-screen measurement |
| **Performance advertisers** | Any size, focused on direct response (clicks, installs, purchases) | CPA/ROAS optimization, conversion API, retargeting | Shopping ads, conversion optimization, attribution |
| **Brand awareness advertisers** | Any size, focused on top-of-funnel (awareness, consideration) | Reach metrics, video completion, Brand Lift | Non-skippable video, bumper ads, masthead, YouTube Select |

**For YouTube Shorts specifically:**

| Segment | Why they matter for Shorts |
|---|---|
| **Performance advertisers** | The demand-side unlock — bringing CPA/ROAS objectives to Shorts inventory raises CPMs without increasing ad load. Currently under-represented on Shorts. |
| **SMB self-serve** | Shorts' native creative (vertical, short, authentic) is easier for SMBs to produce than polished TV ads. Lower creative barrier = more demand. |
| **Social commerce advertisers** | TikTok Shop-native advertisers who would bring shoppable creative to YouTube Shorts if the format existed. The whitespace. |

---

## Cross-Category Patterns — Universal Segments

These segments appear in EVERY product category. When you're stuck, start here:

| Universal segment | Description | Applies to |
|---|---|---|
| **Power users** | Top 10% who drive 50%+ of usage/revenue | Everything — always mention in bias section |
| **Casual/occasional** | Use 1-2x/week, low engagement, high churn risk | Everything — the "silent majority" most metrics miss |
| **New/onboarding** | First 7-30 days, still deciding if product is for them | Everything — activation rate is the critical metric |
| **Churned/lapsed** | Used to be active, stopped | Everything — reactivation is cheaper than new acquisition |
| **Free riders** | Get value without paying (free tier, ad-tolerant) | Freemium products — conversion to paid is the question |

---

## Quick Lookup: Question → Category → Segments

| If the question mentions... | Use category | Go-to segments |
|---|---|---|
| YouTube, Netflix, TikTok, streaming, video | Video/Streaming (#1) | Lean-back / Intentional / Snack-scroller |
| DoorDash, Uber Eats, food delivery, grocery | Food Delivery (#2) | Convenience craver / Explorer / Deal hunter |
| Uber, Lyft, ride-sharing, transportation | Mobility (#3) | Commuter / Night-out / Airport |
| Instagram, Snapchat, Twitter, social media | Social (#4) | Passive scroller / Connector / Creator |
| Spotify, music, podcasts, audio | Music/Audio (#5) | Mood matcher / Explorer / Background player |
| Amazon, Airbnb, marketplace, shopping | E-Commerce (#6) | Need-driven / Discovery / Deal chaser |
| Slack, Notion, Zoom, productivity, workspace | Productivity (#7) | Power organizer / Casual collaborator / Admin |
| PayPal, Venmo, payments, investing | Fintech (#8) | P2P splitter / Micro-investor / Unbanked |
| Peloton, fitness, health, meditation | Health/Fitness (#9) | Routine builder / Goal chaser / Social exerciser |
| Duolingo, learning, education, courses | Education (#10) | Habit learner / Sprint learner / Credential seeker |
| Travel, hotel, flights, Maps | Travel (#11) | Planner / Spontaneous / Business |
| Alexa, smart home, IoT, hardware | Smart Home (#12) | Automation enthusiast / Convenience seeker |
| Ads, advertisers, monetization | Advertising (#13) | SMB self-serve / Performance / Brand awareness |
| "Favorite product" (open-ended) | Pick your product, use its category | Have 3 products ready with segments memorized |

---

## The YouTube Shorts Ads Role — Segments You MUST Know Cold

From your HM prep (`youtube-shorts-ads-hm-prep.md`):

**Three-sided marketplace segments:**

**Viewers** (demand side):
- Snack-scrollers (kill 5 min, low intent, high volume) — the dominant Shorts user
- Intentional discoverers (searching for specific content in Shorts format)
- Cross-format viewers (watch Shorts as discovery → subscribe → watch long-form)

**Creators** (supply side):
- Shorts-native creators (vertical-first, TikTok-crossposters, often small/mid)
- Long-form creators adding Shorts (using Shorts as promotion for their main content)
- Professional creators (media companies, brands posting vertical content)

**Advertisers** (monetization side):
- Performance advertisers (CPA/ROAS — the demand-side unlock)
- Brand awareness advertisers (reach/frequency — already present, lower CPMs)
- Commerce/shopping advertisers (the TikTok Shop gap — the whitespace opportunity)

**The thesis from your HM prep**: *"Biggest unlock is bringing performance demand + native commerce to Shorts; gating constraint is UX trust, so sequence efficiency/format-fit + auction tuning first, then layer commerce."*
