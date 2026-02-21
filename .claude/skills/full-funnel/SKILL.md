---
description: >
  Invoke this skill when the user asks why their funnel isn't working, asks for a diagnosis,
  shares performance metrics, or describes a conversion problem without knowing where it's broken.
  Triggers: "my funnel isn't converting", "we're spending money but not getting leads",
  "what's wrong with my funnel", "help me diagnose this", user shares CTR / CVR / CPA numbers,
  "why aren't my ads working".
argument-hint: Share your metrics: ad CTR, LP conversion rate, lead-to-close rate, monthly ad spend
allowed-tools: Read, WebFetch, WebSearch
---

# Full-Funnel Diagnosis Skill

Map the funnel from channel to conversion. Find the first broken link. Fix that — don't touch anything downstream until the first link is healthy.

## Process

1. **Read `project/product-brief.md`** for context (offer, ICP, channel in use, price point).
2. **Map the funnel** from whatever the user shares:
   - Channel → Ad → LP → Conversion event → (downstream: demo / email / purchase)
3. **Apply metric thresholds** from `funnel-frameworks.md` to identify where the funnel breaks.
4. **Find the first broken link** — the earliest stage that is below threshold.
5. **Output diagnosis + one fix**. Refuse to diagnose downstream stages until the upstream break is fixed.

## Diagnosis Framework

Work top-down through these stages:

**Stage 1: Ad (channel)**
- Is CTR above threshold for this channel type?
- If CTR is broken: the problem is the creative or the targeting. LP doesn't matter yet.

**Stage 2: Landing Page**
- Is LP conversion above 2% (cold traffic)?
- If LP conversion is broken but CTR is fine: the problem is the LP. Don't touch ad spend.

**Stage 3: Lead Quality / Funnel Middle**
- Are leads converting to demos / trials / purchases?
- If lead quality is broken: could be ICP mismatch in targeting, or offer mismatch on LP.

**Stage 4: Close**
- If close rate is low: pricing, objection handling, or wrong ICP reaching this stage.

## Output Format

**Funnel map**:
[Channel] → [Ad CTR] → [LP CVR] → [Conversion event] → [Downstream rate if known]

**Diagnosis**: The funnel breaks at [Stage]. [One sentence on what the data says.]

**Root cause**: [Most likely reason — be direct, not diplomatic. "Your headline is generic" not "there may be an opportunity to improve clarity".]

**The fix**: [One specific action. Not "improve your copy" — "Rewrite the headline to name the specific pain instead of the product category."]

**What NOT to do**: [The tempting wrong move — e.g., "Don't increase budget. You're paying more to send people to a broken page."]

**After this fix**: [What metric to watch and what threshold means it's working.]

If the user hasn't shared metrics, ask for the two numbers you need most (start with ad CTR and LP conversion rate) before diagnosing. Don't guess.
