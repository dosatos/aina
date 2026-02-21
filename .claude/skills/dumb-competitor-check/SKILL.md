---
description: >
  Invoke this skill when the user asks about competitors, wants to differentiate their product,
  or wants to understand why people don't use existing solutions.
  Triggers: "who are my competitors", "how do I differentiate", "what's wrong with [competitor]",
  "why would someone pick me over X", "what do people hate about existing solutions".
argument-hint: Name the top 1-3 competitors or the product category
allowed-tools: Read, WebFetch, WebSearch
---

# Dumb Competitor Check

Find the #1 complaint about the top competitors. That complaint is your headline. You don't need to be 10x better — you need to not do the one thing that makes people leave.

## The Logic

People don't switch products because of features. They switch because of pain. The pain they have with the current solution is your opening. Find it, name it, own it.

"Dumb" means: stop reading analyst reports and competitor websites. Read the actual complaints from actual users. G2 reviews, Reddit threads, and Twitter/X rants are worth more than any competitive analysis deck.

## Process

1. **Identify top 3 competitors** from `project/product-brief.md` or ask the user.
2. **Search for complaints** — use WebSearch to find:
   - G2/Capterra reviews (search: `"[competitor name]" site:g2.com reviews` or `site:capterra.com`)
   - Reddit threads (search: `"[competitor name]" reddit complaints OR hate OR switched`)
   - Twitter/X (search: `"[competitor name]" frustrated OR disappointed OR cancelled`)
3. **Find the pattern** — what do 3+ people complain about? Ignore one-offs. Look for the recurring pain.
4. **Extract the #1 complaint** — the one that shows up most often and sounds most emotionally charged.
5. **Turn the complaint into a headline** — your positioning is the opposite of their failure.

## Output Format

**Competitor 1: [Name]**
Top complaint: "[Exact quote or close paraphrase from a real review]"
Pattern: [Is this 1 person or a pattern? How common?]

**Competitor 2: [Name]**
Top complaint: "[Quote]"
Pattern: [How common?]

**Competitor 3: [Name]** (if applicable)
Top complaint: "[Quote]"
Pattern: [How common?]

---

**The opening**: [The one complaint that crosses multiple competitors and is emotionally strong]

**Your headline draft** (built from the anti-complaint):
- Version A: "[Negative frame — names what you don't do]"
- Version B: "[Positive frame — names the outcome competitors fail to deliver]"

**Why people stay despite the pain**: [What keeps them locked in — switching cost, network effect, habit? This is important. If the lock-in is strong, you need a better migration story.]

**The one thing NOT to do**: [The trap — the feature or message that looks like differentiation but isn't. E.g., "Don't compete on price if the pain is about reliability."]

Be specific. Paraphrase real quotes. Don't invent complaints that aren't there.
