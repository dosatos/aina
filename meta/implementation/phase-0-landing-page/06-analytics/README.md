## Phase 0.6: Analytics Integration (Days 12-13)

**Goal:** Complete event tracking with PostHog

### Tasks

1. **Set Up PostHog Account**
   - Create account at https://posthog.com
   - Create new project: "AINAM Phase 0"
   - Copy project API key
   - Add to `.env.local`: `NEXT_PUBLIC_POSTHOG_KEY=phc_xxxxx`

2. **Implement Analytics Abstraction**

   Create `src/lib/analytics.ts`:
   ```typescript
   import posthog from 'posthog-js';

   export const ANALYTICS_EVENTS = {
     // Landing Page
     PAGE_LOADED: 'page_loaded',
     SCROLL_25: 'scroll_25',
     SCROLL_50: 'scroll_50',
     SCROLL_75: 'scroll_75',
     SCROLL_HOW_IT_WORKS: 'scroll_how_it_works',
     HERO_CTA_CLICK: 'hero_cta_click',
     PRIMARY_CTA_CLICK: 'primary_cta_click',
     TIME_ON_PAGE_2MIN: 'time_on_page_2min',

     // Assessment
     ASSESSMENT_STARTED: 'assessment_started',
     ASSESSMENT_QUESTION_ANSWERED: 'assessment_question_answered',
     ASSESSMENT_COMPLETED: 'assessment_completed',
     ASSESSMENT_ABANDONED: 'assessment_abandoned',

     // Results
     RESULTS_VIEWED: 'results_viewed',
     RESULTS_SHARED: 'results_shared',
     UPGRADE_CLICKED: 'upgrade_clicked',
   } as const;

   class Analytics {
     private initialized = false;

     init() {
       if (typeof window === 'undefined' || this.initialized) return;

       posthog.init(process.env.NEXT_PUBLIC_POSTHOG_KEY!, {
         api_host: process.env.NEXT_PUBLIC_POSTHOG_HOST || 'https://app.posthog.com',
         loaded: (posthog) => {
           if (process.env.NODE_ENV === 'development') {
             posthog.opt_out_capturing();
           }
         },
       });

       this.initialized = true;
     }

     track(event: string, properties?: Record<string, any>) {
       if (!this.initialized) this.init();

       const variant = this.getVariant();

       posthog.capture(event, {
         ...properties,
         variant,
         timestamp: new Date().toISOString(),
       });
     }

     identify(userId: string, traits?: Record<string, any>) {
       if (!this.initialized) this.init();
       posthog.identify(userId, traits);
     }

     private getVariant(): string {
       if (typeof window === 'undefined') return 'unknown';
       return document.cookie
         .split('; ')
         .find(row => row.startsWith('ab_variant='))
         ?.split('=')[1] || 'unknown';
     }
   }

   export const analytics = new Analytics();
   ```

3. **Create Analytics Provider**

   Create `src/components/analytics/AnalyticsProvider.tsx`:
   ```typescript
   'use client';

   import { useEffect } from 'react';
   import { analytics } from '@/lib/analytics';
   import { usePathname } from 'next/navigation';

   export function AnalyticsProvider({ children }: { children: React.ReactNode }) {
     const pathname = usePathname();

     useEffect(() => {
       analytics.init();
     }, []);

     useEffect(() => {
       analytics.track('page_loaded', { pathname });
     }, [pathname]);

     return <>{children}</>;
   }
   ```

4. **Implement Scroll Tracking Hook**

   Create `src/hooks/useScrollTracking.ts`:
   ```typescript
   import { useEffect, useRef } from 'react';
   import { analytics, ANALYTICS_EVENTS } from '@/lib/analytics';

   export function useScrollTracking() {
     const tracked = useRef({
       scroll25: false,
       scroll50: false,
       scroll75: false,
     });

     useEffect(() => {
       const handleScroll = () => {
         const scrollPercentage =
           (window.scrollY / (document.documentElement.scrollHeight - window.innerHeight)) * 100;

         if (scrollPercentage >= 25 && !tracked.current.scroll25) {
           analytics.track(ANALYTICS_EVENTS.SCROLL_25, { percentage: scrollPercentage });
           tracked.current.scroll25 = true;
         }
         if (scrollPercentage >= 50 && !tracked.current.scroll50) {
           analytics.track(ANALYTICS_EVENTS.SCROLL_50, { percentage: scrollPercentage });
           tracked.current.scroll50 = true;
         }
         if (scrollPercentage >= 75 && !tracked.current.scroll75) {
           analytics.track(ANALYTICS_EVENTS.SCROLL_75, { percentage: scrollPercentage });
           tracked.current.scroll75 = true;
         }
       };

       window.addEventListener('scroll', handleScroll, { passive: true });
       return () => window.removeEventListener('scroll', handleScroll);
     }, []);
   }
   ```

5. **Add Analytics to Key Components**

   Update components to track events:
   - Landing page CTA clicks
   - Assessment question answers
   - Assessment completion
   - Results sharing

6. **Create PostHog Dashboard**

   Set up key dashboards in PostHog:
   - **Funnel**: Landing page → CTA click → Assessment start → Completion → Results view
   - **Completion Rate by Variant**: Segment by `variant` property
   - **Scroll Depth**: Average scroll depth by variant
   - **Time on Page**: Histogram distribution

### Files to Create

**Analytics Infrastructure:**
- `landing/src/lib/analytics.ts` - Analytics abstraction
- `landing/src/hooks/useScrollTracking.ts` - Scroll tracking hook
- `landing/src/hooks/useAnalytics.ts` - Analytics React hook
- `landing/src/components/analytics/AnalyticsProvider.tsx` - Analytics provider

### Success Criteria
- [ ] All events appear in PostHog dashboard
- [ ] Can filter events by variant
- [ ] Funnel shows drop-off points
- [ ] Scroll tracking accurate (±5%)
- [ ] Time on page tracked
- [ ] No events in development mode

---

