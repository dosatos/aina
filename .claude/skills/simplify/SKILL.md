---
description: >
  Invoke this skill when the user types /simplify, when a plan is too complex,
  when the user is describing too many things to do at once, or when the scope
  has grown beyond what one person can ship in a week.
  Triggers: "/simplify", "I have too much to do", "the scope is getting big",
  "I don't know where to start", "this is getting complicated", user describes
  a plan with more than 5 things in it.
argument-hint: Paste the full plan or feature list to be simplified
allowed-tools: Read, WebFetch, WebSearch
---

# Simplify — Strip It Down to the MVP of the MVP

Complexity is a founder killer. Every extra feature is a week of your life and a reason for the user not to sign up. The goal is the smallest possible thing that proves the core assumption.

## The Simplification Test

For each feature or task in the plan, ask:
1. **Does it prove or disprove the riskiest assumption?** If not, it's not MVP.
2. **Can we simulate it manually without building it?** If yes, don't build it yet.
3. **Would removing it prevent the first sale?** If not, it's post-launch.
4. **Is it for the user or for the founder?** (Dashboards, analytics, admin panels — all for the founder. Cut them.)

## The "Dumb Version" Rule

For every piece of functionality, ask: what's the dumbest version that still delivers the outcome?
- Instead of an AI matching algorithm → manual curation by the founder
- Instead of automated billing → invoice manually for first 10 customers
- Instead of a dashboard → email report every Monday
- Instead of a mobile app → a Telegram bot
- Instead of user accounts → a shared Google Sheet

## Process

1. **Get the full plan/feature list** from the user.
2. **Apply the simplification test** to each item.
3. **Group into three buckets**: Ship now / Do manually / Post-revenue.
4. **Identify the single core loop** — the one action a user does that creates value. Everything else serves this or is noise.
5. **Output the stripped plan.**

## Output Format

**The core loop**: [One sentence — what the user does, what happens, why they come back]

**Ship now** (must-haves for first sale):
- [Item] — [why it's essential]
- [Item] — [why it's essential]

**Do manually instead** (fake it first):
- [Item] → Manual version: [what you do instead]

**Post-revenue** (only after first 10 paying customers):
- [Item]
- [Item]

**Cut entirely**:
- [Item] — [why it doesn't matter for validation]

**Time to ship the simplified version**: [Realistic estimate in days — if it's more than 7, simplify further]

Be ruthless. The founder's instinct is to keep things. Your job is to cut.
