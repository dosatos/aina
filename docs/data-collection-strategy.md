# Data Collection Strategy

A combined reference synthesizing ideas from four independent brainstorm sessions (`docs/data-collection/`).

---

## 1. Overview & Design Philosophy

### The Core Tension

Seven layers with 40 questions each = 280 questions. Nobody's doing that in one sitting. So the collection strategy *is* the product design.

### The Four Data Streams

The platform becomes elite when it combines at least 3 of these:

| Stream | Source | Strength | Weakness |
|---|---|---|---|
| **Self-Report** | User answers (Likert, forced-choice) | Easy, scalable, validated | Social desirability bias |
| **Behavioral Simulation** | Scenario-based decisions | High signal, reveals actual behavior | Harder to design |
| **Peer Feedback** | Others evaluate the user | Reveals blind spots | Friction to collect |
| **Longitudinal** | Data over time | Shows growth, detects drift | Requires retention |

Most competitors (16Personalities, Truity) stop at self-report. Combining self-report + behavioral simulation + peer feedback in the MVP already puts us ahead.

---

## 2. Collection Methods

### A) Structured Self-Report (Psychometric Backbone)

**What it is:** Likert scales and forced-choice pairs — the traditional foundation of personality measurement.

**Feeds:** Layers 1 (Behavioral Dynamics), 2 (Drive & Motivation), 5 (Relational & Conflict Style)

**How it works:**
- Mix of 5-point Likert items and forced-choice pairs (~60% forced-choice, ~30% Likert, ~10% open-text)
- Draw from the IPIP Big Five item pool (3,329+ public domain items)
- Include reverse-coded items to reduce pattern answering
- Randomize question order

**Forced-choice example:** *"In a crisis, are you more concerned with (A) the speed of the solution or (B) the stability of the team?"* — forces a trade-off, revealing true priorities rather than aspirational answers.

**Why forced-choice matters:** Standard Likert invites "I'm awesome" inflation. When both options are equally positive, people reveal actual preferences instead of social desirability.

---

### B) Scenario-Based Simulations (Major Differentiator)

**What it is:** Mini case studies and hypothetical tradeoffs that measure revealed preferences rather than stated preferences.

**Feeds:** Layers 3 (Risk & Decision Architecture), 4 (Execution & Consistency)

**How it works:**
- Present realistic scenarios with no obvious "right" answer
- Vary context across domains: financial, career, social, reputational
- Add contextual pressure: family responsibility, time constraints, peer influence
- Follow each scenario with a confidence rating ("How confident are you in this decision?")

**Example (Risk layer):**
> *You've been working on a project for 3 months. Results are mediocre. A new opportunity appears that excites you more. Do you: (a) double down on the current project, (b) run both in parallel, (c) cut your losses and switch, (d) ask someone else to evaluate before deciding?*

Someone who always picks "push through" is revealing sunk cost bias even if they'd never self-report it.

**Time-pressure variation:** Show the same scenario type twice — once with "you have 5 seconds to decide" and once with unlimited time. The difference reveals intuitive vs. analytical dominance.

**Domain-specific risk tradeoffs:** *"Would you take a 60% chance at $1,000 or a guaranteed $400?"* — vary across financial, career, social, and reputational domains to build a multi-dimensional risk profile.

---

### C) Peer Survey (360-Degree Feedback Lite)

**What it is:** A short survey sent to 3-5 people the user trusts. Measures the delta between self-perception and external perception.

**Feeds:** Layer 7 (Self-Perception Gap) — also cross-validates Layers 1-6

**How it works:**
- 10-15 forced-choice questions mirroring the user's own assessment (rephrased in third person)
- 1 open-ended question: *"What is one thing this person overestimates about themselves?"* — this question alone is gold
- 2-3 minutes to complete
- Anonymous aggregation only — show gaps as patterns ("Your peers rate your empathy higher than you do"), never individual attributions ("Sarah thinks you're bad at listening")

**Examples:**
> *"This person follows through on commitments."*
> *"This person pushes decisions quickly."*
> *"Is [Name] more likely to: (A) start a fight to be right, or (B) stay silent to keep peace?"*

**Design considerations:**
- It needs to feel *safe* — people are afraid of what others will say
- Show aggregated gaps, not raw individual responses
- Avoid showing raw comments initially (can unlock as a premium feature later)
- Individual response anonymity is essential for honest feedback

**Viral loop:** Every peer survey is an introduction to the platform. The person filling it out gets curious about their own profile. Include a smooth "Want to take your own assessment?" CTA at the end.

---

### D) Reflection Prompts (Qualitative Depth)

**What it is:** Short open-text responses after each assessment section, plus periodic check-ins.

**Feeds:** Cross-layer synthesis, growth tracking

**How it works:**
- After each major section: *"Describe a recent decision you regret."*
- Monthly check-ins: *"What was the hardest decision you made this month? How did you make it?"*
- LLM analysis extracts: emotional tone, attribution style (blame vs. ownership), risk framing language, recurring themes

**Why it matters:** This creates depth beyond multiple choice. If someone claims high discipline in forced-choice questions but describes repeated abandonment stories in reflections, that contradiction is an insight the synthesis engine can surface.

---

### E) Longitudinal Signals (Growth Over Time)

**What it is:** Behavioral data collected over weeks and months — not from a single session.

**Feeds:** Layer 4 (Execution & Consistency), growth-over-time feature

**How it works:**
- **Retest drift:** Compare scores across retakes (every 6 months). Detect whether traits are stable or shifting. Volatility itself becomes a metric.
- **Sprint completion tracking:** When users set 7-day sprint goals (from Actionable Sprints), track: did they complete? Did they log progress? Did they disappear? This is behavioral execution data, not just self-image.
- **Micro-check-ins:** Weekly or biweekly push notifications or emails — "Quick check-in: how did you handle that conflict this week?" Three taps, done.

---

## 3. Collection Architecture (User Journey)

Rather than one massive evaluation, the profile builds progressively:

### Stage 1: Onboarding (10-15 minutes)

A "quick profile" touching Layers 1 and 3 — about 30-40 questions total, mixing Likert, forced-choice, and 2-3 scenarios. The user gets an immediate cross-layer insight ("here's your behavioral style and risk profile") and is hooked to go deeper.

**Critical design rule:** No "complete all 7 layers before seeing results." They get something valuable fast.

### Stage 2: Deep Dives (10-15 minutes each, self-paced)

Each layer gets its own module the user can take when they want. After each deep dive, the synthesis updates — the more layers completed, the richer the cross-layer patterns. This creates a "collect them all" dynamic without forcing a marathon session.

### Stage 3: Peer Survey (triggered after Layer 1)

Once the user has their own behavioral profile, prompt them to send the peer survey. This naturally gates Layer 7 behind enough self-data to make the comparison meaningful.

### Stage 4: Ongoing Micro-Checks

Weekly or biweekly prompts that refine the profile and feed the growth-over-time feature. Captures data in-context rather than in-the-abstract — someone answering "How do you handle conflict?" 10 minutes after an actual conflict gives different (more accurate) data than answering on a random Tuesday afternoon.

### Stage 5: Contextual Triggers

The AI coach can request data when relevant. If a user tells the coach *"I have a stressful meeting coming up,"* the system says: *"To give better advice, I need to understand your conflict style — take this 3-minute survey."* Data collection becomes part of the value, not a prerequisite for it.

---

## 4. Question Design Principles

Regardless of method, these principles guide every question:

**Be specific, not clinical.** "I enjoy meeting new people" is boring and vague. Better: *"At a networking event, you're more likely to: (a) work the room and talk to 10 people briefly, (b) find 2-3 people and have deep conversations, (c) stick with people you already know, (d) find a reason to leave early."* — people can actually picture themselves doing this.

**Avoid transparent "right" answers.** "I care about other people's feelings" — everyone says yes. Better to create tension between two positive options: *"When a teammate is struggling and it's affecting the deadline, do you prioritize supporting them emotionally or addressing the performance gap directly?"* Neither answer is wrong, but they reveal different things.

**Build in validity checks.** Ask the same construct from different angles and flag inconsistencies. Inconsistency itself is data — it might mean the person is context-dependent rather than consistent, which is worth surfacing.

**Add confidence ratings after key decisions.** After scenario-based questions, ask: *"How confident are you in this decision?"* This measures confidence calibration — the gap between confidence and accuracy is a powerful insight, especially when compared to peer ratings.

---

## 5. Data Quality & Bias Mitigation

### Social Desirability Bias (The Biggest Threat)

People answer how they *want* to be, not how they *are*. Mitigations:
- Forced-choice between two equally "good" options
- Scenario-based questions where there's no obvious best answer
- Peer data as a cross-check
- Comparing narrative reflections against quantitative scores — detect when someone claims high discipline but describes repeated abandonment

### Response Pattern Analysis

Measure behind the scenes:
- **Speed anomalies** — if someone answers 120 questions in 2 minutes, flag low reliability
- **Inconsistency** across similar questions asked differently
- **Extreme answering bias** and midpoint bias
- **Straight-lining detection** — answering the same value repeatedly

This produces a **per-layer confidence score**: not just "you scored 78% on risk tolerance" but "your risk tolerance is high (confidence: strong)" vs. "your conflict style is still emerging (take the deep dive for a more stable reading)." We're measuring measurement quality, not just traits.

Response pattern analysis should be disclosed to users ("We also analyze your response patterns, not just your answers") and opt-in.

### Fatigue Effects

Answer quality drops after ~15 minutes. Mitigations:
- Keep modules under 15 minutes (target 8-12)
- Show progress bars
- Let people save and return
- Front-load the most important questions in each module

### Retest Reliability

If someone takes the same layer twice, do they get similar results? Track this and build confidence intervals into outputs.

---

## 6. Anti-Fatigue UX Principles

To keep users from dropping off during the 7-layer journey:

**Progressive disclosure.** Give value before asking for completion. The onboarding assessment gives insights immediately — deeper layers unlock richer patterns.

**"Earned insights."** At natural breakpoints: *"You've answered 10 questions. We've identified your #1 Decision Bias. Want to see it now or finish the set for a full report?"* — partial results reward continued engagement.

**Profile visualization.** A visual representation (e.g., a "brain map" or profile card) that gains resolution and detail as more data is provided. The incomplete visualization itself motivates completion.

**Short modules.** 8-12 minutes each. Never feel like a slog.

---

## 7. Calibration & Validation (Post-Launch)

To build scientific credibility:

### Use Public Domain Item Banks
- IPIP for Big Five (public domain, 3,329+ items)
- Holland RIASEC from O*NET
- Scenario-based items custom-built on Kahneman & Tversky research

### Pilot with 200-500 Users
Run:
- **Internal consistency** (Cronbach's alpha) — do items within each layer measure the same construct?
- **Factor analysis** — do the dimensions hold up empirically?
- **Test-retest reliability** — stable scores on retake?

### Track Predictive Validity
Does "high execution score" correlate with sprint completion? Does "high risk tolerance" correlate with actual career moves? If yes, the model strengthens.

---

## 8. Data Schema

### Core Fields

```
user_id
layer_id
dimension_id
raw_score
normalized_score
confidence_score
timestamp
source (self | peer | simulation | longitudinal)
reliability_index
```

This enables cross-layer synthesis, MCP exposure, and historical trend charts.

### MCP-Ready Structure

| Data Point Type | Collection Method | Storage Format |
|---|---|---|
| **Traits** | Psychometric surveys | Vectorized scores (normalized) |
| **Narrative** | Reflection prompts, AI coaching transcripts | Key-value tags (e.g., `fear_pattern: "rejection"`) |
| **Peer Delta** | Layer 7 surveys | Divergence coefficients |
| **Context** | User profile settings | Environment tags (e.g., `work_env: "high-growth startup"`) |

---

## 9. Ethical & Legal Guardrails

**Results are informational, not diagnostic.** The platform does not provide mental health evaluations, clinical diagnoses, or medical advice. Include clear disclaimers.

**Peer data anonymization.** Show aggregated patterns only — never attribute specific feedback to individual respondents. Individual response anonymity is non-negotiable for honest data.

**Response pattern analysis disclosure.** If we analyze how users interact (speed, consistency, revision patterns), disclose it and make it opt-in.

**Hiring use cases.** If the platform is used for candidate evaluation (B2B), employment testing regulations may apply. Approach with caution — this likely requires legal review before launch.

---

## 10. Phased Rollout

### MVP (Phase 1)

**Collect:**
- Structured self-report with forced-choice emphasis (Layer 1: Behavioral Dynamics)
- Scenario-based risk simulations with confidence ratings (Layer 3: Risk & Decision Architecture)
- Short peer survey, 10-15 items (Layer 7: Self-Perception Gap)
- Basic reflection prompts after each section

**Total user commitment:** ~20 minutes of active assessment, plus waiting for peer responses. They get cross-layer synthesis after just the first two layers.

### Phase 2

**Add:**
- Micro-commitment tracking and sprint completion data (feeds Layer 4)
- Reliability scoring (per-layer confidence from response pattern analysis)
- Growth retesting (6-month retakes with drift detection)

### Phase 3

**Add:**
- Passive data integrations: calendar analysis, communication tone analysis (with explicit consent)
- Social graph mapping for B2B teams (who trusts whom, who defers to whom)
- Advanced NLP on accumulated reflection data
- Gamified behavioral tasks (prioritization exercises, negotiation mini-games)

At Phase 3, the platform moves from "test platform" to "behavior OS."
