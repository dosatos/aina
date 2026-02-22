# Hero Section A/B Test Variants

**Created:** February 21, 2026
**Purpose:** High-conversion hero sections optimized for different psychological triggers
**Source:** Conversion audit feedback

---

## Testing Strategy

**Recommended sequence:**
1. Start with Variant A (safest, highest baseline conversion)
2. Test Variant B vs A (emotional pull vs authority)
3. Use Variant C for engineer-specific campaigns

**Key metrics:**
- Conversion rate (assessment starts)
- Bounce rate
- Time on page
- Scroll depth

---

## Variant A — Diagnostic Authority (BASELINE)

**Best for:** Cold traffic, analytical users, engineers
**Goal:** Brutal clarity + credibility
**Risk level:** Low (safest option)

### Header

```html
<header class="border-b border-dark-border py-3 md:py-4 sticky top-0 bg-dark-bg/95 backdrop-blur-sm z-50">
  <div class="max-w-5xl mx-auto px-6">
    <div class="flex items-center justify-between">
      <div>
        <h1 class="text-xl md:text-2xl font-bold text-white">
          10-Minute Career Diagnosis
        </h1>
        <p class="text-sm text-slate-400 font-mono mt-1">
          For Analytical Professionals
        </p>
      </div>
      <div class="text-sm md:text-base text-slate-400 font-mono">
        Free · No signup
      </div>
    </div>
  </div>
</header>
```

### Hero

```html
<div class="mb-12">
  <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight mb-6">
    Find Out Why You Feel Stuck
  </h2>
  <p class="text-xl md:text-2xl text-slate-300 leading-relaxed mb-6">
    Using validated behavioral data, not guesswork.
  </p>
  <div class="text-sm text-slate-400 font-mono">
    Built on Big Five (IPIP) + O*NET Holland Codes
  </div>
</div>
```

### CTA

```html
<a href="#assessment" class="inline-block bg-neon-cyan hover:bg-neon-cyan/90 text-dark-bg text-xl md:text-2xl font-bold px-12 py-6 transition-all neon-cyan-strong">
  See Why I'm Stuck
</a>
<div class="mt-8 text-slate-400 font-mono">
  <p class="mb-2">Free · No signup · Instant results</p>
  <p class="text-sm text-slate-500">10 minutes · Validated psychometrics</p>
</div>
```

**Why this converts:**
- ✅ Instantly clear what the product is
- ✅ Strong "diagnosis" positioning
- ✅ Removes test anxiety
- ✅ Speaks to rational users
- ✅ Credibility signals prominent

**Expected performance:** Solid baseline, safe for all traffic sources

---

## Variant B — Pain-First (HIGH EMOTIONAL PULL)

**Best for:** Frustrated professionals, LinkedIn traffic, warm audiences
**Goal:** Emotional resonance + self-recognition
**Risk level:** Medium (polarizing but can outperform)

### Header

```html
<header class="border-b border-dark-border py-3 md:py-4 sticky top-0 bg-dark-bg/95 backdrop-blur-sm z-50">
  <div class="max-w-5xl mx-auto px-6">
    <div class="flex items-center justify-between">
      <div>
        <h1 class="text-xl md:text-2xl font-bold text-white">
          Career Fit Diagnosis
        </h1>
      </div>
      <div class="text-sm md:text-base text-slate-400 font-mono">
        Free · 10 minutes
      </div>
    </div>
  </div>
</header>
```

### Hero

```html
<div class="mb-12">
  <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight mb-6">
    You're Not Lazy.<br>
    You're Probably in the Wrong Role.
  </h2>
  <p class="text-xl md:text-2xl text-slate-300 leading-relaxed">
    This 10-minute behavioral assessment shows where the mismatch really is.
  </p>
</div>
```

### CTA

```html
<a href="#assessment" class="inline-block bg-neon-cyan hover:bg-neon-cyan/90 text-dark-bg text-xl md:text-2xl font-bold px-12 py-6 transition-all neon-cyan-strong">
  Diagnose My Career Fit
</a>
<div class="mt-8 text-slate-400 font-mono">
  <p class="mb-2">Free · No signup · Results in 10 minutes</p>
</div>
```

**Why this converts:**
- ✅ Pattern interrupt (scroll-stopping power)
- ✅ Removes self-blame (emotional relief)
- ✅ Creates immediate curiosity
- ✅ High resonance with burned-out professionals

**Expected performance:** Can outperform Variant A with warm/frustrated audiences, may underperform with skeptical/cold traffic

---

## Variant C — Overthinker Hook (VERY TARGETED)

**Best for:** Engineers, product people, high-analysis personalities
**Goal:** Deep ICP resonance
**Risk level:** Medium-High (narrow but sharp)

### Header

```html
<header class="border-b border-dark-border py-3 md:py-4 sticky top-0 bg-dark-bg/95 backdrop-blur-sm z-50">
  <div class="max-w-5xl mx-auto px-6">
    <div class="flex items-center justify-between">
      <div>
        <h1 class="text-xl md:text-2xl font-bold text-white">
          Career Diagnosis Tool
        </h1>
        <p class="text-sm text-slate-400 font-mono mt-1">
          For overthinkers
        </p>
      </div>
      <div class="text-sm md:text-base text-slate-400 font-mono">
        10 min · Free
      </div>
    </div>
  </div>
</header>
```

### Hero

```html
<div class="mb-12">
  <h2 class="text-4xl md:text-6xl font-bold text-white leading-tight mb-6">
    Still Overthinking Your Career Direction?
  </h2>
  <p class="text-xl md:text-2xl text-slate-300 leading-relaxed">
    Run a 10-minute behavioral diagnosis and see what actually fits you.
  </p>
  <div class="text-sm text-slate-400 font-mono mt-6">
    Based on Big Five + Holland Codes
  </div>
</div>
```

### CTA

```html
<a href="#assessment" class="inline-block bg-neon-cyan hover:bg-neon-cyan/90 text-dark-bg text-xl md:text-2xl font-bold px-12 py-6 transition-all neon-cyan-strong">
  Run the Diagnosis
</a>
<div class="mt-8 text-slate-400 font-mono">
  <p class="mb-2">Free · No signup</p>
</div>
```

**Why this converts:**
- ✅ Mirrors internal monologue (immediate recognition)
- ✅ Attracts analytical minds specifically
- ✅ Feels tool-like, not fluffy
- ✅ Strong ICP filtering (reduces wrong traffic)

**Expected performance:** Lower volume but higher quality conversions; best for engineer-heavy channels (HN, r/ExperiencedDevs)

---

## Micro-Optimizations (Apply to All Variants)

**MUST DO:**
- ✅ Make "10-minute" visually prominent (not buried)
- ✅ Make "Free · No signup" directly under CTA (reduces anxiety)
- ✅ Ensure CTA is above the fold on laptop (1280px+ screens)
- ✅ Add subtle trust line near button ("Built on validated psychometrics" or "Based on Big Five")

**OPTIONAL (High Impact):**
- Progress indicator on CTA button hover ("10 minutes → instant results")
- Social proof near CTA if available ("Used by 2,000+ professionals")
- Exit-intent popup with simplified hook if bounce rate > 60%

---

## Testing Plan

### Phase 1: Establish Baseline (Week 1-2)
- Run Variant A for 100-200 visitors
- Track: conversion rate, bounce rate, scroll depth, time on page
- Set baseline metrics

### Phase 2: Test Emotional Pull (Week 3-4)
- A/B test: Variant A vs Variant B
- Split traffic 50/50
- Hypothesis: Variant B will convert frustrated professionals better but may have higher bounce from cold traffic

### Phase 3: Test Engineer Hook (Week 5-6, optional)
- Only if traffic source is engineer-heavy (HN, Reddit r/ExperiencedDevs)
- A/B test: Variant A vs Variant C
- Hypothesis: Variant C will have lower volume but higher completion rate

### Success Metrics by Variant

| Metric | Variant A Target | Variant B Target | Variant C Target |
|--------|------------------|------------------|------------------|
| Conversion rate | 2-3% | 2.5-4% | 3-5% |
| Bounce rate | <65% | <60% | <55% |
| Avg time on page | >90s | >120s | >150s |
| Assessment completion | >70% | >75% | >80% |

---

## Red Flags to Watch

**If Variant A underperforms (<1.5% conversion):**
- Hero headline too generic
- CTA not compelling enough
- Trust layer still too thin

**If Variant B underperforms vs A:**
- Pain hook too strong (alienating)
- Traffic too cold for emotional approach
- Wrong audience (engineers prefer Variant A/C)

**If Variant C underperforms vs A:**
- Too narrow (not enough overthinkers)
- Traffic source mismatch
- "Overthinking" framing feels negative

---

## Quick Swap Guide

All variants share same pain section + how it works section.

**To swap variants:**
1. Replace header (lines 112-125 in index.html)
2. Replace hero headline/subhead (lines 134-150)
3. Replace CTA button text + proof strip (lines 316-327)
4. Test on mobile + desktop
5. Deploy

**Time to swap:** 5 minutes

---

## Current Status

- ✅ Variant A documented
- ✅ Variant B documented
- ✅ Variant C documented
- [ ] Variant A implemented (next step)
- [ ] Testing plan executed
- [ ] Winner identified
