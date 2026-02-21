---
description: >
  Invoke this skill when the user asks where to advertise, what channels to use,
  how to reach their target audience, or which platforms to run ads on.
  Triggers: "where should I advertise", "what channels should I use", "should I run Meta or Google",
  "how do I reach [ICP]", "what's the best platform for my product".
argument-hint: Any context about what's already been tried or ruled out
allowed-tools: Read, WebFetch, WebSearch
---

# Channel Identification Skill

Identify the right acquisition channel for this product and ICP. Rank top 2 options. Be explicit about what NOT to do first and why.

## Rule

**Only recommend paid channels after at least one organic channel has been tested.** Organic validates the message before you pay to amplify it. If organic doesn't convert, paid will just burn money faster.

## Process

1. **Read `project/product-brief.md`** to understand: ICP (who they are, where they spend time), ticket size/price point, offer type (free trial / demo / direct purchase), awareness level.
2. **Check organic channels first** — these cost $0 and validate the message before spending budget.
3. **Apply channel selection logic** from `funnel-frameworks.md` for paid channels:
   - Where does this ICP actually spend time?
   - What is their awareness level? (do they know they have this problem? do they know solutions exist?)
   - Does the ticket size support the channel's typical CAC?
   - What's the sales cycle? Can it close without human touch?
4. **Rank top 2 channels total** (organic first, paid second if warranted).
5. **Name what NOT to do first** — and explain why.

## Organic-First Options (Always Evaluate Before Paid)

**Build in Public (X / LinkedIn)**
- Document the build: revenue numbers, failures, lessons. Specific > inspirational.
- Levels' formula: "[specific number] + [honest context] + [one takeaway]" — not "day 47 of my journey 🚀"
- Cost: $0. Trust-building effect compounds over time. Best for: B2B, developer tools, productivity.

**Community Embedding (Reddit, Slack groups, Discord, Indie Hackers)**
- Fish where the fish are. Find the 2–3 communities your ICP lives in.
- Contribute first (answer questions, share genuine insights) before posting about your product.
- Direct DM outreach to people describing the exact pain you solve.
- Cost: $0. Tabunov: "Don't build a distribution channel. Enter an existing one."

**Engineering-as-Marketing (free tool → main product)**
- Build a small, free tool that solves one specific problem for your ICP and points to the main product.
- Marc Lou model: LogoFast (free) → ShipFast (paid). The free tool ranks on Google, builds trust, converts.
- Only viable if the free tool can be built in < 3 days and is genuinely useful standalone.

**SEO / Programmatic Pages**
- Only if the ICP has search intent (they Google the problem).
- Takes 3–6 months to compound. Not a fast-signal channel. Use as a long-term moat, not first move.

## Marketplace GTM (Hybrid: Built-in Traffic + Competition)

Marketplaces have existing buyer traffic and trust infrastructure. You skip cold audience building but compete within the platform.

**When marketplaces work:**
- Info products, courses, templates, plugins, productized services
- Low-touch offers that don't need custom sales process
- Products with clear value prop that fits marketplace taxonomy
- You can compete on reviews/social proof quickly

**Service Marketplaces**
- Upwork, Fiverr, Toptal, Contra — productized services sold as packages
- Win condition: niche positioning + fast review accumulation + clear deliverable scope
- Start with underpriced offer to build reviews, then raise prices once you hit 10+ five-stars

**Digital Product Marketplaces**
- Gumroad, Lemon Squeezy — info products, templates, design assets, small SaaS
- AppSumo, ProductHunt — launch platforms with built-in audience of early adopters
- ThemeForest, Creative Market — design assets, WordPress themes, web templates
- Win condition: strong launch (first week drives organic ranking), compelling demo/preview

**Plugin/Extension Marketplaces**
- Shopify App Store, WordPress plugins, Figma plugins, Notion templates, Chrome extensions
- Win condition: solve a specific job that the main platform doesn't address well
- Distribution is built-in but saturated — need differentiation or underserved niche

**Course Platforms**
- Udemy, Skillshare, Teachable — educational content
- Win condition: Udemy/Skillshare for discovery (race to bottom on price), Teachable for owned audience + premium pricing

**Marketplace Strategy:**
1. Pick the one marketplace where your ICP already shops for this type of solution
2. Study top 5 performers in your category — what do their titles, previews, and reviews emphasize?
3. Launch with an aggressive intro offer or discount to accumulate reviews fast
4. Optimize for marketplace SEO (title, description, tags) not Google SEO
5. Plan to extract buyers to owned channel (email list, community) — marketplace owns the customer relationship

## Output Format

**Primary Channel (start here):**
[Name — e.g., BIP on X, Reddit community, Gumroad, Upwork]
Type: [Organic / Marketplace / Paid]
Why it fits: [Why this ICP will be reached here + product type match]
Starting point: [Exact first action — what to post, which marketplace, what to build, which sub]

**Secondary Channel (after primary shows traction):**
[Name — e.g., Meta, LinkedIn, Google Search, AppSumo]
Type: [Organic / Marketplace / Paid]
Why it fits: [Match between ICP, awareness, ticket size, and channel mechanics]
Starting point: [Format, targeting angle, budget range to start, or launch strategy]

**Don't start with: [Channel]**
Because: [One specific reason — e.g., "your ICP has never heard of this problem category, so search volume doesn't exist yet"]

**Next step**: One concrete action to take in the next 48 hours.

Don't list 5 channels. Pick 2 and commit. Recommend marketplace only if product type fits (info products, templates, plugins, productized services). If the brief doesn't have enough info to make a call, ask for the one missing piece that would determine the answer.
