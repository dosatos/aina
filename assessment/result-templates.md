# Result Templates: 10-Question Diagnosis

**Purpose:** Transform 10 answers into personalized diagnosis that feels accurate and actionable.

---

## Scoring Logic (Updated for Binary Choices)

### Part 1: Behavioral Wiring Profile (Q1-Q3)

**Q1: Assertiveness (Binary)**
- 2 = High ("Jump in and make decision")
- 1 = Low ("Facilitate until group aligns")

**Q2: Pace Preference (Binary)**
- 2 = Fast ("Make the call at 80%")
- 1 = Slow/deliberate ("Keep researching to 90%+")

**Q3: Task vs People Orientation (Binary)**
- 2 = High task focus ("Reassign work")
- 1 = High people focus ("Talk to them first")

**Operating Velocity Score:** Q1 + Q2 + Q3 (range: 3-6)

### Intensity Scaling Bands (Operating Velocity)

| Score | Band Label | Language Modifier |
|-------|-----------|------------------|
| 6 | Very High | "decisive and fast-moving" |
| 5 | High | "generally decisive" or "quick to act" |
| 4 | Moderate | "balanced between speed and caution" |
| 3 | Low | "deliberate and consensus-oriented" |

### Part 2: Decision Pattern Flags (Q4-Q6)

**Q4: Sunk Cost Bias (Binary)**
- 2 = Low bias ("Sunk cost is sunk")
- 1 = High bias ("Keep trying to make it work")

**Q5: Loss Aversion (Binary)**
- 2 = Low aversion ("Take upside potential")
- 1 = High aversion ("Value certainty")

**Q6: Reputational Risk Tolerance (Binary)**
- 2 = Low aversion ("Post with data")
- 1 = High aversion ("Don't post")

**Risk Posture Score:** Q4 + Q5 + Q6 (range: 3-6)

### Intensity Scaling Bands (Risk Posture)

| Score | Band Label | Language Modifier |
|-------|-----------|------------------|
| 6 | Very High | "comfortable taking visible risks" or "bold in decision-making" |
| 5 | Moderate-High | "takes calculated risks" or "selective about risk" |
| 4 | Moderate | "risk-aware but pragmatic" |
| 3 | Low | "prefers protecting downside" or "values certainty" |

### Part 3: Career Context (Q7-Q10)

**Q7: Primary Drain** (categorical)
- A = Lack of autonomy
- B = Unclear expectations
- C = Repetitive work
- D = Too much people management
- E = Too much solo work
- F = High stress without control
- G = Lack of impact/meaning
- H = Something else (please specify)

**Q8: Ideal Role Emphasis** (categorical)
- A = Deep technical/specialist
- B = Strategic thinking
- C = Building/leading teams
- D = High autonomy/ownership
- E = Structured environment
- F = Fast-paced/dynamic


**Q9: Role Type** (context)
- A = IC
- B = Manager
- C = Senior Leader
- D = Founder/Executive
- E = Between roles

**Q10: Experience Level** (context)
- A = 0-2 years
- B = 3-5 years
- C = 6-10 years
- D = 11-15 years
- E = 16+ years

### How to Use Q9/Q10 (Role Context Injection)

Add role-specific language to make results feel tailored:

**Examples:**

| Q9 | Q10 | Context Language to Add |
|----|-----|------------------------|
| IC | 0-2 years | "As an early-career IC, this pattern often shows up as..." |
| IC | 6-10 years | "With 6-10 years as an IC, you've likely noticed..." |
| Manager | 11-15 years | "As a manager with 11+ years of experience, you know how to..." |
| Senior Leader | 16+ years | "At your level (Director+, 16+ years), this tension manifests as..." |
| Between roles | Any | "This mismatch may be why you're between roles right now..." |

**Where to inject:**
- In "THE MISMATCH" section: "As a [role] with [years] of experience, this hits differently because..."
- In "WHERE YOU SHINE" section: "At your career stage ([role], [years]), look for..."
- In red flags: "For someone at your level, avoid..."

**Effect:** Results feel less like horoscopes, more like someone who understands your specific career situation.

---

## Tension Detection & Prioritization

Based on result-system-design.md, detect and rank tensions using this system:

### Tension Priority Weights

| Tension | Weight | Why |
|---------|--------|-----|
| Sunk Cost Trap | 3 | Concrete, immediately actionable |
| Public-Private Assertiveness Gap | 3 | High "wow that's me" factor |
| Task-People Management Friction | 2 | High-confidence match |
| Speed-Safety Paradox | 2 | Insightful when detected |
| Autonomy-Structure Contradiction | 2 | High value when present |
| Growth-Repetition Conflict | 2 | Requires interpretation |

### Detection Rules

1. **Speed-Safety Paradox:** Q2=2 (Fast) + Q5=1 (High loss aversion)
2. **Public-Private Assertiveness Gap:** Q1=2 (High assertiveness) + Q6=1 (Low reputational risk tolerance)
3. **Task-People Management Friction:** Q3=2 (Task-focused) + Q7=D (Too much people mgmt drains)
4. **Autonomy-Structure Contradiction:** Q7=A (Lack of autonomy drains) + Q8=E (Want structured environment)
5. **Sunk Cost Trap:** Q4=1 (High sunk cost bias) + Q5=1 (High loss aversion)
6. **Growth-Repetition Conflict:** Q7=C (Repetitive work drains) + Q8=A (Want deep technical/specialist)

### Display Logic (Phase 0)

**FREE (no email required):**
- Show ONE tension (highest weight among detected tensions)
- Full narrative with confidence tag

**GATED (requires email):**
- Show remaining 1-2 detected tensions (sorted by weight)
- Full recommendations and red flags

---

## Result Structure Template

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're [pace], [assertiveness], [task/people]-focused.

Decision patterns:
• [Sunk cost behavior]
• [Loss aversion behavior]
• [Reputational risk behavior]

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: [Q7 answer]

This hits you hard because: [connect wiring to drain]

[Specific diagnosis based on wiring + drain combination]

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: [Q8 answer]

Given your wiring, look for:
• [Specific environment characteristic 1]
• [Specific environment characteristic 2]
• [Specific environment characteristic 3]

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. [Criterion based on wiring + ideal role]
2. [Criterion based on primary drain]
3. [Criterion based on decision patterns]

Red flags to avoid:
• [Anti-pattern from drain]
• [Anti-pattern from wiring mismatch]
```

---

## Archetype Examples

### Archetype 1: High-Autonomy IC Trapped in Process-Heavy Role

**Profile:**
- Q1: 2 (High assertiveness)
- Q2: 2 (Fast pace)
- Q3: 2 (Task-focused)
- Q4: 2 (Low sunk cost bias)
- Q5: 2 (Low loss aversion)
- Q6: 2 (Low reputational risk aversion)
- Q7: A (Lack of autonomy drains me)
- Q8: D (Want high autonomy/ownership)
- Q9: A (IC)
- Q10: C (6-10 years)

**Result:**

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're decisive and fast-moving, task-focused with high execution bias.

Operating Velocity: VERY HIGH (6/6)
Risk Posture: VERY HIGH (6/6)

Decision patterns:
• You cut losses fast—sunk cost doesn't trap you
• You take calculated risks for higher upside
• You're comfortable taking visible risks when you have data

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: Lack of autonomy (micromanagement, too many approvals)

This hits you hard because: You're wired for fast decisions and high ownership. Every approval layer feels like friction. You see the solution, know how to execute, and get blocked by process.

Your nervous system interprets this as: "I'm being prevented from doing my job."

The real cost: You're spending energy managing up instead of building. Every delay compounds your frustration because you operate at a faster pace than your environment allows.

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: High autonomy and ownership

Given your wiring, look for:
• Early-stage startups or small teams where you own entire problem domains
• Roles with "build it your way" mandates—outcome accountability, not process compliance
• Managers who give you the problem and trust you to solve it (weekly check-ins, not daily status updates)

Risk-specific fit: With your high risk tolerance (6/6), you should favor roles with significant upside potential—equity, performance bonuses, commission structures. You can handle volatility that others avoid. Don't settle for purely fixed comp.

You'll thrive when: Someone hands you a goal, a deadline, and gets out of your way. As an IC with 6-10 years of experience, you're past the point of needing direction—you need ownership.

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. **Decision authority:** Ask in interviews: "What decisions can I make without approval?"
2. **Manager style:** Look for results-focused leaders, not process-focused ones
3. **Company stage:** Favor <50 people (fewer approval layers)

Red flags to avoid:
• "We have a clear process for everything"
• Multiple sign-offs required for routine decisions
• Manager describes themselves as "hands-on"

Risk-aware red flags:
• Purely fixed compensation (wastes your high risk tolerance—look for equity/bonus structures)
• "We minimize risk at all costs" cultures (you thrive on calculated bets, not safety-first environments)
• Large, bureaucratic orgs optimized for stability over growth
```

---

### Archetype 2: Deliberate Thinker in Fast-Paced Chaos

**Profile:**
- Q1: 1 (Low assertiveness)
- Q2: 1 (Slow/deliberate pace)
- Q3: 1 (People-focused)
- Q4: 1 (Moderate-high sunk cost bias)
- Q5: 1 (High loss aversion)
- Q6: 1 (High reputational risk aversion)
- Q7: B (Unclear expectations / shifting priorities)
- Q8: E (Structured environment with clear processes)

**Result:**

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're deliberate, facilitative, and balanced between task and people.

Decision patterns:
• You prefer certainty—need to fully understand before committing
• You avoid unnecessary risk when stakes are high
• You value depth over speed

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: Unclear expectations or constantly shifting priorities

This hits you hard because: You're wired to think deeply and systematically. You need to understand the full context before you can do your best work. But your environment keeps moving the goalposts.

The signal you're getting: "I can't win. I'm solving the wrong problem."

The real cost: You spend energy adapting to chaos instead of going deep. By the time you understand the problem, the requirements have changed. You never get to leverage your natural strength: thorough, high-quality thinking.

Last 3 performance reviews probably mentioned: "Takes longer to ramp up" or "needs more context than we can provide in a fast-moving environment."

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: Structured environment with clear processes

Given your wiring, look for:
• Mature companies (Series C+, or large enterprises) with established processes
• Roles with defined scope and success criteria—where "done" is measurable
• Teams that value quality over speed—where "did it right" beats "shipped fast"

You'll thrive when: You have 2 weeks to solve a well-defined problem and can go as deep as needed.

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. **Stability:** Ask about roadmap stability. Red flag: "We pivot based on market feedback every 2 weeks"
2. **Process maturity:** Look for "We have a clear planning process" (not "We move fast and break things")
3. **Manager communication:** Ask: "How often do priorities change mid-sprint?"

Red flags to avoid:
• "We're figuring it out as we go"
• "Wear many hats" (code for unclear scope)
• Startup <20 people (too much chaos)
```

---

### Archetype 3: People-Focused IC Doing Too Much Solo Work

**Profile:**
- Q1: 1 (Low assertiveness - facilitative)
- Q2: 2 (Fast pace - moves quickly)
- Q3: 1 (People-focused)
- Q4: 2 (Low sunk cost bias - rational decisions)
- Q5: 2 (Low loss aversion - takes calculated risks)
- Q6: 2 (Low reputational risk aversion - willing to speak up)
- Q7: E (Too much solo work, not enough collaboration)
- Q8: C (Building and leading teams)

**Result:**

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're facilitative, fast-moving, and people-focused.

Decision patterns:
• You balance speed with thoughtfulness
• You're comfortable with calculated risk
• You lead by building consensus, not dictating direction

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: Too much solo work, not enough collaboration

This hits you hard because: You're energized by people. You do your best thinking in conversation. You want to coach, align, build shared understanding. But your current role rewards individual output.

What this actually means: You're isolated. Your natural advantage—helping others succeed—doesn't matter in a role that only measures individual output.

The real cost: You're forcing yourself into deep solo work when your natural advantage is synthesis, alignment, and helping others do their best work. Every Zoom-off head-down day feels draining instead of energizing.

You probably think: "Maybe I'm not technical enough" when the real issue is: you're solving the wrong problems with the wrong tools.

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: Building and leading teams

Given your wiring, look for:
• People management track (lead 2-5 people, own their growth)
• Cross-functional roles (product manager, team lead, program manager)
• Collaborative environments where success = team output, not individual heroics

You'll thrive when: Your job is to make 5 people 20% more effective, not to be a solo 10x contributor.

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. **Management opportunity:** Ask: "What's the path to managing people here?" (Don't wait 3 years)
2. **Collaboration intensity:** Look for roles with "cross-functional" or "team lead" in the title
3. **Success metrics:** Avoid roles measured purely on individual output

Red flags to avoid:
• "We hire people who can work independently"
• "Minimal meetings culture" (your strength is collaboration)
• IC roles at companies with no clear management track
```

---

### Archetype 4: Strategic Thinker Stuck in Execution Mode

**Profile:**
- Q1: 2 (High assertiveness)
- Q2: 1 (Slow/deliberate pace)
- Q3: 2 (Task-focused)
- Q4: 2 (Low sunk cost bias - cuts bad projects)
- Q5: 1 (High loss aversion - prefers stability)
- Q6: 2 (Low reputational risk - challenges assumptions)
- Q7: C (Repetitive work without learning/growth)
- Q8: B (Strategic thinking and planning)

**Result:**

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're deliberate, pragmatic, and task-focused.

Decision patterns:
• You cut bad projects quickly—you see the ROI math
• You prefer stability over high-variance outcomes
• You're willing to challenge assumptions when data supports it

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: Repetitive work without learning/growth

This hits you hard because: You're wired to think systemically. You see patterns, optimize processes, and spot inefficiencies. But your role has you executing the same playbook on repeat.

The real cost: You're spending mental energy on work that doesn't require your full cognitive capacity. You're solving the same problem 12 times instead of solving it once at the system level. You're an architect being asked to lay bricks.

The quiet fear: "I'm getting good at something that doesn't matter."

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: Strategic thinking and planning

Given your wiring, look for:
• Senior IC roles (Staff, Principal) where the job is "solve the hard problems"
• Strategy-adjacent roles (chief of staff, BizOps, strategic initiatives)
• Roles with "design the system" mandates, not "execute the system"

You'll thrive when: Your job is to figure out what the team should build, not to build the same thing 100 times.

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. **Scope:** Ask: "What % of the role is net-new problems vs repeating established processes?"
2. **Seniority:** Target Staff+ IC or strategy roles (avoid "Junior" or "Associate" titles)
3. **Learning budget:** Ask: "How does the company support continuous learning?" (stipend, conference budget, etc.)

Red flags to avoid:
• "Proven playbook" (means: repeat what we already know)
• "High-volume execution" (means: do the same thing 50 times)
• Roles that cap at "Senior" with no Staff+ track
```

---

### Archetype 5: The Assertive Analyst (Mixed Profile)

**Profile:**
- Q1: 2 (High assertiveness - makes calls)
- Q2: 1 (Slow/deliberate pace - needs 90%+ info)
- Q3: 2 (Task-focused)
- Q4: 2 (Low sunk cost bias - cuts bad projects)
- Q5: 1 (High loss aversion - prefers certainty)
- Q6: 2 (Low reputational risk - challenges assumptions)
- Q7: B (Unclear expectations / shifting priorities)
- Q8: B (Strategic thinking and planning)
- Q9: B (Manager)
- Q10: D (11-15 years)

**Result:**

```
═══════════════════════════════════════════════════════════
YOUR WIRING
═══════════════════════════════════════════════════════════

You're decisive but deliberate, task-focused with high standards.

Operating Velocity: MODERATE (4/6) — balanced between speed and caution
Risk Posture: MODERATE-HIGH (5/6) — takes calculated risks

Decision patterns:
• You're assertive—you'll make the call when it needs to be made
• But you need high confidence first—you won't move at 80%
• You cut bad projects quickly when the data is clear
• You're willing to challenge assumptions publicly when logic supports it

The internal tension: You want to lead decisively, but you need time to think first. Teams experience you as confident but cautious—willing to make tough calls, but only after thorough analysis.

═══════════════════════════════════════════════════════════
THE MISMATCH
═══════════════════════════════════════════════════════════

You're drained by: Unclear expectations or constantly shifting priorities

This hits you hard because: You're wired to make high-quality decisions—but that requires stable goals and time to analyze. When priorities shift every two weeks, you can't operate at your best. You're stuck choosing between "decide fast with incomplete info" (uncomfortable) or "analyze thoroughly but miss the window" (frustrating).

The signal you're getting: "By the time I understand the problem well enough to solve it correctly, we're solving a different problem."

The real cost: As a manager with 11+ years of experience, you know how to make complex calls—but you need context stability to do it well. Your team sees you as indecisive, but the real issue is environmental chaos, not your wiring.

═══════════════════════════════════════════════════════════
WHERE YOU SHINE
═══════════════════════════════════════════════════════════

You want: Strategic thinking and planning

Given your wiring, look for:
• Management roles in mature orgs (Series C+) with quarterly planning cycles, not weekly pivots
• Strategy roles where the job is "make the right call" not "make a fast call"
• Companies that value decision quality over decision speed—where "we got it right" beats "we shipped fast"

You'll thrive when: You have 2-3 weeks to analyze a strategic decision, then the authority to make the call and commit the team.

Risk-specific fit: You're comfortable with calculated risks (Risk Posture: 5/6), so favor roles with performance upside, equity, or bonus structures—just ensure the success criteria are stable, not shifting.

═══════════════════════════════════════════════════════════
NEXT STEP
═══════════════════════════════════════════════════════════

Filter your next role for:
1. **Planning cadence:** Ask: "How often do strategic priorities change?" (Target: quarterly, not weekly)
2. **Decision authority:** Ask: "What decisions require my manager's approval vs my own judgment?"
3. **Manager style:** Look for leaders who value "right answer" over "fast answer"

Red flags to avoid:
• "We pivot quickly based on market feedback" (chaos trigger)
• "Fast-paced, rapidly changing environment" (contradicts your deliberate wiring)
• Early-stage startups (pre-Series B)—too much volatility for your operating style

Risk-aware red flags:
• Purely fixed compensation with no upside (underutilizes your risk tolerance)
• Roles with no performance-based rewards (you can handle variable comp)
```

---

## Mismatch Diagnosis Matrix

Use this to map Q7 (drain) + wiring profile → diagnosis insight.

| Drain (Q7) | High Assertiveness + Fast Pace | Low Assertiveness + Slow Pace | High People Focus | High Task Focus |
|------------|--------------------------------|-------------------------------|-------------------|-----------------|
| **Lack of autonomy** | "You're wired for ownership. Approvals feel like roadblocks." | "You need space to think deeply. Micromanagement prevents that." | "You can't build relationships under surveillance." | "You see the path. You're blocked from executing." |
| **Unclear expectations** | "You make fast decisions. Shifting goals waste your speed." | "You need stable goals to go deep. Chaos prevents quality work." | "You can't align people when the target keeps moving." | "You optimize systems. Can't optimize what keeps changing." |
| **Repetitive work** | "You're wired to build new things, not repeat old ones." | "You're wired for depth. Repetition doesn't reward deep thinking." | "You're energized by new people/challenges. Repetition drains that." | "You're a systems thinker. Repetition doesn't use that skill." |
| **Too much people mgmt** | "You're wired for fast execution. People problems slow you down." | "You need thinking time. People management consumes it." | "You're good at it, but it's 100% of your day. No variety." | "You're task-focused. People problems feel like distractions." |
| **Too much solo work** | "You're assertive and decisive. You need people to lead." | "You think by talking. Solo work isolates your best skill." | "You're energized by collaboration. Solo work drains you." | "You're productive solo, but miss the strategic interaction." |
| **High stress without control** | "You're wired to act. Stress without agency is torture." | "You mitigate risk by analyzing. Can't do that when out of control." | "You manage stress through relationships. No support system here." | "You control outcomes through execution. Can't execute = can't cope." |
| **Lack of impact** | "You're wired for visible results. Invisibility feels like failure." | "You invest deeply in quality. If it doesn't matter, why invest?" | "You're energized by helping others. No one to help = no meaning." | "You're task-driven. Need to see output matter." |

---

## Environment Recommendations Matrix

Use this to map Q8 (ideal role) + wiring → specific recommendations.

| Ideal Role (Q8) | High Assertiveness + Fast | Low Assertiveness + Slow | High People Focus | High Task Focus |
|-----------------|---------------------------|--------------------------|-------------------|-----------------|
| **Deep technical/specialist** | "IC track at high-growth startup (build fast, own your domain)" | "Research role or large company (time to go deep)" | "Technical lead (mentor while coding)" | "Specialist IC (focus on craft, not people)" |
| **Strategic thinking** | "Chief of Staff, BizOps (fast strategic decisions)" | "Strategy/planning role (time for analysis)" | "Cross-functional strategy (align people)" | "Staff+ IC (solve hard systems problems)" |
| **Building/leading teams** | "High-growth startup manager (build and scale fast)" | "Mature company people manager (develop people deeply)" | "People management (your natural wiring)" | "Results-focused team lead (lead via systems, not relationships)" |
| **High autonomy/ownership** | "Startup IC or founder (own entire problem)" | "Senior IC with defined domain (deep autonomy)" | "Product manager (own outcomes, work with people)" | "Technical founder or senior IC (own, execute)" |
| **Structured environment** | "Process-heavy scale-up (fast, but within systems)" | "Large enterprise (stable, deep processes)" | "Program manager in structured org" | "Operations role in mature company" |
| **Fast-paced/dynamic** | "Startup or growth-stage company (natural fit)" | "Avoid. Mismatch." | "Agency/consulting (new people, new problems)" | "Early-stage startup IC (ship fast, iterate)" |


---

## Risk-Specific Modifiers (Tier 2 Addition)

Add these to "WHERE YOU SHINE" section based on Risk Posture score:

### High Risk (Score 5-6)

**Add to recommendations:**
- "Favor roles with performance upside—equity, variable comp, bonus structures"
- "Look for environments with asymmetric return potential (early-stage, founder track, commission-based)"
- "You can handle uncertainty—don't over-index on stability"

**Add to red flags:**
- "Purely fixed compensation with no upside (underutilizes your risk tolerance)"
- "Highly bureaucratic environments optimized for safety over growth"
- "Roles where 'don't make mistakes' is more important than 'create breakthroughs'"

### Low Risk (Score 3-4)

**Add to recommendations:**
- "Favor predictable compensation (base salary over variable comp)"
- "Look for stable roadmaps and clear success metrics"
- "Prioritize environments where outcomes are controllable and measurable"

**Add to red flags:**
- "Heavy variable compensation (>30% of total comp at risk)"
- "Undefined success metrics or outcomes dependent on factors outside your control"
- "Roles with high reputational exposure (exec visibility, public-facing)"

---

## Usage Guide for Manual Scoring (Phase 0)

**Implementation approach:** Use **fixed outputs** (route to closest matching archetype example). For Phase 0, write 5-6 pre-written examples covering common profiles. If you get >100 responses, consider dynamic generation.

**Steps:**

1. **Score Q1-Q6** with binary values (1 or 2)
   - Option A typically scores 2 (high on dimension)
   - Option B typically scores 1 (low on dimension)

2. **Calculate axis scores:**
   - **Operating Velocity** = Q1 + Q2 + Q3 (range: 3-6)
   - **Risk Posture** = Q4 + Q5 + Q6 (range: 3-6)

3. **Apply intensity bands** (use language modifiers from tables above):
   - Velocity 6: "decisive and fast-moving"
   - Velocity 5: "generally decisive"
   - Velocity 4: "balanced between speed and caution"
   - Velocity 3: "deliberate and consensus-oriented"
   - (Same for Risk—see Risk Posture table)

4. **Check boundary handling:**
   - If Velocity or Risk = 4 or 5, add "leaning" language
   - Example: Score 5 = "High (leaning toward very high)"

5. **Detect tensions** (see Tension Detection section):
   - Check all 6 detection rules
   - Assign weights (2 or 3)
   - Sort by weight, take top 2-3

6. **Apply email gate logic:**
   - FREE: Show archetype + scores + ONE tension (highest weight)
   - GATED: Remaining 1-2 tensions + full recommendations

7. **Look up mismatch:** Q7 + wiring in Mismatch Matrix → diagnosis

8. **Look up recommendations:** Q8 + wiring in Environment Matrix → base recommendations

9. **Inject risk modifiers:** Add risk-specific recommendations and red flags based on Risk Posture (3-4 vs 5-6)

10. **Add role context from Q9/Q10:**
    - Q9=Manager + Q10=D → "As a manager with 11+ years..."
    - Q9=IC + Q10=B → "As an IC with 3-5 years..."
    - Use role context to make diagnosis feel specific

11. **Route to closest archetype example** or fill template with personalized language

**Time per result (manual):** 3-5 minutes once familiar with matrices.

**Reference:** See `/assessment/result-system-design.md` for complete archetype descriptions and tension narratives.

---

## Next Steps

- ✅ Create result-templates.md (this file)
- ⏭ Create open-ended-questions.md
- ⏭ Update landing page
- ⏭ Build first 8-10 results manually to refine language
- ⏭ Automate if >50 completions + >60% email capture

---

## Quality Check

**Good result feels like:**
- "This described me perfectly"
- "How did you know that?"
- "This explains why I've been stuck"

**Bad result feels like:**
- "Just another personality test"
- "Too generic"
- "Doesn't tell me what to do"

**If results feel generic:**
- Add more specific behavioral examples in mismatch section
- Use their exact language from Q7/Q8
- Include role-level context from Q9/Q10
