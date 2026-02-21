---
description: >
  Invoke this skill after the user has launched a product and needs help with post-launch iterations,
  maintaining momentum, prioritizing feedback, or preventing abandonment.
  Triggers: "what should I work on next", "I launched but don't know what to improve",
  "I'm losing motivation", "should I add [feature]", "people are asking for X and Y and Z",
  "I shipped but nothing's happening", user shares post-launch feedback or metrics.
argument-hint: What you've launched, current metrics, or feedback you've received
allowed-tools: Read, WebFetch, WebSearch
---

# Iteration & Momentum

Set up healthy feedback loops after launch. Prioritize iteration work. Maintain momentum. Finish what you started.

## The Principle

Most products die in the messy middle — after the launch high fades but before traction arrives. The difference between success and abandonment is **systematic iteration** with a tight feedback loop.

**Healthy feedback loop:**
Launch → Measure → Learn → Decide → Ship small → Repeat weekly

**Unhealthy feedback loop (the "smoker" loop):**
Launch → Crickets → Panic → Add random features → Check metrics every hour → Burn out → Abandon

Tabunov: "Launching is 10% of the work. The next 90% is iterating based on signal, not feelings."

## Process

1. **Read `project/product-brief.md`** for context (what was launched, ICP, core value prop).

2. **Establish the feedback loop cadence**:
   - **Week 1–4 post-launch**: Review metrics + user conversations every 3 days. Ship small improvements weekly.
   - **Month 2–3**: Review weekly. Ship every 10–14 days.
   - **After Month 3**: Review biweekly. Ship when there's clear signal.

3. **Triage current feedback** into 4 buckets:
   - **Broken core flow** — something prevents the main job from being done. Fix now.
   - **Frequently requested** — 5+ people asked for it independently. Consider next sprint.
   - **Nice-to-have** — 1–2 requests, or "it would be cool if..." Add to backlog, don't build yet.
   - **Ignore** — feature requests that expand scope beyond the core job, or come from people outside your ICP. Politely decline.

4. **Apply the iteration math**:
   - Can you ship this in < 5 days? → Do it if it's "broken core flow" or "frequently requested."
   - Will this take > 5 days? → Only do it if 10+ people are blocked by its absence AND are paying/engaged users.
   - Will this take > 2 weeks? → You're probably solving the wrong problem. Break it down or cut scope.

5. **Output: One clear next action** for this week. Not a roadmap. One thing to ship by end of week.

---

## Iteration Frameworks

### Framework 1: The 3-Metric Check-In (Weekly Ritual)

Review these three numbers every week for the first 90 days:

1. **Activation metric** — did new users complete the core action? (e.g., sent first invoice, posted first job, ran first report)
   - Threshold: > 40% of signups should activate within 7 days.
   - If below threshold: Onboarding is broken. Don't add features. Fix activation.

2. **Retention metric** — did users return or keep paying?
   - Threshold: > 30% of users should return in Week 2 (for free product), or < 10% monthly churn (for paid).
   - If below threshold: Core value isn't being delivered. Talk to churned users. Don't build new features yet.

3. **Growth metric** — how many new users arrived this week, and from where?
   - Threshold: Week-over-week growth should be > 0% (any growth). Flat or declining = distribution problem.
   - If below threshold: Don't build. Go back to /find-channels. Your product might be fine; nobody sees it.

**Action rule**: Only iterate on the product if metrics 1 + 2 are healthy. If they're broken, adding features makes it worse.

---

### Framework 2: The Feedback Triage Matrix

When people request features, score each request:

| Request | Frequency | ICP Match | Effort | Priority |
|---------|-----------|-----------|--------|----------|
| [Feature name] | [1 person / 3–5 / 10+] | [Yes / No] | [< 3 days / 1 week / 2+ weeks] | [Now / Next / Backlog / Ignore] |

**Priority logic:**
- **Now**: 10+ requests + ICP match + < 3 days effort, OR blocks core job for any user
- **Next**: 5+ requests + ICP match + < 1 week effort
- **Backlog**: 3–5 requests + ICP match, OR 10+ requests but > 1 week effort (break it down first)
- **Ignore**: < 3 requests, OR not ICP match, OR expands scope beyond core job

---

### Framework 3: The Momentum Maintenance System

**Why momentum dies:**
1. No visible progress (metrics don't move, nobody's using it)
2. Unclear next step (too many options, no forcing function)
3. Isolation (no accountability, no one to share wins/losses with)

**Momentum hacks:**

**Daily:**
- Ship something visible every day for first 30 days post-launch (even if it's a tweet, a bug fix, or one customer conversation). Shipping compounds.

**Weekly:**
- Post one update: "This week: [metric or learning]. Next week: [one concrete goal]."
- Marc Lou: "Revenue numbers or GTFO." Transparency forces honesty.

**Monthly:**
- Review: Did activation, retention, or growth improve? If yes: keep doing what's working. If no: talk to 5 users and find out why they didn't stick.

**Accountability forcing function:**
- Build in public on X/LinkedIn (forces weekly updates).
- Join a founder accountability group (Indie Hackers, MegaMaker, WIP, etc.) and post weekly check-ins.
- Set a public goal: "$1K MRR by [date]" or "100 users by [date]." Public commitment increases follow-through.

---

## Output Format

**Current state check:**
- Activation: [metric + threshold status]
- Retention: [metric + threshold status]
- Growth: [metric + threshold status]

**Diagnosis**: [One sentence — e.g., "Activation is broken. Users sign up but don't complete onboarding."]

**Feedback triage:**
[List 3–5 requests with priority — Now / Next / Backlog / Ignore]

**This week's focus**: [One specific thing to ship by end of week]

**Why this matters most**: [One-sentence reasoning — connect back to the broken metric or most-requested item]

**Momentum check**: [Are you posting updates publicly? When was your last shipped iteration? If it's been > 14 days, why?]

**Don't do this**: [The tempting distraction — e.g., "Don't build a mobile app yet. 5 people asked, but 0 people are retained on web."]

---

## Rules

1. **Don't iterate on features if activation or retention is broken.** Fix the core loop first. Adding features to a leaky bucket doesn't work.

2. **Don't optimize growth if activation/retention is broken.** You're just accelerating churn. More users won't fix a broken product.

3. **Don't build what one person asked for unless it's blocking the core job.** Outlier requests are distractions.

4. **Don't take > 2 weeks to ship the next iteration.** If your iteration takes longer, your feedback loop is too slow. Break it down.

5. **Don't abandon after 30 days if metrics are flat.** Give it 90 days of consistent iteration + distribution effort before calling it. Most products take 60–90 days to show real signal.

6. **Do kill it if after 90 days: zero revenue, zero retention, and zero organic word-of-mouth.** That's a real signal. Use /pivot or /kill.

---

## First Question

If user hasn't shared metrics: "What are your current activation, retention, and growth numbers? If you don't track these, let's set up simple tracking first."

If user shares metrics or feedback, go directly to triage and output the weekly focus.
