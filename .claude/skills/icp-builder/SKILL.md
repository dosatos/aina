---
description: >
  Invoke this skill when the user needs to define their ideal customer profile, build their customer avatar,
  or fill out the marketing foundation for a product idea. Also invoke when product-brief.md is incomplete
  or when the user is starting work on a new product.
  Triggers: "who is my customer", "help me define my ICP", "I don't know who to target",
  "fill out my product brief", "I need to understand my avatar", user mentions having an idea but unclear on the customer.
argument-hint: Product idea or category (optional - skill will prompt if needed)
allowed-tools: Read, Edit, Write, WebFetch, WebSearch
---

# ICP Builder (Customer Avatar & Marketing Foundation)

Build a complete Ideal Customer Profile and marketing foundation before building, validating, or launching. Output a filled `project/product-brief.md`.

## The Principle

Most solopreneurs skip this step and go straight to building. Then they can't write a landing page, don't know where to find customers, and the product doesn't sell.

Tabunov: "If you can't describe your customer's painful Tuesday morning in one sentence, you don't know your customer."

**The rule:** Spend 2 hours on this before writing a single line of code or launching a single ad. The clearer your ICP, the easier everything downstream becomes.

---

## Process

1. **Read `project/product-brief.md`** — check what's already filled. If empty, start from scratch.

2. **Walk through the 11 Marketing Blocks** (in order). Extract specifics, reject generic answers. For each block, ask clarifying questions until the answer is concrete.

3. **Segment if necessary** — if the user describes 2+ distinct ICPs, force a choice: pick one primary ICP for MVP. Serve one person well before serving many people poorly.

4. **Fill `project/product-brief.md`** with outputs from all 11 blocks.

5. **Validate completeness** — if any block is still vague, flag it and ask one more targeted question.

---

## The 11 Marketing Blocks

### Block 1: WHO (Demographics & Role)

**Goal:** Define the person, not the category.

**Bad:** "Small business owners"
**Good:** "Solo freelance designers who've been freelancing for 2–5 years and invoice 5–10 clients per month"

**Questions to ask:**
- What is their job title or role?
- How long have they been in this role?
- What does a typical day look like for them?
- Do they work alone, or in a team? (If team: what size? What's their role in it?)

**Output format:**
```
**Who they are:** [Specific role + experience level + key context]
Example: "Freelance web developers, 2–5 years into solo practice, managing 3–8 active clients at a time."
```

---

### Block 2: CORE PAIN (The Specific Problem)

**Goal:** Name the painful moment, not the problem category.

**Bad:** "Time management is hard"
**Good:** "They spend 2 hours every Friday hunting through Slack, email, and text messages to figure out which invoices haven't been paid yet"

**Questions to ask:**
- What is the most frustrating part of their week related to this problem?
- What do they currently do when this problem happens?
- How much time or money does this problem cost them per month?

**Output format:**
```
**Core pain:** [One specific painful moment in their workflow]
Example: "Spend 2+ hours/week manually chasing overdue invoices because clients 'didn't see the email'."
```

---

### Block 3: TRIGGER MOMENT (When Do They Search?)

**Goal:** Identify the event that makes them look for a solution right now.

**Bad:** "When they're frustrated"
**Good:** "After they send a proposal, the client says yes, and then the invoice goes unpaid for 30+ days"

**Questions to ask:**
- What just happened that made them think "I need to fix this"?
- Is there a specific event, threshold, or breaking point? (e.g., lost a client, missed a deadline, got yelled at by a boss, revenue dropped)
- How often does this trigger event happen?

**Output format:**
```
**Trigger moment:** [The event that makes them search for a solution]
Example: "After sending 3+ follow-up emails with no payment, they realize they need a system."
```

---

### Block 4: CURRENT SOLUTION (What They Do Now)

**Goal:** Understand the workaround, manual process, or competitor they currently use.

**Questions to ask:**
- What do they do today to solve or avoid this problem?
- What tools, spreadsheets, or manual processes are they using?
- Why isn't their current solution good enough?

**Output format:**
```
**Current solution:** [The workaround or competitor they use now]
Example: "Manually create invoices in Google Docs, send via Gmail, track payments in a spreadsheet."
```

---

### Block 5: DESIRED OUTCOME (What Success Looks Like)

**Goal:** Define the outcome they're paying for, not the feature.

**Bad:** "A better invoicing tool"
**Good:** "Get paid within 7 days of sending an invoice, without sending follow-ups"

**Questions to ask:**
- If this problem were solved, what would be different in their day/week/month?
- What metric would improve? (time saved, money made, stress reduced)
- How would they describe success to a friend?

**Output format:**
```
**Desired outcome:** [The specific result they want]
Example: "Invoices get paid in < 7 days, automatically, without manual follow-up."
```

---

### Block 6: OBJECTIONS (Why They Won't Buy)

**Goal:** List the top 3 reasons they'll hesitate or say no.

Common objections:
- "Too expensive" (pricing objection)
- "I don't have time to set this up" (friction objection)
- "I don't trust this will work" (credibility objection)
- "I already have a system that's 'good enough'" (status quo bias)

**Questions to ask:**
- What's the #1 reason someone in this ICP would NOT buy this?
- What's the biggest risk they perceive?
- What failed solutions have they tried before?

**Output format:**
```
**Known customer objections:**
1. [Objection] — [Why they believe this]
2. [Objection]
3. [Objection]

Example:
1. "I don't have time to migrate from my current system" — They've already set up templates in Google Docs
2. "What if clients ignore automated emails too?" — Fear it won't work better than manual follow-ups
3. "Is this just another subscription?" — Subscription fatigue
```

---

### Block 7: MECHANISM (How You Solve It Differently)

**Goal:** Explain WHY your solution works when others don't. The mechanism is the "secret" or unique approach.

**Bad:** "Our tool is faster and easier"
**Good:** "Auto-reminds clients 3 days before due date via email + SMS, with one-click payment link embedded. No login required for clients."

**Questions to ask:**
- What do you do differently than the current solution or competitors?
- Why does your approach work better?
- What's the key insight or method that makes this unique?

**Output format:**
```
**Unique mechanism:** [The specific method or approach that differentiates you]
Example: "Sends payment reminders via SMS + email with embedded Stripe link — clients pay in one click, no invoice portal login."
```

---

### Block 8: NAMED ENEMY (What You Stand Against)

**Goal:** Position against an alternative, a bad solution, or a flawed belief.

Examples:
- "Unlike Basecamp, which tries to do everything, we only do X."
- "No more spreadsheet hell."
- "Stop losing money to 'I forgot' excuses."

**Questions to ask:**
- What's the flawed belief or bad solution your ICP is stuck with?
- What do they need to STOP doing or STOP believing?
- What's the competitor or tool you're most different from?

**Output format:**
```
**Named enemy:** [What you're positioned against]
Example: "Manual invoicing in Google Docs + Gmail. It's unprofessional, untrackable, and doesn't get you paid."
```

---

### Block 9: PROOF (Why Should They Trust You?)

**Goal:** Establish credibility — social proof, credentials, results, or founder authority.

**Questions to ask:**
- Do you have testimonials, case studies, or user results?
- What's your personal authority on this problem? (Have you experienced it? Solved it for others?)
- Are there numbers you can share? (X users, $Y in invoices processed, Z hours saved)

**Output format:**
```
**Proof/Credibility:** [Why they should trust you]
Example: "Built by a freelance developer who lost $12K to unpaid invoices in 2022. Processed $240K in invoices for 80 users in beta."
```

---

### Block 10: OFFER (What They Get + Pricing)

**Goal:** Define the offer structure — what do they get, how much does it cost, and what de-risks it?

**Questions to ask:**
- Is this a free trial, freemium, one-time purchase, subscription, or demo-first?
- What's the price point?
- What reduces the risk? (money-back guarantee, free tier, cancel anytime, no credit card required)

**Output format:**
```
**Primary offer:** [What they get when they sign up]
**Price point:** $X/month or $X one-time
**Risk reversal:** [What makes it safe to try]

Example:
**Primary offer:** 14-day free trial, no credit card required
**Price point:** $29/month
**Risk reversal:** "Cancel anytime. First invoice free if you don't get paid in 7 days."
```

---

### Block 11: CALL TO ACTION (What Happens Next?)

**Goal:** Define the one action you want them to take.

**Bad:** "Learn more" or "Sign up"
**Good:** "Send your first invoice in 3 minutes" or "Get your first payment in 7 days"

**Questions to ask:**
- What is the one action you want them to take on the landing page?
- What happens immediately after they take that action?
- Can you describe the outcome, not the action? ("Get paid faster" > "Start free trial")

**Output format:**
```
**Primary conversion goal:** [Email signup / trial / demo / purchase]
**CTA button text:** "[Outcome-focused action]"

Example:
**Primary conversion goal:** Free trial signup
**CTA button text:** "Send my first invoice" (not "Start trial")
```

---

## Segmentation Logic

If the user describes multiple distinct ICPs (e.g., "freelancers and small agencies"), ask:

**"Which one has the most painful version of this problem right now?"**

Then force a choice:
- Start with ONE ICP for MVP and first 100 customers.
- You can expand to adjacent segments later, but don't dilute your message by trying to speak to everyone at once.

If they resist narrowing: **"Positioning for everyone is positioning for no one. Pick the group that will pay the most or hurt the most right now."**

---

## Output Format

After completing all 11 blocks, write or update `project/product-brief.md` with the structured output.

Then confirm:

**"Your ICP is now locked in. Here's the summary:"**

```
Who: [One sentence]
Core pain: [One sentence]
Trigger: [One sentence]
Desired outcome: [One sentence]
Your unique mechanism: [One sentence]
```

**Next steps:**
- Use /structure-lp to write your landing page with this ICP clarity
- Use /find-channels to identify where to reach this specific ICP
- Use /validation-smoke-test to validate demand before building

---

## Rules

1. **Reject vague answers.** If the user says "small business owners," ask "What kind? How big? What industry?" Keep drilling until it's specific.

2. **Don't let them skip blocks.** Every block must be filled. If they don't know the answer, that's a research task: "Go find 5 people who fit this profile and ask them about [Block X]."

3. **Force segmentation.** If they describe 2+ ICPs, make them pick ONE for MVP. Multi-ICP launches dilute messaging and split focus.

4. **Use the ICP's language.** When they describe the pain, write it in first person or second person. Not "Users experience friction" — "You spent 3 hours reformatting the proposal."

5. **Connect blocks to each other.** The pain (Block 2) should match the trigger (Block 3). The mechanism (Block 7) should directly solve the pain. Check for internal consistency.

---

## First Question

If `product-brief.md` is blank or missing blocks:

"Let's build your ICP from scratch. Starting with Block 1: Who is this product for? Describe their role, experience level, and one key detail about their day-to-day work."

If `product-brief.md` is partially filled:

"I see you've filled [X blocks]. Let's complete the rest. Next up is Block [Y]: [Question for that block]."
