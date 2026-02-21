# Delivery Phases

Phased rollout for the self-assessment platform. Each phase has clear exit criteria before moving to the next.

---

## Phase 0: Validation & Marketing Foundation
**Goal:** Prove demand exists before building. Set up conversion infrastructure.

**Timeline:** 1-2 weeks

### Deliverables
- [ ] Landing page (waitlist or pre-order)
- [ ] Channel strategy (where to acquire first users)
- [ ] Ad creative (3-5 hook variations)
- [ ] Smoke test live (email capture or pre-sale)
- [ ] 100+ signups OR $500+ in pre-orders

### Exit Criteria
- LP converting at >2% (cold traffic)
- Clear signal that ICP wants this (qualitative feedback from signups)
- Channel identified with <$25 CPL

### Why This First
Don't build until you know people will pay. A landing page takes 1 day. The product takes 8+ weeks. Validate first.

---

## Phase 1: MVP Build (Core Assessment)
**Goal:** Ship the minimum viable version that delivers the core promise (cross-layer synthesis).

**Timeline:** 6-8 weeks

### Scope
**In scope:**
- Layer 1: Behavioral Dynamics (IPIP Big Five, 50 items)
- Layer 3: Risk & Decision Architecture (custom questions, ~20 items)
- Layer 7: Self-Perception Gap / Blindspot Check (self + peer survey, ~10 items each)
- Basic cross-layer synthesis (pattern detection, 3-5 key insights)
- Profile dashboard (results display, synthesis output)
- Email capture + account creation flow
- Payment integration (Stripe)

**Out of scope (Phase 2+):**
- Full AI coach (scenario-based advice)
- Growth tracking over time
- Layers 2, 4, 5, 6
- MCP integration
- Mobile app

### Deliverables
- [ ] Assessment flow (all 3 layers, ~80 total questions)
- [ ] Scoring engine (validated against research models)
- [ ] Cross-layer synthesis algorithm (AI-powered or rule-based MVP)
- [ ] Profile dashboard UI
- [ ] Peer survey mechanism (shareable link for Blindspot Check)
- [ ] Payment flow (free → paid upsell)
- [ ] Onboarding emails (welcome, results ready, upsell to full profile)

### Exit Criteria
- 10 beta users complete full assessment
- Synthesis output feels valuable (qualitative feedback: "I learned something new")
- Payment flow works end-to-end
- No critical bugs in assessment logic

### Tech Stack (TBD)
- Frontend: React / Next.js / Svelte (decide based on speed)
- Backend: Node.js / Python (depends on AI layer)
- Database: PostgreSQL or Supabase
- Hosting: Vercel / Railway / Render
- AI: OpenAI API or Claude API for synthesis

---

## Phase 2: Launch & First 100 Paid Users
**Goal:** Get the product in front of real users. Learn what works and what breaks.

**Timeline:** 4-6 weeks

### Deliverables
- [ ] Launch sequence (email list from Phase 0, social posts, communities)
- [ ] Paid ads live (channel from Phase 0, $500-1k initial budget)
- [ ] Analytics tracking (funnels, drop-off points, user behavior)
- [ ] User feedback loop (post-assessment survey, email follow-ups)
- [ ] First 100 paid users acquired

### Success Metrics
- LP conversion: >2% (cold traffic)
- Free → Paid conversion: >10% (email nurture)
- CAC < $50
- NPS or feedback score >7/10
- 1-2 testimonials captured

### What to Learn
1. Which pain hooks convert best in ads?
2. Where do users drop off in the assessment flow?
3. What synthesis insights resonate most?
4. What objections come up before payment?
5. Do users come back / refer others?

---

## Phase 3: Iterate & Scale
**Goal:** Fix what's broken. Double down on what works. Add features that drive retention or virality.

**Timeline:** Ongoing

### Priorities (in order)
1. **Fix drop-offs** — if users bail mid-assessment, shorten it or add progress indicators
2. **Improve synthesis quality** — if insights feel generic, add depth or personalization
3. **Increase virality** — if Blindspot Check isn't getting shared, optimize the peer survey UX
4. **Add retention features** — growth tracking, re-assessment after 6 months, coaching sprints
5. **Expand layers** — add Layers 2, 4, 5, 6 based on user demand

### Feature Candidates (Backlog)
- AI coach (scenario-based advice: "Should I take this promotion?")
- Team/relationship mode (compare profiles with partner/coworker)
- MCP integration (profile travels with you across AI tools)
- Mobile app (iOS/Android)
- API for third-party integrations
- Enterprise version (team assessments, manager dashboards)

### When to Scale Ads
- When CAC < LTV/3
- When LP + funnel is stable (conversion rates predictable)
- When product has <5% critical bug rate
- When you have 2-3 winning ad creatives

---

## Current Phase
**→ Phase 0: Validation & Marketing Foundation**

Next step: `/validation-smoke-test` or `/structure-lp` to start building the pre-launch funnel.
