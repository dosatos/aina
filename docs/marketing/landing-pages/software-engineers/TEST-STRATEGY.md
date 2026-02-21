# A/B Test Strategy: Software Engineers Landing Page

**Created:** February 18, 2026
**Status:** Ready for Phase 0 testing
**Target:** IC Engineers, Engineering Managers, Data Scientists (age 25-40)

---

## Funnel Hypothesis

> Engineers convert when they feel a hidden career risk they can't debug.

**Core insight:** Not selling self-help. Selling missing instrumentation for career navigation.

---

## Test Strategy

We test **three psychological entry points**:

| Variant | Psychology | Best For | Predicted Performance |
|---------|-----------|----------|----------------------|
| **Control** | Trust gap | Cold traffic, balanced | Baseline |
| **Variant A** | Social threat (ego + trust risk) | Cold traffic, high performers | **Highest CTR** |
| **Variant B** | Career growth (ambition) | Warm traffic, growth-focused | Medium CTR, good quality |
| **Variant C** | System optimization (analytical) | Senior engineers, tool-driven | Lower CTR, **highest quality** |

---

## What We're Actually Testing

**NOT:** Random creativity

**YES:** Key psychological levers
- Threat vs curiosity
- Career pain vs performance optimization
- Emotional vs analytical entry
- Speed reassurance vs depth promise

---

## Primary Metrics

**Success Metric (Phase 0):**
- ✅ >50% completion rate = language-market fit validated

**Funnel Metrics:**
1. Hero CTR (click CTA above fold)
2. Assessment start rate
3. Assessment completion (end-to-end)
4. Free → paid conversion (bonus, not required Phase 0)

**Diagnostic Metrics:**
- Scroll depth histogram
- Time to first scroll
- Rage clicks near hero
- CTA hover rate

---

## Kill Zones (Where Conversions Die)

### Kill Zone #1: Above the fold hesitation (0-5 seconds)
**Symptoms:** High bounce, low scroll start, low CTA hover
**Fix:** Clear time promise, audience label, social proof above fold

### Kill Zone #2: Mid-pain fatigue (30-55% scroll)
**Symptoms:** >25% drop in scroll depth
**Fix:** Pattern interrupt ("Quick check:" callout)

### Kill Zone #3: Technical overload spike (code block section)
**Symptoms:** Scroll bounce at code examples
**Fix:** Soft reassurance before code ("Here's a simplified example...")

### Kill Zone #4: Pricing hesitation ($49 reveal)
**Symptoms:** Drop after seeing price
**Fix:** "Most users start free. Upgrade only if insights resonate."

### Kill Zone #5: Post-CTA drift (below primary action)
**Symptoms:** Attention leak to secondary content
**Fix:** Keep developer features collapsed, repeat CTA if needed

---

## Launch Plan

### Week 1: Control vs Variant A
- **Traffic:** LinkedIn ads → Software Engineers 25-40, tech hubs
- **Budget:** $500 test ($250 per variant)
- **Duration:** 3-5 days or 500 visitors per variant
- **Decision:** If >50% completion, scale winner to $2K

### Week 2: Winner vs Variant B/C
- **Traffic:** Same source
- **Budget:** $500 ($250 winner, $250 new variant)
- **Decision:** Identify best-performing variant for scale

---

## Traffic Source

**Primary:** LinkedIn Ads
- Target: Software Engineer, Engineering Manager, Data Scientist
- Age: 25-40
- Location: SF Bay Area, Seattle, NYC, Austin, Denver
- Seniority: Senior IC, Staff, Engineering Manager

**Ad copy examples:**
- Variant A: "Your team trusts you less than you think. 10-min assessment for engineers."
- Variant B: "Find what's slowing your engineering career. Free 10-min assessment."
- Variant C: "Debug yourself. Behavioral telemetry for engineers."

---

## Success Criteria (Phase 0)

**Primary Goal:** Validate language-market fit

✅ **>50% completion rate** = messaging resonates
✅ **>2 min time on page** = reading, not bouncing
✅ **>60% scroll to "How It Works"** = engaged
✅ **>5% upgrade rate** = value perceived (bonus)

**If 3-4 hit:** Build the product. You have PMF signal.
**If 1-2 hit:** Iterate messaging, test again.
**If 0 hit:** Wrong audience or wrong value prop.

---

## Prediction (Based on Similar Funnels)

**Variant A (Social Threat):** Likely highest CTR, good completion
**Variant C (Engineer Brain):** Likely highest quality users, lower CTR
**Control:** Mid-pack on both metrics

**Recommendation:** Start with Control vs Variant A to establish baseline and test highest-leverage psychological hook.

---

## Post-Launch Analysis

After 500 completions, analyze:

1. **Quantitative:**
   - Completion rate by variant
   - Time on page distribution
   - Scroll depth heatmap
   - Drop-off points

2. **Qualitative:**
   - Survey completers: "What almost stopped you from finishing?"
   - Record: "Where did you first hear about this?"
   - Ask: "What made you decide to upgrade?" (if applicable)

---

## Iteration Triggers

**If completion <30%:**
- Problem: Language-market fit not there
- Action: Test broader audience or change pain framing

**If completion 30-49%:**
- Problem: Close but not resonating fully
- Action: Iterate header, test Variant B/C

**If completion >50%:**
- Success: Language-market fit validated
- Action: Scale budget, optimize for conversion rate

**If upgrade <3%:**
- Problem: Free tier gives too much OR price anchor wrong
- Action: Test $29 tier, adjust free/paid boundary

**If upgrade >10%:**
- Success: Value proposition clear
- Action: Consider testing $69 tier for expansion revenue

---

## Files in This Directory

- `TEST-STRATEGY.md` (this file) - Overall A/B test approach
- `control.md` - Baseline variant (trust gap framing)
- `variant-a-social-threat.md` - Ego + trust risk hook
- `variant-b-career-acceleration.md` - Ambition + growth hook
- `variant-c-engineer-brain.md` - System optimization hook

---

## Next Action

**Immediate:**
1. Build control landing page
2. Set up conversion tracking (Plausible/PostHog/Mixpanel)
3. Create LinkedIn ad account + campaigns
4. Launch Control vs Variant A with $500 budget

**Week 1 Goal:** Determine which psychological hook drives highest completion rate.
