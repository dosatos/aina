---
description: >
  Invoke this skill when the user wants to validate an idea before building, asks what to build first,
  wants to test demand, asks "should I build this", or describes a product that hasn't been sold yet.
  Triggers: "I want to build X", "how do I validate this", "should I build this",
  "how do I know if anyone wants this", "I have this idea for...".
argument-hint: The idea in one sentence — what it does and who it's for
allowed-tools: Read, WebFetch, WebSearch
---

# Validation Smoke Test

Prove demand before writing a single line of code. The goal is not to build — it's to find out if someone will pay.

## The Principle

A smoke test is a fake door. You put up the minimum possible surface, drive traffic to it, and measure intent. Email signups are weak signal. "Buy Now" clicks are strong signal. Credit card charges are the only true signal.

## Process

1. **Read `project/product-brief.md`** for: ICP, core pain, offer, price point.
2. **Define the one assumption to test**: What is the riskiest belief you're holding? (Usually: "people will pay for this.")
3. **Design the minimum test surface** — pick the right format for the signal you need.
4. **Set the success threshold** before running the test. Not after.
5. **Output the test plan** — what to build, where to drive traffic, what number means "proceed."

## Smoke Test Formats (Cheapest to Most Expensive)

**Tier 0 — CustDev (before anything else)**

If you have fewer than 500 active users, do this before building a page. Talk to 10 people who match the ICP.

- Find them in communities, LinkedIn, Slack groups — wherever they actually are.
- Ask two questions only: "How do you currently solve [pain]?" and "What would make you switch?"
- Do NOT pitch. Do NOT describe your solution. Listen.

**Success threshold**: 3 out of 10 say "I'd pay for that right now" (not "interesting," not "sounds useful") → proceed to Tier 1.
**Kill threshold**: < 2 out of 10 express active pain or current spend → wrong ICP or wrong pain. Stop before building.

Tabunov: "10 honest conversations beat 1,000 anonymous visitors." Don't skip this step because it feels slow. It is the fastest path to not wasting a month.

---

**Tier 1 — Pure intent (< 2 hours)**
- 1-page site (Carrd, Typedream, Framer) with a "Join Waitlist" or "Get Early Access" button
- Measure: clicks on the button vs. visitors (target: > 15% click-through)
- If higher intent needed: button leads to a Stripe payment page ("Pay $X to reserve your spot") — no product yet, refund if you don't build

**Tier 2 — Direct outreach (< 4 hours)**
- Find 20 people who fit the ICP. DM them the problem statement. Offer to solve it for them manually.
- Measure: how many say "yes, when?" vs. "interesting, let me know when it's ready"
- "Let me know when it's ready" = no signal. "How do I get this?" = signal.

**Tier 3 — Paid traffic test (< 48 hours)**
- $50–$100 Meta or Google ad to a smoke test page
- Measure: CTR on ad + conversion on page
- Only use if you have ICP nailed and can target precisely

## Output Format

**The one assumption being tested**: [Specific belief — e.g., "Freelancers will pay $49/mo to avoid chasing invoices"]

**Test format**: [Which tier and why — match to how fast you need signal and how much you can spend]

**What to build**: [Exact spec — e.g., "Carrd page: headline + 3 pain bullets + 'Join Waitlist' button → Typeform with 2 questions"]

**Where traffic comes from**: [Specific source — not "social media." Name it: "post in 3 Reddit subs: r/freelance, r/msp, r/consulting"]

**Success threshold**: [The exact number that means "proceed" — e.g., "10 email signups in 72 hours OR 3 paid reservations"]

**Kill threshold**: [The number that means "pivot or kill" — e.g., "< 5 signups after 500 visitors = wrong ICP or wrong pain"]

**Timeline**: When you'll have signal. Maximum 7 days. If it takes longer, the test is too complex.

---

Don't ask for more information than you need. If the brief has the ICP and the pain, design the test now.
