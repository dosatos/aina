## Phase 0.5: Results Generation & Display (Days 10-11)

**Goal:** AI-generated behavioral profile with shareable results page

### Tasks

1. **Build Profile Generation Logic**

   Create `src/lib/profile-generator.ts`:
   ```typescript
   import OpenAI from 'openai';
   import { BehavioralProfile } from './database.types';

   const openai = new OpenAI({
     apiKey: process.env.OPENAI_API_KEY,
   });

   export async function generateProfile(
     responses: Record<string, any>
   ): Promise<BehavioralProfile & { summary: string; key_insights: string[] }> {
     // Map responses to behavioral dimensions
     const scores = calculateScores(responses);

     // Generate AI-powered insights
     const completion = await openai.chat.completions.create({
       model: 'gpt-4',
       messages: [
         {
           role: 'system',
           content: `You are a behavioral analyst generating insights from assessment responses.

           Based on the scores provided, generate:
           1. A brief profile summary (2-3 sentences)
           2. 3 specific, actionable insights with concrete examples
           3. Cross-layer pattern detection (e.g., high start rate + low finish rate)

           Use the engineering-focused language from the AINAM framework:
           - Map scores to human outcomes
           - Identify blind spots
           - Provide specific behavioral patterns

           Format: JSON with { summary, key_insights[] }`,
         },
         {
           role: 'user',
           content: JSON.stringify(scores),
         },
       ],
       response_format: { type: 'json_object' },
     });

     const insights = JSON.parse(completion.choices[0].message.content!);

     return {
       behavioral_style: scores.behavioral_style,
       decision_architecture: scores.decision_architecture,
       execution_patterns: scores.execution_patterns,
       summary: insights.summary,
       key_insights: insights.key_insights,
     };
   }

   function calculateScores(responses: Record<string, any>) {
     // Scoring logic based on question mappings
     // This would be customized based on your specific questions
     return {
       behavioral_style: {
         assertiveness: 0.73,
         pace: 0.82,
         structure: 0.45,
         empathy: 0.61,
       },
       decision_architecture: {
         risk_tolerance: {
           financial: 0.35,
           career: 0.78,
           interpersonal: 0.52,
         },
         biases: {
           sunk_cost: 0.68,
           overconfidence: 0.42,
           confirmation: 0.55,
         },
       },
       execution_patterns: {
         start_rate: 0.89,
         finish_rate: 0.31,
         drop_off_point: 'week_3',
       },
     };
   }
   ```

2. **Build Results Display Components**

   Create components in `src/components/results/`:

   - **ProfileSummary.tsx** - Overview card with key stats
   - **BehavioralStyleChart.tsx** - Radar chart or bar chart visualization
   - **KeyInsights.tsx** - Top 3 insights with human outcomes
   - **DetailedBreakdown.tsx** - All dimensions with explanations
   - **ShareButtons.tsx** - Social sharing (Twitter, LinkedIn, copy link)
   - **UpgradePrompt.tsx** - CTA for $49 full profile (if free tier)

3. **Create Results Page**

   Create `src/app/results/[id]/page.tsx`:
   ```typescript
   import { supabase } from '@/lib/supabase';
   import { ProfileSummary } from '@/components/results/ProfileSummary';
   import { KeyInsights } from '@/components/results/KeyInsights';
   import { BehavioralStyleChart } from '@/components/results/BehavioralStyleChart';
   import { ShareButtons } from '@/components/results/ShareButtons';
   import { notFound } from 'next/navigation';

   export default async function ResultsPage({
     params,
   }: {
     params: { id: string };
   }) {
     // Fetch result
     const { data: result, error } = await supabase
       .from('results')
       .select('*')
       .eq('id', params.id)
       .single();

     if (error || !result) {
       notFound();
     }

     // Increment view count
     await supabase
       .from('results')
       .update({ viewed_count: result.viewed_count + 1 })
       .eq('id', params.id);

     const shareUrl = `${process.env.NEXT_PUBLIC_BASE_URL}/results/${params.id}`;

     return (
       <main className="min-h-screen bg-slate-900 py-12">
         <div className="container mx-auto max-w-4xl">
           <h1 className="text-4xl font-bold text-white mb-8">
             Your Behavioral Profile
           </h1>

           <ProfileSummary profile={result.profile} summary={result.summary} />

           <KeyInsights insights={result.key_insights} />

           <BehavioralStyleChart style={result.profile.behavioral_style} />

           <ShareButtons url={shareUrl} />

           {/* Optional: Upgrade prompt for paid features */}
           <UpgradePrompt />
         </div>
       </main>
     );
   }
   ```

4. **Add Social Sharing Metadata**

   Update results page with Open Graph tags for rich sharing:
   ```typescript
   export async function generateMetadata({ params }: { params: { id: string } }) {
     const { data: result } = await supabase
       .from('results')
       .select('*')
       .eq('id', params.id)
       .single();

     return {
       title: 'My AINAM Behavioral Profile',
       description: result?.summary || 'Discover your behavioral patterns',
       openGraph: {
         title: 'My AINAM Behavioral Profile',
         description: result?.summary,
         url: `https://ainam.co/results/${params.id}`,
         type: 'website',
       },
       twitter: {
         card: 'summary_large_image',
         title: 'My AINAM Behavioral Profile',
         description: result?.summary,
       },
     };
   }
   ```

### Files to Create

**Profile Generation:**
- `landing/src/lib/profile-generator.ts` - AI-powered profile generation
- `landing/src/lib/scoring.ts` - Response scoring logic

**Components (6 results components):**
- `landing/src/components/results/ProfileSummary.tsx`
- `landing/src/components/results/KeyInsights.tsx`
- `landing/src/components/results/BehavioralStyleChart.tsx`
- `landing/src/components/results/DetailedBreakdown.tsx`
- `landing/src/components/results/ShareButtons.tsx`
- `landing/src/components/results/UpgradePrompt.tsx`

**Pages:**
- `landing/src/app/results/[id]/page.tsx` - Results display page

### Success Criteria
- [ ] Results generate within 5 seconds of submission
- [ ] Profile displays correctly with all dimensions
- [ ] Charts/visualizations render properly
- [ ] Share buttons work (Twitter, LinkedIn, copy link)
- [ ] Open Graph preview works when sharing URL
- [ ] Mobile-responsive results display
- [ ] Results are accessible via unique URL

---

