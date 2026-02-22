# Phase 0: Validation & Marketing Foundation

**Status:** In Progress
**Goal:** Prove demand exists before building. Set up conversion infrastructure.
**Timeline:** 2 weeks (target completion: March 7, 2026)
**Budget:** \$200 (organic-first strategy)

---

## Objectives

1. **Validate demand:** 50-100 email signups (organic-first)
2. **Validate messaging:** Landing page converting at >2% (organic traffic)
3. **Identify best channel:** Find which organic channel resonates most
4. **Get qualitative signal:** 3-5+ comments/DMs saying "I need this"

## Strategy: Organic-First + CLI-First Development

**Why not \$1k-2k in ads right away?**
- Organic validation is stronger signal (people share without you paying)
- Learn what language resonates before spending on ads
- Lower risk (\$200 vs \$2,000)
- Build community from day one

**Why Claude Code direct (not v0/bolt/GUI tools)?**
- Zero context switching (stay in CLI entire time)
- Full control and understanding of code
- Same speed as GUI tools (1-2 hours)
- Matches user preference: "I'd prefer not to change the interface"

**The approach:**
1. Build LP with Claude Code directly (HTML + Tailwind CDN)
2. Launch with organic posts (Reddit, Twitter, LinkedIn, communities)
3. See what gets traction (upvotes, comments, shares)
4. Amplify what works with small paid test (\$100-150)
5. If organic + small paid = validation → scale in Phase 1

**See research/tools/landing-page-builders-comparison.md for full analysis of Claude Code vs v0.app vs bolt.new**

---

## Assets Available

### Research (Already Complete)
- ✅ Product brief populated (`project/product-brief.md`)
- ✅ Persona research (`docs/b2c-persona-research.md`)
- ✅ Market size validation (`docs/market-size.md`)
- ✅ Marketing strategy (`docs/marketing-strategy.md`)
- ✅ Data collection strategy (`docs/data-collection-strategy.md`)

### Landing Page Templates (Production-Ready)
- ✅ Template 1: Career Clarity (Sunday Scaries angle)
- ✅ Template 2: Founders (Decision-making audit)
- ✅ Template 3: Engineers (Execution patterns)

**Source:** `docs/marketing/landing-page-PRODUCTION.md`

---

## Phase 0 Plan (Week by Week)

### Week 1: Build & Launch (Days 1-7)

#### Day 1-2: Landing Page Build
**Goal:** Get one LP variant live and trackable

**Recommended Approach: Claude Code Direct (CLI workflow)**

**Why:** Fastest for CLI-first developers, no context switching, full control, same speed as GUI tools.

**Tasks:**
- [ ] Choose LP template (Recommendation: Template 1 - Career Clarity)
- [ ] Create project directory: `mkdir landing-page && cd landing-page`
- [ ] Use Claude Code to generate single-page HTML with Tailwind CDN
  - Prompt: "Read Template 1 and create index.html with responsive design, email form, Analytics"
  - Time: 10-20 minutes generation + 30-60 min iteration
- [ ] Test locally: `python3 -m http.server 8000` or `npx serve .`
- [ ] Add conversion tracking (Google Analytics script tag)
- [ ] Set up email capture (form → Airtable webhook or Zapier)
- [ ] Deploy: `vercel deploy` or `netlify deploy` (one command)
- [ ] Test on mobile (responsive design)

**Alternative:** Use v0.app if you prefer GUI-based generation (see research/tools/landing-page-builders-comparison.md)

**Deliverable:** Live landing page at a URL

**Success check:** Page loads fast (<3s), form works, tracking fires

**Time estimate:** 1-2 hours total (vs 3-4 hours with manual builders)

---

#### Day 3-4: Smoke Test Design + Organic Seeding
**Goal:** Decide what we're validating

**Three options:**

**Option A: Waitlist (Lowest friction)**
- Copy: "Join the waitlist — get early access when we launch"
- CTA: "Get Early Access"
- Collect: Email + optional "What's your biggest career challenge right now?"
- **Pro:** Easy to set up, low commitment ask
- **Con:** Doesn't validate willingness to pay

**Option B: Pre-Order (Validates payment)**
- Copy: "Pre-order the full assessment — \$39 early-bird (normally \$49)"
- CTA: "Reserve Your Spot - \$39"
- Collect: Email + payment via Stripe
- **Pro:** Proves people will pay
- **Con:** Higher friction, need refund policy

**Option C: Micro-Assessment (Validates engagement)**
- Copy: "Take a 3-minute risk profile quiz — get results + join waitlist for full platform"
- CTA: "Get My Risk Profile"
- Collect: 5 questions → instant result → email capture
- **Pro:** Gives value first, tests completion behavior, viral potential
- **Con:** Requires building a mini-assessment (Google Form or Typeform)

**RECOMMENDATION: Start with Option C (Micro-Assessment)**

**Why:**
- Validates engagement (do they complete?)
- Gives them value before asking for email
- Teaser result creates curiosity for full platform
- Can add payment option later if engagement is high

**Tasks:**
- [ ] Build 3-minute risk profile quiz (5 questions, instant scoring)
- [ ] Write result variations (3-5 result types)
- [ ] Add "Join waitlist for full platform" at end
- [ ] Connect email capture

**Tools:** Google Forms (free) or Typeform (free tier)

---

**Day 3-4: Organic Seeding**

Now that LP + micro-assessment are live, seed them organically.

**Reddit Posts (Organic - \$0)**

Target subreddits:
- r/cscareerquestions (3.9M members)
- r/ExperiencedDevs (178K members)
- r/careerguidance (463K members)
- r/startups (1.4M members) - if testing founder angle

**Post format (value-first, not promotional):**
```
Title: "I analyzed 50 mid-career engineers who felt stuck. Here's the pattern 73% shared."

Body:
[Share 2-3 insights from your persona research]

The common thread: they'd all taken personality tests (MBTI, 16P, StrengthsFinder) but still couldn't figure out WHY they kept making the same career mistakes.

The issue isn't the tests — it's that they're isolated. High risk tolerance + low execution consistency = starts projects but never finishes. But MBTI doesn't measure execution. StrengthsFinder doesn't measure risk.

I built a quick 3-min assessment that does cross-layer pattern detection. If this resonates, here's the link: [your LP]

Happy to share what I'm learning.
```

**Rules:**
- Don't spam multiple subreddits in one day (space them 24-48 hrs apart)
- Engage authentically with every comment
- Don't be defensive if someone criticizes — ask questions
- If mods remove it, message them and ask how to reframe

**Tasks:**
- [ ] Write Reddit post (value-first)
- [ ] Post to first subreddit
- [ ] Engage with comments for 24 hours
- [ ] Iterate based on feedback
- [ ] Post to second subreddit (48 hours later)

---

**Twitter/X Thread (Organic - \$0)**

Thread format that works:
```
You've taken 5 personality tests.

Still stuck in your career.

Here's why (and what actually helps):

🧵

1/ Every test gives you ONE piece of data in a vacuum.

MBTI: You're an INTJ
StrengthsFinder: You're strategic
Risk quiz: You're risk-averse

Cool. Still stuck.

2/ The problem isn't the tests. It's that they don't talk to each other.

High risk tolerance on CAREER moves + low consistency in EXECUTION = you make bold bets but burn out after 18 months.

Neither test catches this pattern.

3/ I spent 6 months interviewing mid-career engineers and PMs who felt stuck.

73% had taken multiple tests.
91% couldn't explain WHY they kept ending up in the same place.

The pattern: isolated data ≠ insight

4/ So I built something different.

A 3-min assessment that does cross-layer pattern detection.

Measures: behavioral style + risk profile + execution patterns

Then shows you what COMBINATION is costing you.

5/ Early version is live. Testing with 50 people this week.

If you're stuck mid-career and want to try it, DM me.

Or just bookmark this if it's useful later.
```

**Tasks:**
- [ ] Write Twitter thread
- [ ] Post thread
- [ ] Reply to every comment/question
- [ ] DM people who engage (offer early access)

---

**LinkedIn Post (Organic - \$0)**

LinkedIn works differently — personal story > clinical analysis.

```
6 months ago, I started interviewing engineers and PMs who felt stuck mid-career.

I wanted to understand why smart people with great résumés kept making the same career mistakes.

Here's what I found:

Every single person had taken personality tests.

MBTI. 16Personalities. StrengthsFinder. Sometimes 3-4 different ones.

And they all said the same thing:

"I got a label. I got a PDF. I'm still stuck."

The problem wasn't the tests.

It was that the tests don't talk to each other.

High risk tolerance + low execution consistency = you start ambitious projects and quit at week 3. Your motivation is real. Your systems aren't.

But no single test catches that COMBINATION.

So I built a tool that does.

3-minute assessment. Cross-layer pattern detection. See what combination is costing you.

Testing it with 50 people this week.

If you're mid-career, feeling stuck, and open to trying something new — comment "interested" or DM me.
```

**Why this works on LinkedIn:**
- Personal journey (not a product pitch)
- Vulnerability (you're learning publicly)
- Clear value prop (solves the "still stuck" problem)
- Low-friction CTA (comment or DM)

**Tasks:**
- [ ] Write LinkedIn post (personal story format)
- [ ] Post from personal profile (NOT company page)
- [ ] Engage with every comment within 1 hour
- [ ] DM people who comment "interested"

---

**Hacker News "Show HN" (Organic - \$0)**

HN is great for getting analytical/engineer types IF you frame it right.

```
Title: Show HN: Cross-layer personality assessment (synthesizes Big Five + risk + execution)

Body:
I've been working on a personality assessment tool that does something I haven't seen before: it combines multiple validated frameworks (Big Five, prospect theory, behavioral economics) and does cross-layer pattern detection.

Example insight: "High risk tolerance (0.78) on career moves + low execution consistency (0.34) = you make bold career bets but struggle to sustain momentum. Last 3 roles: left after 18 months. Root cause: chasing novelty, not alignment."

The idea: every personality test gives you ONE dimension in isolation. But the patterns that actually matter emerge from COMBINATIONS.

Built on:
- IPIP Big Five (public domain item bank)
- Kahneman & Tversky research (prospect theory, cognitive biases)
- Scenario-based behavioral simulations

Early version here: [link]

Would love feedback from this community — especially on the methodology or if you think this is just astrology with extra steps.
```

**Why this works on HN:**
- Technical credibility (cites research)
- Self-aware (acknowledges potential criticism)
- Asks for feedback (not just promoting)
- Open to being wrong

**Tasks:**
- [ ] Write HN post (technical + humble)
- [ ] Post "Show HN"
- [ ] Reply to EVERY comment (especially critical ones)
- [ ] Don't defend — ask questions and iterate

---

**Indie Hackers (Organic - \$0)**

Frame as a build-in-public journey.

```
Title: Building a personality assessment platform that does cross-layer synthesis

I'm working on a tool that synthesizes multiple personality/behavioral assessments into one evolving profile.

The insight: every test (MBTI, Big Five, StrengthsFinder) gives you ONE dimension. But the patterns that matter emerge from COMBINATIONS.

Example: High risk tolerance + low execution = starts projects, never finishes.

**Current status:**
- 6 months of user research (interviewed 50+ mid-career professionals)
- Built 3 landing page variants
- Testing micro-assessment this week
- Goal: 50-100 signups in 2 weeks to validate demand before building full product

**Tech stack (planned):**
- Frontend: React/Next.js
- Backend: Node.js or Python
- AI synthesis: OpenAI/Claude API
- DB: PostgreSQL

Early version: [link]

Open to feedback / questions on approach.
```

**Tasks:**
- [ ] Post on Indie Hackers
- [ ] Share progress updates (weekly)
- [ ] Engage with feedback

---

#### Day 5-7: Monitor Organic Traction
**Goal:** Watch what gets traction organically

**Tasks:**
- [ ] Check Reddit posts multiple times/day — reply to every comment
- [ ] Monitor Twitter thread engagement — reply to every mention
- [ ] Track LinkedIn post reach — DM everyone who comments
- [ ] Watch analytics:
  - Which channel is driving most traffic?
  - Landing page bounce rate
  - Time on page
  - Scroll depth
  - Micro-assessment completion rate
  - Email captures

**Signals to watch (first 100 visitors):**
- **Strong signal:** Reddit post gets >50 upvotes or >10 comments
- **Strong signal:** Twitter thread gets >20 replies or reshares
- **Strong signal:** LinkedIn post gets >100 reactions or >15 comments
- **Warning sign:** Bounce rate > 70% → headline/hook mismatch
- **Warning sign:** Time on page < 30s → not reading, not engaged
- **Warning sign:** Micro-assessment started but not completed → too long or broken

**Engagement rules:**
- Reply to EVERY comment (even negative ones)
- Don't be defensive — ask questions
- Thank people for critical feedback
- DM anyone who says "interested" or "need this"

---

### Week 2: Analyze & Iterate (Days 8-14)

#### Day 8-10: Data Analysis
**Goal:** Understand what's working and what's not

**Analyze:**
1. **Traffic quality by channel**
   - Which channel drove most engaged visitors? (time on page, scroll depth)
   - Which had best cost per visitor?
   - Which had best completion rate?

2. **Landing page performance**
   - Where do people drop off? (use heatmap/scroll map)
   - Do they read the pain section?
   - Do they reach the CTA?
   - What's the form completion rate?

3. **Qualitative feedback**
   - If micro-assessment: what's completion rate?
   - If waitlist: read the "biggest challenge" responses — do they match persona research?
   - Any comments/replies on Reddit/Twitter?

**Tasks:**
- [ ] Pull analytics data (visits, bounces, conversions)
- [ ] Review heatmaps/scroll maps
- [ ] Read all qualitative responses
- [ ] Calculate key metrics:
  - CTR from ads
  - LP conversion rate
  - Cost per lead (CPL)
  - Completion rate (if micro-assessment)

---

#### Day 11-12: Amplify What Works (Small Paid Test)
**Goal:** Take what worked organically and amplify with \$100-150

**If Reddit posts got traction:**
- Run Reddit Ads (\$100) targeting same subreddits
- Use the EXACT language from your organic post that worked
- Target: same demographics as subreddit

**If LinkedIn post did well:**
- Boost the post (\$50-75) to expand reach
- OR create LinkedIn ad using same copy
- Target: 25-40, Software Engineers/PMs, US

**If Twitter thread resonated:**
- Keep posting (organic is free)
- OR test Twitter Ads (\$50) to amplify best-performing thread

**If nothing got traction organically:**
- DON'T spend on ads yet
- Iterate messaging first
- Try different pain points from persona research
- Test Template 2 (Founders) or Template 3 (Engineers)

**Tasks:**
- [ ] Choose best-performing organic channel
- [ ] Set up small paid test (\$100-150)
- [ ] Run for 3-5 days
- [ ] Monitor conversion vs organic

---

#### Day 13-14: Decision Point
**Goal:** Decide whether to proceed to Phase 1

**Evaluate against success criteria:**

✅ **Primary Goal: 50-100 email signups (mostly organic)**
- [ ] Total signups: _____
- [ ] If 50-100 → strong validation, proceed to Phase 1
- [ ] If 30-50 → moderate signal, extend 1 week
- [ ] If <30 → revisit messaging or audience

✅ **Secondary Goal: LP converting at >2%**
- [ ] Conversion rate: _____%
- [ ] If >2% → messaging resonates
- [ ] If 1-2% → iterate headline/CTA
- [ ] If <1% → fundamental mismatch

✅ **Tertiary Goal: Identify best organic channel**
- [ ] Reddit: ____ clicks, ____ signups
- [ ] Twitter: ____ clicks, ____ signups
- [ ] LinkedIn: ____ clicks, ____ signups
- [ ] Hacker News: ____ clicks, ____ signups
- [ ] Best channel: __________

✅ **Qualitative Signal (MOST IMPORTANT)**
- [ ] How many comments/DMs saying "I need this"? _____
- [ ] Do responses confirm persona research?
- [ ] Are people describing the pain we mapped?
- [ ] Any organic shares/retweets? _____

**Key insight:** 30 highly engaged signups > 100 lukewarm signups. Quality matters more than quantity in Phase 0.

**Tasks:**
- [ ] Write Phase 0 retrospective (what worked, what didn't)
- [ ] Update `project/plan.md` with findings
- [ ] Make GO/NO-GO decision for Phase 1

---

## Exit Criteria (To Move to Phase 1)

**Must have 2 of 3:**
1. 50-100 email signups (mostly organic)
2. LP conversion >2% (proves messaging works)
3. 3-5+ qualitative signals ("I need this" comments/DMs)

**Plus:**
- At least ONE post got significant organic traction (>50 upvotes or >10 comments)
- No major red flags (e.g., "this already exists" or "I'd never pay for this")

**If criteria met:** Move to Phase 1 (MVP Build)
**If criteria not met:** Iterate messaging, test different persona segment, or revisit product positioning

**Why organic traction matters:**
- 16Personalities: 18.9M visits/month, zero ad spend
- If it doesn't spread organically in Phase 0, it won't scale virally in Phase 2-3
- Paid ads can buy traffic, but not genuine interest

---

## Budget Breakdown

| Item | Cost | Notes |
|------|------|-------|
| Landing page | \$0 | Claude Code direct (HTML + Tailwind CDN) |
| Hosting | \$0 | Vercel free tier |
| Micro-assessment tool | \$0 | Google Forms (free) |
| Email capture | \$0 | Google Sheets or Airtable free tier |
| Analytics/heatmaps | \$0 | Google Analytics + Microsoft Clarity (free) |
| Domain (optional) | \$12 | Only if you want custom URL (Vercel provides free subdomain) |
| Reddit Ads (small test) | \$100 | Only if organic Reddit posts get traction |
| LinkedIn boost (optional) | \$50 | Only if organic post performs well |
| Buffer | \$38 | For surprises |
| **Total** | **\$200** | **\$0-12 if staying purely organic** |

**Note:** You can do Phase 0 for **\$0-12** if you skip paid amplification and rely purely on organic. The \$200 budget includes small paid tests to amplify what works organically.

**Tools:** All free tier (Claude Code, Vercel, Google Forms, Airtable, Google Analytics)

---

## Risks & Mitigations

| Risk | Mitigation |
|------|------------|
| **Reddit posts get removed by mods** | Message mods, ask how to reframe; try smaller niche subreddits |
| **No organic traction on any channel** | Post is too promotional; rewrite as pure value (insights without CTA) |
| **LP doesn't convert** | Have 3 template variants ready to swap in |
| **People sign up but don't engage** | Add follow-up email asking "What made you sign up?" |
| **Wrong audience** | Persona research is solid, but if completely off, test Template 2 (Founders) or Template 3 (Engineers) |
| **Spent \$200 on ads, got nothing** | Only spend on ads AFTER organic works; don't pay to amplify what doesn't resonate organically |

---

## Success Looks Like

**Minimum viable success:**
- 50 emails collected (mostly organic)
- 2-3% LP conversion
- One post got >50 upvotes or >10 engaged comments
- 3-5 DMs/comments saying "I need this"

**Strong success:**
- 75-100 emails
- 3-4% LP conversion
- Multiple channels working organically
- One post went semi-viral (>200 upvotes or >30 comments)
- People asking "when can I use this?"
- Someone shared it without you asking

**Exceptional success:**
- 150+ emails (purely organic)
- 5%+ conversion
- Organic sharing happening (people posting in other communities)
- Clear product-market fit signal
- Inbound DMs from potential partners/investors/press

---

## Next Actions (Immediate)

**This week (Days 1-4):**
1. Choose LP template (Template 1 - Career Clarity recommended)
2. Build landing page with Claude Code (1-2 hours)
   - `mkdir landing-page && cd landing-page`
   - Prompt Claude to generate index.html with Template 1 copy
   - Test locally, iterate, deploy with `vercel deploy`
3. Build micro-assessment (Google Forms - 5 questions, instant result) (10 min)
4. Set up tracking (Google Analytics) (5 min)
5. Write organic seeding posts:
   - Reddit post (value-first, not promotional)
   - Twitter thread
   - LinkedIn post (personal story)

**Next week (Days 5-7):**
6. Post on Reddit (r/cscareerquestions first)
7. Post Twitter thread
8. Post LinkedIn (personal profile)
9. Engage authentically with every comment
10. Monitor what gets traction

**Week 2 (Days 8-14):**
11. Analyze which channel worked
12. Amplify with small paid test (\$100-150) if warranted
13. Iterate based on feedback
14. Make GO/NO-GO decision

---

## Open Questions to Resolve Before Starting

1. **Product name:** Still TBD — do we need to finalize before Phase 0 or can we launch with "Project Name TBD" / placeholder?
2. **Domain:** Do we buy a domain now or use a subdomain (e.g., carrd.co/yourproject)?
3. **Refund policy:** If we do pre-orders, what's the refund promise? (Suggestion: "Full refund anytime before product launches")
4. **Email follow-up:** Do we send a "thanks for joining" email immediately, or wait until we have more to share?

**Recommendation:** Don't let these block you. Launch with placeholders if needed. Phase 0 is about validation, not perfection.

---

## What's Next After Phase 0

**If validation succeeds:**
- Update delivery-phases.md with findings
- Write Phase 1 build plan
- Scope MVP (which layers to build first)
- Choose tech stack
- Start building

**If validation fails:**
- Analyze why (wrong message, wrong audience, wrong channel, or wrong product)
- Decide: iterate messaging, pivot positioning, or shelve idea
- Document learnings

---

## Current Status

- [x] Research complete
- [x] Landing page templates ready
- [x] Phase 0 plan written
- [ ] LP template chosen
- [ ] Smoke test approach chosen
- [ ] Landing page built
- [ ] Ads live
- [ ] Signups coming in

**Next step:** Review this plan → Make decisions on open questions → Start Day 1 tasks
