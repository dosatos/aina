# Phase 0 MVP Assessment: Compiled Best Questions

**Document Version:** 1.0
**Last Updated:** February 15, 2026
**Sources Analyzed:** Anthropic Claude (ant.md), Google Gemini (gem.md), OpenAI GPT (opai.md)

---

## Executive Summary

### Purpose and Scope

This document represents a curated compilation of the highest-quality Phase 0 assessment questions derived from three independent AI-generated suggestion sets. The original documents contained approximately 90 total questions with ~40% construct overlap. This compilation reduces that to **25-30 strategically selected questions** that maximize signal while minimizing redundancy and completion time.

**Target Completion Time:** 12-15 minutes
**Question Distribution:** 12-14 behavioral dynamics + 12-14 risk/decision architecture + 5 demographics

### Relationship to Main Prompt Generator

- **Main Prompt** (`phase0-question-generator.md`): Instructions for AI systems to generate assessment questions
- **This Document**: Curated examples and best practices from actual AI outputs using that prompt
- **Together**: "Instructions + Proven Examples" for MVP implementation

### Quality Criteria for Selection

Questions were evaluated on:

1. **Signal Strength** (1-10): How effectively does this question reveal the target construct?
2. **Uniqueness**: Does this question capture something other questions miss?
3. **Specificity**: Are the scenarios concrete enough to reveal true preferences?
4. **Forced Trade-offs**: Do options represent equally defensible choices?
5. **Natural Language**: Does it sound like a real decision someone would face?
6. **Low Social Desirability**: Are both/all options acceptable to choose?
7. **Actionability**: Can responses drive meaningful personalized insights?

---

## LAYER 1: BEHAVIORAL DYNAMICS

*Natural behavioral tendencies and social/professional presence*

### 1. Assertiveness (3 questions)

#### Q1: Meeting Facilitation [Forced-Choice]
**Source:** ANT Q1 | **Signal Strength:** 9/10

"When your team is debating two directions and can't agree, you're more likely to:"

○ (A) Make the call yourself so the team can move forward
○ (B) Facilitate the discussion until the group reaches alignment

**Why This Question:**
- Pure assertiveness vs. consensus-building trade-off without confounding variables
- Common scenario that reveals decision-making authority comfort
- Both options are professionally defensible (no social desirability bias)
- High signal for leadership style and meeting presence

**Eliminated Alternatives:**
- GEM Q1: Similar construct but adds confounding "timeline slip" stress variable
- OPAI Q1: Similar but less balanced (option A sounds more aggressive: "even if it creates tension")

---

#### Q2: Critical Feedback Delivery [Forced-Choice]
**Source:** ANT Q2 | **Signal Strength:** 8/10

"A colleague presents an idea you think has a major flaw. You're more likely to:"

○ (A) Point out the issue directly so it gets addressed
○ (B) Ask questions that help them discover the flaw on their own

**Why This Question:**
- Reveals communication directness in intellectually charged situations
- Tests balance between efficiency and relational care
- Socratic vs. direct feedback styles both valid in professional contexts
- Complements Q1 by testing assertiveness in peer (not leadership) context

**Eliminated Alternatives:**
- OPAI Q2: Focuses on missed deadlines (adds conflict/performance management confound)
- GEM Q6: Too focused on senior leadership context (not universally applicable)

---

#### Q3: Proactive Leadership [Likert Scale]
**Source:** OPAI Q3 | **Signal Strength:** 7/10

"How often do you volunteer to lead discussions when a group seems uncertain about next steps?"

Never / Rarely / Sometimes / Often / Always

**Why This Question:**
- Measures proactive vs. reactive assertiveness
- Likert format captures frequency patterns (not just single-instance preferences)
- Complements forced-choice questions with granular measurement
- Low social desirability (both high and low frequencies have valid rationales)

**Eliminated Alternatives:**
- ANT Q3 (reverse-coded): "Let others set agenda" — reverse coding adds cognitive load
- ANT Q4: Negotiation scenario overlaps with risk tolerance questions
- GEM Q14: Deadline negotiation overlaps with people/task orientation

---

### 2. Pace Preference (3 questions)

#### Q4: Launch vs. Analyze [Forced-Choice]
**Source:** OPAI Q5 | **Signal Strength:** 9/10

"When starting a new initiative, you're more likely to:"

○ (A) Launch a rough version quickly and refine based on feedback
○ (B) Analyze risks and edge cases before taking visible action

**Why This Question:**
- Cleanest bias-toward-action vs. deliberation trade-off in the entire set
- Directly applicable to product development and strategic execution
- Both options professionally defensible (fast iteration vs. risk management)
- High correlation with actual workplace behavior patterns

**Eliminated Alternatives:**
- ANT Q5: Similar but uses "unclear requirements" framing (less universal)
- GEM Q13: "Version 0.1 vs 1.0" overlaps but less clean trade-off

---

#### Q5: Decision Pace Under Ambiguity [Likert Scale]
**Source:** OPAI Q6 | **Signal Strength:** 8/10

"When facing ambiguity, I feel energized by moving fast and figuring things out along the way."

Not at all like me / Slightly like me / Moderately like me / Very much like me / Extremely like me

**Why This Question:**
- Measures emotional response to pace (not just behavior)
- "Energized" reveals intrinsic motivation vs. learned behavior
- Captures pace preference specifically in ambiguous contexts (high signal scenario)
- Likert format allows nuanced self-assessment

**Eliminated Alternatives:**
- GEM Q5 (reverse-coded): Adds unnecessary cognitive load
- ANT Q9: "Good decision today vs great decision next week" — too abstract/hypothetical

---

#### Q6: Productivity Rhythm [Forced-Choice]
**Source:** GEM Q2 | **Signal Strength:** 7/10

"In your daily workflow, you feel most productive when:"

○ (A) You have a high volume of varied tasks to knock out in rapid succession
○ (B) You have large blocks of uninterrupted time to go deep into a single complex problem

**Why This Question:**
- Reveals natural productivity rhythm (sprint vs. marathon)
- Orthogonal to strategic pace (Q4-Q5) — measures execution tempo
- Strong predictor of preferred work environment and role fit
- Both options signal competence in different professional contexts

**Eliminated Alternatives:**
- ANT Q7: "Action items assigned immediately" — too dependent on meeting culture
- ANT Q8: Feedback response scenario overlaps with emotional regulation

---

### 3. People vs. Task Orientation (3 questions)

#### Q7: Team Behind Schedule [Forced-Choice]
**Source:** ANT Q10 | **Signal Strength:** 9/10

"You're leading a project that's behind schedule. You're more likely to:"

○ (A) Restructure the timeline and cut scope to hit the deadline
○ (B) Check in with the team to understand what's slowing them down before changing the plan

**Why This Question:**
- High-stakes scenario that forces genuine priority revelation
- Cleanest task-focus vs. people-focus trade-off in the entire set
- Both options are defensible leadership responses (not obviously "good" vs "bad")
- Directly applicable to real project management situations

**Eliminated Alternatives:**
- OPAI Q9: Similar construct but less balanced (B option sounds obviously better)
- GEM Q3: Underperformance scenario adds performance management confound

---

#### Q8: Feedback Delivery Style [Forced-Choice]
**Source:** OPAI Q11 | **Signal Strength:** 8/10

"When giving feedback, you usually:"

○ (A) Prioritize clarity and directness
○ (B) Prioritize how the message will land emotionally

**Why This Question:**
- Pure people/task orientation without confounding variables
- Applicable to all professional levels (no hierarchy assumptions)
- Reveals core communication philosophy
- Both priorities are valid in modern management theory

**Eliminated Alternatives:**
- ANT Q13: Similar but more verbose and adds "feeling about work" context
- GEM Q7: Focuses on "accuracy vs. morale" which adds ethical dimension

---

#### Q9: 1:1 Meeting Depth [Likert Scale]
**Source:** OPAI Q10 | **Signal Strength:** 7/10

"During 1:1 meetings, I naturally spend time understanding the person beyond the task at hand."

Never / Rarely / Sometimes / Often / Always

**Why This Question:**
- Measures frequency of relational investment (not single-instance preference)
- "Naturally" captures intrinsic tendency (not learned behavior)
- Specific to 1:1 context (removes group dynamics confound)
- Complements forced-choice questions with granular data

**Eliminated Alternatives:**
- ANT Q11: "Disengaged performer" scenario overlaps with leadership style
- GEM Q12: "Delivered product vs. high-performing team" — too binary/extreme
- ANT Q12 (reverse-coded): Small talk frustration adds cognitive load

---

### 4. Structure Preference (3 questions)

#### Q10: Planning Approach [Forced-Choice]
**Source:** ANT Q15 | **Signal Strength:** 9/10

"When planning a complex initiative, you prefer to:"

○ (A) Define a rough direction and adapt as you learn more
○ (B) Build a detailed roadmap with milestones and dependencies

**Why This Question:**
- Highest-signal structure question across all three sources
- Directly applicable to strategic planning and project management
- Both approaches are professionally defensible and context-dependent
- Cleanly separates emergent vs. structured planning styles

**Eliminated Alternatives:**
- GEM Q4: "Start of work week" — too low-stakes, easily influenced by role demands
- OPAI Q13: Similar but less specific about planning context

---

#### Q11: Systems Creation [Likert Scale]
**Source:** GEM Q8 | **Signal Strength:** 8/10

"I find it easy to 'standardize' my recurring tasks by creating checklists, templates, or automated workflows."

Scale: 1 (Never) — 5 (Always)

**Why This Question:**
- Measures operationalization capability (unique construct not in other questions)
- "Find it easy" reveals natural tendency vs. forced discipline
- Concrete examples (checklists, templates, automation) reduce ambiguity
- High predictive value for role fit (operations vs. creative roles)

**Eliminated Alternatives:**
- ANT Q16: "How often do you create written plans" — too similar to Q10
- GEM Q11: "Minimize surprises vs. maximize opportunity" — less actionable

---

#### Q12: Comfort with Unstructured Time [Forced-Choice]
**Source:** ANT Q14 | **Signal Strength:** 7/10

"Your calendar for next week is completely empty. You feel:"

○ (A) Excited — you'll figure out priorities as they come
○ (B) Uneasy — you'd rather block time for your key goals now

**Why This Question:**
- Emotional response reveals true preference (not learned behavior)
- Concrete scenario that's universally relatable
- Both responses are professionally valid (flexibility vs. intentionality)
- Complements Q10-Q11 by focusing on personal work rhythm vs. team planning

**Eliminated Alternatives:**
- OPAI Q15: "Loosely structured vs tightly scheduled day" — overlaps but less specific
- GEM Q4: Similar but less emotionally revealing

---

---

## LAYER 3: RISK & DECISION ARCHITECTURE

*Revealed preferences under uncertainty and cognitive bias detection*

### 5. Sunk Cost Bias (3 scenarios)

#### Q13: Internal Tool Development [Scenario]
**Source:** ANT Q17 | **Signal Strength:** 10/10

"You've spent 4 months and $30K of budget building an internal tool your team was excited about. After launch, adoption is at 15% — most people quietly went back to the old process. Your engineering lead believes two more sprints could fix the UX issues. Meanwhile, a teammate flags a well-reviewed off-the-shelf tool that costs $500/month and covers 80% of your use case. You:"

○ (A) Invest the two sprints — your team built this with specific workflows in mind, and the learnings from V1 make V2 much stronger
○ (B) Run both side by side for two weeks and let usage data decide
○ (C) Switch to the off-the-shelf tool and redeploy engineering time to higher-impact work
○ (D) Survey the team to understand why adoption was low before committing to either path

**Why This Question:**
- **TIER 1 ESSENTIAL** — Most detailed financial anchoring in all three sources
- Specific dollar amounts ($30K sunk, $500/month alternative) enable clear cost comparison
- Four options reveal different decision-making philosophies (not just sunk cost)
- Real-world scenario with genuine trade-offs (team learning, switching costs, opportunity cost)
- Option phrasings avoid obvious "right" answers

**Eliminated Alternatives:**
- GEM Q16: Side project scenario with less detailed financial framing
- OPAI Q16: Similar side project scenario but weaker financial specifics

---

#### Q14: Partnership Investment [Scenario]
**Source:** ANT Q19 | **Signal Strength:** 9/10

"You've been pursuing a strategic partnership for 6 months. You've had 12 meetings, built a custom demo, and involved your CEO in two calls. The partner keeps expressing interest but delays signing. A new potential partner reaches out proactively — smaller company, but they're ready to start immediately. You:"

○ (A) Stay focused on the original partner — you're too deep in to walk away, and the bigger deal is worth the wait
○ (B) Pursue both simultaneously, even though it'll stretch your team thin
○ (C) Set a two-week deadline for the original partner and shift focus to the new one if they don't commit
○ (D) Drop the original partner and go all-in on the new opportunity — momentum matters more than size

**Why This Question:**
- Interpersonal sunk cost (relationship investment vs. financial)
- Status bias element (bigger partner vs. smaller)
- Option A explicitly names the sunk cost fallacy ("too deep in to walk away")
- Tests opportunity cost awareness and decisiveness under uncertainty

**Eliminated Alternatives:**
- GEM Q22: Project 80% complete but lower ROI — overlaps with professional incentives
- OPAI Q23: Mentoring investment — good but less business-focused

---

#### Q15: Mentoring Investment [Scenario]
**Source:** OPAI Q23 | **Signal Strength:** 8/10

"You've been mentoring a junior team member for a year. Despite significant time invested, performance hasn't improved much. You're deciding whether to continue investing your time. You:"

○ (A) Continue mentoring — improvement takes time
○ (B) Set a clear performance checkpoint and timeline
○ (C) Transition responsibility to someone else
○ (D) Reassign them to a different role better aligned with strengths

**Why This Question:**
- Interpersonal sunk cost with emotional/relational dimension
- Tests willingness to reallocate personal time investment
- All four options are defensible management approaches
- Complements Q13-Q14 by focusing on people investment vs. financial/strategic

**Eliminated Alternatives:**
- None — this is the best people-focused sunk cost scenario across all sources

---

### 6. Financial Risk Tolerance (3 questions)

#### Q16: Probabilistic Gain (80/20) [Risk Trade-off]
**Source:** OPAI Q24 | **Signal Strength:** 10/10

"Choose one option:

○ (A) 80% chance to gain $50,000; 20% chance to gain nothing
○ (B) Guaranteed $38,000

(Assume this is a one-time investment decision.)"

**Why This Question:**
- **TIER 1 ESSENTIAL** — Pure expected value test with no confounding variables
- Expected value of A = $40K (vs. guaranteed $38K) — close enough to reveal risk preference
- Tests Prospect Theory's gain-frame prediction (risk aversion in gains)
- Clean probabilistic framing eliminates ambiguity
- Mathematically literate respondents can calculate EV; reveals if they choose EV or certainty

**Eliminated Alternatives:**
- GEM Q21: 80% chance $15K vs 20% lose $10K — mixed gain/loss complicates interpretation
- ANT Q20: Salary vs. equity — adds career context and timeline ambiguity

---

#### Q17: Mixed Gain/Loss (50/50) [Risk Trade-off]
**Source:** OPAI Q25 | **Signal Strength:** 10/10

"You must choose one:

○ (A) 50% chance to gain $120,000; 50% chance to lose $40,000
○ (B) Guaranteed gain of $35,000

(Assume you can comfortably absorb the potential loss.)"

**Why This Question:**
- **TIER 1 ESSENTIAL** — Tests loss aversion in mixed frame
- Expected value of A = $40K (vs. guaranteed $35K) — reveals if loss frame shifts preference
- "(Assume you can comfortably absorb the loss)" controls for risk capacity
- Pair with Q16 to detect frame-dependent risk tolerance shifts
- Classic behavioral economics construct measurement

**Eliminated Alternatives:**
- None in other sources match this methodological rigor

---

#### Q18: Salary vs. Equity [Risk Trade-off]
**Source:** ANT Q20 | **Signal Strength:** 8/10

"You're choosing between two compensation packages at companies you're equally excited about:

○ Company A: $160K base salary, standard benefits, predictable 3-5% annual raises
○ Company B: $115K base salary + equity stake. If the company hits its targets (which leadership believes is likely), your equity could be worth $200K-$400K in 3-4 years. If it doesn't, the equity is worth nothing.

Which do you choose?"

**Why This Question:**
- Real-world career decision that candidates actually face
- Longer time horizon (3-4 years) tests patience and belief in upside
- Uncertainty phrase ("which leadership believes is likely") adds ambiguity
- Option A total comp over 4 years ≈ $660K; Option B best case ≈ $660-860K — reveals risk vs. upside preference

**Eliminated Alternatives:**
- GEM Q18: Less detailed financial framing (lacks specific equity value ranges)

---

### 7. Career/Reputational Risk (1 question)

#### Q19: Contrarian LinkedIn Post [Scenario]
**Source:** OPAI Q19 | **Signal Strength:** 9/10

"You're considering publishing a strong contrarian opinion on LinkedIn about an industry trend. It could increase your visibility — but may alienate some peers and potential employers. You:"

○ (A) Publish it as written
○ (B) Tone it down to reduce backlash
○ (C) Share it privately with trusted peers first
○ (D) Decide it's not worth the reputational risk

**Why This Question:**
- **TIER 1 ESSENTIAL** — Pure reputational risk without financial confounds
- Specific platform (LinkedIn) and consequence (alienate peers/employers) reduce ambiguity
- Four options reveal different risk mitigation strategies
- Timely and universally relatable in modern professional context
- Tests willingness to prioritize visibility over safety

**Eliminated Alternatives:**
- ANT Q21: "Senior role vs. lateral move" — conflates learning orientation with risk tolerance
- GEM Q18: "Stable vs. startup role" — overlaps with financial risk (Q16-Q18)

---

### 8. Analytical vs. Intuitive Decision-Making (2 questions)

#### Q20: Hiring Decision [Scenario]
**Source:** OPAI Q20 | **Signal Strength:** 9/10

"You're hiring a senior engineer. One candidate has stronger measurable credentials; another gives you a strong intuitive sense of long-term fit, though their resume is less impressive. You:"

○ (A) Choose the stronger resume
○ (B) Choose the candidate who feels like a better long-term fit
○ (C) Design an additional structured test before deciding
○ (D) Involve more stakeholders to triangulate perspectives

**Why This Question:**
- Direct analytical (credentials) vs. intuitive (gut feel) trade-off
- High-stakes decision that reveals true preference under pressure
- Option C and D reveal tolerance for process/delay vs. decisiveness
- Universally applicable scenario across industries

**Eliminated Alternatives:**
- GEM Q20: Nearly identical but less polished phrasing
- ANT Q22: Technical architecture decision — overlaps with structure preference

---

#### Q21: Market Entry Signal [Scenario]
**Source:** ANT Q23 | **Signal Strength:** 9/10

"You're evaluating whether to enter a new market segment. Your data analysis shows modest but positive indicators — the opportunity looks reasonable but not a slam dunk. However, three customers you deeply respect have independently told you this segment is 'where everything is heading.' You:"

○ (A) Trust the customer signal — pattern recognition from smart people in the market is hard to quantify but often right
○ (B) Invest in a deeper quantitative analysis before making a commitment
○ (C) Run a small, time-boxed pilot to generate your own data
○ (D) Weigh both inputs equally and go with whichever direction they converge on

**Why This Question:**
- Tests intuitive (customer signal) vs. analytical (quantitative) preference
- Unique "smart people you respect" framing raises stakes of ignoring intuition
- Strategic decision context (not just tactical hiring)
- Four options reveal different decision-making philosophies

**Eliminated Alternatives:**
- None — this is unique across all three sources

---

### 9. Loss Aversion (1 question)

#### Q22: Side Project Exit [Scenario]
**Source:** OPAI Q21 | **Signal Strength:** 8/10

"You invested personal savings into a side project. It's not failing, but growth is slower than expected. You could exit now with a small loss — or continue for another year with uncertain upside. You:"

○ (A) Exit now and redeploy capital
○ (B) Continue — there's still a path to upside
○ (C) Reduce involvement but keep optionality
○ (D) Seek external funding to extend runway

**Why This Question:**
- Pure loss aversion without sunk cost confound (explicitly "small loss" not large investment)
- Personal financial stake raises emotional investment
- "Slower than expected" is realistically ambiguous (not clear failure)
- Option C tests optionality thinking (modern sophisticated approach)

**Eliminated Alternatives:**
- GEM Q19: Stock loss scenario is more abstract/hypothetical
- ANT Q25: Product line cannibalization overlaps with strategic planning

---

### 10. Overconfidence / Anchoring (2 questions)

#### Q23: Salary Negotiation Anchoring [Scenario]
**Source:** OPAI Q22 | **Signal Strength:** 8/10

"You're negotiating salary. The employer's first offer is lower than expected. You had privately hoped for more but didn't state a number upfront. You:"

○ (A) Counter slightly above their number
○ (B) Counter with your original internal target
○ (C) Ask for a broader compensation review (bonus, equity, flexibility)
○ (D) Accept if it's within a reasonable range

**Why This Question:**
- Tests susceptibility to anchoring bias (option A = anchored to their number)
- Universally relatable scenario
- Option C reveals creative problem-solving vs. linear negotiation
- Low social desirability (all options defensible)

**Eliminated Alternatives:**
- ANT Q26: Revenue forecasting — requires business context not all respondents have
- GEM Q24: Mentor timeline projection — less universally applicable

---

#### Q24: Mentor Timeline Projection [Scenario]
**Source:** GEM Q24 | **Signal Strength:** 7/10

"A reliable mentor tells you that a new market you are entering is 'extremely difficult' and usually takes 2 years to break even. Your internal projections say you can do it in 9 months. You:"

○ (A) Trust your data-driven projections and stick to the 9-month plan
○ (B) Split the difference and re-forecast for 15 months
○ (C) Adopt the mentor's 2-year timeline as the baseline for your budget

**Why This Question:**
- Tests overconfidence (trusting own projections despite expert warning)
- Anchoring bias (mentor's 2 years becomes reference point)
- Option B reveals anchoring susceptibility (splitting difference)
- Planning conservatism vs. aggressive optimism

**Eliminated Alternatives:**
- ANT Q26: More complex scenario but less focused on overconfidence

---

### 11. Emergency Decision-Making (1 question)

#### Q25: Hotfix vs. Full Solution [Scenario]
**Source:** GEM Q25 | **Signal Strength:** 8/10

"An urgent bug is affecting 5% of your users. You can deploy a 'hotfix' in 10 minutes that has a small chance of breaking things for another 2%, or you can wait 4 hours for a fully tested permanent fix. You:"

○ (A) Deploy the 10-minute hotfix immediately to stop the bleeding
○ (B) Wait the 4 hours to ensure no further regressions occur

**Why This Question:**
- Tests decision-making under time pressure with explicit trade-offs
- Specific numbers (5%, 2%, 10 min, 4 hours) eliminate ambiguity
- Reveals risk tolerance in operational crisis
- Both options are defensible engineering decisions

**Eliminated Alternatives:**
- None in other sources test emergency pace under explicit risk trade-off

---

### 12. Confidence Calibration (2 follow-ups)

#### Q26: Confidence Calibration (After Sunk Cost Scenario) [Scale]
**Source:** ANT Q18 (follows Q13) | **Signal Strength:** 8/10

"How confident are you that your answer to the previous question is the best course of action?"

1 (Not confident at all) → 10 (Extremely confident)

**Why This Question:**
- Detects overconfidence by comparing stated confidence to actual decision quality
- Positioned after high-complexity scenario (Q13 — internal tool with 4 options)
- Metacognitive awareness measurement
- Data can be analyzed against behavioral outcomes

---

#### Q27: Confidence Calibration (After Market Entry Scenario) [Scale]
**Source:** ANT Q24 (follows Q21) | **Signal Strength:** 8/10

"How confident are you that your answer to the previous question is the best course of action?"

1 (Not confident at all) → 10 (Extremely confident)

**Why This Question:**
- Second confidence calibration after different scenario type (analytical vs. intuitive)
- Enables comparison of confidence across different decision domains
- Tests consistency of metacognitive accuracy

**Note:** Both ANT and GEM suggest confidence calibrations; OPAI does not. Consensus is to include 2 strategically positioned calibrations (after complex scenarios).

---

---

## DEMOGRAPHICS

### Q28: Age Range
○ 25–30
○ 31–35
○ 36–40
○ 40+

### Q29: Current Role Type
○ Founder / CEO
○ Engineering / Technical
○ Product / Design
○ Marketing / Sales / Growth
○ Consulting / Advisory
○ Other

### Q30: Years of Professional Experience
○ 0–2
○ 3–5
○ 6–10
○ 11–15
○ 16+

### Q31: Industry
○ Tech / SaaS
○ Finance / Fintech
○ Healthcare
○ Education
○ Consulting / Professional Services
○ Other

### Q32: How did you hear about this assessment?
[Open text field]

---

---

## OPTIONAL ENHANCEMENTS

### Methodological Frameworks from Source Documents

#### 1. Cross-Layer Insight Generation (ANT Methodology)

The Anthropic source included a framework for generating insights by combining Layer 1 (behavioral) and Layer 3 (risk/decision) responses:

**Example Insight Patterns:**

- **High assertiveness (Q1-A, Q2-A) + Loss-averse (Q22-B):**
  *"You're decisive in meetings but protective of what you've built — you push hard on new ideas but struggle to let go of existing ones"*

- **Fast pace (Q4-A, Q5-high) + Intuitive decision-maker (Q20-B, Q21-A):**
  *"You trust your pattern recognition and move quickly — this is a superpower until you're in unfamiliar territory where your patterns don't apply"*

- **Relationship-oriented (Q7-B, Q8-B) + Sunk-cost susceptible (Q13-A, Q14-A):**
  *"You invest deeply in people and projects, which builds loyalty — but you may hold on to underperforming initiatives because of the human investment, not the business case"*

**Implementation Note:**
This framework can be operationalized with if/then logic or LLM-generated insights that reference specific question combinations.

---

#### 2. Cognitive Load Testing (GEM Methodology)

The Gemini source emphasized cognitive load considerations:

- **Reverse-coded items:** Minimize use (adds cognitive load) — keep only if essential for construct validity
- **Likert scales:** Use consistent anchors throughout (don't mix "Never/Always" with "Disagree/Agree")
- **Scenario complexity:** Limit each scenario to one primary trade-off (avoid nested decisions)
- **Completion time monitoring:** Track median time per question type to identify friction points

**This Compilation's Approach:**
- Eliminated most reverse-coded items (kept only essential ones)
- Standardized Likert anchors where possible
- Prioritized single-construct scenarios

---

#### 3. Probabilistic Rigor (OPAI Methodology)

The OpenAI source included sophisticated probabilistic framing:

- **Explicit expected value calculations:** Enable detection of mathematical literacy vs. intuitive decision-making
- **Gain-frame vs. mixed-frame comparison:** Test Prospect Theory predictions (Q16 gain-only vs. Q17 mixed gain/loss)
- **Risk capacity controls:** "Assume you can comfortably absorb the loss" eliminates financial constraint confounds

**This Compilation's Approach:**
- Retained OPAI's Q24 and Q25 as Tier 1 questions (highest rigor)
- Added financial specifics to other risk questions where possible
- Maintained explicit probability statements (no vague "likely" language)

---

#### 4. Post-Submission Reflection Prompt (GEM Suggestion)

The Gemini source suggested an optional post-submission screen:

**"What is one decision you made recently that you still think about?"**
*(Optional – this helps us tune your insights)*

**Why Consider This:**
- Provides qualitative data for insight validation
- Low-pressure optional field reduces completion friction
- Enables detection of blind spots in quantitative assessment
- Can be analyzed with LLM for additional signal

**Implementation Decision:**
Optional for MVP (adds <1 min to completion time if used).

---

---

## DEDUPLICATION NOTES

### High-Duplication Constructs (Consolidated)

#### Assertiveness (12 total → 3 selected)
- **Kept:** ANT Q1 (meeting facilitation), ANT Q2 (feedback delivery), OPAI Q3 (proactive leadership)
- **Eliminated:**
  - ANT Q3 (reverse-coded Likert adds cognitive load)
  - ANT Q4 (negotiation overlaps with risk tolerance)
  - GEM Q1 (similar to ANT Q1 but adds stress confound)
  - GEM Q6 (too focused on senior leadership context)
  - GEM Q14 (deadline negotiation overlaps with people/task)
  - OPAI Q1 (similar to ANT Q1 but less balanced phrasing)
  - OPAI Q2 (missed deadline scenario adds conflict management confound)
  - OPAI Q4 (reverse-coded — eliminated per cognitive load principle)

#### Pace Preference (13 total → 3 selected)
- **Kept:** OPAI Q5 (launch vs. analyze), OPAI Q6 (energized by speed), GEM Q2 (productivity rhythm)
- **Eliminated:**
  - ANT Q5 (similar to OPAI Q5 but less clean)
  - ANT Q6 (vague "push for faster timeline" wording)
  - ANT Q7 (meeting action items — too dependent on meeting culture)
  - ANT Q8 (feedback response overlaps with emotional regulation)
  - ANT Q9 ("good today vs great next week" too abstract)
  - GEM Q5 (reverse-coded — adds cognitive load)
  - GEM Q9 (error correction overlaps with risk tolerance)
  - GEM Q13 (version 0.1 vs. 1.0 overlaps with OPAI Q5)
  - OPAI Q7 (reverse-coded — eliminated per cognitive load principle)
  - OPAI Q8 (debate scenario overlaps with assertiveness)

#### People vs. Task (12 total → 3 selected)
- **Kept:** ANT Q10 (team behind schedule), OPAI Q11 (feedback style), OPAI Q10 (1:1 depth)
- **Eliminated:**
  - ANT Q11 (disengaged performer overlaps with leadership style)
  - ANT Q12 (reverse-coded small talk question — adds cognitive load)
  - ANT Q13 (similar to OPAI Q11 but more verbose)
  - GEM Q3 (underperformance adds performance management confound)
  - GEM Q7 (accuracy vs. morale overlaps with feedback style)
  - GEM Q12 (product vs. team too binary/extreme)
  - GEM Q15 (reverse-coded small talk — adds cognitive load)
  - OPAI Q9 (similar to ANT Q10 but less balanced)
  - OPAI Q12 (reverse-coded "results vs. harmony" — extreme framing)

#### Structure Preference (9 total → 3 selected)
- **Kept:** ANT Q15 (planning approach), GEM Q8 (systems creation), ANT Q14 (empty calendar)
- **Eliminated:**
  - ANT Q16 (frequency of written plans overlaps with Q15)
  - GEM Q4 (work week start too low-stakes)
  - GEM Q11 (minimize surprises vs. maximize opportunity — less actionable)
  - OPAI Q13 (work from plan vs. respond flexibly — overlaps with ANT Q15)
  - OPAI Q14 (creative problem-solving overlaps with pace preference)
  - OPAI Q15 (loosely vs. tightly scheduled overlaps with ANT Q14)

---

### Moderate-Duplication Constructs (Best Version Selected)

#### Hiring Decision (2 versions → 1 selected)
- **Kept:** OPAI Q20 (senior engineer with 4 options)
- **Eliminated:**
  - GEM Q20 (nearly identical but less polished phrasing)

#### Sunk Cost Bias (6 scenarios → 3 selected)
- **Kept:** ANT Q17 (internal tool with detailed financials), ANT Q19 (partnership investment), OPAI Q23 (mentoring investment)
- **Eliminated:**
  - GEM Q16 (side project less detailed than ANT Q17)
  - GEM Q22 (project 80% complete overlaps with professional incentives)
  - OPAI Q16 (side project similar to GEM Q16 but weaker financial specifics)

#### Financial Risk Tolerance (5 questions → 3 selected)
- **Kept:** OPAI Q24 (probabilistic gain 80/20), OPAI Q25 (mixed gain/loss 50/50), ANT Q20 (salary vs. equity)
- **Eliminated:**
  - GEM Q18 (stable vs. startup less detailed than ANT Q20)
  - GEM Q21 (80% gain with 20% loss less clean than OPAI Q24-Q25)

---

### Low-Duplication Constructs (Unique Questions Retained)

- **Career/Reputational Risk:** OPAI Q19 (LinkedIn contrarian post) — unique construct
- **Market Entry Decision:** ANT Q23 (customer signal vs. data) — unique analytical/intuitive test
- **Loss Aversion:** OPAI Q21 (side project exit) — distinct from sunk cost scenarios
- **Anchoring Bias:** OPAI Q22 (salary negotiation), GEM Q24 (mentor timeline) — both unique angles
- **Emergency Decision:** GEM Q25 (hotfix vs. full solution) — unique time-pressure scenario
- **Confidence Calibration:** ANT Q18 & Q24 — strategic positioning after complex scenarios

---

---

## QUALITY ASSESSMENT MATRIX

| Question ID | Source | Construct | Signal Strength | Duplication Risk | Recommendation |
|-------------|--------|-----------|-----------------|------------------|----------------|
| **LAYER 1: BEHAVIORAL DYNAMICS** |
| ANT Q1 | ANT | Assertiveness | 9/10 | Medium | **KEEP (Q1)** |
| ANT Q2 | ANT | Assertiveness | 8/10 | Medium | **KEEP (Q2)** |
| ANT Q3 | ANT | Assertiveness (reverse) | 6/10 | High | OMIT (cognitive load) |
| ANT Q4 | ANT | Assertiveness | 7/10 | High | OMIT (overlaps risk) |
| OPAI Q3 | OPAI | Assertiveness | 7/10 | Medium | **KEEP (Q3)** |
| GEM Q1 | GEM | Assertiveness | 7/10 | High | OMIT (similar to ANT Q1) |
| GEM Q6 | GEM | Assertiveness | 6/10 | Medium | OMIT (narrow context) |
| GEM Q14 | GEM | Assertiveness | 6/10 | High | OMIT (overlaps people/task) |
| OPAI Q1 | OPAI | Assertiveness | 7/10 | High | OMIT (less balanced than ANT Q1) |
| OPAI Q2 | OPAI | Assertiveness | 6/10 | High | OMIT (adds conflict confound) |
| OPAI Q4 | OPAI | Assertiveness (reverse) | 5/10 | High | OMIT (cognitive load) |
| ANT Q5 | ANT | Pace | 8/10 | High | OMIT (similar to OPAI Q5) |
| ANT Q6 | ANT | Pace | 6/10 | Medium | OMIT (vague wording) |
| ANT Q7 | ANT | Pace | 6/10 | Medium | OMIT (culture-dependent) |
| ANT Q8 | ANT | Pace | 6/10 | High | OMIT (overlaps regulation) |
| ANT Q9 | ANT | Pace | 5/10 | High | OMIT (too abstract) |
| OPAI Q5 | OPAI | Pace | 9/10 | Medium | **KEEP (Q4)** |
| OPAI Q6 | OPAI | Pace | 8/10 | Low | **KEEP (Q5)** |
| GEM Q2 | GEM | Pace | 7/10 | Low | **KEEP (Q6)** |
| GEM Q5 | GEM | Pace (reverse) | 6/10 | High | OMIT (cognitive load) |
| GEM Q9 | GEM | Pace | 6/10 | High | OMIT (overlaps risk) |
| GEM Q13 | GEM | Pace | 7/10 | High | OMIT (similar to OPAI Q5) |
| OPAI Q7 | OPAI | Pace (reverse) | 6/10 | High | OMIT (cognitive load) |
| OPAI Q8 | OPAI | Pace | 6/10 | High | OMIT (overlaps assertiveness) |
| ANT Q10 | ANT | People vs Task | 9/10 | Medium | **KEEP (Q7)** |
| ANT Q11 | ANT | People vs Task | 7/10 | High | OMIT (overlaps leadership) |
| ANT Q12 | ANT | People vs Task (reverse) | 6/10 | High | OMIT (cognitive load) |
| ANT Q13 | ANT | People vs Task | 7/10 | High | OMIT (verbose, overlaps Q8) |
| OPAI Q11 | OPAI | People vs Task | 8/10 | Medium | **KEEP (Q8)** |
| OPAI Q10 | OPAI | People vs Task | 7/10 | Low | **KEEP (Q9)** |
| GEM Q3 | GEM | People vs Task | 7/10 | High | OMIT (adds confound) |
| GEM Q7 | GEM | People vs Task | 7/10 | High | OMIT (overlaps Q8) |
| GEM Q12 | GEM | People vs Task | 6/10 | High | OMIT (too binary) |
| GEM Q15 | GEM | People vs Task (reverse) | 5/10 | High | OMIT (cognitive load) |
| OPAI Q9 | OPAI | People vs Task | 7/10 | High | OMIT (less balanced than ANT Q10) |
| OPAI Q12 | OPAI | People vs Task (reverse) | 6/10 | High | OMIT (extreme framing) |
| ANT Q15 | ANT | Structure | 9/10 | Medium | **KEEP (Q10)** |
| ANT Q16 | ANT | Structure | 7/10 | High | OMIT (overlaps Q10) |
| ANT Q14 | ANT | Structure | 7/10 | Medium | **KEEP (Q12)** |
| GEM Q8 | GEM | Structure | 8/10 | Low | **KEEP (Q11)** |
| GEM Q4 | GEM | Structure | 6/10 | High | OMIT (low stakes) |
| GEM Q11 | GEM | Structure | 6/10 | Medium | OMIT (less actionable) |
| OPAI Q13 | OPAI | Structure | 7/10 | High | OMIT (overlaps ANT Q15) |
| OPAI Q14 | OPAI | Structure | 6/10 | High | OMIT (overlaps pace) |
| OPAI Q15 | OPAI | Structure | 6/10 | High | OMIT (overlaps ANT Q14) |
| **LAYER 3: RISK & DECISION ARCHITECTURE** |
| ANT Q17 | ANT | Sunk Cost | 10/10 | Medium | **KEEP (Q13)** ⭐ |
| ANT Q18 | ANT | Confidence Calibration | 8/10 | Low | **KEEP (Q26)** |
| ANT Q19 | ANT | Sunk Cost | 9/10 | Medium | **KEEP (Q14)** |
| ANT Q24 | ANT | Confidence Calibration | 8/10 | Low | **KEEP (Q27)** |
| GEM Q16 | GEM | Sunk Cost | 7/10 | High | OMIT (less detailed than ANT Q17) |
| GEM Q22 | GEM | Sunk Cost | 7/10 | High | OMIT (incentives confound) |
| OPAI Q16 | OPAI | Sunk Cost | 7/10 | High | OMIT (similar to GEM Q16) |
| OPAI Q23 | OPAI | Sunk Cost | 8/10 | Low | **KEEP (Q15)** |
| OPAI Q24 | OPAI | Financial Risk (prob) | 10/10 | Low | **KEEP (Q16)** ⭐ |
| OPAI Q25 | OPAI | Financial Risk (mixed) | 10/10 | Low | **KEEP (Q17)** ⭐ |
| ANT Q20 | ANT | Financial Risk | 8/10 | Medium | **KEEP (Q18)** |
| GEM Q18 | GEM | Financial Risk | 7/10 | High | OMIT (less detailed than ANT Q20) |
| GEM Q21 | GEM | Financial Risk | 7/10 | High | OMIT (less clean than OPAI Q24-25) |
| OPAI Q19 | OPAI | Reputational Risk | 9/10 | Low | **KEEP (Q19)** ⭐ |
| ANT Q21 | ANT | Career Risk | 7/10 | Medium | OMIT (confounds learning with risk) |
| GEM Q18 | GEM | Career Risk | 6/10 | High | OMIT (overlaps financial) |
| OPAI Q20 | OPAI | Analytical vs Intuitive | 9/10 | Medium | **KEEP (Q20)** |
| GEM Q20 | GEM | Analytical vs Intuitive | 8/10 | High | OMIT (duplicate of OPAI Q20) |
| ANT Q22 | ANT | Analytical vs Intuitive | 7/10 | Medium | OMIT (overlaps structure) |
| ANT Q23 | ANT | Analytical vs Intuitive | 9/10 | Low | **KEEP (Q21)** |
| OPAI Q21 | OPAI | Loss Aversion | 8/10 | Low | **KEEP (Q22)** |
| GEM Q19 | GEM | Loss Aversion | 6/10 | Medium | OMIT (too abstract) |
| ANT Q25 | ANT | Loss Aversion | 7/10 | High | OMIT (overlaps strategic planning) |
| OPAI Q22 | OPAI | Anchoring | 8/10 | Low | **KEEP (Q23)** |
| GEM Q24 | GEM | Overconfidence/Anchoring | 7/10 | Low | **KEEP (Q24)** |
| ANT Q26 | ANT | Overconfidence | 7/10 | Medium | OMIT (requires business context) |
| GEM Q25 | GEM | Emergency Decision | 8/10 | Low | **KEEP (Q25)** |
| GEM Q17 | GEM | Confidence Calibration | 7/10 | Medium | OMIT (less strategic than ANT Q18/Q24) |
| GEM Q23 | GEM | Confidence Calibration | 7/10 | Medium | OMIT (less strategic than ANT Q18/Q24) |

**Legend:**
- ⭐ = Tier 1 Essential (highest signal, lowest duplication)
- **KEEP** = Included in compiled assessment
- OMIT = Eliminated due to duplication, cognitive load, or lower signal

---

---

## IMPLEMENTATION GUIDANCE

### For MVP Development

1. **Prioritize Tier 1 Questions First**
   - If reducing further for ultra-short MVP (10 min target), keep all questions marked ⭐ in the matrix
   - Tier 1 set: Q1, Q4, Q7, Q13, Q16, Q17, Q19 = 7 questions + 2 calibrations + 5 demographics = ~10 min

2. **Maintain Construct Balance**
   - If cutting questions, remove evenly across dimensions (don't eliminate entire constructs)
   - Minimum viable coverage: 2 questions per behavioral dimension + 1-2 per bias type

3. **Preserve Methodological Rigor**
   - Keep paired questions (Q16/Q17 gain vs. mixed frame, Q26/Q27 confidence calibrations)
   - Maintain specific financial anchors (don't simplify to vague amounts)
   - Preserve explicit probabilities in risk questions

4. **Test Completion Time**
   - Pilot with 10-15 respondents to validate ~12-15 min target
   - Monitor median time per question type (Likert faster than scenarios)
   - Identify drop-off points if completion rate falls

5. **Scoring Logic Development**
   - Layer 1 (Q1-Q12): Score on 0-100 scale per dimension (Assertiveness, Pace, People/Task, Structure)
   - Layer 3 (Q13-Q27): Binary flags (sunk-cost-susceptible, risk-averse, analytical, etc.) plus confidence scores
   - Cross-layer insights: Use ANT's framework to combine behavioral + decision patterns

6. **Insight Generation**
   - Draft 3-5 templated insight patterns per construct combination
   - Test LLM generation with sample responses
   - Validate insights with pilot users for resonance and accuracy

---

### Verification Checklist

- ✅ **Coverage:** All 4 behavioral dimensions covered (Assertiveness, Pace, People/Task, Structure)
- ✅ **Coverage:** All major bias types covered (Sunk Cost, Loss Aversion, Anchoring, Overconfidence)
- ✅ **Coverage:** Financial, reputational, and career risk tolerance tested
- ✅ **Coverage:** Analytical vs. intuitive decision-making tested
- ✅ **Duplication:** No redundant questions measuring identical constructs
- ✅ **Traceability:** Every kept question links to source document
- ✅ **Rationale:** Every kept question has "Why This Question" explanation
- ✅ **Alternatives:** Eliminated alternatives documented with reasoning
- ✅ **Rigor:** Tier 1 essential questions all included
- ✅ **Methodology:** Frameworks from ANT, GEM, and OPAI captured
- ✅ **Actionability:** Quality matrix enables informed question selection

---

### Success Metrics

**Quantitative:**
- Completion rate >80%
- Median completion time 12-15 minutes
- Dropout rate <15%
- Internal consistency (Cronbach's alpha >0.70 for Layer 1 dimensions)

**Qualitative:**
- Respondent feedback: "This felt relevant and insightful" vs. "personality test fluff"
- Insight resonance: >70% agree insights accurately describe them
- Actionability: Users can name 1-2 specific behavioral changes after reading insights

---

**END OF COMPILED DOCUMENT**

---

## Document History

- **v1.0 (Feb 15, 2026):** Initial compilation from ANT, GEM, OPAI sources
- **Sources:**
  - `docs/prompts/phase-0/ant.md` (Anthropic Claude suggestions)
  - `docs/prompts/phase-0/gem.md` (Google Gemini suggestions)
  - `docs/prompts/phase-0/opai.md` (OpenAI GPT suggestions)
- **Compiled by:** Phase 0 Assessment Team
- **Next Review:** After MVP pilot with 50+ respondents
