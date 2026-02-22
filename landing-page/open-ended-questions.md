# Optional Qualitative Questions (Post-Result)

**Strategic Placement:** These questions appear AFTER the user receives their instant diagnosis result.

**Purpose:**
- Gather rich qualitative data from engaged users
- Capture language patterns for copy/messaging
- Validate diagnosis resonance
- Identify edge cases and refinement opportunities

**Key principle:** These are OPTIONAL. They don't block email capture or completion. Self-selecting quality: only people who found value will respond.

---

## Question 1: Result Resonance

### What resonated most about your result?

**Format:** Text area (3-5 sentences)

**What you're looking for:**
- Which part of the diagnosis hit hardest ("The part about..." signals what's working)
- Specific phrases they quote back ("You said X and that's exactly...")
- Emotional reaction indicators ("This explained why...", "I finally understand...")
- Validation strength ("scary accurate", "described me perfectly", "how did you know")

**Why this matters:**
- Phrases they quote = copy that resonates (use in ads, landing page)
- Parts they skip = diagnosis gaps to improve
- High emotion = differentiation is working
- Generic responses = diagnosis too vague

**Good responses look like:**
> "The part about 'you're an architect being asked to lay bricks' hit me hard. I've been trying to explain that feeling for 2 years and couldn't find the words."

> "When you said my nervous system interprets unclear expectations as 'I can't win,' I literally said 'oh shit' out loud. That's exactly how it feels."

**Bad responses look like:**
> "It was accurate."

> "I learned some things about myself."

→ These signal the diagnosis was too generic or didn't land.

---

## Question 2: Situational Context

### Describe a recent work situation where you felt stuck or misaligned. What happened?

**Format:** Text area (5-10 sentences)

**What you're looking for:**
- Concrete examples of the pain (validates the diagnosis approach)
- Language they use to describe frustration (copy gold)
- Patterns across responses (common scenarios to feature on LP)
- Edge cases your multiple choice questions missed
- Severity indicators (how bad is the pain?)

**Why this matters:**
- Real situations = validation that diagnosis maps to actual experience
- Their words = authentic copy for marketing
- Repeated patterns = which archetypes to prioritize
- New patterns = questions to add in next iteration

**Good responses look like:**
> "Last month my manager asked me to lead a cross-functional initiative. I spent 3 weeks building consensus, got everyone aligned, then leadership changed direction with zero explanation. I wasn't mad about the change—I was mad about the wasted alignment work. Made me realize I need a more stable environment."

> "I've been at my company 4 years. I'm good at my job. But every project is the same: different client, same deliverable. My manager says 'you're so reliable,' but I feel like I'm decaying. I'm 32 and feel like I peaked at 28."

**Bad responses look like:**
> "I feel stuck in my role."

> "My job isn't a good fit."

→ These are too vague to be useful for validation or copy.

---

## Implementation Options

### Option A: Google Form (Recommended for Phase 0)

**After submission of 10 main questions:**

1. User completes assessment → clicks "Submit"
2. Google Form shows confirmation page with text:
   ```
   Thanks for completing the assessment!

   Your diagnosis will arrive via email within 24 hours.

   [OPTIONAL] Help us improve:
   We'd love to hear about your experience. These 2 questions are
   optional, but your insights help us make this more valuable for
   others like you.

   [Button: "Share Your Thoughts" → links to second form]
   ```

3. Second form (separate Google Form):
   - Question 1: What resonated most about your result?
   - Question 2: Describe a recent work situation where you felt stuck...
   - Email field (pre-filled if possible, or ask again)

**Pros:**
- Clean separation (doesn't affect completion rate)
- Easy to iterate
- No code required

**Cons:**
- Two-step process (some drop-off)
- Can't pre-fill email

### Option B: Custom Page (After Validation)

**User flow:**

1. User completes 10 questions
2. Instant result displays
3. Below result:
   ```
   ═══════════════════════════════════════
   HELP US IMPROVE (OPTIONAL)
   ═══════════════════════════════════════

   Your feedback helps us make this more valuable
   for people like you.

   [Expandable section: "Share your thoughts"]

   → When expanded:
     - Question 1 text area
     - Question 2 text area
     - [Submit feedback button]
   ```

4. Email capture modal (separate)

**Pros:**
- Single-page experience
- Can track who left feedback vs who didn't
- Email already captured, can associate responses

**Cons:**
- More build time
- Requires custom implementation

---

## Response Analysis Plan (First 50 Users)

### Week 1 Analysis

**For each response, tag:**
1. **Resonance strength:** High / Medium / Low
2. **Quoted phrases:** Which parts of diagnosis did they quote?
3. **Pain severity:** Urgent / Moderate / Exploring
4. **Archetype match:** Which template did they get?
5. **Copy gold:** Flag specific phrases for marketing

**Look for:**
- Which archetypes get "scary accurate" reactions → prioritize these
- Which archetypes get "interesting but..." reactions → diagnosis needs work
- Common pain patterns → feature on landing page
- Language patterns → use in ads

### Red Flags to Watch For

**If you see 5+ responses like this:**
- "Interesting, but I already knew this" → Not differentiated enough
- "Too vague" → Need more specific diagnosis
- "Just another personality test" → Positioning failed
- "I don't see how this helps me decide" → Missing the action step

**If <30% leave qualitative feedback:**
- Result didn't resonate (they got value but not "wow" value)
- Questions are too hard to answer
- Optional step is too hidden

**If >70% leave qualitative feedback:**
- You're doing something right
- Result resonated strongly
- People want to talk about this

---

## Using Responses in Marketing

### Extract Copy from Qualitative Responses

**Look for:**

1. **Pain language** (use in LP pain section):
   - "I've been trying to explain this feeling for 2 years"
   - "Every project is the same... I feel like I peaked"
   - "Made me realize I need..."

2. **Resonance language** (use in testimonials when you have permission):
   - "Scary accurate"
   - "How did you know that?"
   - "Finally explained why..."

3. **Situation patterns** (use in LP context/examples):
   - "Manager changed direction with zero explanation"
   - "I'm reliable but I feel like I'm decaying"
   - Common frustration scenarios

### Create Ad Hooks from Common Situations

If 10 responses mention "manager changed priorities with no explanation":
→ Ad hook: "Your manager just changed priorities. Again. Zero explanation. If this feels like a pattern, not a coincidence, take the diagnosis."

If 8 responses mention "good at my job but feel like I've peaked":
→ Ad hook: "You're 'reliable.' You're 'consistent.' And you're dying inside. 10-minute diagnosis shows you why."

---

## Timeline for Using This Data

**Days 1-7:** Manually read all responses, tag patterns
**Days 8-14:** Identify top 3 archetypes (highest resonance)
**Days 15-21:** Refine result templates for low-resonance archetypes
**Days 22-30:** Use copy from responses to update LP pain section

**After 50 responses:**
- Write 3 ad hooks based on common situations
- Feature 2-3 testimonials (with permission)
- Decide if any multiple-choice questions need adjustment

---

## Next Steps

- ✅ Create open-ended-questions.md (this file)
- ⏭ Update landing page with "10 diagnostic questions"
- ⏭ Build Google Form with 10 questions + link to optional feedback form
- ⏭ Create second form for optional qualitative questions
- ⏭ Set up response tracking sheet with tagging columns

---

## Success Metrics

**Phase 0 target:**
- 30-50% of users leave qualitative feedback
- 5+ "scary accurate" or "how did you know" reactions
- 3+ clear pain patterns emerge across responses
- 10+ phrases flagged as "copy gold"

**Red flag metrics:**
- <20% leave feedback → result didn't resonate
- >50% generic responses → questions too hard or diagnosis too vague
- Multiple "not helpful" signals → diagnosis approach needs rework
