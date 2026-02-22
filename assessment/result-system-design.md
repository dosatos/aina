# Result System Design (Phase 0 MVP)

**Tone:** Clinical/Direct
**Archetype Names:** Functional (not aspirational)
**Depth:** Moderate (archetype + 2-3 tensions + mismatch flag)
**Email Gate:** After partial result (full PDF requires email)

---

## Scoring System

### Axis 1: Action Orientation (Q1-Q3)
**Score Range:** 3-6

**Calculation:**
```
Action Score = Q1_score + Q2_score + Q3_score
- Q1 (Assertiveness): A=2, B=1
- Q2 (Pace): A=2, B=1
- Q3 (Task/People): A=2, B=1

Total: 3 (Low Action) to 6 (High Action)
```

**Interpretation:**
- 6: High Action (Decisive, Fast, Task-focused)
- 5: Moderate-High Action
- 4: Moderate Action
- 3: Low Action (Collaborative, Deliberate, People-focused)

---

### Axis 2: Risk Posture (Q4-Q6)
**Score Range:** 3-6

**Calculation:**
```
Risk Score = Q4_score + Q5_score + Q6_score
- Q4 (Sunk cost bias): A=2, B=1
- Q5 (Loss aversion): A=1, B=2 (note: inverted)
- Q6 (Reputational risk): A=2, B=1

Total: 3 (Low Risk) to 6 (High Risk)
```

**Interpretation:**
- 6: High Risk (Rational, Bold, Public)
- 5: Moderate-High Risk
- 4: Moderate Risk
- 3: Low Risk (Cautious, Conservative, Private)

---

## The 4 Archetypes (2×2 Grid)

### Archetype 1: The Accelerator
**Profile:** High Action (5-6) + High Risk (5-6)

**One-Paragraph Description:**
You operate at high velocity with high conviction. Your default mode is to move quickly, make clear decisions, and take calculated risks without waiting for perfect information. You prioritize outcomes over process and are willing to absorb short-term friction for long-term gain. In teams, you're the person who breaks deadlocks and pushes projects forward. Your risk: moving faster than alignment can sustain, leaving execution gaps or relationship friction in your wake.

**Operating Style:**
- Assertive in meetings (jumps in, makes calls)
- Fast decision cycle (acts at 80% information)
- Task-oriented (protects deadlines)
- Cuts sunk costs quickly
- Takes financial and reputational risks

**Growth Edge:**
Your advantage is velocity. Your blind spot is assuming others can keep your pace. High-performing teams need your speed, but you'll plateau if you don't learn to build alignment while moving.

---

### Archetype 2: The Strategist
**Profile:** Low Action (3-4) + High Risk (5-6)

**One-Paragraph Description:**
You think systematically and act deliberately, but when you move, you're willing to take bold bets. You don't rush decisions, but you're not risk-averse—you're risk-selective. You optimize for the right answer over the fast answer, and you're comfortable with high-stakes moves once you're confident in the logic. In teams, you're the person who spots flaws in the plan before it launches. Your risk: analysis cycles that feel rigorous internally but read as slow externally.

**Operating Style:**
- Facilitative in meetings (hears perspectives before deciding)
- Deliberate decision cycle (needs 90%+ information)
- Balanced task/people focus
- Rational about sunk costs (evaluates forward)
- Willing to take reputational or financial risk when logic supports it

**Growth Edge:**
Your advantage is precision. Your blind spot is underestimating the cost of delay. High-impact work rewards both insight and timing—your edge is learning to act before you feel fully ready.

---

### Archetype 3: The Executor
**Profile:** High Action (5-6) + Low Risk (3-4)

**One-Paragraph Description:**
You move fast but stay within established boundaries. You're decisive, task-focused, and efficient—but you optimize for consistency over breakthrough. You get things done reliably, and teams value your ability to deliver without drama. Your instinct is to protect what's working rather than bet on what's uncertain. Your risk: speed without boldness creates a ceiling. You may hit your targets but miss asymmetric upside opportunities.

**Operating Style:**
- Assertive in meetings (makes calls quickly)
- Fast decision cycle (acts at 80%)
- Task-oriented (deadlines matter)
- Cautious about sunk costs (gives investments time)
- Conservative on loss aversion (values certainty)
- Risk-averse on reputation (protects relationships)

**Growth Edge:**
Your advantage is reliable execution. Your blind spot is staying too long in safe zones. You can handle more risk than you take—your next level requires occasionally betting on the upside, not just protecting the downside.

---

### Archetype 4: The Analyst
**Profile:** Low Action (3-4) + Low Risk (3-4)

**One-Paragraph Description:**
You reduce chaos and increase stability. You think carefully, move deliberately, and optimize for safety over speed. Your instinct is to gather data, consult stakeholders, and minimize downside before committing. Teams value your ability to spot risks others miss and your focus on sustainable decisions. Your risk: in high-velocity environments, thoroughness reads as drag. What feels like diligence internally can look like hesitation externally.

**Operating Style:**
- Facilitative in meetings (builds consensus)
- Deliberate decision cycle (needs high confidence)
- People-aware (considers impact on team)
- Cautious about sunk costs
- High loss aversion (values certainty)
- Conservative on reputational risk

**Growth Edge:**
Your advantage is reducing costly mistakes. Your blind spot is overweighting risk and underweighting opportunity cost. High-growth environments reward action under uncertainty—your edge is learning to move before the picture is complete.

---

## Tension Detection Rules

### Tension 1: Speed-Safety Paradox
**Detect When:**
- Q2 (Pace) = A (Fast)
- Q5 (Loss Aversion) = A (High aversion / chooses certainty)

**Narrative:**
> **⚠️ Speed-Safety Paradox**
>
> You move quickly—but only inside safe zones. You act at 80% information, but you consistently choose the guaranteed outcome over higher expected value. This creates a hidden ceiling: velocity without bold bets limits upside. You'll hit targets reliably but may miss breakthrough opportunities.
>
> **What this costs you:** You're fast within boundaries but slow to cross them. Competitors who combine your speed with higher risk tolerance will capture asymmetric returns you leave on the table.

---

### Tension 2: Public-Private Assertiveness Gap
**Detect When:**
- Q1 (Assertiveness) = A (High)
- Q6 (Reputational Risk) = B (Low tolerance)

**Narrative:**
> **⚠️ Public-Private Assertiveness Gap**
>
> You push hard in private—meetings, small groups, direct conversations. But you pull punches in public arenas. You're decisive behind closed doors but cautious when visibility increases. This limits your influence ceiling.
>
> **What this costs you:** Your ideas stay in the room. Peers with equal insight but higher public visibility will accumulate more career capital, not because they're smarter, but because they're more visible.

---

### Tension 3: Task-People Friction
**Detect When:**
- Q3 (Task/People) = A (Task-focused)
- Q7 (Drain) = D (Too much people management)

**Narrative:**
> **⚠️ Task-People Management Friction**
>
> You're wired for outcomes, not emotional bandwidth. You optimize for execution, and people management drains you faster than most roles surface. Leadership positions may look like promotions on paper but feel like energy taxes in practice.
>
> **What this costs you:** Standard career progression (IC → Manager → Senior Leader) fights your wiring. You'll perform better and feel better in high-autonomy IC tracks or founder roles where people management is optional, not required.

---

### Tension 4: Autonomy-Structure Contradiction
**Detect When:**
- Q8 (Ideal role) = D (High autonomy) AND E (Structured environment)
  - Note: This can only happen if user picks both in multi-select, or if we detect Q7 drain = A (lack autonomy) but Q8 want = E (structure)

**Alternative Detection:**
- Q7 (Drain) = A (Lack of autonomy)
- Q8 (Want) = E (Structured environment)

**Narrative:**
> **⚠️ Autonomy-Structure Contradiction**
>
> You want freedom and clarity. These rarely coexist. Structured environments create predictability but reduce decision authority. High-autonomy roles offer control but demand comfort with ambiguity. You need to pick which matters more.
>
> **What this costs you:** You're filtering for contradictory environments. Structured orgs will feel constraining. Autonomous roles will feel chaotic. Resolve this before your next move or you'll repeat the pattern.

---

### Tension 5: Sunk Cost Trap
**Detect When:**
- Q4 (Sunk cost) = B (High bias)
- Q5 (Loss aversion) = A (High aversion)

**Narrative:**
> **⚠️ Sunk Cost Trap**
>
> Your decision style systematically protects past investments. You give projects "one more quarter" and you choose certainty over upside. This reduces downside—you avoid costly mistakes—but it traps you in slow-moving bets.
>
> **What this costs you:** You stay in declining positions longer than the data supports. Careers and companies reward fast pivots when the evidence shifts. You're anchored to yesterday's decisions when you should be optimizing for tomorrow's.

---

### Tension 6: Growth-Repetition Conflict
**Detect When:**
- Q7 (Drain) = C (Repetitive work without growth)
- Q8 (Want) = A (Deep technical/specialist work)

**Narrative:**
> **⚠️ Growth-Repetition Conflict**
>
> You're drained by repetitive work but you want deep specialist expertise. Here's the tension: mastery requires repetition. Deep technical work means solving the same class of problem hundreds of times with increasing sophistication.
>
> **What this costs you:** You'll cycle through roles every 18 months chasing "learning" but never build compounding expertise. Specialists tolerate—or even enjoy—repetition because they're optimizing at the micro level. If repetition drains you, you may be a generalist misidentifying as a specialist.

---

## Mismatch Diagnostic Matrix (Q7 × Q8)

### Logic:
Compare what drains them (Q7) to what they want (Q8). Flag coherent vs contradictory pairs.

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
| B (Unclear expectations / shifting priorities) | F (Fast-paced, dynamic environment) | ⚠️ **Contradiction detected.** Fast-paced and dynamic usually means shifting priorities. You're describing the same environment as both drain and desire. Dig deeper: Is it the pace you want or the clarity you need? These rarely coexist. |
| C (Repetitive work) | E (Structured environment) | ⚠️ **Contradiction detected.** Structure creates consistency, which often feels repetitive. Structured orgs have defined playbooks—you'll execute them repeatedly. If repetition drains you, you may need dynamic environments (which contradict structure). |
| A (Lack of autonomy) | E (Structured environment) | ⚠️ **Contradiction detected.** Structured environments have clear processes but limited autonomy. You can't optimize both. Pick: Do you want freedom (high autonomy, ambiguous structure) or clarity (low autonomy, clear structure)? |
| F (High stress without control) | F (Fast-paced, dynamic) | ⚠️ **Contradiction detected.** Fast-paced environments create high stress with limited control. You may be describing the same environment. Ask: Is it the pace you want, or the control you're missing? |

---

## Result Page Structure

### Section 1: Your Operating Mode (Hook)
```
═══════════════════════════════════════════════════════════
YOUR OPERATING MODE
═══════════════════════════════════════════════════════════

[ARCHETYPE NAME]

[One-paragraph archetype description]

═══════════════════════════════════════════════════════════
YOUR PROFILE
═══════════════════════════════════════════════════════════

Action Orientation:  ████████░░ (8/10 - High)
Risk Posture:        ██████░░░░ (6/10 - Moderate)

Decision Style:
• Assertiveness:     ████████░░ High
• Pace:              ████████░░ Fast
• Task/People:       ███████░░░ Task-focused
• Sunk Cost Bias:    ████░░░░░░ Low
• Loss Aversion:     ██████░░░░ Moderate
• Reputational Risk: ████████░░ Low aversion (bold)
```

### Section 2: Hidden Tensions (CORE VALUE)
```
═══════════════════════════════════════════════════════════
YOUR INTERNAL CONTRADICTIONS
═══════════════════════════════════════════════════════════

[Show 2-3 detected tensions with full narratives]

Example:
⚠️ Speed-Safety Paradox
[Full narrative from tension detection rules]

⚠️ Public-Private Assertiveness Gap
[Full narrative]
```

### Section 3: Career Fit Signals
```
═══════════════════════════════════════════════════════════
WHERE YOU THRIVE (AND WHERE YOU DON'T)
═══════════════════════════════════════════════════════════

Based on your wiring + what drains you:

✅ ENVIRONMENTS WHERE YOU THRIVE:
• [Based on archetype + Q8 ideal role]
• [Specific characteristics]
• [Concrete filters for next role]

⚠️ RED FLAGS TO AVOID:
• [Based on detected tensions]
• [Specific anti-patterns]
• [What to filter out in job search]

[Mismatch diagnostic if contradiction detected]
```

### Section 4: What's Missing (Tease Full Platform)
```
═══════════════════════════════════════════════════════════
THIS IS YOUR SURFACE PROFILE
═══════════════════════════════════════════════════════════

This diagnosis is based on 10 questions covering 2 of 7 behavioral layers.

Your full Decision Architecture includes:

Layer 1: Behavioral Dynamics ✅ (measured)
Layer 2: Cognitive Processing (not yet measured)
Layer 3: Risk & Decision Architecture ✅ (measured)
Layer 4: Execution & Consistency Patterns (not yet measured)
Layer 5: Relational & Communication Style (not yet measured)
Layer 6: Energy & Motivation Drivers (not yet measured)
Layer 7: Self-Perception vs Reality Gap (not yet measured)

The cross-layer synthesis reveals:
• Hidden execution gaps (why smart people don't follow through)
• Relationship blind spots (what teams see that you don't)
• Energy optimization (when you're at 10x vs 0.3x)
• Decision consistency patterns (where your logic breaks down)

[CTA: Want the full diagnosis? Enter email for complete PDF]
```

---

## Implementation Priority

**Phase 0 MVP (Ship this):**
1. ✅ Calculate Action + Risk scores
2. ✅ Map to 1 of 4 archetypes
3. ✅ Detect 2-3 tensions (from 6 rules)
4. ✅ Run mismatch diagnostic (Q7 vs Q8)
5. ✅ Show partial result page
6. ✅ Gate full PDF with email

**Phase 1 Enhancements (After validation):**
- Add percentile scoring ("You're more assertive than 73% of professionals")
- Add archetype distribution ("12% of users are Accelerators")
- Add confidence intervals ("Based on 1 question, confidence: low")
- A/B test result page layouts

**Phase 2 (Full platform):**
- Multi-item trait measurement
- Cross-layer tension detection
- Peer perception comparison
- Longitudinal tracking

---

## Success Metrics for Result System

**Qualitative signals (first 50 users):**
- 5+ "This described me perfectly" reactions
- 3+ "How did you know that?" comments
- Users quote specific tensions back to you
- Organic shares with tension screenshots

**Quantitative metrics:**
- Email capture rate: >60% (saw result → gave email)
- Time on result page: >2 minutes (reading, not skimming)
- Social shares: >10% of completions
- Return visits: >20% come back to re-read

**Red flags:**
- "Just another personality test" comments
- Email capture <40%
- Time on page <45 seconds
- No organic shares

---

## Next Steps

1. Review this system for accuracy and tone
2. I'll create the actual result templates (4 archetypes × variations)
3. Build result page HTML mockup
4. Test with 5 people before launch
