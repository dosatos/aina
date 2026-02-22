# Phase 0 Assessment: 10-Question Diagnosis

**Target completion time:** 8-10 minutes
**Format:** Multiple choice (auto-scorable)
**Email capture:** After result delivery

---

## Part 1: Behavioral Wiring (3 Questions)

### Q1: Meeting Facilitation (Assertiveness)

**You're in a strategy meeting. The conversation has been going in circles for 15 minutes.**

What do you do?

- [ ] A) Jump in: "Let's make a decision. Here's what I think we should do."
- [ ] B) Ask: "What if we tried [specific approach]?" and see if others agree
- [ ] C) Wait for someone else to step in, then support the best idea
- [ ] D) Stay quiet unless directly asked for input

**Scoring:**
- A = High assertiveness (4)
- B = Moderate assertiveness (3)
- C = Low assertiveness (2)
- D = Very low assertiveness (1)

---

### Q2: Launch vs Analyze (Pace Preference)

**You've been researching a decision for 2 weeks. You have 80% of the information you need.**

What happens next?

- [ ] A) I make the call and move forward
- [ ] B) I make the call but feel slightly uncomfortable
- [ ] C) I keep researching until I hit 90%+
- [ ] D) I struggle to decide when to stop researching

**Scoring:**
- A = Fast pace (4)
- B = Moderate-fast (3)
- C = Moderate-slow (2)
- D = Slow/deliberate (1)

---

### Q3: Team Behind Schedule (Task vs People Orientation)

**Your team is behind schedule on a critical project. One person is clearly struggling.**

What's your immediate instinct?

- [ ] A) Reassign their work to someone faster. Timeline matters most.
- [ ] B) Talk to them first to understand what's blocking them, then decide
- [ ] C) Offer support and coaching, even if it means pushing the deadline
- [ ] D) Avoid confrontation. Hope they figure it out on their own.

**Scoring:**
- A = High task focus (4)
- B = Balanced (3)
- C = High people focus (2)
- D = Avoid conflict (1)

---

## Part 2: Decision Patterns (3 Questions)

### Q4: Internal Tool Sunk Cost (Bias Awareness)

**Your team built an internal tool 6 months ago. Cost: $40k + 3 months of engineering time. Nobody uses it. Leadership keeps pushing adoption. You have budget for a better off-the-shelf solution.**

What do you do?

- [ ] A) Push for the new solution. Sunk cost is sunk.
- [ ] B) Try one more adoption push, then switch if it fails
- [ ] C) Keep using the internal tool. We already paid for it.
- [ ] D) Wait for leadership to make the call

**Scoring:**
- A = Low sunk cost bias (4)
- B = Moderate awareness (3)
- C = High sunk cost bias (2)
- D = Avoidance (1)

---

### Q5: Mixed Gain/Loss Scenario (Loss Aversion)

**You're choosing between two job offers:**

**Offer A:** Guaranteed $120k salary
**Offer B:** $100k salary + performance bonus that could add $0-40k (depends on factors partly outside your control)

Which do you pick?

- [ ] A) Offer B. Higher upside potential.
- [ ] B) Offer B, but I'd feel slightly anxious about the variability
- [ ] C) Offer A. I value certainty over upside.
- [ ] D) Offer A. The thought of earning less than $120k feels bad.

**Scoring:**
- A = Low loss aversion (4)
- B = Moderate-low (3)
- C = Moderate-high (2)
- D = High loss aversion (1)

---

### Q6: Contrarian LinkedIn Post (Reputational Risk)

**You have a well-researched, contrarian take on a hot topic in your industry. It contradicts what 3 influential people in your network just posted.**

Do you post it?

- [ ] A) Yes. I have data. I'm not afraid to disagree publicly.
- [ ] B) Yes, but I'd soften the language to avoid seeming combative
- [ ] C) No. The potential reputational cost isn't worth it.
- [ ] D) No. I never post contrarian takes publicly.

**Scoring:**
- A = Low reputational risk aversion (4)
- B = Moderate-low (3)
- C = Moderate-high (2)
- D = High reputational risk aversion (1)

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

1. **Assessment (10 questions)** → Auto-scored, ~8-10 minutes
2. **Instant Result Display** → Wiring + Mismatch + Recommendations
3. **Optional Open-Ended Questions** → AFTER result (self-selecting quality)
4. **Email Capture** → "Want full diagnosis? [Email input]"

---

## Implementation Notes

### For Google Form (Option A - Recommended for Phase 0):
- 10 questions = 10 sections in Google Form
- Use required multiple choice for all questions
- Progress bar: Auto-enabled by Google Forms
- After submission: Show link to optional qualitative questions
- Responses → Google Sheets for manual scoring

### For Custom HTML (Option B - After validation):
- JavaScript auto-scoring
- Instant result display
- Optional text boxes appear after result
- POST to Airtable/Zapier

### Scoring Logic:
- Q1-Q3: Average for behavioral wiring profile
- Q4-Q6: Flag high/low on each bias dimension
- Q7-Q10: Categorical matching for diagnosis template

---

## Next Steps After This File

1. ✅ Complete this file (assessment-10q-final.md)
2. ⏭ Create result-templates.md (8 archetype templates)
3. ⏭ Create open-ended-questions.md (2 optional text questions)
4. ⏭ Update landing page index.html
5. ⏭ Build Google Form implementation guide
