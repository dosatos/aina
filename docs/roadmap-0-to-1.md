# Plan: 0-to-1 Roadmap for Self-Evaluation Platform

## Context

This is a greenfield project to build a self-evaluation and insight platform. Three strategic documents exist defining the vision, data collection approach, and marketing strategy. The goal is to create a pragmatic, actionable roadmap from zero to first 1,000 real users.

**The Challenge:** The vision is ambitious (7 assessment layers, AI coach, MCP server, Growth OS). The task is to find the **minimum viable path** to validate the core hypothesis before building the full vision.

**Core Hypothesis:** People will complete a 20-minute multi-layer assessment AND invite peers for feedback if the results are insightful and shareable enough.

**No code exists yet** — only strategic documentation. The repository is currently empty except for docs.

---

## Phase 0: Pre-Build Validation (Week 1-2)

**WHY:** Before writing code, validate that people care. The biggest risk is product-market fit, not technical execution.

### Manual MVP (No-Code Test)

**Build:**
- Google Form with 30 questions:
  - 15 questions: Layer 1 (Behavioral Dynamics) using IPIP public domain items
  - 10 questions: Layer 3 (Risk scenarios)
  - 5 questions: Demographics
- Manually score 20-30 pilot users
- Generate personalized reports using Claude/GPT-4 (copy-paste answers, prompt engineer responses)

**Measure:**
- Do they read the full report?
- Do they share it?
- Do they want more layers?

### Results Page Mock

**Create:**
- Design 3-5 versions of results experience in Figma (or Canva)
- Test which visual format makes people say "I need to share this"
- Key question: Does it pass the "screenshot test" — would you share it on LinkedIn?

### Peer Survey Test

**Test:**
- Manually send 5 people a Google Form peer survey (10 questions about someone)
- Show aggregate results: "Your peers see you as X, you see yourself as Y"
- Measure: Do respondents get curious about their own profile?

### Target Audience Interviews

**Interview 10-15 people** (25-40 age range, career-oriented, founders/engineers)

**IMPORTANT:** Avoid hypothetical "would you" questions - they produce unreliable signals. Focus on past behavior, reaction testing, and real commitment tests.

**Interview Structure:**

**1. Past Behavior (Most Reliable Signal)**
- "Tell me about the last time you tried to understand yourself better professionally"
- "What personality tests or career assessments have you taken? Which did you complete? Which did you abandon halfway?"
- "What have you paid for in this space? What was worth it? What wasn't?"
- "Have you ever shared a personality test result with friends or colleagues? Which one? Why did you share it?"

**2. Current Pain Points (Validates Problem)**
- "What decisions are you struggling with right now in your career or work?"
- "When was the last time you got feedback that surprised you? What was it?"
- "How do you currently figure out if you're in the right role/career?"
- "Tell me about a time when you made a decision you later regretted - what would have helped?"

**3. Show, Don't Tell (Reaction Testing)**
- Show 3 mock results pages: "Would you screenshot and post this on LinkedIn? Why or why not? What would need to change for you to share it?"
- Show peer survey format: "Would you fill this out for a friend? Would you feel comfortable sending this to 4 peers? Why or why not?"
- Walk through the flow concept: "Where would you drop off? What would make you keep going?"
- Point to specific insights: "Does this feel accurate? Generic? Surprising?"

**4. Commitment Tests (Strongest Signal)**
- "Can I send you the Google Form prototype right now? Would you complete it in the next 24 hours?"
- "If I generate your results, would you be willing to hop on a 15-min call to give me feedback?"
- "Would you introduce me to 2 other people who fit this profile?"
- "Can I add you to the beta test list and ping you when it's ready?"
- **Only if very positive:** "If this launched today with lifetime access for $49, would you pre-pay right now?"

**5. Comparative Value (Pricing Context - NOT Hypothetical)**
- "What's the most expensive professional development tool or assessment you've purchased? What made it worth it?"
- "How much did you pay for [16Personalities Pro / CliftonStrengths / coaching / therapy]?"
- "If this saved you from making one bad career decision, what would that be worth to you?"
- "How does this compare to things you already spend money on for growth?"

**6. Open-Ended Discovery**
- "What would make you share the results with your network?"
- "What would make this 10x better than 16Personalities or StrengthsFinder?"
- "What's missing from this concept? What would you add?"
- "What would make you come back in 6 months to retake this?"

**During the Interview:**
- Send them the Google Form link right there - do they complete it immediately or say "I'll do it later"?
- Note their body language when you show mock results - do their eyes light up?
- Listen for unprompted statements like "when can I use this?" or "can you send this to me?"
- Track whether they volunteer to help without you asking

### Success Criteria to Proceed

**Strong Signals (What They DO):**
- ✅ 70%+ completion rate on Google Form (they actually complete it within 24 hours when you send it)
- ✅ 60%+ actually share their manually-generated results (screenshot it, post it, or send to friends)
- ✅ 30%+ complete the form immediately during or right after the interview (not "I'll do it later")
- ✅ 3+ people pre-commit to beta testing or introduce you to others without being asked

**Moderate Signals (What They SAY, backed by past behavior):**
- ✅ 50%+ can name 4 specific people they'd send this to (not vague "yeah, I'd share it")
- ✅ Clear "I feel seen" reactions when reviewing results (emotional response, not polite approval)
- ✅ 80%+ have paid for similar tools before (proves market exists and they spend money here)
- ✅ Strong comparative value: "This is better than [X tool I paid for]"

**Red Flags (Pivot Signals):**
- ❌ <60% completion rate = assessment is too long or not engaging enough
- ❌ <40% actually share results = results aren't shareable/insightful enough
- ❌ Lots of "I would" but no "I will" or "can you send me" = polite rejection
- ❌ "This is interesting" but no clear pain point it solves = nice-to-have, not must-have

**If strong signals don't hit, pivot the concept before building. If moderate signals are weak, iterate on messaging and results format.**

---

## Phase 1: MVP Launch (Week 3-10)

**GOAL:** Build minimum functional product that delivers: multi-layer assessment → insightful results → peer survey loop → growth.

### Core Features (Ruthlessly Prioritized)

#### 1. Assessment Engine (Week 3-5)

**Build:**
- Simple web app: single-page assessment flow
- 3 sections:
  - Section 1 (Layer 1): 20 questions - Behavioral Dynamics (IPIP-based)
  - Section 2 (Layer 3): 15 scenario questions - Risk & Decision Architecture
  - Section 3: Transition prompt - "Want your blindspot analysis? Invite 3 peers"
- Progress bar, save-and-resume
- Target completion time: 12-15 minutes
- Basic response pattern detection (straight-lining, speed anomalies)

**DON'T build:**
- AI Coach (Phase 3)
- All 7 layers (just 2 initially, plus peer survey)
- Complex gamification
- Mobile apps (responsive web only)
- User dashboards (email-based for MVP)

#### 2. Results Experience (Week 5-6)

**Build (THE MOST IMPORTANT FEATURE):**
- Beautiful, shareable results page with:
  - Personal archetype label (e.g., "The Strategic Maverick")
  - 2-3 paragraph narrative summary synthesizing Layers 1 + 3
  - Visual profile card (Spotify Wrapped aesthetic)
  - 3-5 key insights (specific, not generic)
  - One cross-layer synthesis (e.g., "High risk tolerance + avoidant conflict = selective courage")
- Shareable elements:
  - Download profile card as PNG
  - "Share on LinkedIn" button (pre-populated text)
  - "Generate How to Work With Me doc" (simple PDF export)
- Tease Layer 7: "Want to see how others see you? Invite peers"

**DON'T build:**
- Interactive dashboards
- Real-time updates
- Retake/comparison views (Phase 2)
- Deep-dive analytics

#### 3. Peer Survey System (Week 6-7)

**Build:**
- Invitation flow: user enters 3-5 email addresses
- Automated email with unique link
- Short survey (10 forced-choice questions mirroring user's assessment)
- Anonymous aggregation: calculate self vs. peer gaps
- Layer 7 results: "Your peers rate you X, you rate yourself Y"
- At survey end: "Curious about your own profile? Take the assessment" (conversion moment)

**DON'T build:**
- Individual peer responses (aggregate only)
- Peer management dashboard
- Reminder emails (one email only)
- Social graph mapping

#### 4. Backend & Data (Week 3-7, parallel)

**Build:**
- User data model: responses, scores, normalized results
- Assessment scoring engine (weighted algorithms per layer)
- LLM integration for narrative generation (Claude/GPT-4 API)
- Email service (peer invites, results delivery)
- Basic analytics: completion rate, time-to-complete, share rate, peer conversion

**DON'T build:**
- Complex user accounts (use email magic links)
- Payment processing (Phase 2)
- Admin dashboard (use database queries)
- External API integrations

### Tech Stack (Simplest Path)

```
Frontend: Next.js + Tailwind CSS + Shadcn UI
- Fast development, great SEO, easy deployment (Vercel)
- Responsive by default
- Built-in API routes

Backend: Next.js API routes + Supabase (PostgreSQL)
- No separate backend needed
- Supabase: database, auth, real-time (future)
- Alternative: Firebase if you prefer NoSQL

LLM: OpenAI API or Anthropic Claude API
- Generate personalized narrative reports
- Fallback: template-based if cost too high

Email: Resend or SendGrid
- Transactional emails for peer surveys

Hosting: Vercel (frontend) + Supabase Cloud (database)
- Both have generous free tiers
- Total cost: $0-50/month for first 1,000 users

Analytics: PostHog or Plausible
- Track completion rate, drop-off, share rate, peer conversion

Design: Tailwind + Shadcn UI
- Beautiful accessible components
- Fast to customize
```

**DO NOT:**
- Build microservices
- Use Redux (React Context is fine)
- Build native mobile apps
- Over-engineer database schema

### Launch Strategy (Week 8-10)

#### Pre-Launch Waitlist (Week 8)

**Build:**
- Landing page with micro-assessment (5-question risk quiz, 60 seconds)
- Teaser result: "You're top 15% for career risk tolerance"
- CTA: "Join 1,000 Founding Profiles - lifetime free premium"
- Collect emails

**Channels:**
- Post on LinkedIn (personal profile)
- Relevant Slack/Discord communities (indie hackers, founder groups)
- Direct outreach to 50-100 network contacts
- Product Hunt "upcoming" page

**Target: 200-500 waitlist signups**

#### Launch Event (Week 9-10)

**"1,000 Founding Profiles" Campaign:**
- Public goal: need 1,000 users to calibrate AI and build norm data
- Founding users get: lifetime free premium + badge + early access to new layers
- Makes users feel like participants, not customers

**Launch channels (simultaneous):**
1. Product Hunt (aim for top 5 of day)
2. LinkedIn post (personal story, vulnerability)
3. HackerNews "Show HN" post
4. Waitlist email
5. Relevant subreddits (r/startups, r/careerguidance)

**First 48 hours critical:**
- Respond to every comment
- Fix bugs in real-time
- Share early testimonials
- Post progress updates

### Success Metrics (First 1,000 Users)

| Metric | Target | Why It Matters |
|--------|--------|----------------|
| **Assessment completion rate** | 70%+ | Core product validation |
| **Time to complete** | 12-15 min | Attention holding |
| **Peer survey send rate** | 40%+ | Viral loop activation |
| **Peer survey conversion** | 20%+ | Growth engine efficiency |
| **Results share rate** | 30%+ | Organic reach |
| **NPS / qualitative** | 8+ | Product-market fit signal |

**Red flags:**
- <60% completion = too long or boring
- <20% peer send = trust issue or friction
- <10% peer conversion = survey not creating curiosity
- <10% share rate = results not insightful enough

---

## Phase 2: Iterate & Monetize (Week 11-20)

### Iterate Based on Phase 1 Data

**If peer loop working (>25% conversion):**
- Add peer survey reminder email
- Show "X of 4 peers have responded" progress
- Add peer survey prompt to onboarding

**If results not shared (<15% rate):**
- Redesign results page (test 3 variants)
- Add more "aha" moments
- Improve visual design of cards

**If completion rate low (<65%):**
- Shorten assessment (cut to 25 questions)
- Add mid-assessment results tease
- Improve question specificity

### Add Layer 7 Results (If Peer Loop Works)

- Full blindspot analysis page
- Gap visualization: self vs. peers
- Specific insights: "You underestimate X, overestimate Y"

### Monetization (Start Simple)

**Freemium model:**
- Free: Layers 1 + 3, basic results, peer survey
- Premium ($49 one-time or $12/month):
  - Layer 7 detailed analysis
  - "How to Work With Me" PDF generator
  - Downloadable full report
  - Future: Layer 4 & 6 access

**Test pricing with surveys first, then build payment (Stripe).**

### Growth Features

- Referral system: "Invite 3 friends, unlock Premium free"
- Social proof: "Join 4,247 professionals..."
- Data insights content: "We analyzed 5,000 profiles..."

---

## Phase 3: Expand & Scale (Month 6+)

**Only pursue after achieving:**
- 5,000+ completed profiles
- 25%+ peer conversion (viral loop working)
- $10K+ MRR or clear path to it

### Additional Layers

- Layer 4: Execution & Consistency
- Layer 6: Career Alignment
- Layers 2 & 5 (based on demand)

### AI Coach

- Chat interface grounded in profile
- Scenario-based advice
- Weekly nudges

### Profile MCP Server

- Expose profile as structured context to AI tools
- Creates lock-in
- Requires 5+ layers to be valuable

### B2B Features

- Team dashboard: compatibility analysis
- Hiring: candidate assessments
- White-label for coaches

---

## Marketing & Distribution Strategy

### First 100 Users (Week 1-4)

**Do things that don't scale:**
- Personal outreach to entire network
- Post in 20+ relevant communities (be helpful, not spammy)
- DM 100 people on LinkedIn who fit profile
- Ask for intros

**Content (manual):**
- 1 LinkedIn post about building in public
- Early user testimonials
- Insight teasers from manual scoring

### First 1,000 Users (Month 2-4)

**Priority channels:**

1. **Product Hunt** (Day 1, highest impact)
   - Aim for top 5 of day
   - Prepare thumbnail, video, announcement

2. **LinkedIn** (Primary ongoing)
   - Founder personal posts (2-3x/week)
   - User stories
   - Data insights
   - Poll content driving to assessment

3. **HackerNews** (One shot)
   - "Show HN: Platform showing decision-making blind spots"
   - Respond to technical questions

4. **Reddit** (Careful)
   - r/startups, r/careerguidance, r/productivity
   - Provide value first, mention tool second

5. **Direct outreach**
   - Email 200 people from Phase 0
   - Ask early users for intros

**Content that works:**
- User testimonials (quotes + faces)
- Data insights: "73% of founders overestimate risk tolerance"
- Before/after blindspot stories
- Scenario polls: "Would you leave $150K for 40% equity?"

**What NOT to do (Month 1-4):**
- Paid ads (too early, expensive)
- SEO content (too slow, 2-3 pieces max)
- Podcasts (unless inbound)
- PR (unless you have connections)
- Conferences (too much time)

### Growth Loop Priority

**#1: Peer survey viral loop**
- Every user invites 4 → 25% convert = 1.0 viral coefficient
- Optimize ruthlessly:
  - Survey takes 2 minutes max
  - Show respondents micro-insight about themselves
  - Smooth "take your own" CTA

**#2: Social sharing**
- Make results so good people screenshot and share
- Pre-populate LinkedIn text
- Multiple card variants
- Track which insights shared most

**#3: Word of mouth**
- Ask satisfied users for intros
- "Invite 3 friends, get premium" incentive

---

## Customer Development Plan

### What to Test & When

**Pre-Launch (Week 1-2) - Focus on BEHAVIOR, not hypotheticals:**
- **Do** people complete the 15-min Google Form assessment? (Not "would you" - send it and measure)
- **Do** results create "I feel seen" reactions? (Watch for emotional responses, not polite "interesting")
- **Do** people actually share results? (Not "would you share" - give them results and track if they post/send)
- **Do** people complete the peer survey when sent to them? (Actual behavior)
- What specific words do people use to describe the results? (Collect verbatims)
- Can they name 4 specific people they'd send this to? (Vague = weak signal)

**Launch (Week 3-10) - Measure actual behavior:**
- What's the completion rate? (Target: 70%+)
- Where do people drop off? (Which question? Which minute?)
- Which results insights get quoted/shared most? (Track screenshots, social posts)
- What's the peer survey conversion rate? (% who take their own assessment after rating someone)
- Do people come back to see if peers have responded? (Engagement signal)
- What do people say unprompted in feedback? ("I wish..." vs. "This is cool")

**Post-Launch (Month 3+) - Test monetization:**
- **Do** people pay when prompted? (Not "would you pay" - test actual conversion)
- What's the conversion rate at $49 vs $12/month vs $99? (A/B test)
- Do people retake at 6 months? (Growth tracking validation)
- What use cases emerge organically? (Listen for unexpected value)
- What features get requested by 10+ people? (Prioritize by frequency, not interesting ideas)

### Interview Schedule

**Month 1: 20 interviews - Focus on completion and sharing behavior**
- 10 who completed the full assessment → What kept them going? What almost made them quit? Would they actually share results?
- 5 who dropped off → At what point? Why? What would have kept them going?
- 5 peer survey respondents → Did they get curious about their own profile? What would make them take the full assessment?

**Month 2: 15 interviews - Focus on actual sharing behavior**
- 10 who actually shared results → Where? Why? What specific insight made them share? What reaction did they get?
- 5 who didn't share → Why not? What would need to change? Was it the insights, the design, or trust/privacy concerns?

**Month 3: 10 interviews - Focus on willingness to pay (test with real offers)**
- Don't ask "would you pay $X?" → Instead: "We're launching premium for $49 - interested?"
- Track who says yes vs. who hesitates vs. who deflects
- Ask: "What have you paid for similar tools?" (establishes spending behavior)
- Feature prioritization: "If we could only build one thing next, what would make you upgrade?"

### Key Questions to Answer

1. Does cross-layer synthesis insight land? (Core differentiator)
2. Is peer survey creating curiosity in respondents? (Growth engine)
3. Are results shareable in practice?
4. What's minimum layer count that feels complete?
5. Do people want ongoing tracking or one-time insight?

---

## Timeline & Sequencing

### Week-by-Week

**Week 1-2: Validation**
- Manual MVP (Google Forms)
- Results page mock (Figma)
- 10-15 interviews
- Decision: Build or pivot?

**Week 3-4: Foundation**
- Set up tech stack (Next.js + Supabase + Vercel)
- Build assessment engine (Layer 1: 20 questions)
- Design results page
- Set up analytics

**Week 5-6: Core Experience**
- Add Layer 3 (15 risk scenarios)
- Build results generation (LLM integration)
- Design shareable cards
- Build peer invitation flow

**Week 7-8: Polish & Test**
- Peer survey system
- Layer 7 gap analysis (basic)
- Private beta (20-30 users)
- Fix bugs, iterate on results

**Week 9: Pre-Launch**
- Landing page with micro-assessment
- Start "1,000 Founding Profiles" campaign
- Build waitlist (200-500 emails)
- Prepare launch materials

**Week 10: Launch**
- Product Hunt
- LinkedIn, HackerNews, Reddit
- Email waitlist
- Monitor and fix issues real-time

**Week 11-14: Iterate**
- Analyze completion, drop-off
- Optimize peer conversion
- Improve results based on feedback
- Scale content

**Week 15-20: Monetize**
- Add premium tier ($49 or $12/month)
- Test pricing
- Build payment (Stripe)
- Add premium features

---

## Resource Requirements

### Team (Minimum)
- 1 technical founder (full-stack)
- 1 designer (contract/part-time)
- No other hires for MVP

### Time Commitment
- Week 1-10: Full-time (50+ hours/week)
- Week 11-20: 30-40 hours/week if growing

### Budget (Lean Bootstrap)

**Month 1-3:**
- Domain: $15/year
- Hosting (Vercel + Supabase free tiers): $0
- Email (Resend free tier): $0
- LLM API (OpenAI/Anthropic): $50-200/month
- Design tools (Figma): $0-15/month
- **Total: $50-230/month**

**With buffer:**
- Above + designer contract: $1,000-2,000 for results page
- Above + paid analytics: $50/month
- **Total: $1,100-2,280 one-time**

**Not needed until revenue:**
- Paid ads
- Full-time hires
- Office/coworking
- Complex infrastructure

---

## The #1 Priority

**If you do one thing well, make it this:**

> Create a results experience so insightful and beautiful that people screenshot it and share it on LinkedIn.

This single outcome drives everything:
- Validates product-market fit
- Powers organic growth
- Creates social proof
- Attracts paying customers
- Generates marketing content
- Builds credibility

**The Spotify Wrapped principle:** Not a marketing campaign - a product feature that becomes marketing.

**How to test:**
1. Generate 10 manual results for beta users
2. Ask: "Would you share this on LinkedIn? Why or why not?"
3. If <60% say yes, redesign before coding
4. Iterate until 80%+ "yes, I'd share this"

**Invest disproportionately in:**
- Visual design of results page
- Quality of insights (specific, not generic)
- Cross-layer synthesis (differentiator)
- Shareable card aesthetic
- Narrative voice (make people feel seen)

Every dollar and hour spent here pays dividends everywhere else.

---

## Risk Mitigation

### Top Risks & Mitigation

**Risk 1: Nobody completes assessment (too long/boring)**
- ✓ Validate with Google Form first
- ✓ Show value early (partial results after Layer 1)
- ✓ Target 12-15 min, not 30 min

**Risk 2: Results not insightful (no "wow" moment)**
- ✓ Test 3 results formats before building
- ✓ Use LLM for personalized narratives
- ✓ Interview: "What would make you share?"

**Risk 3: Peer survey doesn't convert (viral loop fails)**
- ✓ Test manually first
- ✓ Show respondents micro-insight about themselves
- ✓ Make survey 2 minutes max

**Risk 4: No willingness to pay**
- ✓ Launch free, validate engagement first
- ✓ Test pricing with surveys before building paywall
- ✓ Have B2B backup (team/hiring assessments)

**Risk 5: Can't differentiate from 16Personalities**
- ✓ Cross-layer synthesis (they don't do this)
- ✓ Risk/decision layer (they don't have)
- ✓ Target professionals, not high schoolers

---

## Success Criteria by Stage

### Phase 0 (Manual MVP)
- 70%+ complete Google Form
- 50%+ would invite peers
- "I feel seen" reactions in interviews

### Phase 1 (First 100 Users)
- 65%+ assessment completion
- 30%+ peer survey send
- 15%+ peer survey conversion
- 20%+ share results
- Strong qualitative feedback

### Phase 1 (First 1,000 Users)
- 70%+ assessment completion
- 40%+ peer survey send
- 20%+ peer survey conversion
- 25%+ share results
- Viral coefficient >0.7
- $0 CAC (organic only)

### Phase 2 (Product-Market Fit)
- 5,000+ profiles
- Viral coefficient >1.0
- 10%+ conversion to paid
- $10K+ MRR
- NPS >40

---

## What NOT to Build (Yet)

**Good ideas for Phase 3+, but they'll kill velocity now:**

### Features to Skip in MVP
- All 7 layers (just 2-3)
- AI Coach (Phase 3)
- Profile MCP Server (Phase 3, needs 5+ layers)
- Mobile apps (responsive web enough)
- Retesting/growth tracking (Phase 2)
- Behavioral sprints (Phase 2)
- Team dashboard (Phase 2)
- Complex gamification
- Social features
- Integrations (Slack, Notion, LinkedIn badges)

### Marketing to Skip (Month 1-3)
- Paid ads
- SEO content marketing
- Podcasts (unless inbound)
- PR campaigns
- Events/conferences
- Influencer partnerships
- Complex email sequences

### Infrastructure to Skip
- Microservices
- Complex CI/CD
- Multiple environments beyond staging/prod
- Advanced monitoring
- Database optimization (premature)
- CDN (Vercel does this)
- Load balancing (<10K users)

---

## Decision Framework

When deciding what to build next, ask:

1. **Does this prove/disprove a core hypothesis?** → High priority
2. **Does this make results more shareable?** → High priority
3. **Does this improve peer viral loop?** → High priority
4. **Can this be done manually for first 100 users?** → Do manually, defer building
5. **Will users pay for this?** → Consider for premium

---

## Critical Files & Next Steps

### Documents to Reference

- `/Users/byeldos/playground/ainam/docs/combined-vision.md` - 7-layer framework, focus on Layers 1, 3, 7 for MVP
- `/Users/byeldos/playground/ainam/docs/data-collection-strategy.md` - Question design, forced-choice methodology, peer survey structure
- `/Users/byeldos/playground/ainam/docs/marketing-strategy.md` - Growth loops, shareable card specs, positioning language

### First Code to Write (When Validation Passes)

```
package.json - Next.js + Tailwind + Shadcn + Supabase
app/assessment/page.tsx - Core assessment flow (your product)
lib/scoring.ts - Layer 1 & 3 scoring algorithms
lib/llm.ts - OpenAI/Anthropic for narrative generation
components/results-card.tsx - Shareable profile card (most important UI)
```

---

## Immediate Next Action

**START HERE (Week 1) - Validate with BEHAVIOR, not promises:**

1. **Build Google Form MVP** (30 questions: 15 Layer 1, 10 Layer 3, 5 demographic)
   - Use IPIP public domain items for Layer 1
   - Write scenario-based questions for Layer 3
   - Keep total time under 15 minutes

2. **Test with 20-30 people - measure what they DO:**
   - Send form link → Track: Do they complete it within 24 hours?
   - Set reminder → Track: How many need a nudge vs. complete immediately?
   - Measure drop-off points → Which questions lose them?

3. **Manually generate results using Claude/GPT-4**
   - Create personalized 2-3 paragraph narrative for each person
   - Include 1 cross-layer synthesis insight
   - Generate 3-5 specific (not generic) insights
   - Send results → Track: Do they respond? What do they say?

4. **Design 3 results page variants in Figma/Canva**
   - Test "screenshot test" → Would you share this on LinkedIn?
   - Show to 10 people → Which design makes them say "wow"?
   - Iterate based on reactions, not opinions

5. **Interview 10 target users (using the strengthened questions above)**
   - Focus on past behavior, not hypotheticals
   - Send them the Google Form during the interview → Do they complete it?
   - Show mock results → Do they screenshot it? Do their eyes light up?
   - Ask for commitment: "Can you introduce me to 2 people?"

6. **Decision point: Does core hypothesis hold?**
   - Look for strong behavioral signals (see Success Criteria)
   - If yes → proceed to build
   - If mixed → iterate on results format and messaging
   - If no → pivot the concept

**If yes → Week 3:** Start building Next.js app

**If no → Pivot:** Iterate on concept before coding (you just saved yourself 8 weeks)

---

## Verification

**This plan is ready for execution when these BEHAVIORAL signals are met:**
- ✅ Manual validation completed (Google Form + interviews with 20-30 people)
- ✅ 70%+ completion rate achieved (they actually completed it, didn't just say they would)
- ✅ 60%+ actually shared results (tracked via screenshots, posts, or forwarded emails - not "I would share")
- ✅ 30%+ completed form immediately during or right after interview (strong intent signal)
- ✅ Results format validated (10+ people react with "wow" or equivalent emotional response)
- ✅ 3+ people volunteer to help, make intros, or pre-commit to beta without prompting
- ✅ Peer survey tested manually (5+ people completed it, at least 2 got curious about their own profile)

**RED FLAGS - Do NOT proceed if:**
- ❌ <60% completion rate (assessment too long or boring)
- ❌ <40% actually share results (not shareable/insightful enough)
- ❌ Lots of "I would" but no "I did" or "can you send me" (polite rejection)
- ❌ No emotional reactions to results (generic, not insightful)

**Key deliverables by milestone:**
- **Week 2:** Validation data from 20-30 manual users + behavioral signal analysis
- **Week 8:** Working MVP with Layers 1, 3, peer survey (only if validation passed)
- **Week 10:** Launch, first 100 users
- **Week 20:** First 1,000 users, monetization live
