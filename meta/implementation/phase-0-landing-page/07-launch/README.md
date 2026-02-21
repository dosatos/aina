## Phase 0.7: Polish, QA & Launch (Day 14)

**Goal:** Production-ready site launched with LinkedIn ads

### Tasks

1. **Performance Optimization**
   - Optimize images (convert to WebP, use Next.js Image component)
   - Enable Vercel Analytics for Core Web Vitals
   - Minimize bundle size (check with `npm run build`)
   - Implement code splitting for results page
   - Add loading skeletons for async content

2. **SEO Optimization**

   Update `src/app/layout.tsx`:
   ```typescript
   export const metadata = {
     title: 'AINAM - Behavioral Assessment for Engineers',
     description: 'You debug systems. Debug yourself. 15-minute behavioral assessment built for engineers.',
     keywords: ['behavioral assessment', 'engineers', 'career development', 'self-awareness'],
     openGraph: {
       title: 'AINAM - Behavioral Assessment for Engineers',
       description: 'You debug systems. Debug yourself.',
       url: 'https://ainam.co',
       type: 'website',
       images: ['/og-image.png'],
     },
     twitter: {
       card: 'summary_large_image',
       site: '@ainam',
       title: 'AINAM - Behavioral Assessment for Engineers',
       description: 'You debug systems. Debug yourself.',
       images: ['/og-image.png'],
     },
   };
   ```

   Create `public/robots.txt`:
   ```
   User-agent: *
   Allow: /

   Sitemap: https://ainam.co/sitemap.xml
   ```

   Create `src/app/sitemap.ts`:
   ```typescript
   import { MetadataRoute } from 'next';

   export default function sitemap(): MetadataRoute.Sitemap {
     return [
       {
         url: 'https://ainam.co',
         lastModified: new Date(),
         changeFrequency: 'weekly',
         priority: 1,
       },
       {
         url: 'https://ainam.co/assessment',
         lastModified: new Date(),
         changeFrequency: 'weekly',
         priority: 0.8,
       },
     ];
   }
   ```

3. **Cross-Browser Testing**
   - Test on Chrome, Safari, Firefox, Edge
   - Test on iOS Safari, Chrome Android
   - Fix any browser-specific issues
   - Ensure code blocks render properly on all browsers

4. **Accessibility Audit**
   - Run WAVE browser extension
   - Run Lighthouse accessibility audit (target >90)
   - Ensure keyboard navigation works
   - Add ARIA labels where needed
   - Test with screen reader (VoiceOver on Mac)

5. **Load Testing**
   - Use Vercel's built-in performance monitoring
   - Test with 100+ concurrent users (use k6 or Artillery if needed)
   - Ensure database can handle load
   - Set up Supabase connection pooling

6. **Error Monitoring Setup**
   - Enable Vercel error tracking
   - Add error boundaries to key components
   - Test error states (network failure, API errors)
   - Create 404 and 500 error pages

7. **Create Launch Checklist**

   Create `meta/implementation/phase-0-landing-page/06-deployment/launch-checklist.md`:
   ```markdown
   # Launch Checklist

   ## Pre-Launch (T-1 day)
   - [ ] All 4 variants render correctly
   - [ ] Assessment form works end-to-end
   - [ ] Results generate successfully
   - [ ] Analytics events tracking in PostHog
   - [ ] Mobile responsive (test on real devices)
   - [ ] Lighthouse score >90 (all metrics)
   - [ ] Custom domain configured
   - [ ] SSL certificate active
   - [ ] Environment variables set in Vercel
   - [ ] Error monitoring enabled
   - [ ] 5 people test full flow (feedback collected)

   ## LinkedIn Ads Setup
   - [ ] LinkedIn Campaign Manager account created
   - [ ] 4 ad sets created (one per variant)
   - [ ] Budget: $125 per ad set ($500 total)
   - [ ] Target: Software Engineers, Data Scientists, 25-40, US
   - [ ] Ad creative ready (image + copy)
   - [ ] UTM parameters configured

   ## Launch Day (T+0)
   - [ ] Deploy to production (morning PST)
   - [ ] Verify all pages load correctly
   - [ ] Test analytics (send test events)
   - [ ] Launch LinkedIn ads
   - [ ] Monitor for first 2 hours
   - [ ] Check PostHog dashboard (events flowing?)
   - [ ] Test on mobile devices
   - [ ] Share with 3 engineers for real-time feedback

   ## Monitoring (T+1 to T+7)
   - [ ] Check analytics daily
   - [ ] Review session replays (5 per day)
   - [ ] Monitor variant performance
   - [ ] Track completion rates
   - [ ] Collect qualitative feedback
   - [ ] Daily update to stakeholders

   ## Week 1 Analysis (T+7)
   - [ ] Export PostHog data
   - [ ] Calculate completion rate by variant
   - [ ] Identify winning variant
   - [ ] Review session replays for insights
   - [ ] Qualitative synthesis
   - [ ] Go/no-go decision for Phase 1
   ```

8. **Production Deployment**
   ```bash
   # Ensure all environment variables set in Vercel dashboard
   vercel --prod

   # Set up custom domain in Vercel dashboard
   # Add DNS records as instructed
   ```

9. **Launch LinkedIn Ad Campaign**
   - Create 4 ad sets (one per variant)
   - Use UTM parameters to track variant performance
   - Budget: $125 per variant, $500 total
   - Target: Software Engineers, Data Scientists, Engineering Managers
   - Age: 25-40
   - Location: US tech hubs (SF, Seattle, NYC, Austin, etc.)

### Files to Create

**SEO & Metadata:**
- `landing/public/robots.txt`
- `landing/src/app/sitemap.ts`
- `landing/public/og-image.png` (Open Graph image)

**Documentation:**
- `meta/implementation/phase-0-landing-page/06-deployment/launch-checklist.md`

### Success Criteria (Phase 0 Validation)
- [ ] 50%+ completion rate on any variant
- [ ] 2+ min average time on page
- [ ] 60%+ scroll to "How It Works"
- [ ] 500+ total visitors across variants
- [ ] No critical errors in first 24 hours
- [ ] Lighthouse score >90 (all metrics)

---

