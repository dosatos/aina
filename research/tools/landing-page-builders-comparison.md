# Landing Page Builder Comparison & Recommendation

**Research Date:** February 21, 2026
**Context:** Phase 0 validation — need fastest way to build landing page with AI integration
**Budget:** $0-200 (prefer free tier)

---

## Executive Summary

**UPDATED RECOMMENDATION: Use Claude Code Directly (Pure CLI Workflow)**

After additional research on workflow integration, the optimal approach is:

- **Use Claude Code directly** — no external tools, no context switching
- **Simple HTML + Tailwind CDN** — fast, lightweight, perfect for Phase 0
- **Speed:** 1-2 hours (same as v0, but you control everything)
- **Cost:** $0
- **Workflow:** Never leave Claude Code CLI
- **Deployment:** Vercel CLI (one command)

**Previous recommendation (v0.app) is still valid** if you prefer GUI-based generation, but **pure Claude Code is faster for users who prefer CLI workflows.**

---

## Head-to-Head: v0.app vs bolt.new

| Feature | v0.app (Vercel) ✅ | bolt.new |
|---------|-------------------|----------|
| **Generation Speed** | Minutes | Hours (iterative chat) |
| **Workflow** | Single prompt → generates code → preview | Chat conversation → builds incrementally |
| **Output Type** | React/Next.js UI components | Full stack apps (frontend + backend) |
| **Backend Features** | ❌ Need to add yourself | ✅ Built-in (databases, auth, analytics) |
| **Form Integration** | Manual (Zapier/webhook) | ✅ Built-in |
| **Code Access** | ✅ Full code, GitHub sync | ✅ Full code access |
| **Deployment** | One-click Vercel | Built-in hosting (Bolt Cloud) |
| **Design Iteration** | Visual design mode + re-prompt | Chat to refine |
| **Complexity** | Lower (UI-focused) | Higher (full stack) |
| **Best For** | **Simple landing pages** | Full web apps with backend |
| **Cost** | Free tier | Free tier ($0-30/mo) |

### Why v0.app Wins for Phase 0

**Pros:**
1. **Fastest generation** — "working applications in minutes" (per their site)
2. **Right scope** — UI components only (no backend complexity we don't need)
3. **Clean code** — easy to iterate with AI tools later (Cursor, Claude MCP)
4. **GitHub integration** — automatic version control
5. **Vercel deployment** — industry-leading hosting, free tier, fast edge network
6. **Simpler** — no database setup, no auth flows, just what we need

**What we don't need from bolt.new:**
- Built-in databases (using Google Sheets/Airtable for Phase 0)
- User authentication (no accounts needed yet)
- Backend complexity (static LP + form is enough)

### When to Use bolt.new Instead

**Use bolt.new for:**
- Phase 1 MVP (when building full assessment platform with database)
- Apps requiring user accounts/auth
- Complex backend logic
- Integrated analytics/SEO features

---

## Claude Code Direct Workflow (CLI-First Approach)

**UPDATED RECOMMENDATION: Best option for CLI-first developers**

### What It Is
Use Claude Code CLI directly to build the landing page without external tools. No context switching, full control, same speed.

### Why This Wins for CLI Users

**Context from research:**
- v0.app and bolt.new require **context switching** (web UI → code → back to web UI)
- Both support code export, but you're adding an extra step
- User preference: "I'd prefer not to change the interface of building up the project"

**Advantages:**
1. ✅ **Zero context switching** — never leave Claude Code CLI
2. ✅ **Full control** — understand every line of code
3. ✅ **Same speed** — 1-2 hours (vs v0's 1-2 hours)
4. ✅ **Simpler stack** — HTML + Tailwind CDN (no React/Next.js needed for Phase 0)
5. ✅ **Free** — $0
6. ✅ **Easy deployment** — `vercel deploy` (one command)

### The Workflow

```bash
# 1. Create project directory
mkdir landing-page
cd landing-page

# 2. Use Claude Code to generate
# Prompt Claude: "Create single-page HTML landing page with Tailwind CDN
# using copy from docs/marketing/landing-page-PRODUCTION.md (Template 1).
# Include: responsive design, email form validation, Analytics placeholder."

# Claude generates:
# - index.html (complete page)
# - inline CSS (critical path)
# - vanilla JS (form validation)

# 3. Test locally
python -m http.server 8000
# or
npx serve .

# 4. Iterate in Claude Code
# "Make CTA button more prominent"
# "Add form validation for email"
# "Improve mobile spacing"

# 5. Deploy
vercel deploy
# or
netlify deploy
# or
git push (if using GitHub Pages)
```

### Time Estimate
- **Generation:** 10-20 minutes (Claude writes HTML/CSS/JS)
- **Review/iteration:** 30-60 minutes
- **Deploy/test:** 15-30 minutes
- **Total:** 1-2 hours (same as v0, but never leave CLI)

### What You Get

**Single HTML file:**
```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://cdn.tailwindcss.com"></script>
  <title>Your Assessment Platform</title>
</head>
<body>
  <!-- Hero section -->
  <section class="hero">
    <h1>You've taken 5 personality tests...</h1>
    <button onclick="scrollToForm()">Get Your Profile</button>
  </section>

  <!-- Pain points -->
  <section class="pain-points">...</section>

  <!-- How it works -->
  <section class="how-it-works">...</section>

  <!-- Email form -->
  <form id="emailForm" onsubmit="handleSubmit(event)">
    <input type="email" required>
    <button>Get Early Access</button>
  </form>

  <script>
    // Form validation and submission
    async function handleSubmit(e) {
      e.preventDefault();
      // Send to Airtable/webhook
    }
  </script>
</body>
</html>
```

**Benefits of simple HTML approach:**
- Fast loading (no React bundle)
- Easy to understand and modify
- Perfect for Phase 0 validation
- Can upgrade to React later if needed

### Comparison to v0.app Workflow

| Step | v0.app | Claude Code Direct |
|------|--------|-------------------|
| 1. Generate | Web UI (5 min) | Claude Code CLI (10 min) |
| 2. Preview | v0.app preview | Local server |
| 3. Iterate | v0 design mode | Claude Code CLI |
| 4. Export | GitHub sync | Already local |
| 5. Deploy | Vercel (1 click) | Vercel CLI (1 command) |
| **Total time** | 1-2 hours | 1-2 hours |
| **Context switches** | 3-4 times | 0 times |

### When to Use Claude Code Direct

✅ **Use this when:**
- You prefer CLI workflows
- You want full control and understanding
- You're comfortable with HTML/CSS/JS
- You want to avoid context switching
- You're building a simple landing page

❌ **Use v0.app instead when:**
- You want visual design mode
- You prefer GUI-based tools
- You need React/Next.js components
- You want to see live preview while prompting

---

## v0.app Detailed Analysis

**Source:** https://v0.app/ (redirects from v0.dev)

### What It Is
AI-powered web development platform by Vercel that generates working applications from natural language prompts.

### Key Features
1. **Prompt-Based Creation** — Describe your vision, AI generates code
2. **AI Planning & Building** — System plans, creates tasks automatically
3. **Design Mode** — Visual controls for fine-tuning with live preview
4. **GitHub Integration** — Code syncs directly to repositories
5. **One-Click Deployment** — Instant publishing on Vercel infrastructure

### Workflow (Estimated 1-2 hours for simple LP)
```
1. Sign up at v0.app (free)
2. Enter prompt: "Create a landing page for [product]. Structure: [describe]. Copy: [paste Template 1]"
3. AI generates React/Next.js components (< 5 minutes)
4. Preview → use design mode to refine visually
5. Export to GitHub (automatic sync)
6. Deploy to Vercel (one click, free hosting)
7. Add form integration (Zapier → Airtable, ~20 min)

Total: 1-2 hours from prompt to live URL
```

### Output Example
```jsx
// Clean, maintainable React component
export default function LandingPage() {
  return (
    <div className="min-h-screen">
      <Hero
        headline="You've taken 5 personality tests. Still don't know why you're stuck."
        cta="Get Your Profile in 10 Minutes"
      />
      <PainPoints bullets={[...]} />
      <HowItWorks steps={[...]} />
      <EmailCapture />
    </div>
  )
}
```

### Pricing
- **Free tier:** Available
- **Pro:** Pricing not specified in research (check v0.app for current rates)

### Best For
- Simple landing pages
- UI component generation
- Rapid prototyping
- Projects deploying to Vercel
- Developers who want clean code to iterate on

---

## bolt.new Detailed Analysis

**Source:** https://bolt.new

### What It Is
"#1 professional vibe coding tool" — web-based platform for creating websites/apps through natural language conversations with AI coding agents.

### Key Features
1. **Chat-Based Development** — "Vibe coding" through conversation
2. **Full Stack Integration** — Backend, databases, auth, SEO, hosting, analytics all built-in
3. **Error Reduction** — Claims 98% error reduction through auto-testing
4. **Scale Management** — Handles projects "1,000x larger" with improved context
5. **Multi-Role Support** — Marketers can "spin up campaign pages in hours"
6. **Design System Integration** — Build on-brand with existing design systems

### Workflow (Estimated 2-4 hours for simple LP)
```
1. Sign up at bolt.new (free tier available)
2. Chat: "Build me a landing page for [product]..."
3. AI builds incrementally, back-and-forth conversation
4. Refine through continued chat:
   - "Make the CTA button bigger"
   - "Add email form connected to database"
   - "Change color scheme"
5. Deploy with built-in Bolt Cloud hosting

Total: 2-4 hours (more back-and-forth than v0.app)
```

### Pricing
- **Free tier:** Available
- **Premium:** Up to $30/month

### Best For
- Full web applications
- Projects needing built-in backend
- Users who prefer chat-based iteration
- Marketing teams (per their positioning)
- Complex projects with database requirements

### Why It's Slower for Simple LP
- More comprehensive (builds full stack even when you don't need it)
- Chat-iterative approach takes longer than single prompt
- More features = more configuration decisions
- Overkill for static landing page + form

---

## Traditional Tools (Slower, Less AI Integration)

### Webflow

**Source:** https://webflow.com

**What It Is:** Visual website builder with recent AI features

**Key Features:**
- Three approaches: AI site builder (new), templates, or blank canvas
- Drag-and-drop page building
- CMS integration
- Built-in hosting and SEO
- Interaction/animation tools

**Speed:** Days (even with AI builder)
**AI Integration:** 🟡 New AI builder feature (less mature than v0/bolt)
**Cost:** $14+/month
**Best For:** Design-heavy sites, designers who prefer visual editors

**Why Not for Phase 0:**
- Slower than AI-first tools
- Requires subscription ($14/mo minimum)
- More learning curve for non-designers
- AI features are new/immature

---

### Framer

**Source:** https://framer.com

**What It Is:** "No code website builder loved by designers"

**Key Features:**
- Designer-focused visual editor
- No-code development
- Professional quality output
- E-commerce integration

**Speed:** Days (manual design work)
**AI Integration:** ❌ No AI features identified
**Cost:** Free tier available
**Best For:** Designers, visually complex sites

**Why Not for Phase 0:**
- No AI integration (slower iteration)
- Designer-focused (steeper learning curve)
- Manual design process
- Not optimized for speed

---

### Carrd

**Key Features:**
- Simple one-page site builder
- Template-based
- Very affordable
- Quick setup for basic pages

**Speed:** Hours (but manual)
**AI Integration:** ❌ None
**Cost:** Free tier (limited), $19/year pro
**Best For:** Ultra-simple pages, tight budgets

**Why Not for Phase 0:**
- No AI = slower iteration
- Limited customization
- Manual form integration
- Less flexibility for future changes

---

## Comparison Matrix

| Tool | Speed | AI Native | Cost | Code Access | Backend | Deployment | Best Use Case |
|------|-------|-----------|------|-------------|---------|------------|---------------|
| **Claude Code** | ⚡️⚡️⚡️ 1-2 hrs | ✅ Yes | Free | ✅ Full control | ➕ Add yourself | Vercel CLI | **Phase 0 LP (CLI users)** ✅ |
| **v0.app** | ⚡️⚡️⚡️ 1-2 hrs | ✅ Yes | Free | ✅ GitHub | ❌ Add yourself | Vercel (1-click) | Phase 0 LP (GUI users) |
| **bolt.new** | ⚡️⚡️ 2-4 hrs | ✅ Yes | Free-$30 | ✅ Yes | ✅ Built-in | Bolt Cloud | Phase 1 MVP |
| **Webflow** | ⚡️ Days | 🟡 New feature | $14+/mo | ❌ No | 🟡 CMS | Built-in | Design-heavy |
| **Framer** | ⚡️ Days | ❌ No | Free tier | ❌ No | ❌ No | Built-in | Designers |
| **Carrd** | ⚡️ Hours | ❌ No | Free-$19/yr | ❌ No | ❌ No | Built-in | Ultra-simple |

---

## Decision Framework

### Use Claude Code Direct when: ✅ RECOMMENDED
- ✅ You prefer CLI workflows (no context switching)
- ✅ You want full control over every line of code
- ✅ You're comfortable with HTML/CSS/JS
- ✅ You want to stay in your development environment
- ✅ Simple landing page (no complex frontend framework needed)
- ✅ Fastest for CLI-first developers

### Use v0.app when:
- ✅ You prefer GUI-based tools
- ✅ You want visual design mode
- ✅ You need React/Next.js components
- ✅ You want to see live preview while prompting
- ✅ You prefer clicking over typing commands

### Use bolt.new when:
- Building full web app (Phase 1 MVP)
- Need integrated backend (database, auth)
- Prefer chat-based iteration
- Want everything in one platform
- Not concerned about extra features

### Use Webflow when:
- Design is critical (visual brand identity)
- Non-technical team
- Need CMS features
- Budget allows $14+/month

### Use Framer when:
- Designers on team who know Framer
- Need animation/interaction heavy site
- Visual design takes priority over speed

### Use Carrd when:
- Absolute simplest page possible
- Budget is $0
- Don't need any customization

---

## Recommendation for Phase 0

**Use Claude Code Direct (CLI Workflow)** ✅

**Time to Launch:** 1-2 hours total
- Claude Code LP generation: 10-20 minutes
- Review and iteration: 30-60 minutes
- Deploy and test: 15-30 minutes
- Google Forms quiz: 10 minutes (separate, as planned)

**Why This Works:**
1. **Zero context switching** — stay in Claude Code CLI entire time
2. **Same speed as v0** — 1-2 hours total
3. **Free** — fits $200 Phase 0 budget perfectly
4. **Full control** — understand every line, easy to modify
5. **Simple stack** — HTML + Tailwind CDN (no build step)
6. **User preference** — "I'd prefer not to change the interface"

**Alternative:** If you prefer GUI tools, v0.app is still excellent (see workflow below)

**Claude Code Direct Workflow for Your Phase 0:**

```bash
# 1. Create project directory (from your current location)
cd /Users/byeldos/playground/ainam
mkdir landing-page
cd landing-page

# 2. Use Claude Code (you're already here!)
# Prompt:
# "Read /Users/byeldos/playground/ainam/docs/marketing/landing-page-PRODUCTION.md
#  (Template 1: Career Clarity section) and create a single-page HTML landing page.
#
#  Requirements:
#  - Use Tailwind CDN for styling
#  - Mobile-responsive (mobile-first)
#  - Email capture form with validation
#  - Fast loading (inline critical CSS)
#  - Google Analytics placeholder
#  - Clean, semantic HTML
#
#  Create: index.html"

# Claude generates index.html in ~10 minutes

# 3. Test locally
python3 -m http.server 8000
# Visit http://localhost:8000

# 4. Iterate with Claude Code
# "Make the CTA button larger and more prominent"
# "Add smooth scroll to form on button click"
# "Improve mobile spacing in pain points section"
# "Connect form to Airtable webhook"

# 5. Deploy to Vercel
npm i -g vercel  # one-time install
vercel deploy    # deploy in seconds

# Done! Live URL ready.
```

**Alternative: v0.app Workflow (if you prefer GUI)**

```
1. Go to v0.app
2. Prompt: [same as above]
3. Preview generated page
4. Iterate with design mode
5. Export to GitHub
6. Deploy to Vercel (1 click)
7. Connect form via Zapier/webhook
8. Add Analytics
```

---

## Future Considerations

**Phase 1 (MVP Build):**
- Consider bolt.new for full assessment platform
- OR use Cursor + Claude MCP for custom build
- OR continue with Next.js from v0.app + add backend

**Phase 2 (Scale):**
- v0.app-generated code can scale on Vercel
- May need custom optimization for high traffic
- Consider edge functions for global performance

---

## Sources

1. v0.app — https://v0.app/ (AI-powered React/Next.js generation by Vercel)
2. bolt.new — https://bolt.new (Full stack AI coding platform)
3. Webflow — https://webflow.com (Visual website builder with new AI features)
4. Framer — https://framer.com (No-code designer-focused builder)
5. Carrd — Industry knowledge (simple landing page builder)

**Research Method:** Direct web fetch of current tool documentation (February 2026)

---

## Key Takeaways

1. **AI-first tools (v0.app, bolt.new) are 10x faster than traditional builders**
2. **v0.app is fastest for GUI-based generation** (minutes to generate code)
3. **bolt.new is better for full apps** (backend built-in)
4. **Traditional tools (Webflow, Framer) are slower** but good for specific use cases
5. **For CLI-first developers: Claude Code direct is optimal** (no context switching)
6. **For Phase 0 validation, speed + workflow fit matters most**

**Bottom line:**
- **If you prefer CLI:** Use Claude Code directly (1-2 hours, never leave terminal)
- **If you prefer GUI:** Use v0.app (generates in minutes, then continue in CLI)
