---
description: >
  Invoke this skill when the user shares a landing page URL, pastes landing page content,
  or asks to evaluate, review, audit, or critique a landing page or website homepage.
  Triggers: "look at this page", "what do you think of my LP", "audit my landing page",
  "review this URL", user pastes page copy for review.
argument-hint: LP URL or paste the page content/copy
allowed-tools: Read, WebFetch, WebSearch
---

# LP Audit Skill

Score the landing page against the four-part LP anatomy framework. Be direct about what's broken. Give specific rewrites for the sections that fail.

## Process

1. **Fetch the page** (if URL provided) or read the pasted content.
2. **Score each section** against the LP anatomy from `funnel-frameworks.md`:
   - Headline: Does it stop the right person? Is it specific? Is it in customer language?
   - Pain section: Does it name specific painful moments? Does it use first/second-person voice?
   - Product/mechanism: Does it show the how, not just the what? Is there a clear demo or flow?
   - CTA: Single action? Outcome-oriented button text? Risk-reducing microcopy?
3. **Flag corporate-speak** — any word that could appear on a competitor's page (seamless, powerful, robust, cutting-edge, next-generation, revolutionize, world-class).
4. **Output verdict + rewrites**.

## Output Format

**Verdict**: [Pass / Needs work / Broken] — one sentence on the biggest issue.

**Section scores** (for each of the 4 sections):
- Status: Pass / Flag / Broken
- What's wrong (if not passing): specific, direct
- Rewrite: exact copy replacement for broken sections (not suggestions — write the actual thing)

**Top priority fix**: The one change that would move the needle most. Be specific about what to change and why.

Do not soften feedback. If the headline is bad, say it's bad and write a better one. Don't hedge.
