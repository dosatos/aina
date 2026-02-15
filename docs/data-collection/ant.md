Great — let's think through how to actually collect the data that powers each layer. This is where the product either feels *good* to use or becomes a chore people abandon halfway through.

## The Core Tension

There's a fundamental tradeoff: **depth of insight vs. user patience.** Seven layers with 40 questions each = 280 questions. Nobody's doing that in one sitting. So the collection strategy *is* the product design.

---

## Collection Methods — A Toolkit

**1. Traditional Questionnaires (Self-Report)**

This is the backbone — Likert scales, forced-choice pairs, and scenario-based questions. But the execution matters enormously.

For **Layers 1 (Behavioral Dynamics), 2 (Drive & Motivation), and 5 (Relational & Conflict Style)**, self-report works well because these are subjective by nature — how you *feel* you show up, what motivates you, how you handle conflict. The established research (Big Five via IPIP, Self-Determination Theory) already has validated item pools we can draw from.

The key design decisions here: Do we use classic Likert ("strongly agree → strongly disagree") or something more engaging? Forced-choice pairs like "Would you rather lead a team through a crisis OR design a system that prevents the crisis?" can feel more natural and reduce the "just pick 4 on everything" problem. A mix is probably ideal — Likert for speed on straightforward items, forced-choice for the dimensions where people struggle to self-assess accurately.

**2. Scenario-Based / Situational Judgment**

For **Layer 3 (Risk & Decision Architecture)** and **Layer 4 (Execution & Consistency)**, abstract self-report is weak. People are terrible at predicting their own behavior under pressure. Instead, present realistic scenarios:

*"You've been working on a project for 3 months. Results are mediocre. A new opportunity appears that excites you more. Do you: (a) double down on the current project, (b) run both in parallel, (c) cut your losses and switch, (d) ask someone else to evaluate before deciding?"*

This is more engaging AND more accurate — you're measuring revealed preferences rather than stated preferences. It also lets us detect cognitive biases *in real time* (someone who always picks "push through" is showing sunk cost bias even if they'd never self-report it).

For the Risk layer specifically, we could use modified gambling-style scenarios (not actual gambling — just hypothetical tradeoffs): "Would you take a 60% chance at $1,000 or a guaranteed $400?" Vary the domains — financial, career, social, reputational — to build a multi-dimensional risk profile.

**3. Peer Surveys (360° Feedback Lite)**

This is specifically for **Layer 7 (Self-Perception Gap)** but it's also one of the most powerful data sources across the entire platform.

The mechanic: After completing their own assessment, the user sends a short survey (2-3 minutes, 10-15 questions max) to 3-5 people they trust — colleagues, friends, a partner. The questions mirror what the user answered about themselves but phrased in third person: "How does [Name] typically handle disagreements?" The AI then computes the delta.

Design considerations for this: it needs to feel *safe*. People are afraid of what others will say. So we need to think about whether responses are shown raw or only as aggregated patterns. My instinct is to show aggregated gaps ("Your peers rate your empathy higher than you do") rather than individual attributions ("Your colleague Sarah thinks you're bad at listening"). Anonymity of individual responses is probably essential for honest feedback.

The viral loop here is real — every peer survey is an introduction to the platform. The person filling it out gets curious about their own profile. We should have a smooth "Want to take your own assessment?" CTA at the end of the peer survey.

**4. Behavioral / Interactive Tasks**

Beyond asking people *about* themselves, we could observe them *doing* things. This is more complex to build but produces far richer data.

Examples: A prioritization exercise where you rank 10 items under time pressure (measures decision speed, analytical vs. intuitive style, how you handle insufficient information). A short "inbox simulation" where you triage 8 fictional emails — do you respond to the urgent-but-unimportant ones first, or the important-but-not-urgent? A simple negotiation mini-game where you split resources with an AI counterpart — measures your actual conflict style, not your reported one.

This data would feed into **Layers 3, 4, and 5** and would also create a powerful cross-check against self-reported data. If someone *says* they're collaborative but *plays* competitively in the negotiation game, that's a blindspot we can surface.

The tradeoff: these are expensive to design and build. Probably Phase 2 or 3 material. But even one or two interactive tasks in the MVP could be a major differentiator — it would make the experience feel like a *product* rather than another Google Form.

**5. Contextual / Micro-Assessments Over Time**

Instead of one massive evaluation session, drip questions into the user's daily or weekly routine. A push notification or email: "Quick check-in: What was the hardest decision you made this week? How did you make it?" Three taps, done.

This serves two purposes — it feeds the **Growth Over Time** feature (tracking how someone evolves) and it captures data in-context rather than in-the-abstract. Someone answering "How do you handle conflict?" on a Tuesday afternoon gives a different answer than someone answering it 10 minutes after an actual conflict.

This is the "Growth OS" play — turning the platform from a one-time assessment into an ongoing relationship. It also dramatically increases engagement and retention.

**6. Passive / Inferred Data (Use Carefully)**

This one's sensitive but worth considering: Can we infer anything from *how* the user interacts with the platform itself?

Response time patterns (do they answer quickly or deliberate?), consistency of answers across similar questions asked differently, whether they change answers when reviewing, how they react to challenging results (do they dig in or dismiss?). This metadata is a secondary signal about decision style, openness, and self-awareness.

We'd need to be transparent about this — "We also analyze your response patterns, not just your answers" — and it should be opt-in. But it adds a layer of insight that pure self-report can't.

---

## The Collection Architecture — How It All Fits Together

Here's how I'd structure the actual user experience:

**Onboarding (10-15 minutes):** A "quick profile" that touches Layers 1 and 3 lightly — maybe 30-40 questions total mixing Likert, forced-choice, and 2-3 scenarios. This gives the user enough for an initial cross-layer insight ("here's your behavioral style and risk profile") and hooks them to go deeper. The key is that they get *something valuable* fast. No "complete all 7 layers before seeing results."

**Deep Dives (10-15 minutes each, self-paced):** Each layer gets its own module the user can take when they want. Layer 1 deep dive, Layer 3 deep dive, etc. After each one, the synthesis updates — the more layers you complete, the richer the cross-layer patterns become. This creates a "collect them all" dynamic without forcing a marathon session.

**Peer Survey (sent after Layer 1 is complete):** Once the user has their own behavioral profile, prompt them to send the peer survey. This naturally gates Layer 7 behind enough self-data to make the comparison meaningful.

**Ongoing micro-checks (after initial profile is built):** Weekly or biweekly prompts that refine the profile and feed the growth-over-time feature.

---

## Question Design Principles

Regardless of method, some principles should guide every question we write:

The questions should feel *personal and specific*, not clinical. "I enjoy meeting new people" is boring and vague. "At a networking event, I'm more likely to: (a) work the room and talk to 10 people briefly, (b) find 2-3 people and have deep conversations, (c) stick with people I already know, (d) find a reason to leave early" — that's something people can actually picture themselves doing.

Avoid transparent questions where the "right" answer is obvious. "I care about other people's feelings" — everyone says yes. Better to create tension between two positive options: "When a teammate is struggling and it's affecting the deadline, do you prioritize supporting them emotionally or addressing the performance gap directly?" Neither answer is wrong, but they reveal different things.

Build in validity checks — ask the same construct from different angles and flag inconsistencies. Not as a "gotcha" but as data: inconsistency itself is an insight (it might mean the person is context-dependent rather than consistent, which is worth surfacing).

---

## Data Quality Considerations

**Social desirability bias** is the biggest threat. People answer how they *want* to be, not how they *are*. Mitigations: forced-choice between two equally "good" options, scenario-based questions where there's no obvious best answer, peer data as a cross-check, and behavioral tasks that measure actions not self-reports.

**Fatigue effects** — answer quality drops after ~15 minutes. Keep modules short. Show progress bars. Let people save and return. And front-load the most important questions in each module.

**Retest reliability** — if someone takes the same layer twice, do they get similar results? We need to track this and build confidence intervals into our outputs. Rather than "You are 78% risk-tolerant," show "Your risk tolerance is high (confidence: strong)" or "Your conflict style is still emerging (take the deep dive for a more stable reading)."

---

## What This Looks Like for the MVP

For the Phase 1 launch (Layers 1, 3, and 7):

Layer 1 (Behavioral Dynamics) uses a mix of Likert items from the IPIP Big Five pool plus forced-choice pairs. Roughly 25-30 questions, taking about 8 minutes. Layer 3 (Risk & Decision Architecture) uses primarily scenario-based questions plus a few domain-specific risk tradeoffs. Around 15-20 questions/scenarios, taking about 10 minutes. Layer 7 (Self-Perception Gap) uses a peer survey of 10-12 questions that mirror the user's Layer 1 and Layer 3 answers, sent to 3-5 people.

Total user commitment for the core profile: about 20 minutes of active assessment, plus waiting for peer responses. That's manageable, and they get cross-layer synthesis after just the first two layers.

---

Want to go deeper on any of these — the scenario design for the Risk layer, the peer survey mechanics, the interactive task concepts, or the micro-assessment strategy?