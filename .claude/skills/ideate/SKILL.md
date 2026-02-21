---
description: >
  Invoke this skill when the user wants to generate product ideas, asks what to build,
  feels stuck on idea generation, or wants to explore opportunities based on their expertise.
  Triggers: "what should I build", "I want to start something but don't have an idea",
  "help me generate ideas", "I don't know what product to create", "what problems should I solve".
argument-hint: Your background, expertise, or constraints (optional - skill will prompt if needed)
allowed-tools: Read, WebFetch, WebSearch
---

# Idea Generation (Idea Factory)

Generate a structured list of product ideas based on personal expertise, observed problems, and market patterns. Output ideas on an evaluation board for testing.

## The Principle

Good ideas come from the intersection of three things:
1. **Personal authority** — what you know better than most people
2. **Observed pain** — problems you've seen people struggle with (including yourself)
3. **Willingness to pay** — evidence that people already spend money/time on this problem

Most people skip #1 and #3. They generate ideas in categories they don't understand, for pains nobody's paying to solve.

## Process

1. **Extract personal concept** — mine the user's expertise, experience, and positioning
   - What have you done professionally for 2+ years?
   - What do people ask you for help with?
   - What have you built for yourself that others noticed?
   - What category do you follow obsessively (even if not your job)?

2. **Identify pain clusters** — find specific problems within your domain of authority
   - Not "email marketing is hard" — that's too broad
   - "Freelancers lose 20% of proposals because follow-up emails go to spam" — that's specific
   - Look for: repeated complaints in communities, workarounds people have built, money already being spent on partial solutions

3. **Generate 5–10 ideas** using these filters:
   - You can explain why this problem exists (authority)
   - You've seen 3+ people struggle with this in the past 6 months (observed pain)
   - People are already paying for adjacent solutions or spending time on manual workarounds (willingness to pay)

4. **Score each idea** on the Ideas Testing Board using these criteria:
   - **Authority (1-5)**: How well do you understand this problem space?
   - **Pain intensity (1-5)**: How painful is this problem right now for the ICP?
   - **Existing spend (1-5)**: Are people already paying money to solve or avoid this?
   - **Distribution clarity (1-5)**: Can you name exactly where to find 100 people with this problem?
   - **Build confidence (1-5)**: Can you build an MVP in < 2 weeks?

5. **Output top 3 ideas** ranked by total score, with next step for each (validation plan).

## Idea Generation Frameworks

**Framework 1: Pain Mining (from personal experience)**

Start with: "I wasted [time/money] on [task] because [system/tool] didn't [specific thing]."

Examples:
- "I wasted 4 hours reformatting client proposals because Google Docs doesn't preserve layouts when exporting to PDF"
- "I lost a client because I didn't see their email reply until 3 days later — it went to spam"

For each pain: Is this pain shared by others in a specific group? What do they do now?

**Framework 2: Productized Expertise**

Start with: "People pay me to [service]. I do [specific repeatable process] every time. The part they're really paying for is [outcome]."

Examples:
- "People pay me to set up Facebook ads. I do the same pixel + conversion API setup every time. The part they're really paying for is 'not losing attribution data'."
- Turn that into: "One-click Pixel + CAPI setup tool for Shopify stores" (30-min process → 3-min product)

**Framework 3: Workflow Observation**

Start with: "Every [role] I know uses [Tool A] + [Tool B] + [spreadsheet] to do [job]. That's insane."

Examples:
- "Every content creator I know uses Notion + Google Sheets + Zapier to track sponsorships. That's insane." → Sponsorship CRM for creators
- "Every Amazon seller uses Helium10 + manual spreadsheets + ChatGPT to write listings. That's insane." → AI listing optimizer that pulls Helium10 data

**Framework 4: Obvious-But-Missing**

Start with: "[Big platform] has [feature] but doesn't let you [specific thing]. Everyone hacks around it with [workaround]."

Examples:
- "Notion has databases but doesn't let you auto-generate invoices. Everyone exports to Excel then uses another tool." → Notion invoice generator
- "Shopify has product pages but doesn't let you A/B test layouts. Everyone uses external tools or duplicates stores." → Shopify A/B testing app

## Ideas Testing Board Output Format

For each idea, output:

**Idea name**: [Short, descriptive — not the final brand name, just a clear label]

**One-liner**: [What it does and who it's for in one sentence]

**The pain**: [The specific painful moment this solves — not a category]

**Scores**:
- Authority: X/5 — [Why this score]
- Pain intensity: X/5 — [Evidence — complaints, time spent on workarounds]
- Existing spend: X/5 — [What people pay for now that's adjacent]
- Distribution: X/5 — [Exact communities, job titles, or platforms where ICP lives]
- Build confidence: X/5 — [Why this is easy/hard to build in 2 weeks]
- **Total: X/25**

**Validation approach**: [Which smoke test tier from validation-smoke-test skill — CustDev / intent test / paid traffic]

**Red flag check**: [One reason this could fail — wrong ICP, commoditized market, requires behavior change, etc.]

---

## Rules

1. **Don't generate ideas outside the user's domain of authority.** If they're a developer, don't suggest "meal planning app for parents" unless they are a parent and have seen this pain firsthand.

2. **Don't generate ideas in saturated commodity markets without a differentiation angle.** (e.g., "another project management tool" or "AI writing assistant" without a specific underserved niche)

3. **Prioritize ideas with existing spend.** If nobody's paying for a solution or workaround right now, it's extremely hard to create a new market as a solopreneur.

4. **Every idea must name the ICP.** Not "people who need X" — "freelance designers who invoice 5+ clients per month."

5. **Force a choice.** Output max 5 ideas. Rank them by score. Don't let the user walk away with 20 half-baked ideas.

---

## First Question

If user hasn't shared their background: "What have you spent 2+ years doing professionally, or what skill/domain do people ask you for help with?"

If user has shared background, go directly to idea generation using the frameworks above.
