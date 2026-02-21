## Phase 0.4: Assessment Form Implementation (Days 7-9)

**Goal:** Multi-step assessment form with 15-20 behavioral questions

### Tasks

1. **Design Question Structure**

   Reference existing question content from docs if available, or create based on Template 3 specifications:

   Create `src/content/questions.ts`:
   ```typescript
   export interface Question {
     id: string;
     type: 'forced-choice' | 'scenario' | 'scale';
     category: 'behavioral' | 'decision' | 'execution';
     text: string;
     options?: Array<{
       value: string;
       label: string;
       measures?: string; // What trait this measures
     }>;
     scenario?: string; // For decision scenarios
   }

   export const assessmentQuestions: Question[] = [
     // Behavioral Style (5 questions)
     {
       id: 'q1',
       type: 'forced-choice',
       category: 'behavioral',
       text: 'In team meetings, you typically:',
       options: [
         { value: 'a', label: 'Jump in quickly with ideas', measures: 'assertiveness_high' },
         { value: 'b', label: 'Listen first, contribute when you have something concrete', measures: 'assertiveness_low' },
       ],
     },
     // ... 14-19 more questions
   ];
   ```

2. **Build Form Components**

   Create components in `src/components/assessment/`:

   - **AssessmentContainer.tsx** - Main form wrapper with progress tracking
   - **QuestionCard.tsx** - Individual question display
   - **ForcedChoiceQuestion.tsx** - A/B choice questions
   - **ScenarioQuestion.tsx** - Scenario-based decision questions
   - **ProgressBar.tsx** - Visual progress indicator
   - **NavigationButtons.tsx** - Previous/Next/Submit buttons

3. **Implement Form State Management**

   Use React Hook Form with Zod validation:

   Create `src/components/assessment/AssessmentForm.tsx`:
   ```typescript
   'use client';

   import { useForm } from 'react-hook-form';
   import { zodResolver } from '@hookform/resolvers/zod';
   import { z } from 'zod';
   import { useState } from 'react';
   import { useRouter } from 'next/navigation';

   const assessmentSchema = z.object({
     responses: z.record(z.string()),
     email: z.string().email().optional(),
     job_title: z.string().optional(),
   });

   type AssessmentFormData = z.infer<typeof assessmentSchema>;

   export function AssessmentForm({ variant }: { variant: string }) {
     const [currentStep, setCurrentStep] = useState(0);
     const [startTime] = useState(Date.now());
     const router = useRouter();

     const form = useForm<AssessmentFormData>({
       resolver: zodResolver(assessmentSchema),
       defaultValues: { responses: {} },
     });

     const onSubmit = async (data: AssessmentFormData) => {
       const completionTime = Math.floor((Date.now() - startTime) / 1000);

       const response = await fetch('/api/submit', {
         method: 'POST',
         headers: { 'Content-Type': 'application/json' },
         body: JSON.stringify({
           variant,
           responses: data.responses,
           email: data.email,
           job_title: data.job_title,
           completion_time: completionTime,
         }),
       });

       const { assessment_id, result_id } = await response.json();

       // Track completion
       analytics.track('assessment_completed', {
         variant,
         completion_time: completionTime,
         assessment_id,
       });

       // Redirect to results
       router.push(`/results/${result_id}`);
     };

     return (
       <form onSubmit={form.handleSubmit(onSubmit)}>
         <ProgressBar current={currentStep} total={assessmentQuestions.length} />
         <QuestionCard question={assessmentQuestions[currentStep]} form={form} />
         <NavigationButtons
           onPrevious={() => setCurrentStep(s => Math.max(0, s - 1))}
           onNext={() => setCurrentStep(s => Math.min(assessmentQuestions.length - 1, s + 1))}
           isFirst={currentStep === 0}
           isLast={currentStep === assessmentQuestions.length - 1}
         />
       </form>
     );
   }
   ```

4. **Create Assessment Page**

   Create `src/app/assessment/page.tsx`:
   ```typescript
   'use client';

   import { useVariant } from '@/lib/variants';
   import { AssessmentForm } from '@/components/assessment/AssessmentForm';
   import { useAnalytics } from '@/hooks/useAnalytics';
   import { useEffect } from 'react';

   export default function AssessmentPage() {
     const variant = useVariant();
     const analytics = useAnalytics();

     useEffect(() => {
       analytics.track('assessment_started', { variant });
     }, [variant]);

     return (
       <main className="min-h-screen bg-slate-900 py-12">
         <div className="container mx-auto max-w-3xl">
           <h1 className="text-3xl font-bold text-white mb-8">
             Behavioral Assessment
           </h1>
           <AssessmentForm variant={variant} />
         </div>
       </main>
     );
   }
   ```

5. **Create Submission API Route**

   Create `src/app/api/submit/route.ts`:
   ```typescript
   import { NextRequest, NextResponse } from 'next/server';
   import { supabaseAdmin } from '@/lib/supabase';
   import { generateProfile } from '@/lib/profile-generator';

   export async function POST(request: NextRequest) {
     try {
       const body = await request.json();
       const { variant, responses, email, job_title, completion_time } = body;

       // Insert assessment
       const { data: assessment, error: assessmentError } = await supabaseAdmin
         .from('assessments')
         .insert({
           variant,
           responses,
           email,
           job_title,
           completion_time,
           completed: true,
         })
         .select()
         .single();

       if (assessmentError) throw assessmentError;

       // Generate profile (AI-powered)
       const profile = await generateProfile(responses);

       // Insert result
       const { data: result, error: resultError } = await supabaseAdmin
         .from('results')
         .insert({
           assessment_id: assessment.id,
           profile,
           summary: profile.summary,
           key_insights: profile.key_insights,
           share_token: generateShareToken(),
         })
         .select()
         .single();

       if (resultError) throw resultError;

       return NextResponse.json({
         assessment_id: assessment.id,
         result_id: result.id,
       });
     } catch (error) {
       console.error('Submission error:', error);
       return NextResponse.json(
         { error: 'Failed to submit assessment' },
         { status: 500 }
       );
     }
   }

   function generateShareToken(): string {
     return Math.random().toString(36).substring(2, 15) +
            Math.random().toString(36).substring(2, 15);
   }
   ```

### Files to Create

**Question Content:**
- `landing/src/content/questions.ts` - All assessment questions

**Components (6 assessment components):**
- `landing/src/components/assessment/AssessmentContainer.tsx`
- `landing/src/components/assessment/AssessmentForm.tsx`
- `landing/src/components/assessment/QuestionCard.tsx`
- `landing/src/components/assessment/ForcedChoiceQuestion.tsx`
- `landing/src/components/assessment/ProgressBar.tsx`
- `landing/src/components/assessment/NavigationButtons.tsx`

**Pages & API:**
- `landing/src/app/assessment/page.tsx` - Assessment page
- `landing/src/app/api/submit/route.ts` - Submission endpoint

### Success Criteria
- [ ] Form displays all questions in sequence
- [ ] Progress bar updates correctly
- [ ] Previous/Next navigation works
- [ ] Form validation prevents incomplete submissions
- [ ] Submission creates database records
- [ ] Completion time tracked accurately
- [ ] Mobile-friendly (easy to tap options)

---

