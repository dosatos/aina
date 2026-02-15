# Phase 0 Assessment: Overview & Implementation Guidance

**Document Version:** 1.0
**Last Updated:** February 15, 2026
**Sources Analyzed:** Anthropic Claude (ant.md), Google Gemini (gem.md), OpenAI GPT (opai.md)

---

## Executive Summary

### Purpose and Scope

This document set represents a curated compilation of the highest-quality Phase 0 assessment questions derived from three independent AI-generated suggestion sets. The original documents contained approximately 90 total questions with ~40% construct overlap. This compilation reduces that to **25-30 strategically selected questions** that maximize signal while minimizing redundancy and completion time.

**Target Completion Time:** 12-15 minutes
**Question Distribution:** 12 behavioral dynamics + 15 risk/decision architecture + 5 demographics

### Document Structure

- **00-overview-and-guidance.md** (this file): Purpose, usage instructions, implementation guidance
- **01-behavioral-dynamics-questions.md**: Layer 1 questions (Q1-Q12) with full rationale
- **02-risk-decision-questions.md**: Layer 3 questions (Q13-Q27) + demographics with full rationale
- **03-methodology-and-analysis.md**: Optional enhancements, deduplication notes, quality matrix

### Relationship to Main Prompt Generator

- **Main Prompt** (`phase0-question-generator.md`): Instructions for AI systems to generate assessment questions
- **These Documents**: Curated examples and best practices from actual AI outputs using that prompt
- **Together**: "Instructions + Proven Examples" for MVP implementation

---

## Quality Criteria for Selection

Questions were evaluated on:

1. **Signal Strength** (1-10): How effectively does this question reveal the target construct?
2. **Uniqueness**: Does this question capture something other questions miss?
3. **Specificity**: Are the scenarios concrete enough to reveal true preferences?
4. **Forced Trade-offs**: Do options represent equally defensible choices?
5. **Natural Language**: Does it sound like a real decision someone would face?
6. **Low Social Desirability**: Are both/all options acceptable to choose?
7. **Actionability**: Can responses drive meaningful personalized insights?

---

## Key Findings from Analysis

### Duplication Summary

- **Total Questions Analyzed:** ~90 across 3 files (30 each)
- **Duplication Rate:** ~40% of constructs overlap
- **Optimal Consolidated Set:** 25-30 questions (down from 90)

### Tier 1 Essential Questions (Highest Signal, Lowest Duplication)

Marked with ⭐ in the question files:

1. **ANT Q17** (now Q13) - Sunk cost with detailed financial anchors ($30K vs $500/month)
2. **OPAI Q24-Q25** (now Q16-Q17) - Dual probability scenarios testing Prospect Theory
3. **OPAI Q19** (now Q19) - Reputational risk (LinkedIn contrarian post)

### High-Duplication Areas (Consolidated)

- **Assertiveness**: 12 total → 3 selected
- **Pace Preference**: 13 total → 3 selected
- **People vs Task**: 12 total → 3 selected
- **Structure**: 9 total → 3 selected

---

## Implementation Guidance

### For MVP Development

#### 1. Prioritize Tier 1 Questions First

If reducing further for ultra-short MVP (10 min target), keep all questions marked ⭐:
- **Minimum viable set**: Q1, Q4, Q7, Q13, Q16, Q17, Q19 = 7 questions + 2 calibrations + 5 demographics ≈ 10 min

#### 2. Maintain Construct Balance

If cutting questions, remove evenly across dimensions:
- Don't eliminate entire constructs (e.g., don't remove all assertiveness questions)
- **Minimum coverage**: 2 questions per behavioral dimension + 1-2 per bias type

#### 3. Preserve Methodological Rigor

- Keep paired questions (Q16/Q17 gain vs. mixed frame, Q26/Q27 confidence calibrations)
- Maintain specific financial anchors (don't simplify to vague amounts)
- Preserve explicit probabilities in risk questions

#### 4. Test Completion Time

- Pilot with 10-15 respondents to validate ~12-15 min target
- Monitor median time per question type (Likert faster than scenarios)
- Identify drop-off points if completion rate falls

#### 5. Scoring Logic Development

**Layer 1 (Q1-Q12): Dimensional Scores**
- Score on 0-100 scale per dimension:
  - Assertiveness (Q1-Q3)
  - Pace Preference (Q4-Q6)
  - People vs Task Orientation (Q7-Q9)
  - Structure Preference (Q10-Q12)
- Weight forced-choice and Likert responses appropriately
- Consider reverse-coding where noted

**Layer 3 (Q13-Q27): Binary Flags + Confidence**
- Binary flags: sunk-cost-susceptible, risk-averse, loss-averse, analytical, etc.
- Confidence scores from Q26-Q27 (metacognitive awareness)
- Financial risk profile from Q16-Q18 (risk-seeking, risk-neutral, risk-averse)

**Cross-Layer Insights**
- Use frameworks in `03-methodology-and-analysis.md` to combine patterns
- Example: High assertiveness + loss averse → "Decisive but protective of existing investments"

#### 6. Insight Generation

- Draft 3-5 templated insight patterns per construct combination
- Test LLM generation with sample responses
- Validate insights with pilot users for resonance and accuracy
- See "Cross-Layer Insight Generation" in `03-methodology-and-analysis.md` for examples

---

## Verification Checklist

Use this before finalizing your MVP question set:

- ✅ **Coverage - Behavioral:** All 4 dimensions covered (Assertiveness, Pace, People/Task, Structure)
- ✅ **Coverage - Risk:** All major bias types covered (Sunk Cost, Loss Aversion, Anchoring, Overconfidence)
- ✅ **Coverage - Risk Types:** Financial, reputational, and career risk tolerance tested
- ✅ **Coverage - Decision Style:** Analytical vs. intuitive decision-making tested
- ✅ **Duplication:** No redundant questions measuring identical constructs
- ✅ **Traceability:** Every kept question links to source document
- ✅ **Rationale:** Every kept question has "Why This Question" explanation
- ✅ **Alternatives:** Eliminated alternatives documented with reasoning
- ✅ **Rigor:** Tier 1 essential questions (⭐) all included
- ✅ **Methodology:** Frameworks from ANT, GEM, and OPAI captured
- ✅ **Actionability:** Quality matrix enables informed question selection

---

## Success Metrics

### Quantitative

- **Completion rate:** >80%
- **Median completion time:** 12-15 minutes
- **Dropout rate:** <15%
- **Internal consistency:** Cronbach's alpha >0.70 for Layer 1 dimensions

### Qualitative

- **Respondent feedback:** "This felt relevant and insightful" vs. "personality test fluff"
- **Insight resonance:** >70% agree insights accurately describe them
- **Actionability:** Users can name 1-2 specific behavioral changes after reading insights

---

## Quick Reference: Question Distribution

### Layer 1: Behavioral Dynamics (12 questions)

| Dimension | Questions | Format |
|-----------|-----------|--------|
| Assertiveness | Q1-Q3 | 2 Forced-Choice + 1 Likert |
| Pace Preference | Q4-Q6 | 2 Forced-Choice + 1 Likert |
| People vs Task | Q7-Q9 | 2 Forced-Choice + 1 Likert |
| Structure Preference | Q10-Q12 | 2 Forced-Choice + 1 Likert |

### Layer 3: Risk & Decision Architecture (15 questions)

| Construct | Questions | Format |
|-----------|-----------|--------|
| Sunk Cost Bias | Q13-Q15 | 3 Scenarios (4 options each) |
| Financial Risk Tolerance | Q16-Q18 | 3 Risk Trade-offs |
| Career/Reputational Risk | Q19 | 1 Scenario (4 options) |
| Analytical vs Intuitive | Q20-Q21 | 2 Scenarios (4 options each) |
| Loss Aversion | Q22 | 1 Scenario (4 options) |
| Overconfidence/Anchoring | Q23-Q24 | 2 Scenarios (3-4 options) |
| Emergency Decision | Q25 | 1 Scenario (2 options) |
| Confidence Calibration | Q26-Q27 | 2 Scales (1-10) |

### Demographics (5 questions)

- Age range, Current role, Years of experience, Industry, How did you hear about this

---

## Usage Recommendations

### When to Use This Compilation

**Primary Use Case:**
When generating actual MVP questions, use this compilation to:
1. Select specific questions from Tier 1 & 2
2. Understand why certain questions were chosen over alternatives
3. Reference methodological frameworks for insight generation
4. Make informed trade-offs between coverage and completion time

**Secondary Use Cases:**
- Validate new questions against quality criteria
- Understand construct coverage and duplication patterns
- Reference best practices from multiple AI generation approaches

### How to Navigate These Documents

1. **Start here** (00-overview-and-guidance.md) - Understand context and implementation strategy
2. **Browse questions** (01 & 02) - Review actual questions with rationale
3. **Deep dive** (03-methodology-and-analysis.md) - Understand frameworks and see full deduplication analysis

---

## Next Steps After MVP Launch

### Post-Launch Analysis

1. **Completion Time Validation**
   - Compare actual median time to 12-15 min target
   - Identify questions with unexpectedly long completion times
   - Consider simplifying or removing high-friction questions

2. **Internal Consistency Testing**
   - Calculate Cronbach's alpha for each Layer 1 dimension
   - If α < 0.70, review question alignment within dimension
   - Consider removing questions that don't correlate with dimension

3. **Insight Resonance Testing**
   - Survey respondents: "How accurately do these insights describe you?" (1-10)
   - Target: >70% rate 7+ out of 10
   - Collect qualitative feedback on most/least resonant insights

4. **Predictive Validity (Long-term)**
   - Track if assessment predictions correlate with actual behavior
   - Example: Do people rated "high pace" actually launch faster?
   - Adjust scoring weights based on predictive performance

### Iteration Priorities

**If completion rate is low (<80%):**
- Reduce total questions to 20-22 (remove lowest signal questions from each dimension)
- Simplify scenario complexity (reduce 4-option scenarios to 3 options)
- Add progress indicator to reduce uncertainty about time commitment

**If insights feel generic:**
- Review cross-layer insight generation framework (see `03-methodology-and-analysis.md`)
- Increase specificity in templated insights
- Add more conditional logic based on question combinations

**If dropout happens at specific questions:**
- Review those questions for cognitive load, ambiguity, or sensitivity
- Consider reframing or replacing with eliminated alternatives
- Test revised versions with small cohort before full deployment

---

## Document History

- **v1.0 (Feb 15, 2026):** Initial compilation from ANT, GEM, OPAI sources
- **Sources:**
  - `docs/prompts/phase-0/ant.md` (Anthropic Claude suggestions)
  - `docs/prompts/phase-0/gem.md` (Google Gemini suggestions)
  - `docs/prompts/phase-0/opai.md` (OpenAI GPT suggestions)
- **Compiled by:** Phase 0 Assessment Team
- **Next Review:** After MVP pilot with 50+ respondents

---

## Contact & Feedback

For questions about this compilation or to report issues:
- Review full deduplication analysis in `03-methodology-and-analysis.md`
- Reference quality matrix for alternative question options
- Consult source files (`ant.md`, `gem.md`, `opai.md`) for additional context
