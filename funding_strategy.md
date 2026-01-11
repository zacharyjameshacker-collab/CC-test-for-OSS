# FUNDING STRATEGY - Automated Strategy Document Generator

## USAGE
```bash
claude funding_strategy --project "[project_name]" --from-research "[research_file.csv]"
```

## PURPOSE
Creates a professional 2-3 page Funding Strategy document that outlines which grants to pursue, when to pursue them, and project prerequisites. Serves as organizational roadmap and funder communication tool.

---

## INPUT REQUIREMENTS

**MUST HAVE COMPLETED:**
- [ ] Grant Research Funnel (all 3 stages)
- [ ] Top pursuits identified and ranked
- [ ] Competitiveness calculated for each grant
- [ ] Funder conversations completed
- [ ] Project budget drafted
- [ ] Total funding need determined

**LOADS DATA FROM:**
- `[project]_top_pursuits.csv`
- `[project]_budget_master.xlsx`
- `[project]_funder_contacts.csv`
- `[project]_action_items.md`

---

## DOCUMENT STRUCTURE

### SECTION 1: PROJECT OVERVIEW

**AUTOMATED PROMPTS:**
```
What is your project? (1 paragraph)
_______________________________________________

What problem does it solve?
_______________________________________________

Why is this problem important? (backed by data)
_______________________________________________

Who are the primary beneficiaries?
- Population: _______________
- Number served: ___________
- Geographic area: __________
```

**GENERATES:**
```markdown
## Project Overview

[Organization Name] proposes [project name], a [duration] initiative to [core purpose]. This project addresses [problem statement] by [solution approach]. 

Currently, [data point showing need]. This impacts [number] individuals/families in [geographic area] by [specific consequences]. 

[Project name] will [primary activities] to achieve [measurable outcome]. Upon completion, the project will [long-term impact].
```

---

### SECTION 2: TANGIBLE TRANSFORMATION

**PROMPT:**
```
Complete this sentence:

I help [identity] get [transformation], 
so they can [ONE pain point or deep desire].

Example: "I help at-risk youth get job skills training and mentorship, so they can break cycles of poverty in their families."
```

**VALIDATION:**
- ⚠️ Did you list multiple outcomes? (Pick ONE!)
- ⚠️ Is it memorable and specific?
- ✅ Does it pass the "so what?" test?

---

### SECTION 3: ACTION ITEMS NEEDED

**AUTOMATED EXTRACTION FROM:**
- Project planning toolkit
- Funder conversation notes
- Eligibility requirements

**GENERATES:**
```markdown
## Prerequisites Before Grant Submission

The following items must be completed before implementing this Funding Strategy:

### Immediate (Complete within 2 weeks):
1. [Action item] - Responsible: [Name] - Deadline: [Date]
2. [Action item] - Responsible: [Name] - Deadline: [Date]

### Short-term (Complete within 4-6 weeks):
3. [Action item] - Responsible: [Name] - Deadline: [Date]
4. [Action item] - Responsible: [Name] - Deadline: [Date]

### Ongoing:
5. [Action item] - Responsible: [Name] - Deadline: [Date]
```

**COMMON ACTION ITEMS:**
- Partnership agreements signed
- Board resolution approving grant pursuit
- Updated organizational documents (501c3, bylaws)
- Environmental/historical reviews completed
- Community engagement/input documented
- Letters of support commitments secured
- Match funding sources identified
- Project scope of work finalized
- Cost estimates refined
- Preliminary site plans completed

---

### SECTION 4: FUNDING OPPORTUNITIES MATRIX

**AUTOMATED TABLE GENERATION:**

Pulls from `top_pursuits.csv` and formats:

```markdown
## Top Funding Opportunities

| Priority | Funder | Program | Amount | Deadline | Competitiveness | What It Funds | Strategy |
|----------|--------|---------|--------|----------|----------------|---------------|----------|
| 1 | [Name] | [Program] | $150,000 | March 15 | 25% (30/120) | Equipment, Personnel | Apply Year 1; use as leverage |
| 2 | [Name] | [Program] | $75,000 | Rolling | 40% (20/50) | Operating, Match | Apply after Grant #1 awarded |
| 3 | [Name] | [Program] | $200,000 | June 30 | 22% (15/68) | Construction, Design | 50% match required - use Grants #1-2 |
```

**COLUMN DEFINITIONS:**
- **Priority**: Pursuit order (1 = first to pursue)
- **Funder**: Organization name
- **Program**: Specific grant program name
- **Amount**: Award request (or range)
- **Deadline**: Application due date
- **Competitiveness**: Success % (awards/applicants)
- **What It Funds**: Eligible expense categories
- **Strategy**: Pursuit approach and dependencies

**AUTOMATED STRATEGY NOTATION:**
- "Apply immediately" (20%+ rate, rolling deadline)
- "Wait for leverage" (requires other funding first)
- "Use as match source" (for grants requiring match)
- "Final piece" (fills remaining budget gap)
- "Backup option" (if primary grant fails)

---

### SECTION 5: FUNDING STACK ANALYSIS

**AUTOMATED BUDGET ALLOCATION:**

```markdown
## How Grants Work Together

Total Project Budget: $500,000

| Funding Source | Amount | Purpose | Status | Timeline |
|----------------|--------|---------|--------|----------|
| Grant #1 | $150,000 | Equipment & Staff | Pending | Apply Q1 2026 |
| Grant #2 | $75,000 | Operations | Planned | Apply Q2 2026 |
| Grant #3 | $200,000 | Construction | Planned | Apply Q3 2026 |
| Org Match | $50,000 | In-kind space | Committed | Ongoing |
| Donor Campaign | $25,000 | Cash match | In progress | Complete Q2 2026 |
| **TOTAL** | **$500,000** | | | |

### Funding Dependencies:
- Grant #2 requires 25% match → Use in-kind space ($50k)
- Grant #3 requires 50% match → Use Grants #1-2 + donations ($250k)
- All grants require letters of support → Secure by [date]
```

**VISUAL REPRESENTATION:**
```
[ASCII or Mermaid diagram showing funding flow and dependencies]

Grant #1 ($150k) ──┐
                   ├──> Combined Match ──> Grant #3 ($200k)
Grant #2 ($75k) ───┤
                   │
Org Match ($50k) ──┘

Timeline: →→→→→→→→→→→→→→→→→→→→→
          Q1      Q2      Q3      Q4
```

---

### SECTION 6: DETAILED GRANT PROFILES

**FOR EACH TOP PURSUIT:**

```markdown
### [Funder Name] - [Program Name]

**Award Amount:** $_______ (Range: $_____ - $_____)
**Deadline:** _______ (Annual/Rolling)
**Match Required:** ___% (Type: Cash/In-kind/Either)

**Eligibility:**
- Organization type: _______
- Geographic: _______
- Project type: _______
- Special requirements: _______

**Funding Priorities:** (from funder materials)
[Bullet points of what they want to fund]

**What We'll Request:**
- Personnel: $_______
- Equipment: $_______  
- [Other categories]: $_______
- **Total Request:** $_______

**Competitiveness Analysis:**
- Applications received (last year): ___
- Awards made: ___
- Success rate: ___%
- Average award: $_______

**Why This is a Good Fit:**
1. [Alignment reason #1]
2. [Alignment reason #2]
3. [Past giving to similar projects]

**Funder Contact:**
- Name: _______
- Title: _______
- Email: _______
- Phone: _______
- Last contact: _______

**Key Insights from Funder Conversation:**
- [Note #1]
- [Note #2]
- [Any concerns to address]
- [Strengths they identified]

**Application Requirements:**
- Narrative pages: ___
- Budget format: _______
- Attachments: (list)
- Pre-application required: Y/N
- Site visit: Y/N

**Timeline:**
- Start application: _______
- Internal deadline: _______
- Submit by: _______
- Award notification: _______
```

---

### SECTION 7: MASTER SCHEDULE

**AUTOMATED GANTT-STYLE TIMELINE:**

```markdown
## Implementation Schedule

### Year 1 (2026)
**Q1 (Jan-Mar):**
- Jan 15: Complete partnership agreements
- Feb 1: Begin Grant #1 application  
- Feb 15: Request letters of support
- Mar 10: Internal review Grant #1
- Mar 15: SUBMIT Grant #1
- Mar 20: Begin Grant #2 application

**Q2 (Apr-Jun):**
- Apr 15: SUBMIT Grant #2
- May 1: Expected Grant #1 award notification
- May 15: Secure cash match commitments
- Jun 1: Begin Grant #3 application (if Grants #1-2 successful)
- Jun 30: SUBMIT Grant #3

**Q3 (Jul-Sep):**
- Jul 15: Expected Grant #2 award notification
- Aug 1: Begin project implementation (if funded)
- Sep 15: Expected Grant #3 award notification

**Q4 (Oct-Dec):**
- Oct 1: Full project launch (if all grants awarded)
- Ongoing: Quarterly reporting to funders
```

**MILESTONE MARKERS:**
- 🔴 Critical deadlines
- 🟡 Dependent milestones
- 🟢 Flexible timing
- ⏰ Expected responses

---

## CONTINGENCY PLANNING

**AUTOMATED SCENARIOS:**

```markdown
## What If Scenarios

### Scenario 1: Grant #1 Not Awarded
**Action Plan:**
- Move to backup Grant #4 (Foundation X)
- Adjust timeline by 3 months
- Reduce project scope to match available funding
- OR: Pursue additional donor campaign

### Scenario 2: Partial Award (Less than Requested)
**Action Plan:**
- Reduce personnel hours
- Phase equipment purchases
- Extend project timeline
- Seek supplemental funding

### Scenario 3: All Grants Delayed
**Action Plan:**
- Use organizational reserves for bridge funding
- Implement pilot phase with existing resources
- Reapply in next funding cycle
- Maintain relationships with funders
```

---

## RISK ASSESSMENT

**AUTOMATED ANALYSIS:**

```markdown
## Funding Strategy Risk Factors

### Low Risk (Unlikely to Impact Success):
- ✅ Organization has strong track record
- ✅ Multiple funding sources identified
- ✅ Competitiveness rates are favorable (20%+)

### Medium Risk (Monitor Closely):
- ⚠️ Grant #3 requires 50% match (dependent on other grants)
- ⚠️ Timeline is aggressive (12 months for all funding)
- ⚠️ One grant is invite-only (working on introduction)

### High Risk (Mitigation Required):
- 🔴 [If applicable]

### Mitigation Strategies:
1. [Strategy for each risk]
2. [Backup options identified]
3. [Contingency funding sources]
```

---

## FUNDER ENGAGEMENT PLAN

**AUTOMATED TRACKING:**

```markdown
## Ongoing Funder Communication

| Funder | Contact Frequency | Next Touchpoint | Purpose | Responsible |
|--------|------------------|----------------|---------|-------------|
| Grant #1 | Quarterly | Feb 1 | Send project update | [Name] |
| Grant #2 | As needed | Mar 15 | Invitation to site visit | [Name] |
| Grant #3 | Monthly | Jan 30 | Share Funding Strategy | [Name] |
```

**COMMUNICATION TEMPLATES:**
- Progress update email template
- Meeting request template
- Thank you after funder conversation
- Award notification response
- Decline notification response

---

## BOARD/LEADERSHIP APPROVAL

**AUTOMATED SECTION:**

```markdown
## Recommendation & Next Steps

Based on this analysis, we recommend:

1. **Approve** pursuit of the identified grant opportunities
2. **Allocate** necessary staff time and resources for applications
3. **Commit** organizational match as outlined ($______)
4. **Assign** board liaison for funder relationships
5. **Schedule** quarterly Funding Strategy review meetings

### Resource Requirements:
- Grant writer time: ___ hours over ___ months
- Finance staff time: ___ hours
- Leadership time: ___ hours
- Board involvement: ___ meetings

### Expected ROI:
- Total funding sought: $_______
- Investment in grant writing: $_______
- Potential return: ___x investment

**Approval Requested By:** _______
**Decision Needed By:** _______
```

---

## APPENDICES

**AUTOMATICALLY ATTACHED:**

1. **Appendix A:** Complete grant research findings
2. **Appendix B:** Funder contact information
3. **Appendix C:** Competitiveness calculations
4. **Appendix D:** Preliminary project budget
5. **Appendix E:** Letters of support tracking
6. **Appendix F:** Partnership agreements (drafts)
7. **Appendix G:** Past successful applications (if available)

---

## FORMATTING & BRANDING

**AUTOMATED STYLING:**
- Organization letterhead on cover page
- Table of contents with page numbers
- Professional fonts and spacing
- Color-coded priority levels
- Charts and graphs where beneficial
- Executive summary (1 page)

**OUTPUT FORMATS:**
- `.docx` for editing and collaboration
- `.pdf` for formal presentation
- `.md` for version control
- PowerPoint deck for board presentation

---

## REVIEW & REFINEMENT WORKFLOW

**AUTOMATED REVIEW CHECKLIST:**

```
FUNDING STRATEGY QUALITY CHECK:

Content:
[ ] Project overview is clear and compelling
[ ] Problem statement backed by data
[ ] Tangible transformation is specific
[ ] All action items assigned with deadlines
[ ] Top 5-10 grants identified and ranked
[ ] Competitiveness calculated for each
[ ] Funding amounts add up to total budget
[ ] Match requirements addressed
[ ] Timeline is realistic with buffer time
[ ] Contingency plans included

Format:
[ ] Document is 2-3 pages (plus appendices)
[ ] Executive summary included
[ ] Visual elements enhance clarity
[ ] Professional appearance
[ ] Contact information current
[ ] All hyperlinks working

Approval:
[ ] Reviewed by finance department
[ ] Reviewed by program staff
[ ] Reviewed by executive director
[ ] Presented to board (if required)
[ ] Shared with key funders for feedback
```

---

## LIVING DOCUMENT MAINTENANCE

**QUARTERLY REVIEW PROTOCOL:**

```bash
claude funding_strategy --update --project "[name]" --review_date "[date]"
```

**UPDATES BASED ON:**
- Grant awards received/denied
- New funding opportunities identified
- Changes in funder priorities
- Project scope adjustments
- Budget modifications
- Timeline shifts

**VERSION CONTROL:**
- `funding_strategy_v1.0_initial.pdf` (Jan 2026)
- `funding_strategy_v2.0_q2_update.pdf` (Apr 2026)
- `funding_strategy_v3.0_post_awards.pdf` (Jul 2026)

---

## USAGE EXAMPLES

### Example 1: Community Program (Single Funder)
```bash
claude funding_strategy \
  --project "Youth_Mentoring" \
  --budget "$75000" \
  --single_funder "true" \
  --duration "12_months"
```
*Output: Simplified 1-page strategy for single grant pursuit*

### Example 2: Capital Project (Multiple Funders)
```bash
claude funding_strategy \
  --project "Community_Center" \
  --budget "$2500000" \
  --funders "7" \
  --duration "36_months" \
  --complexity "high"
```
*Output: Comprehensive 3-page strategy with detailed funding stack*

### Example 3: Update Existing Strategy
```bash
claude funding_strategy \
  --update \
  --project "Community_Center" \
  --grant_award "Foundation_X_$150000" \
  --grant_denied "Foundation_Y" \
  --revise_timeline "true"
```
*Output: Updated strategy reflecting recent award/denial*

---

## SHARING WITH FUNDERS

**AUTOMATED COVER EMAIL:**

```
Subject: Funding Strategy for [Project Name] - Your Feedback Requested

Dear [Funder Name],

Thank you for your recent conversation about [grant program]. As discussed, I'm sharing our comprehensive Funding Strategy for [project name].

This document outlines:
- Our complete project vision
- How we plan to fund the entire initiative
- Why your grant program is a strategic fit
- Timeline for securing all necessary funding

We would greatly appreciate your feedback on:
1. Does our timeline align with your program's funding cycle?
2. Have we accurately understood your priorities?
3. Are there areas you'd recommend we strengthen?
4. Do you see any challenges we should address?

I'm happy to schedule a brief call to discuss any questions. Thank you for considering our project!

Best regards,
[Your Name]
```

**BENEFITS OF SHARING:**
- Demonstrates seriousness and preparation
- Invites constructive feedback
- Shows how their grant fits the bigger picture
- Builds relationship and trust
- Increases likelihood of funding

---

## SUCCESS METRICS

**TRACK THESE INDICATORS:**
- Funding Strategy completion time: ___ weeks
- Board/leadership approval time: ___ days
- Funder feedback responses: ___% positive
- Grants submitted per strategy: ___
- Grants awarded: ___
- Success rate: ___%
- Total funding secured: $_______
- Time from strategy to full funding: ___ months

---

## DELIVERABLES

**GENERATED FILES:**
1. `[project]_funding_strategy_v1.0.docx` - Editable document
2. `[project]_funding_strategy_v1.0.pdf` - Presentation version
3. `[project]_funding_strategy_executive_summary.pdf` - 1-page overview
4. `[project]_funding_strategy_presentation.pptx` - Board deck
5. `[project]_funding_timeline.xlsx` - Detailed Gantt chart
6. `[project]_funder_communication_log.xlsx` - Tracking system

---

## TIME SAVINGS

**Manual Process:**
- Research compilation: 4-6 hours
- Document drafting: 6-8 hours
- Review and revisions: 2-4 hours
- Formatting and finalization: 2-3 hours
- **Total: 14-21 hours**

**Automated Process:**
- Data input and review: 2-3 hours
- Content refinement: 2-3 hours
- Stakeholder feedback: 1-2 hours
- **Total: 5-8 hours**

**TIME SAVED: 62%+**

---

## RELATED COMMANDS
- `research_funnel` - Generate initial grant findings
- `budget_prep` - Create project budget for strategy
- `timeline_generator` - Detailed grant pursuit schedule
- `board_presentation` - Create PowerPoint from strategy
- `funder_outreach` - Email templates for sharing strategy

**Version 1.0** | **Based on:** Meredith Noble Ch. 13 Funding Strategy
