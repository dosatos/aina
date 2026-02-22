# Result System Design (Phase 0 MVP)

**Tone:** Clinical/Direct
**Archetype Names:** Functional (not aspirational)
**Depth:** Moderate (archetype + 2-3 tensions + mismatch flag)
**Email Gate:** After partial result (full PDF requires email)

**Last Updated:** Feb 21, 2026 - Fixed: score visualization, boundary handling, tension confidence, archetype neutrality

---

## Critical Fixes Applied

### 1. Honest Score Visualization
- **Removed:** Fake /10 precision bars
- **Added:** Band labels (Very High, High, Moderate, Low) + raw score
- **Why:** Raw range is 3-6, mapping to /10 is mathematically dishonest

### 2. Boundary Handling
- **Added:** "Primary mode + secondary lean" for scores at boundaries
- **Why:** Prevents hard cliff feeling (score 4 vs 5 feeling arbitrarily different)

### 3. Tension Confidence
- **Added:** Confidence tags (Preliminary / Moderate / High) for each tension
- **Why:** Single-item measurements need qualification

### 4. Neutral Archetype Names
- Accelerator → **Driver** (less aspirational)
- Executor → **Operator** (more neutral)
- Strategist → **Architect** (kept)
- Analyst → **Evaluator** (parallel structure)

### 5. Honest Axis Labeling
- "Action Orientation" → **"Operating Velocity"**
- **Why:** More honest about measuring "how quickly/forcefully you move decisions"

---

## Scoring System

### Axis 1: Operating Velocity (Q1-Q3)
**Score Range:** 3-6

**What it measures:** How quickly and forcefully you move decisions forward (combines assertiveness, pace, and task focus)

**Calculation:**
```
Operating Velocity = Q1 + Q2 + Q3
- Q1 (Assertiveness): A=2, B=1
- Q2 (Pace): A=2, B=1
- Q3 (Task/People): A=2, B=1

Total: 3 (Deliberate) to 6 (Fast)
```

**Display Format:**
```
Operating Velocity: VERY HIGH (Score: 6/6)

NOT this: ████████░░ (8/10) ← fake precision
```

**Band Labels:**
- 6: Very High
- 5: High
- 4: Moderate
- 3: Low

---

### Axis 2: Risk Posture (Q4-Q6)
**Score Range:** 3-6

**What it measures:** Risk tolerance across domains (cognitive bias, behavioral economics, social risk). These correlate but aren't identical constructs.

**Calculation:**
```
Risk Posture = Q4 + Q5 + Q6
- Q4 (Sunk cost bias): A=2, B=1
- Q5 (Loss aversion): A=1, B=2 (inverted)
- Q6 (Reputational risk): A=2, B=1

Total: 3 (Conservative) to 6 (Bold)
```

**Display Format:**
```
Risk Posture: MODERATE-HIGH (Score: 5/6)
```

**Band Labels:**
- 6: Very High
- 5: Moderate-High
- 4: Moderate
- 3: Low

---

## The 4 Archetypes (Revised Names)

### Archetype 1: The Driver
**Profile:** High Velocity (5-6) + High Risk (5-6)

**One-Paragraph Description:**
You operate at high velocity with high risk tolerance. Your default mode is to move quickly, make clear decisions, and take calculated risks without waiting for perfect information. You prioritize outcomes over process and are willing to absorb short-term friction for long-term gain. In teams, you're the person who breaks deadlocks and pushes projects forward. Your constraint: moving faster than alignment can sustain, leaving execution gaps or relationship friction in your wake.

**Operating Style:**
- Assertive in meetings (jumps in, makes calls)
- Fast decision cycle (acts at 80% information)
- Task-oriented (protects deadlines)
- Cuts sunk costs quickly
- Takes financial and reputational risks

**Growth Edge:**
Your advantage is velocity. Your constraint is moving faster than systems can sustain. High-performing teams need your speed, but you'll plateau if you don't build alignment while moving.

---

### Archetype 2: The Architect
**Profile:** Low Velocity (3-4) + High Risk (5-6)

**One-Paragraph Description:**
You think systematically and act deliberately, but when you move, you're willing to take bold bets. You don't rush decisions, but you're not risk-averse—you're risk-selective. You optimize for the right answer over the fast answer, and you're comfortable with high-stakes moves once you're confident in the logic. In teams, you're the person who spots flaws in the plan before it launches. Your constraint: analysis cycles that feel rigorous internally but read as slow externally.

**Operating Style:**
- Facilitative in meetings (hears perspectives before deciding)
- Deliberate decision cycle (needs 90%+ information)
- Balanced task/people focus
- Rational about sunk costs (evaluates forward)
- Willing to take reputational or financial risk when logic supports it

**Growth Edge:**
Your advantage is precision. Your constraint is underestimating the cost of delay. High-impact work rewards both insight and timing—your edge is acting before you feel fully ready.

---

### Archetype 3: The Operator
**Profile:** High Velocity (5-6) + Low Risk (3-4)

**One-Paragraph Description:**
You move fast but stay within established boundaries. You're decisive, task-focused, and efficient—but you optimize for consistency over breakthrough. You get things done reliably, and teams value your ability to deliver without drama. Your instinct is to protect what's working rather than bet on what's uncertain. Your constraint: speed without boldness creates a ceiling. You may hit your targets but miss asymmetric upside opportunities.

**Operating Style:**
- Assertive in meetings (makes calls quickly)
- Fast decision cycle (acts at 80%)
- Task-oriented (deadlines matter)
- Cautious about sunk costs (gives investments time)
- Conservative on loss aversion (values certainty)
- Risk-averse on reputation (protects relationships)

**Growth Edge:**
Your advantage is reliable execution. Your constraint is staying too long in safe zones. You can handle more risk than you take—your next level requires occasionally betting on upside, not just protecting downside.

---

### Archetype 4: The Evaluator
**Profile:** Low Velocity (3-4) + Low Risk (3-4)

**One-Paragraph Description:**
You reduce chaos and increase stability. You think carefully, move deliberately, and optimize for safety over speed. Your instinct is to gather data, consult stakeholders, and minimize downside before committing. Teams value your ability to spot risks others miss and your focus on sustainable decisions. Your constraint: in high-velocity environments, thoroughness reads as drag. What feels like diligence internally can look like hesitation externally.

**Operating Style:**
- Facilitative in meetings (builds consensus)
- Deliberate decision cycle (needs high confidence)
- People-aware (considers impact on team)
- Cautious about sunk costs
- High loss aversion (values certainty)
- Conservative on reputational risk

**Growth Edge:**
Your advantage is reducing costly mistakes. Your constraint is overweighting risk and underweighting opportunity cost. High-growth environments reward action under uncertainty—your edge is moving before the picture is complete.

---

## Boundary Handling (NEW)

### Problem: Hard Cliffs
- Score 4 → Evaluator
- Score 5 → Driver
- Behaviorally nearly identical

### Solution: "Primary + Leaning"

**Detection Logic:**
```python
if velocity_score == 4:
    lean = "leaning toward high velocity"
elif velocity_score == 5:
    lean = "leaning toward moderate velocity"

if risk_score == 4:
    lean = "leaning toward bold"
elif risk_score == 5:
    lean = "leaning toward moderate"
```

**Display Format:**
```
═══════════════════════════════════════════════════════════
YOUR OPERATING MODE
═══════════════════════════════════════════════════════════

Primary Mode: THE OPERATOR
Secondary Lean: Driver tendencies (at high velocity boundary)

Operating Velocity: HIGH (5/6) — leaning toward very high
Risk Posture: MODERATE (4/6) — leaning toward conservative

You're at the boundary between Operator and Driver modes.
This means you combine fast execution with selective risk-taking.
```

---

## Tension Detection Rules (with Confidence)

### Tension Priority Order:
1. Sunk Cost Trap (concrete, immediately actionable)
2. Public-Private Assertiveness Gap ("wow that's me" factor)
3. Task-People Management Friction (high-confidence match)
4. Speed-Safety Paradox (insightful but preliminary)
5. Autonomy-Structure Contradiction (high-value when detected)
6. Growth-Repetition Conflict (requires most interpretation)

**Display Rule:** Show top 2-3 detected tensions, sorted by confidence + priority

---

### Tension 1: Speed-Safety Paradox
**Detect When:**
- Q2 (Pace) = A (Fast)
- Q5 (Loss Aversion) = A (High aversion)

**Confidence:** Preliminary
*Based on 2 single-item indicators*

**Narrative:**
> **⚠️ Speed-Safety Paradox** [Preliminary Signal]
>
> You move quickly—but only inside safe zones. You act at 80% information, but you consistently choose the guaranteed outcome over higher expected value. This creates a hidden ceiling: velocity without bold bets limits upside. You'll hit targets reliably but may miss breakthrough opportunities.
>
> **What this costs you:** You're fast within boundaries but slow to cross them. Competitors who combine your speed with higher risk tolerance will capture asymmetric returns you leave on the table.
>
> *Confidence: Preliminary (based on early indicators)*

---

### Tension 2: Public-Private Assertiveness Gap
**Detect When:**
- Q1 (Assertiveness) = A (High)
- Q6 (Reputational Risk) = B (Low tolerance)

**Confidence:** Moderate
*Consistent behavioral pattern across contexts*

**Narrative:**
> **⚠️ Public-Private Assertiveness Gap** [Moderate Signal]
>
> You push hard in private—meetings, small groups, direct conversations. But you pull punches in public arenas. You're decisive behind closed doors but cautious when visibility increases. This limits your influence ceiling.
>
> **What this costs you:** Your ideas stay in the room. Peers with equal insight but higher public visibility will accumulate more career capital, not because they're smarter, but because they're more visible.
>
> *Confidence: Moderate (consistent behavioral pattern)*

---

### Tension 3: Task-People Management Friction
**Detect When:**
- Q3 (Task/People) = A (Task-focused)
- Q7 (Drain) = D (Too much people management)

**Confidence:** High
*Direct alignment between wiring and stated drain*

**Narrative:**
> **⚠️ Task-People Management Friction** [High Signal]
>
> You're wired for outcomes, not emotional bandwidth. You optimize for execution, and people management drains you faster than most roles surface. Leadership positions may look like promotions on paper but feel like energy taxes in practice.
>
> **What this costs you:** Standard career progression (IC → Manager → Senior Leader) fights your wiring. You'll perform better and feel better in high-autonomy IC tracks or founder roles where people management is optional, not required.
>
> *Confidence: High (wiring matches stated drain)*

---

### Tension 4: Autonomy-Structure Contradiction
**Detect When:**
- Q7 (Drain) = A (Lack of autonomy)
- Q8 (Want) = E (Structured environment)

**Confidence:** High
*Direct contradiction in stated preferences*

**Narrative:**
> **⚠️ Autonomy-Structure Contradiction** [High Signal]
>
> You want freedom and clarity. These rarely coexist. Structured environments create predictability but reduce decision authority. High-autonomy roles offer control but demand comfort with ambiguity. You need to pick which matters more.
>
> **What this costs you:** You're filtering for contradictory environments. Structured orgs will feel constraining. Autonomous roles will feel chaotic. Resolve this before your next move or you'll repeat the pattern.
>
> *Confidence: High (stated contradiction)*

---

### Tension 5: Sunk Cost Trap
**Detect When:**
- Q4 (Sunk cost) = B (High bias)
- Q5 (Loss aversion) = A (High aversion)

**Confidence:** Moderate
*Converging risk-averse pattern*

**Narrative:**
> **⚠️ Sunk Cost Trap** [Moderate Signal]
>
> Your decision style systematically protects past investments. You give projects "one more quarter" and you choose certainty over upside. This reduces downside—you avoid costly mistakes—but it traps you in slow-moving bets.
>
> **What this costs you:** You stay in declining positions longer than the data supports. Careers and companies reward fast pivots when the evidence shifts. You're anchored to yesterday's decisions when you should be optimizing for tomorrow's.
>
> *Confidence: Moderate (pattern across 2 risk dimensions)*

---

### Tension 6: Growth-Repetition Conflict
**Detect When:**
- Q7 (Drain) = C (Repetitive work without growth)
- Q8 (Want) = A (Deep technical/specialist work)

**Confidence:** Moderate
*Requires nuanced interpretation*

**Narrative (REVISED):**
> **⚠️ Growth-Repetition Conflict** [Moderate Signal]
>
> You're drained by repetitive work but you want deep specialist expertise. Here's the nuance: mastery involves high-complexity repetition. If it's the low-stakes repetition that drains you (same basic task), specialization may still fit. If it's repetition itself—even complex variants of hard problems—that's worth examining.
>
> **What this costs you:** You may cycle through roles every 18 months chasing "learning" without building compounding expertise. True specialists find satisfaction in solving the same class of problem with increasing sophistication. If that doesn't appeal, you might be a generalist misidentifying as a specialist.
>
> *Confidence: Moderate (requires deeper exploration)*

---

## Mismatch Diagnostic Matrix (Q7 × Q8)

### Coherent Pairs (Affirm)

| Q7 Drain | Q8 Want | Diagnosis |
|----------|---------|-----------|
| A (Lack autonomy) | D (High autonomy) | ✅ **Coherent alignment.** You know what's draining you and what you need. Filter next role for decision authority and minimal approvals. |
| E (Too much solo work) | C (Building/leading teams) | ✅ **Coherent alignment.** You're people-energized and currently isolated. Look for collaborative environments or management tracks. |
| C (Repetitive work) | B (Strategic thinking) | ✅ **Coherent alignment.** You're intellectually wired for big-picture work but stuck in execution mode. Target Staff+ IC or strategy roles. |
| D (Too much people mgmt) | A (Deep technical work) | ✅ **Coherent alignment.** You want to return to craft. Seek senior IC tracks at companies with strong technical ladders. |

### Contradictory Pairs (Diagnose)

| Q7 Drain | Q8 Want | Diagnosis |
|----------|---------|-----------|
| B (Unclear expectations) | F (Fast-paced, dynamic) | ⚠️ **Contradiction.** Fast-paced and dynamic usually means shifting priorities. You're describing the same environment as both drain and desire. Dig deeper: Is it the pace you want or the clarity you need? |
| C (Repetitive work) | E (Structured environment) | ⚠️ **Contradiction.** Structure creates consistency, which often feels repetitive. Structured orgs have defined playbooks—you'll execute them repeatedly. |
| A (Lack of autonomy) | E (Structured environment) | ⚠️ **Contradiction.** Structured environments have clear processes but limited autonomy. You can't optimize both. Pick: freedom (high autonomy, ambiguous structure) or clarity (low autonomy, clear structure)? |
| F (High stress without control) | F (Fast-paced, dynamic) | ⚠️ **Contradiction.** Fast-paced environments create high stress with limited control. You may be describing the same environment. |

---

## Result Page Structure

### Section 1: Your Operating Mode
```
═══════════════════════════════════════════════════════════
YOUR OPERATING MODE
═══════════════════════════════════════════════════════════

Primary Mode: THE DRIVER
[Secondary Lean: if at boundary]

Operating Velocity: VERY HIGH (6/6)
Risk Posture: HIGH (5/6)

[One-paragraph archetype description]

Note: This profile is based on 10 single-question indicators.
It's directional, not definitive. The full assessment uses
multi-item measurement to validate or challenge what you see here.
```

### Section 2: Hidden Tensions (CORE VALUE - Partially FREE)
```
═══════════════════════════════════════════════════════════
YOUR INTERNAL CONTRADICTIONS
═══════════════════════════════════════════════════════════

[Show 1 tension FREE, gate remaining 1-2]

⚠️ Sunk Cost Trap [Moderate Signal]
[Full narrative with "What this costs you"]
*Confidence: Moderate*

[GATED: Unlock 2 more tensions with email]
```

### Section 3: Career Fit Signals (GATED)
```
═══════════════════════════════════════════════════════════
UNLOCK YOUR FULL DIAGNOSIS
═══════════════════════════════════════════════════════════

You've seen your operating mode and one key tension.

Your complete diagnosis includes:
• 2 additional internal contradictions
• Full career mismatch analysis (Q7 vs Q8)
• Detailed environment recommendations
• PDF download

[Email input]
[Get Full Diagnosis button]
```

### Section 4: What's Missing (Platform Tease)
```
This is your surface profile from 10 questions (2 of 7 layers).

Your full Decision Architecture includes:
• Execution patterns (Layer 4)
• Relational dynamics (Layer 5)
• Energy optimization (Layer 6)
• Self-perception vs reality gap (Layer 7)
```

---

## FREE vs GATED Split

**FREE (No email required):**
- Primary archetype + boundary lean
- Operating scores (velocity + risk) with band labels
- ONE tension (highest priority/confidence)
- "Directional not definitive" disclaimer

**GATED (Requires email):**
- Remaining 1-2 tensions
- Full mismatch diagnostic (Q7 vs Q8)
- Detailed "where you thrive" breakdown
- "Red flags to avoid" section
- PDF download

**Why this works:**
- Shows enough value to earn trust
- Gates high-value mismatch diagnostic
- Mismatch analysis is compelling carrot for email

---

## Implementation Checklist

**Before launch:**
- [ ] Remove all /10 score bars from display
- [ ] Implement band labels (Very High, High, Moderate, Low)
- [ ] Add boundary detection ("leaning" logic)
- [ ] Add confidence tags to all 6 tensions
- [ ] Prioritize tension display (show strongest first)
- [ ] Use new archetype names (Driver, Architect, Operator, Evaluator)
- [ ] Add "directional not definitive" disclaimer
- [ ] Define FREE vs GATED split in UI
- [ ] Test with 5 users: "Does this feel accurate?"
- [ ] Check: No "fake precision" complaints

---

## Success Metrics

**Qualitative (first 50 users):**
- 5+ "This described me perfectly" reactions
- 3+ "How did you know that?" comments
- 2+ users quote specific tensions
- 0 "scores don't make sense" complaints

**Quantitative:**
- Email capture: >60%
- Time on result page: >2 min
- Social shares: >10%
- Boundary cases feel accurate

**Red flags:**
- "Scores are fake precision" complaints
- "I'm between two types" (boundary handling failed)
- "Tensions feel generic" (confidence/priority issues)
- Email capture <40%

---

## Next Steps

1. Review this updated system
2. Update result-templates.md with new scoring display
3. Build result page HTML with honest visualization
4. Test boundary cases with 5 users
5. Iterate based on "this described me" feedback
