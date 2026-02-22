# Phase 0 Assessment: 10-Question Diagnosis

**Target completion time:** 5-7 minutes
**Format:** Binary choice (2 options for Q1-Q6, multiple choice for Q7-Q10)
**Email capture:** After result delivery

---

## Part 1: Behavioral Wiring (3 Questions)

### Q1: Meeting Facilitation (Assertiveness)

**You're in a strategy meeting. The conversation has been going in circles for 15 minutes.**

Which sounds more like you?

- [ ] A) I jump in: "We need to make a call. Here's what I think we should do."
- [ ] B) I keep the discussion going: "Let's hear one more perspective before deciding."

**Scoring:**
- A = High assertiveness (2)
- B = Low assertiveness (1)

---

### Q2: Launch vs Analyze (Pace Preference)

**You've been researching a decision for 2 weeks. You have 80% of the information you need.**

What happens next?

- [ ] A) I make the call and move forward.
- [ ] B) I keep researching until I hit 90%+.

**Scoring:**
- A = Fast pace (2)
- B = Slow/deliberate (1)

---

### Q3: Team Behind Schedule (Task vs People Orientation)

**Your team is behind schedule on a critical project. One person is clearly struggling.**

What's your immediate instinct?

- [ ] A) Reassign their work to someone faster. Timeline matters most.
- [ ] B) Talk to them first to understand what's blocking them, then decide.

**Scoring:**
- A = High task focus (2)
- B = High people focus (1)

---

## Part 2: Decision Patterns (3 Questions)

### Q4: Internal Tool Sunk Cost (Bias Awareness)

**Your team built an internal tool 6 months ago. Cost: $40k + 3 months of engineering time. Nobody uses it. Leadership keeps pushing adoption. You have budget for a better off-the-shelf solution.**

Which argument feels more compelling to you?

- [ ] A) "Sunk cost is sunk. Let's cut losses and switch now."
- [ ] B) "We invested heavily. Let's give it one more quarter before giving up."

**Scoring:**
- A = Low sunk cost bias (2)
- B = High sunk cost bias (1)

---

### Q5: Mixed Gain/Loss Scenario (Loss Aversion)

**You're choosing between two job offers:**

**Offer A:** Guaranteed $120k salary
**Offer B:** $100k salary + performance bonus that could add $0-40k (partly outside your control)

Which do you pick?

- [ ] A) Offer A. I value certainty.
- [ ] B) Offer B. Higher upside potential.

**Scoring:**
- A = High loss aversion (1)
- B = Low loss aversion (2)

---

### Q6: Contrarian LinkedIn Post (Reputational Risk)

**You have a well-researched, contrarian take on a hot topic in your industry. It contradicts what 3 influential people in your network just posted.**

Do you post it?

- [ ] A) Yes. I have data and I'm not afraid to disagree publicly.
- [ ] B) No. The potential reputational cost isn't worth it.

**Scoring:**
- A = Low reputational risk aversion (2)
- B = High reputational risk aversion (1)

---

## Part 3: Career Context (4 Questions)

### Q7: What Drains You Most in Your Current Role?

**Select the one that drains you MOST:**

- [ ] A) Lack of autonomy (micromanagement, too many approvals)
- [ ] B) Unclear expectations or constantly shifting priorities
- [ ] C) Repetitive work without learning/growth
- [ ] D) Too much people management, not enough deep work
- [ ] E) Too much solo work, not enough collaboration
- [ ] F) High stress without control over outcomes
- [ ] G) Lack of impact/meaning
- [ ] H) None of these / Not currently drained

**Scoring:** Categorical (used for mismatch diagnosis)

---

### Q8: Ideal Next Role Emphasis

**If you could design your ideal next role, what would you emphasize MOST?**

- [ ] A) Deep technical/specialist work
- [ ] B) Strategic thinking and planning
- [ ] C) Building and leading teams
- [ ] D) High autonomy and ownership
- [ ] E) Structured environment with clear processes
- [ ] F) Fast-paced, dynamic environment
- [ ] G) Mix of several (can't pick just one)

**Scoring:** Categorical (used for environment recommendations)

---

### Q9: Current Role Type

**What best describes your current role?**

- [ ] A) Individual Contributor (IC)
- [ ] B) People Manager
- [ ] C) Senior Leader (Director+)
- [ ] D) Founder/Executive
- [ ] E) Between roles

**Scoring:** Categorical (context for interpretation)

---

### Q10: Years of Experience

**How many years of professional experience do you have?**

- [ ] A) 0-2 years
- [ ] B) 3-5 years
- [ ] C) 6-10 years
- [ ] D) 11-15 years
- [ ] E) 16+ years

**Scoring:** Categorical (context for interpretation)

---

## User Flow Summary

1. **Assessment (10 questions)** → Auto-scored, ~5-7 minutes
2. **Instant Result Display** → Wiring + Mismatch + Recommendations
3. **Optional Open-Ended Questions** → AFTER result (self-selecting quality)
4. **Email Capture** → "Want full diagnosis? [Email input]"

---

## Implementation Notes

### For Google Form (Option A - Recommended for Phase 0):
- 10 questions = 10 sections in Google Form
- Q1-Q6: Use required multiple choice (2 options each - fast to answer)
- Q7-Q10: Use required multiple choice (categorical selections)
- Progress bar: Auto-enabled by Google Forms
- After submission: Show link to optional qualitative questions
- Responses → Google Sheets for manual scoring

### For Custom HTML (Option B - After validation):
- JavaScript auto-scoring
- Instant result display
- Optional text boxes appear after result
- POST to Airtable/Zapier

### Scoring Logic:
- Q1-Q3: Binary scoring (1 or 2) for behavioral wiring profile
- Q4-Q6: Binary scoring (1 or 2) for decision patterns
- Q7-Q10: Categorical matching for diagnosis template

**Key Change:** Simplified Q1-Q6 from 4 options to 2 options (binary choice)
- Faster to answer (less decision fatigue)
- Higher completion rate
- Still captures the essential behavioral pattern
- Target time reduced from 8-10 minutes to 5-7 minutes

---

## Next Steps After This File

1. ✅ Complete this file (assessment-10q-final.md)
2. ⏭ Update result-templates.md (adjust scoring for binary 1-2 scale)
3. ⏭ Update google-form-implementation-guide.md (reflect 2-option structure)
4. ⏭ Create open-ended-questions.md (2 optional text questions)
5. ⏭ Update landing page index.html
