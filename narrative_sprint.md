# NARRATIVE SPRINT - Fast & Furious Grant Writing Command

## USAGE
```bash
claude narrative_sprint --section "[section_name]" --wordcount "[target]" --time "[minutes]"
```

## PURPOSE
Implements the Fast and Furious writing method: 25-minute focused sprints to draft grant narratives quickly, overcoming perfectionism and writer's block.

---

## CORE PRINCIPLES

### "Write Terribly on Purpose"
- **First draft = verbal diarrhea** (Meredith Noble's words!)
- Speed creates momentum
- Editing comes LATER (separate session)
- Minimum word counts, not perfection
- Sequential sections (don't jump around)

### Why This Works:
1. **Eliminates perfectionism** - Can't edit while sprinting
2. **Builds confidence** - Progress is visible
3. **Captures ideas** - Before they disappear
4. **Creates momentum** - Success breeds success
5. **Reduces anxiety** - Just focus on THIS sprint

---

## SPRINT SETUP

**AUTOMATED PREPARATION:**

```bash
# System prompts you for:
Grant section to write: _________________
Word count target: _____ words
Sprint duration: _____ minutes (default: 25)
Number of sprints: _____ (default: 1)
```

**CREATES WRITING ENVIRONMENT:**
- Blank document with header
- Timer display (countdown)
- Word count tracker (live)
- Distraction blocker prompts
- Progress bar visualization

---

## SECTION-SPECIFIC TEMPLATES

### 1. STATEMENT OF NEED/PROBLEM

**SPRINT PROMPTS:**
```
What problem are you solving? (100 words min)
________________________________

Who is affected by this problem? (75 words min)
________________________________

What data proves this problem exists? (100 words min)
________________________________

What happens if this problem isn't solved? (75 words min)
________________________________
```

**WRITING TRIGGERS:**
- "Currently, [data point showing need]..."
- "This problem affects [number] individuals by..."
- "Without intervention, [consequence]..."
- "Research shows that [evidence]..."

**MINIMUM TARGET:** 350 words in 25 minutes (14 wpm)

---

### 2. PROJECT DESCRIPTION/METHODOLOGY

**SPRINT PROMPTS:**
```
What will you DO to solve the problem? (150 words min)
________________________________

Who will implement each activity? (100 words min)
________________________________

What is the timeline for activities? (75 words min)
________________________________

Why is this approach effective? (75 words min)
________________________________
```

**WRITING TRIGGERS:**
- "This project will implement..."
- "Phase 1 will focus on..."
- "Participants will receive..."
- "Our approach is based on..."

**MINIMUM TARGET:** 400 words in 25 minutes (16 wpm)

---

### 3. ORGANIZATIONAL CAPACITY

**SPRINT PROMPTS:**
```
What experience does your org have? (100 words min)
________________________________

Who are the key staff and their qualifications? (100 words min)
________________________________

What systems are in place for success? (75 words min)
________________________________

What is your track record? (75 words min)
________________________________
```

**WRITING TRIGGERS:**
- "Since [year], our organization has..."
- "[Name], [Title], brings [years] years of..."
- "We have successfully completed..."
- "Our systems include..."

**MINIMUM TARGET:** 350 words in 25 minutes

---

### 4. GOALS & OBJECTIVES

**SPRINT PROMPTS:**
```
What is your overall goal? (50 words min)
________________________________

What are 3-5 SMART objectives? (150 words min)
- Objective 1:
- Objective 2:
- Objective 3:
________________________________

How will you measure success for each? (100 words min)
________________________________
```

**SMART OBJECTIVE TEMPLATE:**
```
By [date], [target population] will [measurable change] as measured by [indicator], representing a [percentage/number] improvement from baseline of [current stat].
```

**MINIMUM TARGET:** 300 words in 20 minutes

---

### 5. EVALUATION PLAN

**SPRINT PROMPTS:**
```
What data will you collect? (100 words min)
________________________________

How will you collect it? (100 words min)
________________________________

How often will you assess progress? (50 words min)
________________________________

Who will conduct evaluation? (50 words min)
________________________________

How will you use evaluation findings? (75 words min)
________________________________
```

**MINIMUM TARGET:** 375 words in 25 minutes

---

### 6. SUSTAINABILITY/FUTURE FUNDING

**SPRINT PROMPTS:**
```
How will project continue after grant ends? (100 words min)
________________________________

What other funding sources exist? (75 words min)
________________________________

How will impact be maintained? (75 words min)
________________________________
```

**MINIMUM TARGET:** 250 words in 20 minutes

---

### 7. BUDGET NARRATIVE

**SPRINT PROMPTS:**
```
For each major budget category, explain WHY needed:

Personnel justification (per position): (50 words each)
________________________________

Equipment/supplies justification (per item): (25 words each)
________________________________

Travel justification (per trip): (40 words each)
________________________________
```

**MINIMUM TARGET:** Varies by budget complexity

---

## SPRINT EXECUTION PROTOCOL

### BEFORE SPRINT:
```
PREPARATION CHECKLIST:
[ ] Funding guidelines open and reviewed
[ ] Project notes/data accessible
[ ] Timer set (25 minutes default)
[ ] Distractions eliminated
    - Phone on silent
    - Email closed
    - Slack notifications off
    - Door closed
[ ] Water/coffee ready
[ ] Section outline clear
[ ] Word count target set
```

---

### DURING SPRINT:

**AUTOMATED TIMER DISPLAYS:**
```
┌─────────────────────────────────┐
│  SPRINT TIMER: 25:00            │
│  Section: Statement of Need     │
│  Target: 350 words              │
│  Current: 187 words (53%)       │
│  ████████░░░░░░░░ 53%           │
└─────────────────────────────────┘
```

**SPRINT RULES:**
1. ✅ **DO:** Write continuously
2. ✅ **DO:** Write in full sentences
3. ✅ **DO:** Use brackets [FIND STAT] for gaps
4. ✅ **DO:** Keep typing even if you're writing nonsense
5. ✅ **DO:** Focus on quantity over quality

6. ❌ **DON'T:** Edit anything
7. ❌ **DON'T:** Delete anything
8. ❌ **DON'T:** Stop to research
9. ❌ **DON'T:** Reread what you've written
10. ❌ **DON'T:** Check word count (system shows it)

**POMODORO INTEGRATION:**
- 25 minutes writing
- 5 minutes break
- Repeat 3-4 times
- 15-30 minute longer break

**MOTIVATIONAL PROMPTS:**
```
[At 5 minutes] "Great start! Keep the momentum!"
[At 12 minutes] "Halfway there! You're doing great!"
[At 18 minutes] "Final push! Almost done!"
[At 25 minutes] "SPRINT COMPLETE! Excellent work!"
```

---

### AFTER SPRINT:

**AUTOMATED SUMMARY:**
```
SPRINT COMPLETE! 🎉

Duration: 25 minutes
Words written: 427
Target: 350 words
Achievement: 122% ✅

Speed: 17.08 words/minute
Quality: Editing needed (expected!)

Next step: Take 5-minute break
Then: Sprint #2 or Edit session
```

**SAVE OPTIONS:**
```bash
# Auto-save with timestamp
[section]_sprint_[timestamp].docx

# Example:
statement_of_need_sprint_2026-01-11_14-30.docx
```

---

## MULTI-SPRINT WORKFLOW

### FULL NARRATIVE COMPOSITION:

**AUTOMATED SESSION PLANNER:**
```
NARRATIVE WRITING SESSION
Project: [Name]
Total sections: 6
Estimated time: 3 hours (with breaks)

SPRINT SCHEDULE:
┌────────────────────────────────────────┐
│ Sprint 1: Statement of Need (25 min)   │
│ Break (5 min)                          │
│ Sprint 2: Project Description (25 min) │
│ Break (5 min)                          │
│ Sprint 3: Goals & Objectives (20 min)  │
│ LONGER BREAK (15 min)                  │
│ Sprint 4: Evaluation Plan (25 min)     │
│ Break (5 min)                          │
│ Sprint 5: Org Capacity (25 min)        │
│ Break (5 min)                          │
│ Sprint 6: Sustainability (20 min)      │
│ COMPLETE!                              │
└────────────────────────────────────────┘

Total writing time: 2 hours 20 minutes
Total breaks: 40 minutes
Expected output: 2,000-2,500 words
```

---

## GAP NOTATION SYSTEM

**DURING SPRINTS, USE BRACKETS:**
```
Example draft text:

"According to [FIND CDC STAT], obesity rates in [COUNTY NAME] have increased by [PERCENTAGE] since [YEAR]. This affects approximately [NUMBER] children under age [AGE]."

"The program director [NAME] has [NUMBER] years of experience in [FIELD]. She holds a [DEGREE] from [UNIVERSITY] and previously worked at [ORGANIZATION]."

"Equipment costs are based on quotes from [VENDOR NAME] dated [DATE] (see Attachment [X])."
```

**AUTOMATED GAP TRACKING:**
- Creates checklist of all [BRACKETS]
- Assigns research tasks
- Tracks completion
- Updates narrative automatically

**GAP RESOLUTION SESSION:**
(Separate from writing sprints)
```
RESEARCH PHASE:
[ ] Find CDC obesity statistics
[ ] Confirm county name
[ ] Calculate percentage increase
[ ] Verify program director credentials
[ ] Locate vendor quote
```

---

## EDITING PROTOCOLS

**CRITICAL RULE:** Never edit while sprinting!

**EDITING HAPPENS LATER:**

### EDITING SESSION 1 (Content Review)
- Fill in [GAPS] with research
- Verify all claims have citations
- Check logic flow
- Add transitions
- Strengthen weak paragraphs
- Remove redundancy

### EDITING SESSION 2 (Style & Clarity)
- Simplify jargon
- Strengthen verbs
- Vary sentence length
- Check readability (Grade 10-12 level)
- Enhance storytelling

### EDITING SESSION 3 (Compliance)
- Verify against funding guidelines
- Check page limits
- Confirm all questions answered
- Review required elements
- Format per requirements

### EDITING SESSION 4 (Proofreading)
- Spell check
- Grammar check
- Punctuation
- Consistency (dates, names, numbers)
- Final polish

---

## OBSTACLE MANAGEMENT

### "I DON'T KNOW WHAT TO WRITE"

**AUTOMATED PROMPT GENERATOR:**
```
Stuck on Statement of Need?

Try these sentence starters:
- "The primary problem facing [population] is..."
- "Recent data from [source] shows that..."
- "Community members report that..."
- "Without addressing [problem], [consequence]..."

Still stuck?
- Review funding guidelines Q&A
- Look at past successful proposals
- Interview project stakeholders
- Free write for 3 minutes (no rules)
```

---

### "THIS SECTION IS TOO COMPLEX"

**AUTOMATED BREAK-DOWN:**
```
Complex section detected!

RECOMMENDED APPROACH:
Instead of one 25-min sprint, try:

Mini-Sprint 1 (15 min): Write overview paragraph
Mini-Sprint 2 (15 min): Detail Activity 1
Mini-Sprint 3 (15 min): Detail Activity 2
Mini-Sprint 4 (15 min): Detail Activity 3
Mini-Sprint 5 (15 min): Timeline & wrap-up

Total: 75 minutes = 3 standard sprints
```

---

### "I'M NOT HITTING WORD COUNTS"

**AUTOMATED EXPANSION PROMPTS:**
```
Current: 180 words
Target: 350 words
Gap: 170 words needed

TRY ADDING:
- Another data point/statistic
- A specific example or story
- Comparison to national average
- Quote from stakeholder
- Consequence if problem continues
- Historical context
- Geographic details
- Affected population characteristics
```

---

## COLLABORATIVE SPRINT FEATURES

**TEAM WRITING SESSIONS:**
```bash
claude narrative_sprint --team-session \
  --participants "3" \
  --sections "divided"
```

**FEATURES:**
- Simultaneous section assignments
- Shared timer
- Combined word count
- Group break synchronization
- Compilation of sections

**TEAM SPRINT PROTOCOL:**
```
9:00 AM - Team kickoff (15 min)
  - Review outline
  - Assign sections
  - Clarify questions

9:15 AM - Sprint 1 (25 min)
  - Everyone writes assigned section

9:40 AM - Break (5 min)

9:45 AM - Sprint 2 (25 min)
  - Continue or start new section

10:10 AM - Team check-in (10 min)
  - Share progress
  - Identify gaps
  - Adjust plan

10:20 AM - Continue sprints...
```

---

## PROGRESS TRACKING

**AUTOMATED DASHBOARD:**
```
GRANT NARRATIVE PROGRESS

Project: Youth Mentoring Program
Grant: Community Foundation
Due: March 15, 2026

SECTIONS COMPLETED:
✅ Statement of Need (100%)
✅ Project Description (100%)
✅ Goals & Objectives (100%)
⏳ Evaluation Plan (60%)
⏳ Organizational Capacity (40%)
❌ Sustainability (0%)
❌ Budget Narrative (0%)

OVERALL: 50% complete

STATS:
- Total words written: 1,847
- Target total: 3,500
- Remaining: 1,653 words
- Estimated time: 3 more sprints
- On track for: [date]
```

---

## INTEGRATION WITH OTHER COMMANDS

**WORKFLOW:**
```
1. research_funnel → Identify grants
2. budget_prep → Create budget
3. funding_strategy → Prioritize grants
4. narrative_sprint → WRITE narratives
5. letter_requests → Get support letters
6. final_review → Polish and submit
```

---

## DELIVERABLES

**GENERATED FILES:**
1. `[section]_sprint_[timestamp].docx` - Each sprint output
2. `[project]_narrative_compiled.docx` - Combined draft
3. `[project]_gaps_to_research.md` - [BRACKET] tracking
4. `[project]_sprint_log.csv` - Session statistics
5. `[project]_narrative_final.docx` - Edited version

---

## SUCCESS METRICS

**TRACK THESE:**
- Avg words per minute: ___
- Avg sprint completion: ___%
- Total sprints to complete section: ___
- Ratio of writing time to editing time: ___
- Days from start to final draft: ___

**TYPICAL RESULTS:**
- First-time users: 12-15 wpm
- Experienced users: 18-25 wpm
- Total narrative (3,000 words): 6-8 sprints
- First draft to final: 3-5 days

---

## TIME SAVINGS

**TRADITIONAL WRITING:**
- Constant editing while writing
- Frequent research breaks
- Procrastination
- Perfectionism paralysis
- **Average: 8-12 hours per section**

**SPRINT METHOD:**
- Focused writing bursts
- No interruptions
- Momentum maintained
- **Average: 25-45 minutes per section**

**TIME SAVED: 80%+ on drafting**
(Editing still required, but faster with complete draft)

---

## USAGE EXAMPLES

### Example 1: Single Section Sprint
```bash
claude narrative_sprint \
  --section "statement_of_need" \
  --wordcount "400" \
  --time "25"
```

### Example 2: Full Narrative Session
```bash
claude narrative_sprint \
  --full-narrative \
  --sections "6" \
  --total-time "180" \
  --breaks "pomodoro"
```

### Example 3: Team Collaborative Sprint
```bash
claude narrative_sprint \
  --team-session \
  --participants "3" \
  --duration "90" \
  --sections "statement_of_need,project_description,evaluation"
```

---

## RELATED COMMANDS
- `outline_generator` - Create section outlines before sprinting
- `gap_researcher` - Resolve [BRACKET] notations
- `readability_checker` - Assess draft clarity
- `compliance_review` - Verify against guidelines
- `final_polish` - Professional editing pass

**Version 1.0** | **Based on:** Meredith Noble Ch. 1 (Step 5) & Fast/Furious Method
