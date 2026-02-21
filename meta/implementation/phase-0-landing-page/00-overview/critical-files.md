## Critical Files Reference

### Highest Priority (Build First)

1. **`landing/src/content/types.ts`**
   - Defines all TypeScript interfaces
   - Contract between content and components
   - Prevents type errors throughout

2. **`landing/src/lib/supabase.ts`**
   - Database connection
   - Required for all data operations

3. **`landing/src/lib/analytics.ts`**
   - Analytics abstraction
   - Critical for Phase 0 validation metrics

4. **`landing/middleware.ts`**
   - A/B test variant assignment
   - Must work for meaningful experiment

5. **`landing/src/content/control.ts`**
   - First complete content object
   - Pattern for other variants

### Key Integration Points

- **Landing → Assessment**: CTA buttons link to `/assessment` with variant preserved
- **Assessment → Results**: Submission API creates result and redirects to `/results/[id]`
- **Results → Sharing**: Share buttons generate URLs with Open Graph metadata
- **All Pages → Analytics**: Every interaction tracked via analytics abstraction

---

