## Verification

### End-to-End Testing

1. **Landing Page Flow**
   ```
   1. Visit landing page
   2. Verify correct variant assigned (check cookie)
   3. Scroll through all sections
   4. Verify scroll events tracked in PostHog
   5. Click CTA button
   6. Verify redirected to /assessment
   ```

2. **Assessment Flow**
   ```
   1. Start assessment
   2. Answer all questions (track time)
   3. Submit form
   4. Verify assessment created in Supabase
   5. Wait for profile generation (<5 seconds)
   6. Verify redirected to /results/[id]
   ```

3. **Results Flow**
   ```
   1. View results page
   2. Verify profile displays correctly
   3. Click share button
   4. Verify share URL copied/posted
   5. Open share URL in incognito
   6. Verify results accessible without auth
   ```

4. **Analytics Flow**
   ```
   1. Check PostHog dashboard
   2. Verify events appearing in real-time
   3. Filter by variant
   4. Verify funnel shows correct drop-offs
   5. Check session replay feature
   ```

### Automated Testing (Optional, if time permits)

```bash
# Unit tests
npm run test

# E2E tests with Playwright
npm run test:e2e

# Lighthouse CI
npm run lighthouse
```

---

