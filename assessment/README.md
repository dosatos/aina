# Assessment Framework & Methodology

**Purpose:** This directory contains the core product methodology for the behavioral assessment system—the evaluation framework, scoring logic, result generation, and archetype definitions.

---

## What's Here

### Core Methodology Files

**`result-system-design.md`** — The complete result system design
- Scoring algorithms (Action Orientation + Risk Posture)
- The 4 archetypes (Accelerator, Strategist, Executor, Analyst)
- 6 tension detection rules
- Mismatch diagnostic logic
- Result page structure
- Success metrics

**`result-templates.md`** — Scoring and archetype implementation
- Detailed scoring logic for Q1-Q6
- Binary scoring system (1-2 scale)
- Archetype profile examples with scores
- Mismatch diagnosis matrix
- Environment recommendations matrix
- Manual scoring guide

---

## What's NOT Here (Lives in `/landing-page/`)

**Implementation files** (user-facing):
- `assessment-10q-final.md` — The actual 10 questions for Google Form
- `google-form-implementation-guide.md` — How to build the form
- `open-ended-questions.md` — Optional feedback questions
- `index.html` — Landing page
- Hero/pain variants — Copy testing

**Why the separation?**
- `/assessment/` = Product methodology (how the system works)
- `/landing-page/` = Implementation (what users see/do)

---

## File Relationships

```
/assessment/
  ├── result-system-design.md     ← Defines HOW results are generated
  └── result-templates.md          ← Contains scoring formulas

/landing-page/
  ├── assessment-10q-final.md      ← The questions (references scoring from above)
  ├── google-form-implementation-guide.md ← References questions
  └── index.html                   ← Landing page (links to assessment)
```

**Flow:**
1. User takes assessment (`assessment-10q-final.md`)
2. Responses scored using logic in `result-templates.md`
3. Results generated using framework in `result-system-design.md`

---

## Development Status

**✅ Complete:**
- Scoring system (2-axis: Action + Risk)
- 4 archetype definitions
- 6 tension detection rules
- Mismatch diagnostic matrix
- Result page structure

**🚧 Next Steps:**
- Build actual result page HTML
- Create result generation script (manual scoring for Phase 0)
- Test with 5 users
- Iterate based on "this described me" feedback

---

## Key Design Decisions

**Tone:** Clinical/Direct (not aspirational)
**Archetype Names:** Functional (Accelerator, not "Visionary")
**Depth:** Moderate (archetype + 2-3 tensions + mismatch)
**Email Gate:** After partial result (full PDF requires email)

**Why:**
- Target audience = analytical professionals (engineers, founders)
- They're allergic to "fluffy" personality tests
- Value proposition = tension detection, not static labels

---

## Related Documentation

**Product Vision:** `/docs/combined-vision.md`
**Phase 0 Plan:** `/meta/phases/phase-0-validation.md`
**Persona Research:** `/docs/b2c-persona-research.md`

---

## Version History

**v1.0** (Feb 21, 2026)
- Initial framework design
- 2-axis scoring system
- 4 archetypes with clinical tone
- 6 tension patterns identified
- Mismatch diagnostic logic

**Next:** v1.1 will add result page HTML and manual scoring workflow
