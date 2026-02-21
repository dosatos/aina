## Phase 0.2: Landing Page Implementation (Days 3-5)

**Goal:** Fully styled Template 3 landing page with 4 variants and A/B testing

### Tasks

1. **Define Content Type System**

   Create `src/content/types.ts`:
   ```typescript
   export interface LandingPageContent {
     variant: 'control' | 'variant-a' | 'variant-b' | 'variant-c';
     hero: {
       headline: string;
       subheadline: string;
       ctaText: string;
       trustSignals: string[];
     };
     painPoints: {
       intro: string;
       weeklyBlockers: Array<{
         day: string;
         scenario: string;
       }>;
       invisibleWall: string[];
       costMetrics: string[];
     };
     // ... (full structure based on Template 3)
   }
   ```

2. **Convert Markdown Content to TypeScript**

   Reference files:
   - `/Users/byeldos/playground/ainam/docs/marketing/landing-pages/software-engineers/control.md`
   - `/Users/byeldos/playground/ainam/docs/marketing/landing-pages/software-engineers/variant-a-social-threat.md`
   - `/Users/byeldos/playground/ainam/docs/marketing/landing-pages/software-engineers/variant-b-career-acceleration.md`
   - `/Users/byeldos/playground/ainam/docs/marketing/landing-pages/software-engineers/variant-c-engineer-brain.md`

   Create content objects in `src/content/`:
   - `control.ts` - "Why Your Team Trusts You Less Than You Think"
   - `variant-a.ts` - Social threat framing
   - `variant-b.ts` - Career acceleration framing
   - `variant-c.ts` - Engineer brain optimization framing

3. **Build Landing Page Components**

   Components to create in `src/components/landing/`:

   - **Hero.tsx** - Headline, subheadline, CTA button, trust signals
   - **PainPoints.tsx** - Weekly blockers (Monday/Thursday/Friday), invisible wall, cost metrics
   - **WhyNow.tsx** - Urgency section with compound effect visualization
   - **HowItWorks.tsx** - 4-step process with optional code blocks
   - **TrustLayer.tsx** - Methodology, research frameworks, validation stats
   - **WhatYouGet.tsx** - Free tier vs. paid tier comparison
   - **ComparisonTable.tsx** - AINAM vs. MBTI/360 Reviews/Career Coaching
   - **CallToAction.tsx** - Primary CTA to assessment form
   - **DeveloperFeatures.tsx** - Collapsible section for API/export features

   Shared components in `src/components/shared/`:
   - **Button.tsx** - Shadcn button with custom variants
   - **CodeBlock.tsx** - Syntax-highlighted code display
   - **Collapsible.tsx** - Shadcn collapsible wrapper

4. **Implement A/B Testing Middleware**

   Create `middleware.ts`:
   ```typescript
   import { NextRequest, NextResponse } from 'next/server';

   const VARIANTS = ['control', 'variant-a', 'variant-b', 'variant-c'] as const;

   export function middleware(request: NextRequest) {
     let variant = request.cookies.get('ab_variant')?.value;

     if (!variant || !VARIANTS.includes(variant as any)) {
       // Equal 25% distribution
       const random = Math.random();
       variant = random < 0.25 ? 'control' :
                 random < 0.50 ? 'variant-a' :
                 random < 0.75 ? 'variant-b' : 'variant-c';
     }

     const response = NextResponse.next();
     response.cookies.set('ab_variant', variant, {
       maxAge: 60 * 60 * 24 * 30, // 30 days
       httpOnly: false,
       sameSite: 'lax',
     });

     return response;
   }

   export const config = { matcher: '/' };
   ```

5. **Build Main Landing Page**

   Create `src/app/page.tsx`:
   ```typescript
   'use client';

   import { useVariant } from '@/lib/variants';
   import { controlContent } from '@/content/control';
   import { variantAContent } from '@/content/variant-a';
   // ... imports

   const CONTENT_MAP = {
     'control': controlContent,
     'variant-a': variantAContent,
     'variant-b': variantBContent,
     'variant-c': variantCContent,
   };

   export default function LandingPage() {
     const variant = useVariant();
     const content = CONTENT_MAP[variant] || controlContent;

     return (
       <main className="min-h-screen bg-slate-900">
         <Hero variant={variant} content={content.hero} />
         <PainPoints variant={variant} content={content.painPoints} />
         <WhyNow variant={variant} content={content.whyNow} />
         <HowItWorks variant={variant} content={content.howItWorks} />
         <TrustLayer variant={variant} content={content.trustLayer} />
         <WhatYouGet variant={variant} content={content.whatYouGet} />
         <ComparisonTable variant={variant} content={content.comparison} />
         <CallToAction variant={variant} content={content.cta} />
         <DeveloperFeatures variant={variant} />
       </main>
     );
   }
   ```

6. **Responsive Design Implementation**
   - Mobile-first approach (320px - 1920px)
   - Breakpoints: sm (640px), md (768px), lg (1024px), xl (1280px)
   - Test on iOS Safari, Chrome Android
   - Ensure code blocks scroll horizontally on mobile

### Files to Create

**Content Files:**
- `landing/src/content/types.ts` - All TypeScript interfaces
- `landing/src/content/control.ts` - Control variant
- `landing/src/content/variant-a.ts` - Social threat variant
- `landing/src/content/variant-b.ts` - Career acceleration variant
- `landing/src/content/variant-c.ts` - Engineer brain variant

**Components (9 landing sections):**
- `landing/src/components/landing/Hero.tsx`
- `landing/src/components/landing/PainPoints.tsx`
- `landing/src/components/landing/WhyNow.tsx`
- `landing/src/components/landing/HowItWorks.tsx`
- `landing/src/components/landing/TrustLayer.tsx`
- `landing/src/components/landing/WhatYouGet.tsx`
- `landing/src/components/landing/ComparisonTable.tsx`
- `landing/src/components/landing/CallToAction.tsx`
- `landing/src/components/landing/DeveloperFeatures.tsx`

**Shared Components:**
- `landing/src/components/shared/Button.tsx`
- `landing/src/components/shared/CodeBlock.tsx`
- `landing/src/components/shared/Collapsible.tsx`

**Infrastructure:**
- `landing/middleware.ts` - A/B test variant assignment
- `landing/src/lib/variants.ts` - Variant utility functions
- `landing/src/app/page.tsx` - Main landing page

### Success Criteria
- [ ] All 4 variants render correctly
- [ ] A/B testing cookie persists across reloads
- [ ] Mobile responsive (test on iPhone, Android)
- [ ] Code blocks display properly with styling
- [ ] CTA buttons link to `/assessment`
- [ ] Can override variant via URL param (`?variant=control`) for testing
- [ ] Lighthouse accessibility score >90

---

