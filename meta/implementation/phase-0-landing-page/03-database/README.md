## Phase 0.3: Database Schema & Setup (Day 6)

**Goal:** Supabase database ready to store assessment responses and results

### Tasks

1. **Design Database Schema**

   Create the following tables via Supabase SQL Editor:

   ```sql
   -- Assessments table (stores raw responses)
   CREATE TABLE assessments (
     id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
     created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
     variant TEXT NOT NULL,
     email TEXT,
     job_title TEXT,
     responses JSONB NOT NULL,
     completed BOOLEAN DEFAULT FALSE,
     completion_time INTEGER, -- seconds taken
     utm_source TEXT,
     utm_medium TEXT,
     utm_campaign TEXT
   );

   -- Results table (stores generated profiles)
   CREATE TABLE results (
     id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
     assessment_id UUID REFERENCES assessments(id),
     created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
     profile JSONB NOT NULL, -- Full profile data
     summary TEXT, -- Short summary
     key_insights TEXT[], -- Array of top insights
     share_token TEXT UNIQUE, -- For shareable links
     viewed_count INTEGER DEFAULT 0
   );

   -- Analytics events table (backup for PostHog)
   CREATE TABLE analytics_events (
     id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
     created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
     event_name TEXT NOT NULL,
     variant TEXT,
     properties JSONB,
     session_id TEXT
   );

   -- Indexes for performance
   CREATE INDEX idx_assessments_variant ON assessments(variant);
   CREATE INDEX idx_assessments_created_at ON assessments(created_at);
   CREATE INDEX idx_results_share_token ON results(share_token);
   CREATE INDEX idx_analytics_events_name ON analytics_events(event_name);
   ```

2. **Set Up Row Level Security (RLS)**

   ```sql
   -- Enable RLS
   ALTER TABLE assessments ENABLE ROW LEVEL SECURITY;
   ALTER TABLE results ENABLE ROW LEVEL SECURITY;
   ALTER TABLE analytics_events ENABLE ROW LEVEL SECURITY;

   -- Public can insert assessments
   CREATE POLICY "Allow public insert" ON assessments
     FOR INSERT WITH CHECK (true);

   -- Anyone with share_token can view results
   CREATE POLICY "Allow public read with token" ON results
     FOR SELECT USING (true);

   -- Public can insert analytics events
   CREATE POLICY "Allow public analytics" ON analytics_events
     FOR INSERT WITH CHECK (true);
   ```

3. **Create Supabase Client Utility**

   Create `src/lib/supabase.ts`:
   ```typescript
   import { createClient } from '@supabase/supabase-js';

   const supabaseUrl = process.env.NEXT_PUBLIC_SUPABASE_URL!;
   const supabaseAnonKey = process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY!;

   export const supabase = createClient(supabaseUrl, supabaseAnonKey);

   // Server-side client with service role (for API routes)
   export const supabaseAdmin = createClient(
     supabaseUrl,
     process.env.SUPABASE_SERVICE_ROLE_KEY!,
     { auth: { persistSession: false } }
   );
   ```

4. **Create Database Types**

   Create `src/lib/database.types.ts`:
   ```typescript
   export interface Assessment {
     id: string;
     created_at: string;
     variant: string;
     email?: string;
     job_title?: string;
     responses: Record<string, any>;
     completed: boolean;
     completion_time?: number;
     utm_source?: string;
     utm_medium?: string;
     utm_campaign?: string;
   }

   export interface Result {
     id: string;
     assessment_id: string;
     created_at: string;
     profile: BehavioralProfile;
     summary: string;
     key_insights: string[];
     share_token: string;
     viewed_count: number;
   }

   export interface BehavioralProfile {
     behavioral_style: {
       assertiveness: number;
       pace: number;
       structure: number;
       empathy: number;
     };
     decision_architecture: {
       risk_tolerance: {
         financial: number;
         career: number;
         interpersonal: number;
       };
       biases: {
         sunk_cost: number;
         overconfidence: number;
         confirmation: number;
       };
     };
     execution_patterns: {
       start_rate: number;
       finish_rate: number;
       drop_off_point: string;
     };
   }
   ```

### Files to Create
- `landing/src/lib/supabase.ts` - Supabase client
- `landing/src/lib/database.types.ts` - Database TypeScript types

### Success Criteria
- [ ] Tables created in Supabase dashboard
- [ ] RLS policies active and tested
- [ ] Can insert test assessment via SQL
- [ ] Can query results via Supabase client
- [ ] TypeScript types match database schema

---

