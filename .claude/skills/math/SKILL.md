---
description: >
  Invoke this skill when the user needs to sanity-check pricing, calculate unit economics (LTV vs CAC),
  understand what scale is required to hit a revenue target, or asks if the business math works.
  Triggers: "does the pricing make sense", "how many users do I need", "is $X/mo realistic",
  "what do I need to charge to make $Y", "can I make money at this price", "is this viable",
  "my CAC is $X", user shares pricing or revenue numbers or ad spend.
argument-hint: Price point, revenue target, CAC, churn rate, or revenue numbers
allowed-tools: Read, WebFetch, WebSearch
---

# Math — Economics & Pricing Sanity Check

If the math doesn't work on paper, it won't work in the market. Run this before setting a price, before running ads, and before celebrating early traction.

This skill handles two types of checks:
1. **Forward math**: Revenue target → customers needed → is that realistic?
2. **Backward math**: LTV vs CAC → is this profitable?

## The Core Questions

**Revenue target → required users:**
How many paying customers do you need at this price to hit your monthly target?

**Users → required market:**
Is that number realistic for this niche? (A niche with 1,000 people can support 100 customers. A niche with 10 people cannot.)

**Price → required value:**
Does your price match the value delivered? Rule of thumb: charge 10% of the value you create. If you save someone $5k/mo, $500/mo is defensible.

**LTV vs CAC:**
Lifetime Value must exceed Customer Acquisition Cost by at least 3x. If CAC > LTV, you're paying to lose money.

**Payback period:**
How long until a customer pays back their acquisition cost? < 3 months is healthy. > 12 months is dangerous.

## The Quick Math

Show work in plain numbers. No formulas. No variables. Just: "At $49/mo, you need X customers to make $Y."

**Standard targets for reference:**
- "Ramen profitable" (one person, cheap city): ~$3,000–5,000/mo
- "Real salary" (one person, comfortable): ~$8,000–12,000/mo
- "Small team" (2–3 people): ~$30,000–50,000/mo

## Process

1. **Read `project/product-brief.md`** for price point, offer type, revenue target.
2. **Determine which check to run**:
   - If user asks about scale/customers needed → run forward math
   - If user shares CAC/revenue numbers → run LTV:CAC check
   - If unclear → run both
3. **Show the work** in plain numbers. No formulas. No variables.
4. **Give verdict + one lever to pull** if numbers don't work.

## Output Format

Choose one or both sections based on what the user needs:

### Forward Math (Revenue Target → Customers Needed)

**At $[price]/mo:**
- Monthly revenue target: $[X]
- Customers needed: [X ÷ price]
- Annual churn assumption: [X]% → you need to acquire [Y] new customers/mo just to stay flat

**Reality check**: [Is this user count realistic? How big is the addressable market? What % conversion rate does it require from your total ICP?]

**The pricing trap for this offer type**: [One specific mistake — e.g., "Charging $9/mo for a B2B tool signals low value. B2B buyers expect $50–500/mo. Low price creates distrust, not conversion."]

---

### Backward Math (LTV vs CAC)

**The math:**
- Price: $[X]/mo (or one-time $[X])
- Estimated churn: [X]%/mo → avg lifespan [Y] months
- **LTV**: $[price × lifespan]
- Estimated CAC: $[Z] (based on [channel benchmark or actual data])
- **Payback period**: [CAC ÷ monthly price] months
- **LTV:CAC ratio**: [LTV ÷ CAC]:1

**Verdict**:
- < 1:1 = STOP. You're paying to lose money.
- 1:1–3:1 = WARNING. Break-even or marginal.
- 3:1+ = PASS. Healthy unit economics.
- 5:1+ = You're leaving money on the table.

**If WARNING or STOP — pick one lever** (not all three):
- Raise price to $[X] → LTV:CAC becomes [ratio]
- Cut CAC by switching to [channel] where benchmarks suggest $[lower CAC]
- Reduce churn: one extra month of retention moves LTV from $[X] to $[Y]

---

**The recommendation**: [One number or one lever to pull — the price you should test first, the channel to switch to, or the retention fix]

**Early-stage check**: If you have < 10 paying customers, don't optimize unit economics yet — get to 10 first. [Flag if applicable.]

Don't hedge on the recommendation. Pick a number or action.
