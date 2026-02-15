# Methodology & Quality Analysis

This document provides the analytical foundation for the compiled question set, including:
- Optional enhancement frameworks from each AI source
- Complete deduplication notes showing what was eliminated and why
- Quality assessment matrix rating all 90 original questions

---

## OPTIONAL ENHANCEMENTS

Methodological frameworks from the three source documents that can enhance insight generation and assessment quality.

---

### 1. Cross-Layer Insight Generation Framework (ANT Methodology)

The Anthropic source included a framework for generating insights by combining Layer 1 (behavioral) and Layer 3 (risk/decision) responses.

**Core Principle:** The most valuable insights emerge from cross-layer pattern combinations, not individual dimensions in isolation.

#### Example Insight Patterns

**Pattern 1: Decisive but Protective**
- **Conditions:** High assertiveness (Q1-A, Q2-A) + Loss-averse (Q22-B)
- **Insight:** *"You're decisive in meetings but protective of what you've built — you push hard on new ideas but struggle to let go of existing ones"*
- **Actionable Guidance:** *"When evaluating whether to continue a project, explicitly separate past investment from future value. Ask: 'If I were starting fresh today, would I begin this?'"*

**Pattern 2: Fast Pattern-Matcher in Familiar Territory**
- **Conditions:** Fast pace (Q4-A, Q5-high) + Intuitive decision-maker (Q20-B, Q21-A)
- **Insight:** *"You trust your pattern recognition and move quickly — this is a superpower until you're in unfamiliar territory where your patterns don't apply"*
- **Actionable Guidance:** *"In new domains, deliberately slow down. Your speed advantage works when patterns are valid; force yourself to gather data in unfamiliar contexts."*

**Pattern 3: Relationship-Driven Commitment**
- **Conditions:** Relationship-oriented (Q7-B, Q8-B) + Sunk-cost susceptible (Q13-A, Q14-A)
- **Insight:** *"You invest deeply in people and projects, which builds loyalty — but you may hold on to underperforming initiatives because of the human investment, not the business case"*
- **Actionable Guidance:** *"When evaluating whether to continue a people investment (hiring, partnerships, mentoring), explicitly distinguish between relationship value and business value. Both matter, but they're different."*

**Pattern 4: Structured Risk-Taker**
- **Conditions:** High structure preference (Q10-B, Q11-high) + Financial risk-seeking (Q16-A, Q17-A)
- **Insight:** *"You take calculated financial risks but prefer them within structured frameworks — you're comfortable with uncertainty in outcomes, not in process"*
- **Actionable Guidance:** *"Your sweet spot is high-risk ventures with clear plans. Build detailed roadmaps for risky initiatives to channel your structured thinking into bold moves."*

**Pattern 5: Task-Focused but Analysis-Paralyzed**
- **Conditions:** Task-oriented (Q7-A, Q8-A) + Analytical decision-maker (Q20-A, Q21-B)
- **Insight:** *"You prioritize outcomes over relationships and trust data over intuition — but this can slow you down when perfect data doesn't exist"*
- **Actionable Guidance:** *"Set decision deadlines for yourself. When data quality plateaus, shift to 'good enough' mode and move forward. Your execution focus will compensate for imperfect inputs."*

**Pattern 6: Confident Fast-Mover with Blind Spots**
- **Conditions:** Fast pace (Q4-A) + Intuitive (Q21-A) + High confidence calibration (Q26-Q27 > 8)
- **Insight:** *"You move quickly with strong conviction — this works brilliantly when you're right, but overconfidence in ambiguous situations can amplify mistakes"*
- **Actionable Guidance:** *"Before committing to high-stakes decisions, do a 'pre-mortem': Assume the decision failed. What would have gone wrong? This forces you to examine blind spots."*

#### Implementation Guide for Cross-Layer Insights

**Step 1: Identify Dominant Patterns**
- Score Layer 1 dimensions (0-100 scale)
- Flag Layer 3 biases (binary flags)
- Identify "extreme" scores (>75 or <25 on Layer 1, 3/3 flags on same bias in Layer 3)

**Step 2: Detect Reinforcing vs. Contradictory Combinations**
- **Reinforcing:** Fast pace + intuitive + high confidence → Amplified pattern
- **Contradictory:** High assertiveness + low confidence → Internal tension to explore

**Step 3: Generate Contextualized Insights**
- Template: "[Layer 1 pattern] + [Layer 3 pattern] → [Implication] — [Actionable guidance]"
- Prioritize patterns with strongest signal (Tier 1 questions)
- Avoid generic insights that could apply to anyone

**Step 4: Validate with Confidence Calibration**
- If Q26-Q27 confidence is high (>8) on scenarios where user chose biased options → Flag overconfidence
- If confidence is low (<4) consistently → Flag chronic uncertainty/analysis paralysis

---

### 2. Cognitive Load Testing (GEM Methodology)

The Gemini source emphasized minimizing cognitive load to maximize completion rates and response quality.

#### Key Principles

**Minimize Reverse-Coded Items**
- **Rationale:** Reverse coding ("I do NOT prefer...") adds cognitive burden
- **This Compilation's Approach:** Eliminated most reverse-coded items (ANT Q3, Q12; GEM Q5, Q15; OPAI Q4, Q7, Q12)
- **Kept only when essential:** None in final set (all eliminated)

**Standardize Likert Anchors**
- **Problem:** Mixing "Never/Always" with "Disagree/Agree" with "Not like me/Like me" creates confusion
- **This Compilation's Approach:**
  - Frequency questions use: Never / Rarely / Sometimes / Often / Always
  - Self-description questions use: Not at all like me / Slightly like me / Moderately like me / Very much like me / Extremely like me
  - No agreement scales (Disagree/Agree) to avoid double negatives

**Limit Scenario Complexity**
- **Principle:** Each scenario should test ONE primary construct (no nested trade-offs)
- **Example of Good Complexity:** Q13 (internal tool) — tests sunk cost with clear alternatives
- **Example of Bad Complexity:** Avoided scenarios that mix sunk cost + team dynamics + financial + reputational risk simultaneously

**Completion Time Monitoring**
- **Recommendation:** Track median time per question type in pilot
  - Forced-choice: Target 15-20 seconds
  - Likert: Target 10-15 seconds
  - Simple scenario (2 options): Target 30-40 seconds
  - Complex scenario (4 options): Target 45-60 seconds
- **Total Target:** 12-15 minutes for 27 core questions

#### Post-Launch Optimization

**If median completion time exceeds 18 minutes:**
1. Identify slowest questions (>90 seconds median)
2. Simplify scenario complexity (reduce options from 4 to 3)
3. Shorten scenario text (aim for <100 words per scenario)
4. Consider removing lowest-signal questions from that construct

**If dropout rate exceeds 20%:**
1. Check where dropouts occur (early vs. late)
2. If early dropout: Reduce perceived time commitment (show progress bar, reduce total questions)
3. If late dropout: Fatigue setting in, remove questions from second half

---

### 3. Probabilistic Rigor (OPAI Methodology)

The OpenAI source demonstrated sophisticated probabilistic framing that enables detection of mathematical literacy vs. heuristic-driven decision-making.

#### Core Principles

**Explicit Expected Value Calculations**
- **Q16 Example:** 80% × $50K = $40K expected value vs. $38K guaranteed
- **Purpose:** Enables detection of whether respondents calculate EV or use heuristics
- **Analysis:** If choosing B despite higher EV in A → Risk aversion overcomes mathematical optimization

**Gain-Frame vs. Mixed-Frame Comparison**
- **Q16 (gain-only):** 80% gain $50K vs. guaranteed $38K
- **Q17 (mixed gain/loss):** 50% gain $120K / 50% lose $40K vs. guaranteed $35K
- **Prospect Theory Prediction:** People should be more risk-averse in Q16 (gain frame) than Q17 (mixed frame)
- **Analysis Pattern:**
  - Q16-B + Q17-A = Inconsistent risk preference (frame-dependent)
  - Q16-A + Q17-A = Consistent risk-seeking (EV maximizer)
  - Q16-B + Q17-B = Consistent risk-averse (certainty preference)

**Risk Capacity Controls**
- **Q17 includes:** "(Assume you can comfortably absorb the potential loss)"
- **Purpose:** Eliminates financial constraint confounds — tests pure risk preference, not risk capacity
- **Implementation:** Add similar controls to other risk questions if needed

#### Advanced Analysis: Risk Preference Mapping

**Identify Risk Profile Archetypes:**

1. **EV Maximizer** (Q16-A, Q17-A, Q18-B)
   - Calculates expected value and acts on it
   - Willing to accept variance for higher expected returns
   - Likely has mathematical/analytical background

2. **Certainty Seeker** (Q16-B, Q17-B, Q18-A)
   - Strong risk aversion across all frames
   - Prefers guaranteed outcomes even at lower expected value
   - May have lower risk capacity or high loss aversion

3. **Frame-Dependent** (Q16-B, Q17-A)
   - Risk aversion shifts based on framing (classic Prospect Theory pattern)
   - Susceptible to cognitive biases in risk assessment
   - Decisions may be inconsistent depending on how options are presented

4. **Sophisticated Risk Manager** (Q16-A, Q17-B, Q18-context-dependent)
   - Recognizes different risk contexts require different strategies
   - Takes risks in abstract scenarios, more cautious in career decisions
   - May indicate mature risk management philosophy

---

### 4. Post-Submission Reflection Prompt (GEM Suggestion)

**Optional Enhancement:** Add after final demographic question (Q32)

**Prompt:**
"What is one decision you made recently that you still think about?"
*(Optional – this helps us tune your insights)*

**Why Consider This:**
- Provides qualitative data for insight validation
- Low-pressure optional field reduces completion friction
- Enables detection of blind spots in quantitative assessment
- Can be analyzed with LLM to identify themes (regret, uncertainty, complexity)

**Implementation Decision:**
- **For MVP:** Optional (adds <1 min if used, <5 seconds if skipped)
- **Analysis Approach:** Use LLM to categorize responses into decision types (career, financial, strategic, interpersonal) and emotional valence (regret, pride, uncertainty)
- **Validation Use:** Compare reflection themes to Layer 3 bias flags (e.g., if someone flags sunk cost bias, do they mention a decision they "held onto too long"?)

**Sample Response Analysis:**

| Response | Category | Emotional Valence | Cross-Reference to Assessment |
|----------|----------|-------------------|------------------------------|
| "Stayed in a job too long despite red flags" | Career | Regret | Check sunk cost bias (Q13-15) |
| "Took a pay cut to join a startup" | Financial | Mixed | Check risk tolerance (Q16-18) |
| "Called out a bad decision in a meeting" | Interpersonal | Uncertain | Check assertiveness (Q1-3) |
| "Launched product before it was perfect" | Strategic | Pride | Check pace preference (Q4-6) |

---

---

## DEDUPLICATION NOTES

Complete accounting of all questions eliminated from the original 90 across three sources.

---

### High-Duplication Constructs (Consolidated)

#### ASSERTIVENESS (12 total → 3 selected)

**✅ KEPT:**
- **ANT Q1** (now Q1): Meeting facilitation — cleanest trade-off, no confounds
- **ANT Q2** (now Q2): Critical feedback delivery — tests peer-level assertiveness
- **OPAI Q3** (now Q3): Proactive leadership Likert — captures frequency patterns

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| ANT Q3 | Reverse-coded Likert | Adds cognitive load; "let others set agenda" is confusing phrasing |
| ANT Q4 | Negotiation scenario | Overlaps with risk tolerance questions (Q18, Q23) |
| GEM Q1 | Meeting facilitation with timeline stress | Similar to ANT Q1 but adds "timeline slip" confound (mixes assertiveness with urgency) |
| GEM Q6 | Senior leadership meeting | Too narrow context (not applicable to non-senior roles) |
| GEM Q14 | Deadline negotiation | Overlaps with people/task orientation (protecting team vs. stakeholder management) |
| OPAI Q1 | Cross-functional conflict | Similar to ANT Q1 but option A phrasing ("even if it creates tension") sounds more aggressive, less balanced |
| OPAI Q2 | Missed deadline by teammate | Adds conflict management confound (not pure assertiveness) |
| OPAI Q4 | Reverse-coded responsibility preference | Reverse coding adds cognitive load; also very similar to ANT Q3 |

---

#### PACE PREFERENCE (13 total → 3 selected)

**✅ KEPT:**
- **OPAI Q5** (now Q4): Launch vs. analyze — cleanest bias-toward-action trade-off
- **OPAI Q6** (now Q5): Energized by speed — captures emotional response, not just behavior
- **GEM Q2** (now Q6): Productivity rhythm (volume vs. depth) — orthogonal to strategic pace

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| ANT Q5 | Starting with unclear requirements | Similar to OPAI Q5 but "unclear requirements" framing is less universal |
| ANT Q6 | Push for faster timelines | Vague wording ("how often do you push") — unclear reference point |
| ANT Q7 | Action items after meeting | Too dependent on specific meeting culture (some orgs don't assign action items) |
| ANT Q8 | Feedback response (sit with it vs. act immediately) | Overlaps with emotional regulation, not pure pace preference |
| ANT Q9 | Good decision today vs. great next week | Too abstract/hypothetical; not grounded in specific scenario |
| GEM Q5 | Reverse-coded gut-call drain | Adds cognitive load; also tests stress tolerance as much as pace |
| GEM Q9 | Minor error correction in report | Overlaps with risk tolerance (reputational risk of small errors) |
| GEM Q13 | Version 0.1 vs. 1.0 polish | Similar to OPAI Q5 but less clean trade-off (overlaps with structure: "iterate vs. polish") |
| OPAI Q7 | Reverse-coded data gathering before decisions | Adds cognitive load; similar to OPAI Q5 but reversed |
| OPAI Q8 | Debate strategy (decide vs. explore alternatives) | Overlaps with assertiveness (pushing for decision) |

---

#### PEOPLE VS. TASK ORIENTATION (12 total → 3 selected)

**✅ KEPT:**
- **ANT Q10** (now Q7): Team behind schedule — high-stakes scenario forces genuine priority reveal
- **OPAI Q11** (now Q8): Feedback delivery style (clarity vs. emotional landing) — pure construct without confounds
- **OPAI Q10** (now Q9): 1:1 meeting depth — measures relational investment frequency

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| ANT Q11 | Disengaged performer response | Overlaps with leadership style (giving challenging work vs. emotional check-in) |
| ANT Q12 | Reverse-coded small talk at work events | Adds cognitive load; also tests introversion as much as task focus |
| ANT Q13 | Feedback to direct report (outcomes vs. feelings) | Similar to OPAI Q11 but more verbose; adds "how they're feeling about work" which is less clear |
| GEM Q3 | Underperforming teammate | Adds performance management confound (reviewing data vs. coffee chat mixes task focus with management philosophy) |
| GEM Q7 | Accuracy vs. morale in feedback | Similar to OPAI Q11 but adds ethical dimension ("accuracy" sounds objectively better) |
| GEM Q12 | Delivered product vs. high-performing team | Too binary/extreme; framed as mutually exclusive when both are possible |
| GEM Q15 | Reverse-coded frustration with small talk in meetings | Adds cognitive load; also very similar to ANT Q12 |
| OPAI Q9 | Project behind schedule | Similar to ANT Q10 but less balanced (option B "check on how team is feeling" sounds obviously better in modern management culture) |
| OPAI Q12 | Reverse-coded "results vs. harmony" | Extreme framing ("results matter MORE than harmony"); adds cognitive load |

---

#### STRUCTURE PREFERENCE (9 total → 3 selected)

**✅ KEPT:**
- **ANT Q15** (now Q10): Planning approach (rough direction vs. detailed roadmap) — highest signal for structure
- **GEM Q8** (now Q11): Systems creation capability — unique operationalization construct
- **ANT Q14** (now Q12): Empty calendar emotional response — reveals true preference via emotion

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| ANT Q16 | Frequency of creating written plans | Too similar to ANT Q15 (both about planning); less emotionally revealing |
| GEM Q4 | Work week start preference | Too low-stakes; easily influenced by role demands (some jobs require structured weeks) |
| GEM Q11 | Minimize surprises vs. maximize opportunity | Less actionable; also conflates structure with risk tolerance |
| OPAI Q13 | Work from plan vs. respond flexibly | Very similar to ANT Q15 but less specific about planning context |
| OPAI Q14 | Creative problem-solving (define constraints vs. explore freely) | Overlaps with pace preference (structured brainstorm vs. free exploration) |
| OPAI Q15 | Loosely vs. tightly scheduled day | Similar to ANT Q14 but less emotionally revealing (asks about preference, not feeling) |

---

### Moderate-Duplication Constructs (Best Version Selected)

#### HIRING DECISION (2 versions → 1 selected)

**✅ KEPT:**
- **OPAI Q20** (now Q20): Senior engineer with 4 options (stronger credentials vs. intuitive fit + process options)

**❌ ELIMINATED:**
- **GEM Q20:** Nearly identical scenario but less polished phrasing ("felt 'off' in culture interview" vs. OPAI's clearer "strong intuitive sense of long-term fit")

---

#### SUNK COST BIAS (6 scenarios → 3 selected)

**✅ KEPT:**
- **ANT Q17** (now Q13): Internal tool with detailed financial anchors ($30K, $500/month) — Tier 1 Essential
- **ANT Q19** (now Q14): Partnership investment (12 meetings, 6 months, CEO involved) — interpersonal sunk cost
- **OPAI Q23** (now Q15): Mentoring investment (1 year, no performance improvement) — people-focused

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| GEM Q16 | Side project ($50K, 6 months, competitor launches) | Less detailed financial framing than ANT Q17; also conflates sunk cost with competitive threat |
| GEM Q22 | Project 80% complete but lower ROI | Overlaps with professional incentives (bonus tied to completion) — not pure sunk cost |
| OPAI Q16 | Side project (5 months, lukewarm adoption) | Similar to GEM Q16 but weaker financial specifics; less clear trade-offs |

---

#### FINANCIAL RISK TOLERANCE (5 questions → 3 selected)

**✅ KEPT:**
- **OPAI Q24** (now Q16): Probabilistic gain 80/20 ($50K vs. $38K) — Tier 1 Essential, pure EV test
- **OPAI Q25** (now Q17): Mixed gain/loss 50/50 ($120K/-$40K vs. $35K) — Tier 1 Essential, loss frame test
- **ANT Q20** (now Q18): Salary vs. equity (3-4 year horizon, specific ranges) — real-world career decision

**❌ ELIMINATED:**

| Original ID | Reason for Elimination | Weakness vs. Kept Questions |
|-------------|------------------------|----------------------------|
| GEM Q18 | Stable vs. startup role ($200K vs. 50/50 equity upside) | Less detailed financial framing than ANT Q20 (lacks specific equity value ranges) |
| GEM Q21 | 80% gain $15K / 20% lose $10K | Mixed gain/loss complicates interpretation vs. OPAI Q24 (pure gain); also less clean EV calculation |

---

### Low-Duplication Constructs (Unique Questions Retained)

These questions had no or minimal overlap with others and were retained based on signal strength:

| Question ID | Construct | Uniqueness | Signal |
|-------------|-----------|------------|--------|
| **OPAI Q19** (now Q19) | Reputational risk (LinkedIn post) | Only pure reputational risk scenario across all sources | 9/10 ⭐ |
| **ANT Q23** (now Q21) | Analytical vs. intuitive (market entry) | Unique "smart people signal" framing | 9/10 |
| **OPAI Q21** (now Q22) | Loss aversion (side project exit) | Distinct from sunk cost (small loss vs. large investment) | 8/10 |
| **OPAI Q22** (now Q23) | Anchoring (salary negotiation) | Universally relatable, tests anchoring directly | 8/10 |
| **GEM Q24** (now Q24) | Overconfidence (mentor timeline) | Tests overconfidence via expert warning | 7/10 |
| **GEM Q25** (now Q25) | Emergency decision (hotfix vs. full fix) | Only time-pressure scenario with explicit risk numbers | 8/10 |
| **ANT Q18** (now Q26) | Confidence calibration after Q13 | Strategic positioning after complex scenario | 8/10 |
| **ANT Q24** (now Q27) | Confidence calibration after Q21 | Enables cross-domain confidence comparison | 8/10 |

---

---

## QUALITY ASSESSMENT MATRIX

Complete evaluation of all 90 original questions from ANT, GEM, and OPAI sources.

**Rating Scale:**
- **Signal Strength:** 1-10 (how effectively does this reveal the target construct?)
- **Duplication Risk:** Low / Medium / High
- **Recommendation:** KEEP (included in final set) / OMIT (eliminated)

---

### LAYER 1: BEHAVIORAL DYNAMICS

#### Assertiveness Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q1 | Assertiveness | 9/10 | Medium | **KEEP (Q1)** | Cleanest meeting facilitation trade-off |
| ANT Q2 | Assertiveness | 8/10 | Medium | **KEEP (Q2)** | Tests peer-level assertiveness |
| ANT Q3 | Assertiveness (reverse) | 6/10 | High | OMIT | Reverse coding adds cognitive load |
| ANT Q4 | Assertiveness | 7/10 | High | OMIT | Overlaps with risk tolerance questions |
| GEM Q1 | Assertiveness | 7/10 | High | OMIT | Similar to ANT Q1, adds stress confound |
| GEM Q6 | Assertiveness | 6/10 | Medium | OMIT | Too narrow (senior leadership only) |
| GEM Q14 | Assertiveness | 6/10 | High | OMIT | Overlaps with people/task orientation |
| OPAI Q1 | Assertiveness | 7/10 | High | OMIT | Less balanced phrasing than ANT Q1 |
| OPAI Q2 | Assertiveness | 6/10 | High | OMIT | Adds conflict management confound |
| OPAI Q3 | Assertiveness | 7/10 | Medium | **KEEP (Q3)** | Likert format captures frequency |
| OPAI Q4 | Assertiveness (reverse) | 5/10 | High | OMIT | Reverse coding, high cognitive load |

#### Pace Preference Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q5 | Pace | 8/10 | High | OMIT | Similar to OPAI Q5, less universal framing |
| ANT Q6 | Pace | 6/10 | Medium | OMIT | Vague wording, unclear reference point |
| ANT Q7 | Pace | 6/10 | Medium | OMIT | Too dependent on meeting culture |
| ANT Q8 | Pace | 6/10 | High | OMIT | Overlaps with emotional regulation |
| ANT Q9 | Pace | 5/10 | High | OMIT | Too abstract/hypothetical |
| GEM Q2 | Pace | 7/10 | Low | **KEEP (Q6)** | Unique productivity rhythm construct |
| GEM Q5 | Pace (reverse) | 6/10 | High | OMIT | Reverse coding, tests stress tolerance |
| GEM Q9 | Pace | 6/10 | High | OMIT | Overlaps with risk tolerance |
| GEM Q13 | Pace | 7/10 | High | OMIT | Similar to OPAI Q5, less clean |
| OPAI Q5 | Pace | 9/10 | Medium | **KEEP (Q4)** | Cleanest bias-toward-action trade-off |
| OPAI Q6 | Pace | 8/10 | Low | **KEEP (Q5)** | Captures emotional response to pace |
| OPAI Q7 | Pace (reverse) | 6/10 | High | OMIT | Reverse coding, similar to OPAI Q5 |
| OPAI Q8 | Pace | 6/10 | High | OMIT | Overlaps with assertiveness |

#### People vs. Task Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q10 | People vs Task | 9/10 | Medium | **KEEP (Q7)** | High-stakes scenario, cleanest trade-off |
| ANT Q11 | People vs Task | 7/10 | High | OMIT | Overlaps with leadership style |
| ANT Q12 | People vs Task (reverse) | 6/10 | High | OMIT | Reverse coding, tests introversion |
| ANT Q13 | People vs Task | 7/10 | High | OMIT | More verbose than OPAI Q11 |
| GEM Q3 | People vs Task | 7/10 | High | OMIT | Adds performance management confound |
| GEM Q7 | People vs Task | 7/10 | High | OMIT | Adds ethical dimension (accuracy) |
| GEM Q12 | People vs Task | 6/10 | High | OMIT | Too binary/extreme framing |
| GEM Q15 | People vs Task (reverse) | 5/10 | High | OMIT | Reverse coding, similar to ANT Q12 |
| OPAI Q9 | People vs Task | 7/10 | High | OMIT | Less balanced than ANT Q10 |
| OPAI Q10 | People vs Task | 7/10 | Low | **KEEP (Q9)** | Measures relational investment frequency |
| OPAI Q11 | People vs Task | 8/10 | Medium | **KEEP (Q8)** | Pure construct, no confounds |
| OPAI Q12 | People vs Task (reverse) | 6/10 | High | OMIT | Extreme framing, reverse coding |

#### Structure Preference Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q14 | Structure | 7/10 | Medium | **KEEP (Q12)** | Emotional response reveals preference |
| ANT Q15 | Structure | 9/10 | Medium | **KEEP (Q10)** | Highest-signal structure question |
| ANT Q16 | Structure | 7/10 | High | OMIT | Too similar to ANT Q15 |
| GEM Q4 | Structure | 6/10 | High | OMIT | Too low-stakes, role-influenced |
| GEM Q8 | Structure | 8/10 | Low | **KEEP (Q11)** | Unique operationalization construct |
| GEM Q11 | Structure | 6/10 | Medium | OMIT | Less actionable, conflates with risk |
| OPAI Q13 | Structure | 7/10 | High | OMIT | Similar to ANT Q15, less specific |
| OPAI Q14 | Structure | 6/10 | High | OMIT | Overlaps with pace preference |
| OPAI Q15 | Structure | 6/10 | High | OMIT | Similar to ANT Q14, less revealing |

---

### LAYER 3: RISK & DECISION ARCHITECTURE

#### Sunk Cost Bias Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q17 | Sunk Cost | 10/10 | Medium | **KEEP (Q13)** ⭐ | **TIER 1:** Most detailed financial anchoring |
| ANT Q19 | Sunk Cost | 9/10 | Medium | **KEEP (Q14)** | Interpersonal sunk cost, status bias |
| GEM Q16 | Sunk Cost | 7/10 | High | OMIT | Less detailed than ANT Q17, adds competitive threat |
| GEM Q22 | Sunk Cost | 7/10 | High | OMIT | Overlaps with professional incentives |
| OPAI Q16 | Sunk Cost | 7/10 | High | OMIT | Similar to GEM Q16, weaker financials |
| OPAI Q23 | Sunk Cost | 8/10 | Low | **KEEP (Q15)** | People-focused sunk cost, unique angle |

#### Financial Risk Tolerance Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q20 | Financial Risk | 8/10 | Medium | **KEEP (Q18)** | Real-world career decision, specific ranges |
| GEM Q18 | Financial Risk | 7/10 | High | OMIT | Less detailed than ANT Q20 |
| GEM Q21 | Financial Risk | 7/10 | High | OMIT | Mixed gain/loss complicates vs. OPAI Q24 |
| OPAI Q24 | Financial Risk (prob) | 10/10 | Low | **KEEP (Q16)** ⭐ | **TIER 1:** Pure EV test, gain frame |
| OPAI Q25 | Financial Risk (mixed) | 10/10 | Low | **KEEP (Q17)** ⭐ | **TIER 1:** Mixed frame, tests loss aversion |

#### Career/Reputational Risk Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q21 | Career Risk | 7/10 | Medium | OMIT | Conflates learning orientation with risk |
| GEM Q18 | Career Risk | 6/10 | High | OMIT | Overlaps with financial risk (same as GEM Q18 above) |
| OPAI Q19 | Reputational Risk | 9/10 | Low | **KEEP (Q19)** ⭐ | **TIER 1:** Pure reputational risk, no confounds |

#### Analytical vs. Intuitive Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q22 | Analytical vs Intuitive | 7/10 | Medium | OMIT | Overlaps with structure preference |
| ANT Q23 | Analytical vs Intuitive | 9/10 | Low | **KEEP (Q21)** | Unique "smart people signal" framing |
| GEM Q20 | Analytical vs Intuitive | 8/10 | High | OMIT | Duplicate of OPAI Q20, less polished |
| OPAI Q20 | Analytical vs Intuitive | 9/10 | Medium | **KEEP (Q20)** | Direct credentials vs. intuitive fit trade-off |

#### Loss Aversion Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q25 | Loss Aversion | 7/10 | High | OMIT | Overlaps with strategic planning (cannibalization) |
| GEM Q19 | Loss Aversion | 6/10 | Medium | OMIT | Too abstract/hypothetical (stock scenario) |
| OPAI Q21 | Loss Aversion | 8/10 | Low | **KEEP (Q22)** | Distinct from sunk cost, personal stake |

#### Overconfidence / Anchoring Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q26 | Overconfidence | 7/10 | Medium | OMIT | Requires specific business context (revenue forecasting) |
| GEM Q24 | Overconfidence/Anchoring | 7/10 | Low | **KEEP (Q24)** | Tests overconfidence via mentor warning |
| OPAI Q22 | Anchoring | 8/10 | Low | **KEEP (Q23)** | Universally relatable salary negotiation |

#### Emergency Decision / Other Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| GEM Q25 | Emergency Decision | 8/10 | Low | **KEEP (Q25)** | Only time-pressure scenario with explicit risk numbers |

#### Confidence Calibration Questions

| Original ID | Construct | Signal | Duplication | Recommendation | Notes |
|-------------|-----------|--------|-------------|----------------|-------|
| ANT Q18 | Confidence Calibration | 8/10 | Low | **KEEP (Q26)** | After high-complexity scenario (Q13) |
| ANT Q24 | Confidence Calibration | 8/10 | Low | **KEEP (Q27)** | After analytical/intuitive scenario (Q21) |
| GEM Q17 | Confidence Calibration | 7/10 | Medium | OMIT | Less strategically positioned than ANT Q18/Q24 |
| GEM Q23 | Confidence Calibration | 7/10 | Medium | OMIT | Less strategically positioned than ANT Q18/Q24 |

---

### Summary Statistics

**Total Questions Analyzed:** 90 (30 ANT + 30 GEM + 30 OPAI)

**Questions Kept:** 27 core questions
- From ANT: 8 questions (27%)
- From GEM: 4 questions (13%)
- From OPAI: 15 questions (50%)

**Questions Omitted:** 63 (70% reduction)
- Due to high duplication: 42 questions (67%)
- Due to cognitive load (reverse coding): 8 questions (13%)
- Due to confounding variables: 9 questions (14%)
- Due to lower signal strength: 4 questions (6%)

**Tier 1 Essential Questions (⭐):** 5 questions
- ANT Q17 → Q13 (sunk cost with financial detail)
- OPAI Q24 → Q16 (probabilistic gain)
- OPAI Q25 → Q17 (mixed gain/loss)
- OPAI Q19 → Q19 (reputational risk)
- [Q1, Q4, Q7 also could be considered Tier 1 for Layer 1 coverage]

---

---

## ADDITIONAL NOTES

### Why OPAI Questions Dominated Final Selection (50%)

**Reasons for High OPAI Representation:**

1. **Probabilistic Rigor:** OPAI questions included explicit expected value calculations and frame-dependent risk scenarios that other sources lacked
2. **Clean Trade-offs:** OPAI consistently framed options as equally defensible without obvious "right" answers
3. **Low Confounds:** OPAI questions tested single constructs without mixing variables (e.g., pure reputational risk vs. reputational + financial)
4. **Modern Context:** OPAI scenarios felt most applicable to modern work (LinkedIn posts, startup equity) vs. more generic scenarios

**This doesn't mean OPAI's entire set was superior** — ANT's sunk cost questions (Q17, Q19) were the best across all sources, and GEM's systems creation question (Q8) was unique. OPAI just had more questions that survived deduplication at high signal.

---

### Limitations of This Compilation

**What This Compilation Doesn't Address:**

1. **Demographic Representativeness:** Questions were not tested across age, cultural, or professional diversity — some scenarios may not translate universally
2. **Predictive Validity:** No longitudinal data linking assessment responses to actual behavioral outcomes
3. **Test-Retest Reliability:** No data on whether responses remain consistent over time
4. **Social Desirability Validation:** While questions were designed to minimize bias, no empirical validation was performed

**Recommended Next Steps:**

1. Pilot with diverse cohort (50+ respondents across roles, industries, experience levels)
2. Conduct cognitive interviews to identify unexpected ambiguities or confounds
3. Calculate internal consistency (Cronbach's alpha) for Layer 1 dimensions
4. Validate insights against self-reported behavior or peer assessments

---

### Document Maintenance

**When to Update This Compilation:**

- After MVP pilot if completion time significantly exceeds 15 minutes
- If dropout analysis reveals specific high-friction questions
- If internal consistency analysis reveals low correlation within dimensions
- If new behavioral constructs emerge as important for insight generation
- After significant user feedback about confusing or irrelevant questions

**Version Control:**
- Current version: 1.0 (Feb 15, 2026)
- Source documents: ANT, GEM, OPAI (accessed Feb 2026)
- Next planned review: After 50+ MVP respondents
