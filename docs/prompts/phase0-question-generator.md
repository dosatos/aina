# AI Prompt: Generate Phase 0 MVP Assessment Questions

You are an expert psychometrician and assessment designer. Your task is to create 30 high-quality assessment questions for a self-evaluation platform's MVP validation. These questions will be used in a Google Form to test whether people complete the assessment and find the results insightful enough to share.

## Target Audience
- Age: 25-40
- Profile: Career-oriented professionals, founders, engineers, analytical types
- Context: They're taking this to gain insight into their behavioral patterns and decision-making style
- Completion time goal: 15-20 minutes total (30 questions)
  - Layer 1 (15 questions): 7-9 minutes (30-40 seconds each)
  - Layer 3 (10 questions): 8-10 minutes (60-90 seconds for scenarios)
  - Demographics (5 questions): 1-2 minutes

---

## Part 1: Layer 1 - Behavioral Dynamics (15 questions)

### What This Layer Measures

**Purpose:** How you naturally behave in social and professional settings. Answers the question: "How do I show up — and why do people experience me the way they do?"

**Dimensions to Evaluate:**
1. **Assertiveness spectrum:** Directive ↔ Accommodating
2. **Pace preference:** Fast/action-oriented ↔ Deliberate/reflective
3. **People orientation:** Task-focused ↔ Relationship-focused
4. **Structure preference:** Spontaneous ↔ Systematic

**Research Foundation:** Big Five (OCEAN) via IPIP public domain items + DISC behavioral theory. You must draw from established public domain personality research, not proprietary frameworks.

### Question Format Requirements

**Mix breakdown:**
- 10 forced-choice pairs (67%)
- 5 Likert scale items (33%)

**Note:** Open-ended questions significantly reduce completion rates in Google Forms. All Layer 1 questions should use structured formats (forced-choice or Likert). If you want to include an optional reflection question, place it at the very end after demographics.

**Forced-choice structure:** Present two equally valid options that force a trade-off. Both should be neutral or positive to avoid social desirability bias.

**Example forced-choice (GOOD):**
> "In team meetings, you're more likely to:
> - (A) Push for a decision quickly, even if not everyone agrees
> - (B) Take time to ensure everyone feels heard before deciding"

**Example Likert (GOOD):**
> "At a work event with strangers, how often do you seek out new people to connect with rather than staying with familiar faces?"
> - Never / Rarely / Sometimes / Often / Always

**Likert scale guidance:**
For Likert items, use **frequency scales** (Never → Always) or **intensity scales** (Not at all like me → Very much like me) rather than Agree/Disagree scales. Match the scale type to what's being measured: behaviors use frequency, beliefs use agreement.

### Design Principles - CRITICAL

**✅ DO:**
- Be **specific and contextual** - use concrete scenarios people can visualize
- Use workplace/professional contexts (not abstract personality traits)
- Include reverse-coded items (some measure high, some measure low on the same dimension)
- Make both options in forced-choice questions equally "good" or neutral
- Vary question formats to prevent pattern answering

**❌ DON'T:**
- Use clinical language ("I am extroverted" - too abstract)
- Create obvious "right" answers ("I care about others' feelings" - everyone says yes)
- Use jargon or academic terms ("I exhibit high conscientiousness")
- Make questions that are clearly measuring the same thing in the same way
- Create questions where one option is clearly superior

**Example of BAD question:**
> "I am a people person" (too vague, clinical, socially desirable answer)

**Example of GOOD question:**
> "When starting a new project, I'm more likely to:
> - (A) Jump in and figure it out as I go
> - (B) Map out a detailed plan before taking action"

### Coverage Requirements

Make sure the 15 questions collectively measure all 4 dimensions:
- 4 questions on assertiveness/directiveness
- 4 questions on pace/tempo
- 4 questions on people vs. task orientation
- 3 questions on structure/spontaneity

**Reverse coding:**
- **For Likert items only:** Include 2-3 reverse-coded items to detect acquiescence bias. For example, if one item measures "I enjoy taking charge in group settings," include another like "I prefer to let others lead while I contribute from the sidelines."
- **For forced-choice items:** These are inherently bipolar - no additional reverse coding needed.

---

## Part 2: Layer 3 - Risk & Decision Architecture (10 questions)

### What This Layer Measures

**Purpose:** How you make decisions under uncertainty and where your cognitive blind spots live. Answers: "How do I actually make decisions — and where am I systematically wrong?"

**Dimensions to Evaluate:**
1. **Risk tolerance across domains:** Financial, career, social, reputational, intellectual
2. **Cognitive bias susceptibility:** Sunk cost, overconfidence, loss aversion, confirmation bias, anchoring
3. **Decision style:** Analytical vs. intuitive, speed vs. accuracy trade-offs
4. **Avoidance vs. approach:** Do they lean in or defer/delay?

**Research Foundation:** Kahneman & Tversky's prospect theory and behavioral economics research (public domain).

### Question Format Requirements

**All questions should be scenario-based simulations** - mini case studies with no obvious "right" answer. These measure revealed preferences, not stated preferences.

**Structure:**
- 7 realistic scenarios with multiple-choice responses
- 2 risk trade-off questions with probability
- 1 confidence calibration follow-up (not a separate question, follows a key scenario)

### Scenario Design Principles

**✅ DO:**
- Present **realistic, specific scenarios** the target audience would face
- Vary domains: financial, career/professional, social/team, reputational
- Include contextual details (time pressure, stakes, constraints)
- Create multiple defensible answers (no obviously right choice)
- Add a confidence rating after 2-3 key scenarios: "How confident are you in this decision?"

**❌ DON'T:**
- Use extreme or unrealistic scenarios
- Make one option clearly superior
- Create hypothetical scenarios too far removed from professional life
- Telegraph which bias you're testing
- State the bias explicitly in answer options (e.g., "you've invested too much to quit now" for sunk cost). Make the reasoning sound plausible and rational.

**Example GOOD scenario (tests sunk cost bias):**
> "You've spent 4 months building a feature for your product. Initial user testing shows weak engagement, but you believe with a few more iterations it could work. A new opportunity emerges that looks more promising but requires starting from scratch. Your team can only focus on one. You:
> - (A) Continue refining the current feature - you've learned a lot about what users need
> - (B) Run a quick parallel test to compare both approaches
> - (C) Pivot to the new opportunity and apply your learnings there
> - (D) Step back and get an outside perspective before deciding"

**Example GOOD risk trade-off (tests risk tolerance in financial domain):**
> "You're offered two job opportunities with similar total expected value:
> - Company A: $140K salary, stable, established company
> - Company B: $100K salary + equity that has a 40% chance of being worth $100K in 3 years, 60% chance of being worth $0
>
> Which do you choose?"

*(Company A EV = $140K, Company B EV = $100K + $40K = $140K)*

**Risk trade-off guidance:**
For risk trade-off questions, ensure expected values are approximately equal. The goal is to measure risk tolerance, not mathematical ability. Your target audience (analytical professionals) will calculate EVs.

**Example confidence calibration:**
> After a scenario: "On a scale of 1-10, how confident are you that this was the right decision?"

### Coverage Requirements

Make sure the 10 questions collectively cover:
- 2 scenarios testing sunk cost bias
- 2 scenarios testing risk tolerance (1 financial, 1 career/reputational)
- 2 scenarios testing analytical vs. intuitive decision-making
- 1 scenario testing loss aversion
- 1 scenario testing overconfidence or anchoring
- 2 risk trade-off questions with balanced probabilities

**Note:** Some overlap is acceptable (e.g., a risk tolerance scenario can also reveal analytical vs intuitive style).

---

## Part 3: Demographics (5 questions)

**Keep these simple and non-invasive:**

1. Age range (25-30, 31-35, 36-40, 40+)
2. Current role type (Founder/CEO, Engineering/Technical, Product/Design, Marketing/Sales, Consultant, Other)
3. Years of professional experience (0-2, 3-5, 6-10, 11-15, 16+)
4. Industry (Tech/SaaS, Finance, Healthcare, Education, Consulting, Other)
5. "How did you hear about this assessment?" (Open text field)

---

## Validation Checklist

Before finalizing the questions, verify:

✅ **Completion time:** Should take 15-20 minutes realistically. Scenario questions take longer than quick-response items.
✅ **Specificity:** Every question uses concrete scenarios, not abstract traits
✅ **Bias mitigation:** No obvious "right" answers; forced-choice options are balanced
✅ **Variety:** Mix of formats (forced-choice, Likert, scenarios, confidence ratings)
✅ **Coverage:** All dimensions are measured across the question set
✅ **Reverse coding:** At least 2 items measure the opposite end of a spectrum
✅ **Professional context:** Questions use workplace/career scenarios relevant to target audience
✅ **No jargon:** Accessible language, no academic or clinical terms
✅ **Google Form compatible:** All questions can be easily formatted in Google Forms (multiple choice, radio buttons, scales)
✅ **Response variance:** After pilot testing (20-30 people), verify that responses distribute across all options. If >70% choose the same answer for any question, revise it.

---

## Output Format

Please generate the questions in this format:

```
## LAYER 1: BEHAVIORAL DYNAMICS

Q1 [Forced-Choice - Assertiveness]
"In team meetings, you're more likely to:"
○ (A) Push for a decision quickly, even if not everyone agrees
○ (B) Take time to ensure everyone feels heard before deciding

Q2 [Likert Scale - Pace Preference]
"When facing a tight deadline, I prefer to:"
- Strongly Disagree / Disagree / Neutral / Agree / Strongly Agree
*"Act quickly and course-correct later rather than analyzing all options first"*

[Continue for all 15 Layer 1 questions...]

## LAYER 3: RISK & DECISION ARCHITECTURE

Q16 [Scenario - Sunk Cost Bias]
"You've spent 4 months building a feature..."
○ (A) Double down on the current feature
○ (B) Run both in parallel
○ (C) Cut losses and pivot
○ (D) Ask a colleague to evaluate first

Q17 [Confidence Calibration]
"How confident are you in your answer to Q16?"
[1-10 scale]

[Continue for all 10 Layer 3 questions...]

## DEMOGRAPHICS

Q26: Age range...
Q27: Current role type...
[Continue for all 5 demographic questions...]
```

---

## Additional Context: What Happens After

These questions will be used to:
1. Test if people complete a 15-minute assessment (target: 70%+ completion)
2. Generate personalized insights using an LLM (Claude/GPT-4)
3. Measure if results are shareable (target: 60%+ share their results)
4. Validate the core product hypothesis before building the platform

The insights generated from these questions should reveal:
- **Cross-layer patterns:** "Your high assertiveness + risk-averse financial style = you're bold in meetings but conservative with money"
- **Specific, actionable observations:** Not "you're an extrovert" but "you push for speed in decisions but this creates friction with deliberate collaborators"
- **Blind spots:** Where their decision-making systematically breaks down

**Quality bar:** The questions should be good enough that when results are generated, people react with "I feel seen" and want to share their insights on LinkedIn.

---

## Now Generate the Questions

Using all the guidelines above, please generate 30 assessment questions (15 Layer 1 + 10 Layer 3 + 5 Demographics) optimized for:
- Target audience: career-oriented professionals, founders, engineers (25-40 age range)
- Completion time: 12-15 minutes
- Platform: Google Forms
- Goal: Validate core hypothesis (will people complete it, find it insightful, and share it?)

Format your output as shown in the "Output Format" section above.

---

## Implementation Notes

**After generating questions:**
1. Review against the validation checklist
2. Test completion time (aim for 15-20 minutes)
3. Check for any accidentally transparent "right" answers
4. Ensure good mix of formats (not all forced-choice)
5. Verify coverage of all dimensions
6. Create Google Form with these questions
7. Test with 20-30 people before full launch

**Scoring approach (for later):**
- Layer 1: Map responses to Big Five / DISC dimensions, normalize scores
- Layer 3: Flag bias patterns (e.g., always choosing "push through" = sunk cost), measure risk tolerance across domains
- Use LLM (Claude/GPT-4) to synthesize results into narrative insights

**Framing for MVP:**
- This is an exploratory assessment for hypothesis validation, not a clinically validated instrument
- Insights are generated via LLM synthesis, not standardized norm-referenced scoring
- You can say "inspired by behavioral science research" but avoid claiming "scientifically validated"
- After MVP validation, consider formal psychometric validation if building the full platform
