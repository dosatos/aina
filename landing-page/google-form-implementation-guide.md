# Google Form Implementation Guide (Option A - Fastest Path)

**Goal:** Build functional Phase 0 assessment in 1 hour. Manual scoring for first 50 responses.

**Why Google Form for Phase 0:**
- Ship today (no code required)
- Test messaging before automating
- Learn which archetypes resonate
- Validate completion rate before building custom solution

---

## Part 1: Create Main Assessment Form (30 minutes)

### Step 1: Create New Google Form

1. Go to [forms.google.com](https://forms.google.com)
2. Click "Blank form"
3. Title: **"10-Minute Career Diagnosis"**
4. Description:
   ```
   Find out why you're stuck.

   10 diagnostic questions. No right answers. Just behavioral patterns.

   Your result will be sent within 24 hours.
   ```

### Step 2: Configure Form Settings

1. Click Settings gear icon (top right)
2. **General tab:**
   - ✅ Limit to 1 response (optional, helps prevent spam)
   - ✅ Respondents can edit after submit (helpful if they want to revise)
   - ✅ See summary charts and text responses (turn OFF - you'll use Sheets)
3. **Presentation tab:**
   - ✅ Show progress bar
   - Confirmation message:
     ```
     Thanks for completing the assessment!

     Your personalized diagnosis will arrive via email within 24 hours.

     We'd love your feedback to make this more valuable:
     [LINK TO OPTIONAL FEEDBACK FORM]

     (This link will also be sent via email)
     ```

### Step 3: Add Questions (copy from /assessment/assessment-10q-final.md)

**For each question:**
- Question type: **Multiple choice**
- Mark as **Required**

---

#### Q1: Meeting Facilitation

**Question text:**
```
You're in a strategy meeting. The conversation has been going in circles for 15 minutes.

What do you do?
```

**Options:**
- Jump in: "Let's make a decision. Here's what I think we should do."
- Ask: "What if we tried [specific approach]?" and see if others agree
- Wait for someone else to step in, then support the best idea
- Stay quiet unless directly asked for input

---

#### Q2: Launch vs Analyze

**Question text:**
```
You've been researching a decision for 2 weeks. You have 80% of the information you need.

What happens next?
```

**Options:**
- I make the call and move forward
- I make the call but feel slightly uncomfortable
- I keep researching until I hit 90%+
- I struggle to decide when to stop researching

---

#### Q3: Team Behind Schedule

**Question text:**
```
Your team is behind schedule on a critical project. One person is clearly struggling.

What's your immediate instinct?
```

**Options:**
- Reassign their work to someone faster. Timeline matters most.
- Talk to them first to understand what's blocking them, then decide
- Offer support and coaching, even if it means pushing the deadline
- Avoid confrontation. Hope they figure it out on their own.

---

#### Q4: Internal Tool Sunk Cost

**Question text:**
```
Your team built an internal tool 6 months ago. Cost: $40k + 3 months of engineering time. Nobody uses it. Leadership keeps pushing adoption. You have budget for a better off-the-shelf solution.

What do you do?
```

**Options:**
- Push for the new solution. Sunk cost is sunk.
- Try one more adoption push, then switch if it fails
- Keep using the internal tool. We already paid for it.
- Wait for leadership to make the call

---

#### Q5: Mixed Gain/Loss Scenario

**Question text:**
```
You're choosing between two job offers:

Offer A: Guaranteed $120k salary
Offer B: $100k salary + performance bonus that could add $0-40k (depends on factors partly outside your control)

Which do you pick?
```

**Options:**
- Offer B. Higher upside potential.
- Offer B, but I'd feel slightly anxious about the variability
- Offer A. I value certainty over upside.
- Offer A. The thought of earning less than $120k feels bad.

---

#### Q6: Contrarian LinkedIn Post

**Question text:**
```
You have a well-researched, contrarian take on a hot topic in your industry. It contradicts what 3 influential people in your network just posted.

Do you post it?
```

**Options:**
- Yes. I have data. I'm not afraid to disagree publicly.
- Yes, but I'd soften the language to avoid seeming combative
- No. The potential reputational cost isn't worth it.
- No. I never post contrarian takes publicly.

---

#### Q7: What Drains You Most

**Question text:**
```
What drains you MOST in your current role?

(Select the one that drains you most)
```

**Options:**
- Lack of autonomy (micromanagement, too many approvals)
- Unclear expectations or constantly shifting priorities
- Repetitive work without learning/growth
- Too much people management, not enough deep work
- Too much solo work, not enough collaboration
- High stress without control over outcomes
- Lack of impact/meaning
- None of these / Not currently drained

---

#### Q8: Ideal Next Role Emphasis

**Question text:**
```
If you could design your ideal next role, what would you emphasize MOST?
```

**Options:**
- Deep technical/specialist work
- Strategic thinking and planning
- Building and leading teams
- High autonomy and ownership
- Structured environment with clear processes
- Fast-paced, dynamic environment
- Mix of several (can't pick just one)

---

#### Q9: Current Role Type

**Question text:**
```
What best describes your current role?
```

**Options:**
- Individual Contributor (IC)
- People Manager
- Senior Leader (Director+)
- Founder/Executive
- Between roles

---

#### Q10: Years of Experience

**Question text:**
```
How many years of professional experience do you have?
```

**Options:**
- 0-2 years
- 3-5 years
- 6-10 years
- 11-15 years
- 16+ years

---

#### Q11: Email Address (LAST QUESTION)

**Question type:** Short answer

**Question text:**
```
Where should we send your diagnosis?
```

**Validation:**
- Response validation: Text → Email

---

### Step 4: Test the Form

1. Click "Preview" (eye icon, top right)
2. Complete the form yourself
3. Check:
   - All questions display correctly
   - Progress bar works
   - Takes ~8-10 minutes
   - Mobile experience is smooth
4. View responses in spreadsheet (Responses tab → Create Spreadsheet)

---

## Part 2: Create Optional Feedback Form (10 minutes)

### Step 1: Create Second Form

1. New Google Form
2. Title: **"Assessment Feedback (Optional)"**
3. Description:
   ```
   Thanks for taking the career diagnosis!

   Your feedback helps us make this more valuable for others.

   These questions are optional, but we'd love to hear your thoughts.
   ```

### Step 2: Add Feedback Questions

#### Q1: What Resonated Most

**Question type:** Paragraph

**Question text:**
```
What resonated most about your result?

(3-5 sentences)
```

**Required:** No

---

#### Q2: Situation Description

**Question type:** Paragraph

**Question text:**
```
Describe a recent work situation where you felt stuck or misaligned. What happened?

(5-10 sentences)
```

**Required:** No

---

#### Q3: Email (for matching)

**Question type:** Short answer

**Question text:**
```
Your email (so we can match your feedback to your assessment)
```

**Validation:** Email

**Required:** Yes

---

### Step 3: Get Shareable Link

1. Click "Send" (top right)
2. Copy link
3. Paste into main form's confirmation message

---

## Part 3: Link Form to Landing Page (5 minutes)

### Option A: Direct Link

1. Go to main assessment form
2. Click "Send" → Copy link
3. Shorten with [bit.ly](https://bit.ly) or similar (e.g., bit.ly/career-diagnosis-10min)
4. Update landing page CTA href:
   ```html
   <a
     href="https://bit.ly/career-diagnosis-10min"
     class="inline-block bg-neon-cyan hover:bg-neon-cyan/90 text-dark-bg text-xl md:text-2xl font-bold px-12 py-6 transition-all neon-cyan-strong"
   >
     See Why I'm Stuck
   </a>
   ```

### Option B: Embedded Form (More Polish)

1. Form → Send → Embed (< >)
2. Copy iframe code
3. Create `/landing-page/assessment.html`:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>10-Minute Career Diagnosis | Assessment</title>
     <style>
       body { margin: 0; padding: 0; background: #0a0e1a; }
       iframe { border: none; width: 100%; height: 100vh; }
     </style>
   </head>
   <body>
     [PASTE IFRAME HERE]
   </body>
   </html>
   ```
4. Update CTA href to `/assessment.html` or hosted URL

---

## Part 4: Set Up Response Tracking (15 minutes)

### Step 1: Open Response Spreadsheet

1. Main form → Responses → Create Spreadsheet (or open existing)
2. Spreadsheet auto-updates with each submission

### Step 2: Add Scoring Columns

Add these columns to the right of the responses:

| Column | Formula | Purpose |
|--------|---------|---------|
| **Assertiveness** | Manual (1-4) | Q1 score |
| **Pace** | Manual (1-4) | Q2 score |
| **Task/People** | Manual (1-4) | Q3 score |
| **Sunk Cost** | Manual (1-4) | Q4 score |
| **Loss Aversion** | Manual (1-4) | Q5 score |
| **Reputational Risk** | Manual (1-4) | Q6 score |
| **Archetype** | Text | "High-Autonomy IC" etc |
| **Template Used** | Number (1-4) | Which template from result-templates.md |
| **Result Sent** | Checkbox | Track if emailed |
| **Feedback Received** | Checkbox | If they completed optional form |

### Step 3: Create Scoring Reference Sheet

In the same spreadsheet, create a second tab called "Scoring Key":

```
Question | Option | Score
Q1 | Jump in: "Let's make a decision..." | 4
Q1 | Ask: "What if we tried..." | 3
Q1 | Wait for someone else | 2
Q1 | Stay quiet unless asked | 1
Q2 | I make the call and move forward | 4
Q2 | I make the call but feel uncomfortable | 3
Q2 | I keep researching until 90%+ | 2
Q2 | I struggle to decide when to stop | 1
[...continue for all questions]
```

Copy the scoring from `/assessment/assessment-10q-final.md`

---

## Part 5: Manual Scoring Process (First 50 Responses)

### Time per response: 3-5 minutes

**Steps:**

1. **Score Q1-Q6 numerically** (use scoring key tab)
   - Look up their answer → enter 1-4 in scoring columns

2. **Identify archetype** (use result-templates.md)
   - High assertiveness (3-4) + High pace (3-4) + Lack of autonomy (Q7) = "High-Autonomy IC"
   - Low assertiveness (1-2) + Slow pace (1-2) + Unclear expectations (Q7) = "Deliberate Thinker in Chaos"
   - Look up in result-templates.md for closest match

3. **Select template** (1-4 or custom)
   - Use archetype examples from result-templates.md
   - Customize with their Q7/Q8 specifics

4. **Copy template + personalize**
   - Fill in:
     - Wiring description (Q1-Q3)
     - Decision patterns (Q4-Q6)
     - Mismatch diagnosis (Q7 + wiring)
     - Recommendations (Q8 + wiring)

5. **Email result**
   - Subject: "Your 10-Minute Career Diagnosis"
   - Body:
     ```
     Hi [Name if you have it],

     Thanks for completing the assessment. Here's your diagnosis:

     [PASTE RESULT]

     ═══════════════════════════════════════

     We'd love your feedback (optional):
     [LINK TO FEEDBACK FORM]

     Want to chat about this? Reply to this email.

     Best,
     [Your name]
     ```

6. **Mark as sent** (check box in spreadsheet)

---

## Part 6: Validation Metrics

### Track These Numbers:

| Metric | Target | Red Flag |
|--------|--------|----------|
| **Started → Completed** | >60% | <40% (form too long) |
| **Completed → Email given** | >90% | <80% (email ask too early?) |
| **Received result → Left feedback** | >30% | <20% (result didn't resonate) |
| **"Scary accurate" reactions** | >5 in first 50 | <3 (diagnosis too generic) |
| **Median completion time** | 8-10 min | >12 min (too long, cut questions) |

### How to Track:

1. **Started → Completed:**
   - Google Forms tracks this automatically (Responses → Summary)
   - Or use landing page analytics (clicked CTA → submitted form)

2. **Email capture:**
   - Count responses with email vs without (should be 100% since required)

3. **Feedback rate:**
   - Count: Feedback form responses / Main form responses

4. **Qualitative reactions:**
   - Tag feedback responses: "scary accurate", "how did you know", "this described me"
   - Need 5+ of these in first 50 responses

5. **Completion time:**
   - Google Forms shows timestamp
   - Calculate: Submission time - Start time (if you have start tracking)
   - Or ask 5 people to time themselves

---

## When to Automate (Decision Point)

### Build custom page with instant results IF:

✅ Completion rate >60%
✅ Email capture >90%
✅ Feedback rate >30%
✅ 5+ "scary accurate" reactions
✅ You're getting >10 submissions per day

### Stay with manual scoring IF:

⚠️ Completion rate <60% (fix questions first)
⚠️ Feedback rate <20% (result not resonating)
⚠️ <5 submissions per day (not worth automating yet)

**Manual scoring is sustainable for:**
- First 50-100 responses
- 3-5 minutes per response
- 5-10 responses per day = 15-50 minutes per day

**Automate when:**
- Manual work >1 hour/day
- Completion metrics are strong
- You've refined templates based on feedback

---

## Quick Start Checklist

### Hour 1: Build
- [ ] Create main assessment form (30 min)
- [ ] Add all 10 questions + email field
- [ ] Configure settings (progress bar, confirmation message)
- [ ] Create optional feedback form (10 min)
- [ ] Link feedback form in confirmation message
- [ ] Set up response spreadsheet with scoring columns (15 min)
- [ ] Test both forms end-to-end (5 min)

### Hour 2: Launch
- [ ] Get shareable link (or create embedded page)
- [ ] Update landing page CTA
- [ ] Send to 5 test users
- [ ] Verify responses flowing to spreadsheet
- [ ] Manually score first 3 responses
- [ ] Send first 3 results via email
- [ ] Time yourself (should be <5 min per result)

### Week 1: Validate
- [ ] Track completion rate daily
- [ ] Manually score and send all results within 24 hours
- [ ] Tag qualitative feedback responses
- [ ] Watch for "scary accurate" reactions
- [ ] Note completion time from test users

### Decision Point (After 50 completions):
- [ ] Review metrics vs targets
- [ ] If metrics good → build custom page with instant results
- [ ] If metrics weak → iterate on questions/templates first

---

## Troubleshooting

### Low completion rate (<40%)

**Diagnose:**
- Check form analytics: which question has most drop-off?
- Ask test users: "Where did you want to quit?"

**Fix:**
- Shorten question text (cut to 1 sentence)
- Simplify answer options (remove wordy explanations)
- Remove 1-2 questions (prioritize Q1-Q6, Q7-Q8)

### Low feedback rate (<20%)

**Diagnose:**
- Read results you sent: do they feel generic?
- Ask test users: "Did the diagnosis surprise you?"

**Fix:**
- Add more specific language in templates
- Include career context (Q9-Q10) in diagnosis
- Use their exact words from Q7/Q8

### Taking too long (>12 minutes)

**Diagnose:**
- Time yourself taking the assessment
- Check: are answer options too wordy?

**Fix:**
- Cut answer option text by 50%
- Remove explanation text in parentheses
- Consider removing Q10 (experience level) if not critical

### Results don't feel personal

**Fix:**
- Use "you" language (not "people like you")
- Include specific quotes from their Q7/Q8 answers
- Add role context: IC vs Manager makes diagnosis different
- Reference their decision pattern scores specifically

---

## Next Steps After This Guide

1. ✅ Build main assessment form (30 min)
2. ✅ Build optional feedback form (10 min)
3. ✅ Set up tracking spreadsheet (15 min)
4. ✅ Test with 5 people
5. ✅ Update landing page CTA
6. ✅ Launch (post on Reddit, Twitter, LinkedIn)
7. ⏭ Manually score first 50 responses
8. ⏭ Track metrics
9. ⏭ Decide: automate or iterate?

---

## Resources

- **Assessment questions:** `/assessment/assessment-10q-final.md`
- **Result templates:** `/landing-page/result-templates.md`
- **Feedback questions:** `/landing-page/open-ended-questions.md`
- **Landing page:** `/landing-page/index.html`

**Estimated total time to launch:** 2 hours (1 hr build + 1 hr test/deploy)
