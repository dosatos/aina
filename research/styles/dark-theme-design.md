# Dark Theme Design System

**Created:** February 21, 2026
**Inspiration:** career-fork-now.base44.app
**Applied to:** AINAM landing page (index-dark.html)

---

## Design Philosophy

**Developer-first aesthetic.** Technical, precise, no-nonsense. Code metaphors as first-class visual language. High contrast, sharp edges, neon accents on dark canvas.

---

## Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| **Dark BG** | `#0a0e1a` | Main background (navy-black) |
| **Dark Surface** | `#131824` | Cards, sections, elevated elements |
| **Dark Border** | `#1e293b` | Subtle borders, dividers |
| **Neon Cyan** | `#22d3ee` | Primary CTA, links, key metrics |
| **Neon Magenta** | `#ff79c6` | Highlights, warnings, emphasis |
| **Neon Green** | `#50fa7b` | Success states, checkmarks |
| **Neon Yellow** | `#f1fa8c` | Scores, alerts, numbers |
| **Neon Purple** | `#bd93f9` | Secondary accents |

**Why:** Syntax highlighting color scheme. Familiar to developers. High contrast = legibility. Neon pops on dark = attention hierarchy.

---

## Typography

- **Body:** Inter (clean, modern, tech-friendly)
- **Code/Numbers:** JetBrains Mono (developer aesthetic, data feel)
- **Sizes:** Large headlines (4xl-6xl), readable body (lg), small mono captions
- **Weight:** Bold headlines, medium body, mono for technical elements

---

## Key Design Elements

### 1. Sharp Borders (No Rounded Corners)
- Brutalist aesthetic
- Sharp, precise, no-softness
- `border: 1px solid #1e293b` (subtle)
- Hover states: border becomes neon (`border-neon-cyan/50`)

### 2. Code Blocks as Visual Metaphor
```javascript
while (uncertain) {
  research();  // Infinite loop metaphor
}
```
- Syntax highlighting (keyword, function, comment colors)
- Communicates patterns visually
- Developer-native language

### 3. Neon Glow Effects
- Primary CTA: `box-shadow: 0 0 30px rgba(34, 211, 238, 0.6)`
- Subtle glow on interactive elements
- Not overdone (only on key actions)

### 4. Minimal Shadows
- No soft shadows (no `shadow-lg` everywhere)
- Glow effects only where intentional
- Elevation through borders, not shadows

### 5. Icons as Symbols
- `×` for failed/wrong
- `✓` for correct/match
- `→` for progression
- `•` for bullets
- Monospace font = consistent width

---

## Layout Patterns

**Single column, max-width 5xl (1280px):**
- Narrow content = focus
- No sidebars, no distractions
- Generous vertical spacing (mb-12, mb-16, mb-20)

**Sticky header with backdrop blur:**
- Always accessible navigation
- Semi-transparent (`bg-dark-bg/95`)
- Maintains context without blocking content

**Grid for comparisons:**
- 2-column grid on desktop (md:grid-cols-2)
- "Current role" vs "You're wired for"
- Visual contrast = clear mismatch

---

## Why This Works

1. **Target audience alignment:** Mid-career tech professionals expect dark mode, code aesthetics
2. **Differentiation:** Stands out from typical career coaching sites (warm, soft, rounded)
3. **Trust signal:** Technical precision = credible, data-driven (not fluffy self-help)
4. **Attention hierarchy:** Neon accents guide eye to CTA, key insights
5. **Developer familiarity:** Syntax highlighting = "this tool speaks my language"

---

## Implementation Notes

**Fonts:**
- Inter: `font-family: 'Inter', sans-serif`
- JetBrains Mono: `font-family: 'JetBrains Mono', monospace`

**Tailwind config:**
```javascript
colors: {
  'dark-bg': '#0a0e1a',
  'dark-surface': '#131824',
  'dark-border': '#1e293b',
  'neon-cyan': '#22d3ee',
  'neon-magenta': '#ff79c6',
  'neon-green': '#50fa7b',
}
```

**Key CSS:**
- No border-radius (sharp corners)
- Custom scrollbar (dark theme)
- Neon glow: `box-shadow` with rgba colors
- Syntax highlighting: `.token-keyword`, `.token-function`, etc.

---

## Contrast with Light Theme

| Element | Light Theme | Dark Theme |
|---------|-------------|------------|
| Background | White/Slate-50 | Navy-black (#0a0e1a) |
| Primary CTA | Blue-600 gradient | Neon cyan (#22d3ee) |
| Corners | Rounded-2xl | Sharp (border-0) |
| Shadows | Soft blur shadows | Neon glow (selective) |
| Vibe | Friendly, warm, accessible | Technical, precise, developer-first |

---

**File:** `/landing-page/index-dark.html`
**Status:** Production-ready for Phase 0 validation
