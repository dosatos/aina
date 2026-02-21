---
description: >
  Invoke this skill when the user asks for ad copy, hooks, angles, headlines for ads,
  creative concepts, or messaging ideas for advertising.
  Triggers: "write me some ad copy", "give me hooks", "what angles should I test",
  "write creatives for Meta/TikTok/LinkedIn", "help me with ad messaging",
  "what should my ads say".
argument-hint: Specific channel or format if known (e.g., "Meta video hooks", "LinkedIn text ads")
allowed-tools: Read, WebFetch, WebSearch
---

# Ad Hooks & Angles Generator

Generate 5–8 ad hooks grounded in specific ICP pain moments. Each hook should sound like something a customer said — not something a marketer wrote.

## Process

1. **Read `project/product-brief.md`** to extract:
   - ICP: who they are, their core pain, the trigger moment that makes them look for a solution
   - Competitor alternatives and named enemies
   - Customer objections
   - Voice/tone guidance
2. **Generate hooks** — one per specific pain moment or trigger scenario. Each hook must:
   - Open with a pain, a provocative question, or a specific scenario (not the product)
   - Use the customer's own language (plain, specific, emotional — not marketing adjectives)
   - Be short enough for a scroll-stop moment (1–3 lines max for the opening)
3. **Match each hook to a channel** where the format fits best.

## Output Format

For each hook:

**Hook [N]: [Opening line]**
Full hook: [2–5 lines if it's a longer format]
Pain moment it targets: [One sentence — what specific thing just happened to them]
Best channel fit: [Meta / TikTok / LinkedIn / YouTube / Google Search]
Format: [Static image headline / Video hook / Text post / Search ad headline]

---

**What NOT to write**: After the hooks, name 1–2 angles that seem obvious but won't work for this ICP and why. (e.g., "Don't lead with ROI stats — this ICP is in execution mode, not buying-committee mode")

If the brief has no ICP pain or trigger moment filled in, stop and ask for it before writing anything. Generic hooks are worse than no hooks.
