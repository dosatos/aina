# Software Engineers Landing Page Variants

**Created:** February 18, 2026
**Status:** Ready for Phase 0 A/B testing
**Target:** IC Engineers, Engineering Managers, Data Scientists (25-40)

---

## Quick Reference

| Variant | Hook | Psychology | Best For | Predicted CTR | Predicted Quality |
|---------|------|-----------|----------|---------------|-------------------|
| **Control** | Trust gap | Balanced | Baseline | Medium | Medium |
| **Variant A** | Social threat | Loss + ego | Cold traffic, high performers | **HIGHEST** | Good |
| **Variant B** | Career growth | Gain + ambition | Warm traffic, growth-focused | Medium | **HIGH** |
| **Variant C** | System debug | Analytical | Senior engineers, tool-driven | Lower | **HIGHEST** |

---

## Files in This Directory

### Core Strategy
- **`TEST-STRATEGY.md`** - Overall A/B testing approach, metrics, kill zones, launch plan

### Landing Page Variants
- **`control.md`** - Baseline variant (trust gap framing)
- **`variant-a-social-threat.md`** - Highest CTR expected (ego + trust risk)
- **`variant-b-career-acceleration.md`** - Growth-focused (positive framing)
- **`variant-c-engineer-brain.md`** - Highest quality expected (debugger mindset)

---

## Phase 0 Testing Recommendation

### Week 1: Control vs Variant A
**Why:** Establish baseline and test highest-leverage psychological hook

**Setup:**
- LinkedIn ads → Software Engineers, 25-40, tech hubs
- $500 budget ($250 per variant)
- 3-5 days or 500 visitors per variant

**Primary Metric:** Completion rate (>50% = language-market fit)

**Decision:**
- If Variant A wins by >15%: Scale Variant A to $2K
- If Control wins or tie: Test Control vs Variant B/C

---

### Week 2: Winner vs Next Variant
**Why:** Find best-performing variant before scaling

**Setup:**
- Winner from Week 1 vs Variant B or C
- $500 budget
- Same audience

**Decision:**
- Identify champion variant
- Scale to $2K+ budget if >50% completion achieved

---

## Success Criteria (Phase 0)

✅ **>50% completion rate** = language-market fit validated
✅ **>2 min time on page** = reading, not bouncing
✅ **>60% scroll to "How It Works"** = engaged
✅ **>5% upgrade rate** = value perceived (bonus, not required)

**If 3-4 hit:** Build the product. PMF signal confirmed.
**If 1-2 hit:** Iterate messaging.
**If 0 hit:** Wrong audience or value prop.

---

## Variant Details

### Control: Trust Gap Framing
**Header:** "Why Your Team Trusts You Less Than You Think"
**Hook:** Perception mismatch between self-view and team experience
**Tone:** Balanced emotional + analytical
**Best for:** Establishing baseline, broad appeal

**Key strengths:**
- Relatable weekly scenarios (Monday/Thursday/Friday)
- Dual emotional track (frustrated + ambitious)
- Clear time promise + social proof
- Invisible wall metaphor

---

### Variant A: Social Threat Hook
**Header:** "Why Your Team Trusts You Less Than You Think"
**Hook:** Loss aversion + ego gap + status anxiety
**Tone:** Threat-focused, emotional urgency
**Best for:** Cold traffic, high performers who care about perception

**Key strengths:**
- **Strongest psychological trigger** (trust gap + exclusion)
- Specific loss framing ("discussions happen without you")
- Front-loads social threat
- Likely **highest CTR**

**Risk:** May alienate confident engineers who don't feel threatened

---

### Variant B: Career Acceleration Hook
**Header:** "The Fastest Way to Find What's Slowing Your Engineering Career"
**Hook:** Gain framing + forward momentum + ambition
**Tone:** Positive, growth-oriented, aspirational
**Best for:** Warm traffic, referrals, growth-minded engineers

**Key strengths:**
- Less threatening than Variant A
- Appeals to ambitious high performers
- Focuses on unlocking potential (not fixing problems)
- Likely **highest quality traffic**

**Risk:** May not create enough urgency for immediate action

---

### Variant C: Engineer Brain Hook
**Header:** "You're Debugging Production. But Not Yourself."
**Hook:** System optimization + debugger mindset + instrumentation gap
**Tone:** Technical, analytical, tool-framed
**Best for:** Senior engineers, staff+, systems thinkers

**Key strengths:**
- Speaks directly to debugger mindset
- Code blocks throughout (visual credibility)
- Anti-fluff positioning ("Not astrology")
- Likely **highest completion rate among converters**

**Risk:** Narrower appeal, may be too technical for some

---

## Conversion Kill Zones (All Variants)

### #1 Above the fold hesitation (0-5 sec)
**Symptoms:** High bounce, low scroll start
**Fix:** Clear time promise, audience label, social proof visible

### #2 Mid-pain fatigue (30-55% scroll)
**Symptoms:** >25% drop in scroll depth
**Fix:** Pattern interrupt ("Quick check:" callout)

### #3 Technical overload spike (code blocks)
**Symptoms:** Scroll bounce at examples
**Fix:** Soft reassurance ("Here's a simplified example...")

### #4 Pricing hesitation ($49 reveal)
**Symptoms:** Drop after seeing price
**Fix:** "Most users start free" messaging

### #5 Post-CTA drift (below primary action)
**Symptoms:** Attention leak to secondary content
**Fix:** Developer features in collapsed section

---

## Ad Copy Recommendations

### For Variant A (Social Threat)
> "Your team trusts you less than you think. 10-min assessment for engineers."

### For Variant B (Career Acceleration)
> "Find what's slowing your engineering career. Free 10-min assessment."

### For Variant C (Engineer Brain)
> "Debug yourself. Behavioral telemetry for engineers."

---

## Analytics Setup Required

**Before launching, set up tracking for:**

1. **Primary metrics:**
   - Hero CTA click rate
   - Assessment start rate
   - Assessment completion rate
   - Free → paid conversion rate

2. **Diagnostic metrics:**
   - Scroll depth histogram
   - Time to first scroll
   - Rage clicks near hero
   - CTA hover rate

3. **Qualitative feedback:**
   - Survey completers: "What almost stopped you?"
   - Ask: "Where did you first hear about this?"
   - If upgrade: "What made you decide to pay?"

---

## Next Actions

**Immediate (before launching):**
1. ✅ Variants created (done)
2. ⏳ Build control landing page (HTML/React)
3. ⏳ Set up conversion tracking (Plausible/PostHog/Mixpanel)
4. ⏳ Create LinkedIn ad account + campaigns
5. ⏳ Prepare A/B testing infrastructure

**Week 1:**
- Launch Control vs Variant A
- $500 budget test
- Monitor completion rate daily
- Collect qualitative feedback

**Week 2:**
- Analyze results
- Launch winner vs next variant
- Iterate based on data

---

## Expected Outcomes (Predictions)

**If targeting is correct:**

**Variant A:** 45-60% completion, highest CTR, good quality
**Variant B:** 40-55% completion, medium CTR, high quality
**Variant C:** 55-70% completion, lower CTR, highest quality
**Control:** 40-50% completion, medium CTR, medium quality

**Key insight:** Variant A likely brings most volume, Variant C brings best fit.

**Recommendation:** Test A first for volume validation, then C for quality validation.

---

## Contact & Iteration

As results come in, iterate based on:

1. **Quantitative signals:** Completion rate, scroll depth, time on page
2. **Qualitative signals:** User feedback, survey responses
3. **Behavioral patterns:** Where users drop off, what they click

Update this README with:
- Actual performance data
- Winning variant identification
- Iteration recommendations

---

**Last updated:** February 18, 2026
**Status:** Ready for Phase 0 deployment
