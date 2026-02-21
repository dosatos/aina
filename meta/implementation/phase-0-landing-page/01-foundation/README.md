## Phase 0.1: Foundation Setup (Days 1-2)

**Goal:** Working Next.js application with basic structure deployed to Vercel

### Tasks

1. **Initialize Next.js Project**
   ```bash
   cd /Users/byeldos/playground/ainam
   npx create-next-app@latest landing --typescript --tailwind --app --src-dir --import-alias "@/*"
   cd landing
   ```

2. **Install Core Dependencies**
   ```bash
   # UI Components
   npm install @radix-ui/react-collapsible @radix-ui/react-scroll-area
   npm install class-variance-authority clsx tailwind-merge

   # Analytics
   npm install posthog-js

   # Forms & Validation
   npm install react-hook-form zod @hookform/resolvers

   # Database
   npm install @supabase/supabase-js

   # Utilities
   npm install next-client-cookies react-intersection-observer date-fns

   # Shadcn UI
   npx shadcn-ui@latest init
   npx shadcn-ui@latest add button
   npx shadcn-ui@latest add collapsible
   npx shadcn-ui@latest add progress
   npx shadcn-ui@latest add radio-group
   ```

3. **Create Directory Structure**
   ```
   landing/
   ├── src/
   │   ├── app/
   │   │   ├── layout.tsx
   │   │   ├── page.tsx                    # Landing page
   │   │   ├── assessment/
   │   │   │   └── page.tsx                # Assessment form
   │   │   ├── results/
   │   │   │   └── [id]/page.tsx           # Results display
   │   │   └── api/
   │   │       ├── variant/route.ts        # A/B variant assignment
   │   │       ├── submit/route.ts         # Assessment submission
   │   │       └── results/[id]/route.ts   # Fetch results
   │   ├── components/
   │   │   ├── landing/                    # Landing page sections
   │   │   ├── assessment/                 # Assessment form components
   │   │   ├── results/                    # Results display components
   │   │   ├── shared/                     # Reusable components
   │   │   └── analytics/                  # Analytics wrappers
   │   ├── lib/
   │   │   ├── supabase.ts                # Supabase client
   │   │   ├── analytics.ts               # Analytics abstraction
   │   │   ├── variants.ts                # A/B testing logic
   │   │   └── utils.ts                   # Utilities
   │   ├── content/
   │   │   ├── types.ts                   # TypeScript types
   │   │   ├── control.ts                 # Control variant content
   │   │   ├── variant-a.ts               # Variant A content
   │   │   ├── variant-b.ts               # Variant B content
   │   │   └── variant-c.ts               # Variant C content
   │   └── hooks/
   │       ├── useAnalytics.ts
   │       └── useScrollTracking.ts
   ```

4. **Set Up Supabase Project**
   - Create Supabase account at https://supabase.com
   - Create new project: "ainam-phase0"
   - Copy project URL and anon key
   - Create `.env.local` file:
     ```
     NEXT_PUBLIC_SUPABASE_URL=https://xxxxx.supabase.co
     NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJxxx...
     SUPABASE_SERVICE_ROLE_KEY=eyJxxx...

     NEXT_PUBLIC_POSTHOG_KEY=phc_xxxxx
     NEXT_PUBLIC_POSTHOG_HOST=https://app.posthog.com

     OPENAI_API_KEY=sk-xxxxx
     ```

5. **Deploy Skeleton to Vercel**
   ```bash
   npm i -g vercel
   vercel login
   vercel
   # Follow prompts to create project
   ```

### Files to Create

**Critical Files:**
- `landing/src/lib/supabase.ts` - Supabase client configuration
- `landing/src/content/types.ts` - TypeScript type definitions for all content
- `landing/.env.local` - Environment variables (not committed)
- `landing/.env.example` - Environment variables template

### Success Criteria
- [ ] Next.js app runs locally (`npm run dev`)
- [ ] Tailwind CSS styling works
- [ ] TypeScript compiles without errors
- [ ] Supabase client connects successfully
- [ ] Skeleton deploys to Vercel (ainam-landing.vercel.app)

---

