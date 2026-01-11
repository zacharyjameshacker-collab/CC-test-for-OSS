# Grant Writing Unicorn Custom Commands

## Grant Research & Strategy Commands

### research-grants
**Purpose:** Execute Stage 1 of the Grant Research Funnel  
**Usage:** `claude code research-grants --keywords="youth development" --org-type="nonprofit" --location="Alaska"`

**Process:**
1. Search grant databases using provided criteria
2. Generate list of 100+ potential opportunities
3. Export to funding matrix template
4. Provide summary statistics
5. Flag immediate opportunities

**Output:** `funding_matrix_[date].xlsx` with all prospects

---

### evaluate-grants
**Purpose:** Filter grants through Stages 2 and 3 of Grant Research Funnel  
**Usage:** `claude code evaluate-grants --stage=2 --matrix="funding_matrix.xlsx"`

**Stage 2 Process (100+ to ~20):**
1. Check funder's giving priorities for alignment
2. Verify eligible use of funds
3. Review funding history (990s or past awards)
4. Quick keep/cut decisions
5. Flag for Stage 3 evaluation

**Stage 3 Process (~20 to Top 3-5):**
1. Calculate competitiveness (target 20%+)
2. Deep organizational alignment check
3. Assess project readiness
4. Evaluate match requirements
5. Review all restrictions
6. Analyze award size vs. effort
7. Confirm timeline feasibility
8. Generate funder outreach questions

**Output:** Ranked list with recommendations and justifications

---

### create-funding-strategy
**Purpose:** Develop comprehensive 2-3 page funding strategy memorandum  
**Usage:** `claude code create-funding-strategy --project="Community Center" --total="2500000"`

**Process:**
1. Analyze project scope and budget
2. Identify funding needs by phase
3. Research and recommend grant prospects
4. Sequence applications strategically
5. Identify match/leverage opportunities
6. Create timeline with deadlines
7. Flag planning requirements
8. Calculate success probability

**Output:** Professional funding strategy document with:
- Executive summary
- Project overview
- Funding needs breakdown
- Grant prospect analysis (top 5-7)
- Application sequence and timeline
- Match strategy
- Risk mitigation
- Next steps

---

### analyze-990
**Purpose:** Extract and analyze foundation giving patterns from 990 forms  
**Usage:** `claude code analyze-990 --foundation="Smith Foundation" --file="990.pdf"`

**Analysis:**
1. Total annual giving amount
2. Average grant size
3. Geographic distribution
4. Issue area breakdown
5. Organization type preferences
6. Multi-year giving patterns
7. Matching previous recipients to your profile
8. Likelihood assessment

**Output:** Foundation profile report with fit recommendation

---

## Application Development Commands

### analyze-guidelines
**Purpose:** Deep analysis of grant guidelines/RFP (Step 1)  
**Usage:** `claude code analyze-guidelines --file="RFP.pdf" --grant="EPA Brownfields"`

**Analysis Includes:**
1. All narrative questions/prompts
2. Scoring criteria and point values
3. Required attachments with formats
4. Eligibility requirements
5. Key dates and deadlines
6. Match requirements
7. Restrictions and limitations
8. Evaluation process
9. Keyword frequency analysis
10. Special instructions flagged

**Output:** 
- Comprehensive guidelines summary
- Requirements checklist
- Red flags and concerns
- Strategic recommendations

---

### create-skeleton
**Purpose:** Create grant narrative skeleton (Step 2)  
**Usage:** `claude code create-skeleton --grant="EPA Brownfields" --guidelines="analysis.json"`

**Process:**
1. Extract all narrative prompts from guidelines
2. Format with proper headers/subheaders
3. Add scoring criteria under each section
4. Insert brainstorming bullet point placeholders
5. Identify information gaps
6. Flag questions for kick-off meeting
7. Estimate word counts per section

**Output:** 
- `narrative_skeleton.docx` with all sections
- `information_gaps.md` with needed data
- `kickoff_questions.md` for meeting prep

---

### plan-kickoff
**Purpose:** Generate complete kick-off meeting package (Step 3)  
**Usage:** `claude code plan-kickoff --grant="EPA Brownfields" --date="2024-01-15" --team="team.json"`

**Package Includes:**
1. Meeting agenda with timing
2. Narrative skeleton for review
3. Team member assignments
4. Schedule with deadlines
5. Information request list
6. Appreciation ideas (food options)
7. Progress meeting schedule
8. Follow-up email template

**Output:** Complete meeting package ready to send

---

### develop-budget
**Purpose:** Create comprehensive grant budget (Step 4)  
**Usage:** `claude code develop-budget --grant="EPA Brownfields" --total="500000" --match="25%"`

**Process:**
1. Load base camp budget template
2. Input project costs by category
3. Calculate match requirements
4. Format per funder requirements
5. Validate calculations
6. Generate budget narrative draft
7. Create assumptions documentation
8. Identify cost share sources

**Output:**
- `grant_budget.xlsx` with all calculations
- `budget_narrative.docx` with justifications
- `match_strategy.md` with sources
- `assumptions.md` documentation

---

### write-narrative
**Purpose:** Draft grant narrative sections (Step 5)  
**Usage:** `claude code write-narrative --section="need" --grant="EPA Brownfields" --skeleton="skeleton.docx"`

**Writing Process:**
1. Load narrative skeleton for section
2. Review scoring criteria
3. Apply persuasive writing techniques
4. Use strengths-based approach (80/20 rule)
5. Insert XX% placeholders for missing data
6. Establish urgency appropriately
7. Answer every question explicitly
8. Format with clear headers

**Writing Principles Applied:**
- Show don't tell
- Data-driven claims
- Sensory details and stories
- Excessively clear responses
- No context switching (placeholders)
- 20% deficit, 80% strengths

**Output:** Draft section with:
- Tracked changes enabled
- XX% data needs flagged
- Word count for target
- Suggested improvements

---

### enhance-narrative
**Purpose:** Strengthen existing narrative draft  
**Usage:** `claude code enhance-narrative --section="need" --draft="need_v1.docx"`

**Enhancement Areas:**
1. Strengthen urgency/catastrophic elements
2. Add sensory details and stories
3. Balance deficit/strengths language
4. Verify all questions answered
5. Improve data integration
6. Clarify vague statements
7. Tighten word count
8. Enhance transitions

**Output:** Enhanced draft with suggestions tracked

---

### check-completeness
**Purpose:** Verify narrative answers all requirements  
**Usage:** `claude code check-completeness --narrative="draft_v3.docx" --skeleton="skeleton.docx"`

**Verification:**
1. Cross-reference all prompts
2. Confirm scoring criteria addressed
3. Check word count compliance
4. Verify data completeness (no XX%)
5. Ensure header structure matches
6. Validate formatting requirements
7. Flag missing elements

**Output:** Completeness report with gaps identified

---

## Attachment Commands

### prepare-attachments
**Purpose:** Coordinate all attachment preparation (Step 6)  
**Usage:** `claude code prepare-attachments --grant="EPA Brownfields" --guidelines="analysis.json"`

**Coordinates:**
1. Budget narrative
2. Resolution preparation
3. Letters of support
4. Required forms
5. Organizational documents
6. Supplementary materials
7. Timeline for approvals

**Output:** Attachment tracker with assignments and deadlines

---

### draft-los
**Purpose:** Generate letter of support draft  
**Usage:** `claude code draft-los --partner="Tribal Council" --project="project_overview.pdf" --focus="community-support"`

**Letter Elements:**
1. Relationship to project
2. Community impact emphasis
3. Specific support offered
4. Alignment with partner mission
5. Urgency and importance
6. Commitment language
7. Contact information

**Output:** Professional letter draft on letterhead template

---

### prepare-resolution
**Purpose:** Draft board/council resolution  
**Usage:** `claude code prepare-resolution --grant="EPA Brownfields" --amount="500000" --match="125000"`

**Resolution Includes:**
1. Whereas clauses (background)
2. Project description
3. Funding amount and match
4. Authority to apply
5. Authority to accept
6. Compliance commitments
7. Authorized signatories
8. Effective date

**Output:** Resolution draft matching funder requirements

---

### generate-budget-narrative
**Purpose:** Write detailed budget justification  
**Usage:** `claude code generate-budget-narrative --budget="budget.xlsx" --categories="all"`

**Narrative Sections (by category):**
1. Personnel - roles, rates, time commitment
2. Fringe Benefits - calculation methodology
3. Travel - purpose, destinations, costs
4. Equipment - necessity, quotes, useful life
5. Supplies - itemized list, justification
6. Contractual - scope, procurement process
7. Construction - scope, quotes, timeline
8. Other - any additional categories

**Output:** Exhaustively detailed budget narrative

---

## Quality Assurance Commands

### qa-check
**Purpose:** Comprehensive quality assurance before submission  
**Usage:** `claude code qa-check --grant="EPA Brownfields" --package="./final/"`

**Checks:**
1. ✅ All narrative sections complete
2. ✅ Scoring criteria addressed
3. ✅ Word counts within limits
4. ✅ All attachments included
5. ✅ Formatting requirements met
6. ✅ Required signatures obtained
7. ✅ Budget calculations accurate
8. ✅ No XX% placeholders remain
9. ✅ Consistent naming/terminology
10. ✅ All forms completed correctly
11. ✅ Page limits observed
12. ✅ File formats correct

**Output:** QA report with pass/fail for each item

---

### compliance-check
**Purpose:** Verify eligibility and compliance  
**Usage:** `claude code compliance-check --grant="EPA Brownfields" --org="org_profile.json"`

**Verification:**
1. Organization eligibility
2. Geographic eligibility
3. Project eligibility
4. Match requirements met
5. No conflicts of interest
6. Certification requirements
7. Registration requirements (SAM, grants.gov)
8. Debarment status
9. Federal debt status
10. Required policies in place

**Output:** Compliance checklist with evidence

---

### calculate-competitiveness
**Purpose:** Determine likelihood of success  
**Usage:** `claude code calculate-competitiveness --grant="EPA Brownfields" --historical="stats.json"`

**Calculation:**
1. Number of applicants (previous year)
2. Number of awards made
3. Success rate percentage
4. Your organizational profile match
5. Project alignment score
6. Geographic advantage
7. Past relationship with funder
8. Overall likelihood rating

**Output:** Competitiveness score with justification

---

## Project Management Commands

### create-timeline
**Purpose:** Generate detailed grant preparation timeline  
**Usage:** `claude code create-timeline --grant="EPA Brownfields" --deadline="2024-03-15" --start="2024-01-15"`

**Timeline Includes:**
1. Kick-off meeting
2. Budget completion
3. Narrative drafts (v1-v4+)
4. Attachment deadlines
5. Resolution approval
6. Letters of support
7. Internal reviews
8. Final assembly
9. Submission buffer
10. Progress meetings

**Output:** 
- Gantt chart
- Task list with assignments
- Calendar file (.ics)
- Email reminders

---

### track-progress
**Purpose:** Monitor completion against timeline  
**Usage:** `claude code track-progress --grant="EPA Brownfields" --timeline="timeline.json"`

**Tracking:**
1. Tasks completed vs. scheduled
2. Percentage complete by section
3. Red flags and delays
4. Critical path items
5. Upcoming deadlines (7-day lookout)
6. Team member workload

**Output:** Progress dashboard and alert emails

---

### generate-meeting-agenda
**Purpose:** Create progress meeting agenda  
**Usage:** `claude code generate-meeting-agenda --grant="EPA Brownfields" --week="2"`

**Agenda Items:**
1. Progress since last meeting
2. Completed sections review
3. Challenges and blockers
4. Information gaps remaining
5. Upcoming deadlines
6. Action items assignment
7. Next meeting date/time

**Output:** Meeting agenda ready to send

---

## Analysis & Reporting Commands

### analyze-successful-application
**Purpose:** Learn from funded applications  
**Usage:** `claude code analyze-successful-application --file="funded_app.pdf" --program="EPA Brownfields"`

**Analysis:**
1. Narrative structure and approach
2. Persuasive techniques used
3. Data integration methods
4. Strengths-based language ratio
5. Budget presentation
6. Letters of support quality
7. Key success factors
8. Lessons for future applications

**Output:** Strategic insights report

---

### compare-drafts
**Purpose:** Track improvements across versions  
**Usage:** `claude code compare-drafts --v1="draft_v1.docx" --v2="draft_v2.docx"`

**Comparison:**
1. Word count changes
2. Content additions/deletions
3. Strengthened arguments
4. Data improvements
5. Clarity enhancements
6. Scoring criteria coverage
7. Remaining gaps

**Output:** Side-by-side comparison with highlights

---

### export-for-review
**Purpose:** Package application for internal review  
**Usage:** `claude code export-for-review --grant="EPA Brownfields" --version="v3"`

**Package Contents:**
1. Current narrative draft
2. Budget and budget narrative
3. Draft attachments
4. Completeness checklist
5. Specific review questions
6. Deadline reminder
7. Change tracking enabled

**Output:** Review package with instructions

---

## Utility Commands

### create-project-overview
**Purpose:** Generate one-page project prospectus  
**Usage:** `claude code create-project-overview --project="Community Center" --length="1-page"`

**Overview Sections:**
1. Organization background
2. Project description
3. Community need
4. Project impact
5. Total budget
6. Funding request
7. Timeline
8. Contact information

**Output:** Professional one-pager (PDF)

---

### prepare-funder-outreach
**Purpose:** Draft email to funding representative  
**Usage:** `claude code prepare-funder-outreach --funder="EPA" --purpose="eligibility" --grant="Brownfields"`

**Email Elements:**
1. Professional introduction
2. Brief project description
3. Specific questions
4. Project overview attached
5. Meeting request (if appropriate)
6. Professional close
7. Follow-up plan

**Output:** Email draft ready to send

---

### calculate-roi
**Purpose:** Determine if grant worth pursuing  
**Usage:** `claude code calculate-roi --grant="EPA Brownfields" --hours="60" --award="500000"`

**ROI Analysis:**
1. Estimated preparation hours
2. Cost of staff time
3. Award amount
4. Match requirements
5. Likelihood of success
6. Expected value calculation
7. Go/no-go recommendation

**Output:** ROI analysis with recommendation

---

### organize-files
**Purpose:** Set up proper file structure  
**Usage:** `claude code organize-files --grant="EPA Brownfields" --base-path="."`

**Creates Structure:**
```
EPA_Brownfields/
├── 00_research/
├── 01_strategy/
├── 02_application/
│   ├── drafts/
│   └── final/
├── 03_attachments/
└── 04_submission/
```

**Output:** Organized directory structure with README in each folder

---

## Meta Commands

### help
**Purpose:** Display all available commands  
**Usage:** `claude code help [command]`

**Shows:**
- Command list with descriptions
- Usage examples
- Required vs. optional parameters
- Output file descriptions

---

### status
**Purpose:** Show current grant project status  
**Usage:** `claude code status`

**Reports:**
- Active grants
- Upcoming deadlines
- Completion percentages
- Blocker flags
- Team assignments

---

### template-list
**Purpose:** Show available templates  
**Usage:** `claude code template-list [category]`

**Categories:**
- Narratives
- Budgets
- Letters
- Resolutions
- Strategies
- Forms

---

## Command Chaining Examples

### Complete Application Workflow
```bash
# Full workflow from start to submission
claude code analyze-guidelines --file="RFP.pdf" | \
claude code create-skeleton | \
claude code plan-kickoff --date="2024-01-15" | \
claude code develop-budget --total="500000" | \
claude code write-narrative --all-sections | \
claude code prepare-attachments | \
claude code qa-check | \
claude code export-for-review
```

### Research to Strategy Workflow
```bash
# From research to funding strategy
claude code research-grants --keywords="education" | \
claude code evaluate-grants --stage=2 | \
claude code evaluate-grants --stage=3 | \
claude code create-funding-strategy
```

### Quick Application Assessment
```bash
# Determine if grant worth pursuing
claude code analyze-guidelines --file="RFP.pdf" | \
claude code calculate-competitiveness | \
claude code calculate-roi | \
claude code recommend-decision
```

---

## Configuration

### Setting Default Values
Create `.grantrc` file in project root:

```json
{
  "organization": "Your Nonprofit Name",
  "default_location": "Alaska",
  "default_org_type": "nonprofit",
  "target_success_rate": 20,
  "default_reviewer": "jane@org.org",
  "database": "instrumentl",
  "templates_path": "./templates/custom/"
}
```

### Custom Templates
Place custom templates in specified path. Commands will automatically detect and offer them as options.

---

**Pro Tip:** Chain commands together for efficient workflows, or use interactive mode for step-by-step guidance.

All commands follow the Grant Writing Unicorn Method™ and incorporate Meredith Noble's best practices. 🦄
