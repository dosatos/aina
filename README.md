# AINAM - Self-Evaluation & Insight Platform

> **"A User Manual for Your Life"** — A comprehensive self-evaluation platform that synthesizes personality, risk profile, execution patterns, and peer feedback into a unified, evolving profile.

## Project Status

**Pre-launch / Planning Phase** — Comprehensive strategic documentation complete. No code written yet. Currently in Phase 0 (Pre-Build Validation).

---

## What Is This?

AINAM is a next-generation self-assessment platform that solves a fundamental problem: **personality tests exist in silos**. Take a DISC test and a Gallup StrengthsFinder, and you get two separate PDFs that don't talk to each other.

### The Core Innovation

**Cross-layer synthesis** — connecting insights across multiple dimensions to reveal patterns no single assessment can surface:

- "Your high risk tolerance + low execution consistency = you start ambitious projects but abandon them mid-way"
- "You're bold in career moves but conflict-avoidant in meetings = selective courage"
- "Your peers rate your empathy higher than you do — you're undervaluing a real strength"

### Target Audience

Primary: Career-oriented professionals (25-40), founders, engineers, and analytical types seeking to:
- Make better career decisions
- Understand their behavioral patterns
- Identify blind spots
- Improve decision-making quality

---

## The 7 Assessment Layers

The platform evaluates users across seven interconnected dimensions, all built on public domain research:

| Layer | Focus | Key Question |
|-------|-------|--------------|
| **1. Behavioral Dynamics** | How you naturally show up in professional settings | "Why do people experience me the way they do?" |
| **2. Drive & Motivation** | What actually fuels you vs. drains your energy | "What motivates me at a deep level?" |
| **3. Risk & Decision Architecture** | How you make decisions under uncertainty + cognitive blind spots | "Where am I systematically wrong?" |
| **4. Execution & Consistency** | The gap between intention and results | "Why do I start things but not finish?" |
| **5. Relational & Conflict Style** | How you handle people, feedback, and disagreement | "Why do my team dynamics play out this way?" |
| **6. Career & Interest Alignment** | Whether your current path matches who you are | "Am I in the right field?" |
| **7. Self-Perception Gap** | Delta between how you see yourself vs. how others see you | "What are my biggest blind spots?" |

### Research Foundation

All layers are built on public domain research:
- Big Five (OCEAN) via IPIP items (3,329+ public domain questions)
- Kahneman & Tversky's behavioral economics research
- Holland Codes (RIASEC) via O*NET
- Conflict resolution frameworks (Blake & Mouton)
- Self-Determination Theory (Deci & Ryan)

**No proprietary frameworks** — fully copyright/trademark-safe.

---

## Key Differentiators

What sets this apart from 16Personalities, CliftonStrengths, and other existing tools:

1. **Cross-Assessment Synthesis** — Unified profile, not isolated test results
2. **Risk & Cognitive Bias Layers** — No competitor measures this alongside personality
3. **The Blindspot Check** — Peer surveys reveal self-perception gaps (Layer 7)
4. **Living Profile** — Evolves over time, not a one-time PDF
5. **AI-Powered Contextual Analysis** — Personalized insights, not generic type descriptions
6. **Growth Tracking** — Retake every 6 months to track evolution
7. **Profile MCP Server** (future) — Expose your profile to AI tools like Claude, making it infrastructure, not just a destination

---

## MVP Strategy

### Phase 0: Pre-Build Validation (Current)

**Before writing any code**, validate core hypothesis: *People will complete a 20-minute multi-layer assessment AND invite peers for feedback if results are insightful enough.*

**Validation Approach:**
1. Manual Google Form MVP (30 questions: 15 Layer 1 + 10 Layer 3 + 5 demographic)
2. Manually score 20-30 pilot users
3. Generate personalized reports using Claude/GPT-4
4. Test peer survey mechanics manually
5. Interview 10-15 target users

**Success Criteria to Proceed:**
- ✅ 70%+ completion rate on Google Form
- ✅ 60%+ actually share their results
- ✅ 30%+ complete form immediately during interview
- ✅ Strong "I feel seen" reactions

### Phase 1: MVP Launch (Week 3-10)

**Build:**
- Simple web app (Next.js + Supabase + Tailwind)
- 3 assessment layers: Behavioral Dynamics (Layer 1), Risk & Decision Architecture (Layer 3), Self-Perception Gap (Layer 7)
- Beautiful, shareable results experience
- Peer survey system (viral growth loop)
- LLM-powered narrative generation

**Target:** First 1,000 users via "1,000 Founding Profiles" campaign

### Phase 2: Iterate & Monetize (Week 11-20)

**Add:**
- Freemium monetization ($49 one-time or $12/month)
- Additional layers (4 & 6) based on demand
- Growth tracking features
- Referral system

### Phase 3: Scale (Month 6+)

**Expand to:**
- All 7 layers
- AI Coach integration
- Profile MCP Server
- B2B features (team dashboards, hiring tools)
- White-label for coaches

---

## Planned Tech Stack

```
Frontend:       Next.js + Tailwind CSS + Shadcn UI
Backend:        Next.js API routes + Supabase (PostgreSQL)
LLM:            OpenAI API / Anthropic Claude API
Email:          Resend or SendGrid
Hosting:        Vercel (frontend) + Supabase Cloud (database)
Analytics:      PostHog or Plausible
```

**Cost:** $0-50/month for first 1,000 users

---

## Market Opportunity

### Market Size

- **Personality Assessment Market:** $10-12B (2025), growing 12-15% CAGR
- **Personal Development Market:** $48-58B (2024)
- **AI Coaching Market:** $1.2B (2025) → $8.2B (2032) at 27% CAGR
- **Serviceable Addressable Market:** $3-5B today → $8-12B by 2031

### Competitive Validation

- **16Personalities:** 18.9M monthly visits, 1B+ tests taken, 2-person team
- **Gallup CliftonStrengths:** 30M assessments, $600M+ from strengths vertical
- **MBTI:** $2B annual revenue

### The Gap

No current player offers cross-assessment synthesis, risk/cognitive bias layers, living dashboards, AI coaching, or peer perception comparison.

---

## Growth Strategy

### Built-In Growth Loops

1. **Peer Survey Viral Loop** — Every user invites 3-5 peers; respondents get curious about their own profile (target: 25%+ conversion = 1.0 viral coefficient)
2. **Shareable Results Cards** — Spotify Wrapped aesthetic for behavioral insights
3. **"How to Work With Me" Manual** — One-pager users share with teams (introduces platform to others)
4. **Cross-Layer Unlock Sequence** — More layers = richer insights = "collect them all" dynamic

### Distribution Channels

- **Primary:** LinkedIn (career-oriented audience, B2B lead gen)
- **Awareness:** TikTok/Instagram Reels, Twitter/X
- **High-Trust:** Podcasts, partnerships with coaches/accelerators
- **SEO:** Long-tail career/self-awareness content

### Launch Strategy

**"1,000 Founding Profiles" Campaign:**
- Public goal to calibrate AI and build norm data
- Founding users get lifetime free premium
- Makes early users feel like participants, not customers

---

## Data Collection Strategy

Four data streams combined:

1. **Self-Report** — Likert scales + forced-choice pairs (60/30 split)
2. **Behavioral Simulation** — Scenario-based decisions revealing actual behavior
3. **Peer Feedback** — 10-minute survey to 3-5 people (Layer 7)
4. **Longitudinal** — Growth tracking over time (6-month retakes)

**Progressive Architecture:**
- Stage 1: Quick profile (Layers 1 & 3) in 10-15 min → immediate insights
- Stage 2: Deep dives (10-15 min each, self-paced)
- Stage 3: Peer survey (triggered after Layer 1)
- Stage 4: Ongoing micro-checks (weekly/biweekly prompts)
- Stage 5: Contextual triggers (AI coach requests data when relevant)

**Quality Controls:**
- Response pattern analysis (speed anomalies, straight-lining, inconsistencies)
- Forced-choice to reduce social desirability bias
- Peer data as cross-validation
- Per-layer confidence scores

---

## Business Model

### B2C Revenue

| Model | Pricing | Details |
|-------|---------|---------|
| **Freemium** | Free basic / $15-30/mo premium | 2-3 basic layers free, full suite behind paywall |
| **One-time assessment** | $49-99 | Comprehensive evaluation package |
| **Subscription** | $10-25/mo | Continuous growth tracking, AI coach access |

### B2B Revenue

| Model | Pricing | Details |
|-------|---------|---------|
| **Team/Enterprise** | Per-seat | Team-building, leadership development |
| **Hiring** | $50-150/candidate | Recruitment assessment tool |
| **White-label** | Custom | For coaches, HR consultants, therapists |

### Additional Streams

- Coaching marketplace (referral fees)
- Accelerator partnerships
- MCP server premium tier

---

## Repository Structure

```
docs/
├── combined-vision.md              # Complete product vision & 7-layer framework
├── roadmap-0-to-1.md               # Pragmatic roadmap from 0 to 1,000 users
├── market-size.md                  # Market analysis & opportunity sizing
├── data-collection-strategy.md     # Question design & data architecture
├── marketing-strategy.md           # Growth loops & distribution channels
├── vision/                         # Individual brainstorm sessions
│   ├── gem-1.md
│   ├── opai-1.md
│   ├── ant-1.md
│   └── overlap-and-generic-layers.md
├── data-collection/                # Layer-specific data collection research
│   ├── gem.md
│   ├── opai-1.md
│   ├── opai-2.md
│   └── ant.md
├── marketing/                      # Marketing research & positioning
│   ├── gem.md
│   ├── opai.md
│   └── ant.md
├── market-size/                    # Market analysis by source
│   ├── gem.md
│   ├── opai.md
│   └── ant.md
└── prompts/                        # LLM prompts for content generation
    ├── phase0-question-generator.md
    └── phase-0/                    # Layer-specific question sets
        ├── opai.md
        ├── gem.md
        ├── ant.md
        └── compiled-questions/     # Final question compilation
            ├── 00-overview-and-guidance.md
            ├── 01-behavioral-dynamics-questions.md
            ├── 02-risk-decision-questions.md
            └── 03-methodology-and-analysis.md
```

---

## Next Steps (Immediate)

### Week 1-2: Manual MVP

1. **Build Google Form** with 30 questions (15 Layer 1 + 10 Layer 3 + 5 demographic)
2. **Test with 20-30 people** — measure actual completion rates, not hypothetical interest
3. **Manually generate results** using Claude/GPT-4
4. **Design 3 results page variants** in Figma — test which passes the "screenshot test"
5. **Interview 10 target users** — focus on past behavior, not "would you" questions
6. **Decision point:** Does core hypothesis hold?

### If Validation Passes → Week 3+

1. Set up Next.js + Supabase + Vercel
2. Build assessment engine (Layers 1 & 3)
3. Build results generation (LLM integration)
4. Build peer invitation flow
5. Private beta (20-30 users)
6. Launch "1,000 Founding Profiles" campaign

### If Validation Fails → Pivot

Iterate on concept before writing any code (saving 8+ weeks of wasted development).

---

## Key Metrics

| Metric | Target | Why It Matters |
|--------|--------|----------------|
| **Assessment completion** | 70%+ | Core product validation |
| **Time to complete** | 12-15 min | Attention holding |
| **Peer survey send rate** | 40%+ | Viral loop activation |
| **Peer survey conversion** | 20%+ | Growth engine efficiency |
| **Results share rate** | 30%+ | Organic reach |
| **Retake rate (6 months)** | 40%+ | Growth OS stickiness |

---

## Philosophy & Principles

### Product Design

- **Progressive disclosure** — Give value before asking for completion
- **Earned insights** — Partial results reward continued engagement
- **Specific, not clinical** — "You push for speed but miss signals" vs. "You are Type D"
- **Living profile** — Evolves over time, not static
- **No jargon** — Accessible to everyone, not just psychologists

### Growth Strategy

> **The #1 Priority:** Create a results experience so insightful and beautiful that people can't help but share it.

The Spotify Wrapped principle: Not a marketing campaign — a product feature that *becomes* marketing.

### Ethical Guardrails

- Results are informational, not diagnostic
- Peer data anonymization (aggregate patterns only)
- Transparent data collection practices
- Clear disclaimers (not mental health evaluation)
- Employment testing compliance (if used for hiring)

---

## References & Research

### Key Resources

- IPIP Big Five items (public domain): [https://ipip.ori.org/](https://ipip.ori.org/)
- Holland RIASEC via O*NET: [https://www.onetonline.org/](https://www.onetonline.org/)
- Kahneman & Tversky behavioral economics research (public domain academic papers)
- Market data sources: Future Market Insights, Mordor Intelligence, Credence Research

### Inspiration

- **16Personalities** — Virality + accessibility (but scientifically weak)
- **CliftonStrengths** — Gold standard credibility (but one-dimensional)
- **Spotify Wrapped** — Shareable results design
- **Crystal** — Professional application of personality data

---

## Contributing

This project is currently in pre-launch planning phase. Once MVP validation is complete, contribution guidelines will be added.

---

## License

Not yet determined. All strategic documentation is proprietary until further notice.

---

## Contact & Updates

Project Name: **AINAM** (working title)
Status: Phase 0 - Pre-Build Validation
Last Updated: February 2026

---

## Appendix: Strategic Questions

### Open Decisions

1. **Product Direction:** Psychological self-discovery vs. performance optimization?
2. **Tone:** Fun & accessible vs. serious & analytical?
3. **Scientific Validation:** Core brand pillar or secondary concern?
4. **Go-to-Market:** B2C first or B2B first?
5. **Experience:** One-time test or ongoing growth system?
6. **Platform:** Mobile-first or web app?
7. **AI Depth:** Report generation only or full coaching experience?
8. **MVP Scope:** Which 2-3 layers for 8-week launch?

### Validated Assumptions

- Cross-layer synthesis is genuinely differentiated
- Peer survey mechanics create viral growth
- Target audience (25-40, career-oriented) has willingness to pay
- $10-12B market with clear whitespace
- Public domain research provides sufficient scientific foundation

### Key Risks

- **Product-market fit:** Will people complete assessments AND find results shareable?
- **Peer loop:** Will the viral mechanic actually convert at 20%+?
- **Monetization:** Can we convert free users to paid at 10%+?
- **Differentiation:** Can we prove value beyond 16Personalities/CliftonStrengths?
- **Retention:** Will users return for growth tracking?

**Mitigation:** Phase 0 validation BEFORE building anything.

---

**The Vision:** From a one-time personality test to a Growth OS — infrastructure for self-knowledge that becomes more valuable over time.
