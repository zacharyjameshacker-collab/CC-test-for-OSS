# GRANT RESEARCH FUNNEL - Automated Workflow Command

## USAGE
```bash
claude research_funnel --project "[project_name]" --type "[organization_type]" --location "[geographic_area]"
```

## PURPOSE
Guides user through the complete three-stage Grant Research Funnel process from 100+ initial findings to top grant pursuits worth pursuing.

---

## WORKFLOW EXECUTION

### STAGE 1: Find 100+ Grants (Broad Search)

**PROMPT USER FOR:**
1. Organization type(s): 
   - Nonprofit 501(c)(3)
   - Local government
   - Tribal organization
   - Educational institution
   - Other (specify)

2. Project type/field of work:
   - Keywords describing project
   - Primary beneficiary population
   - Geographic scope

3. Minimum award size: $______
4. Maximum award size: $______

**AUTOMATED ACTIONS:**
- Generate search parameters for grant databases
- Create initial prospect tracking spreadsheet with columns:
  * Funder Name
  * Program Name
  * Award Size Range
  * Deadline
  * Geographic Scope
  * Keywords/Focus Areas
  * Status (Keep/Cut)
  * Notes

**OUTPUT:**
- `[project]_stage1_prospects.csv` with 100+ initial findings
- Search parameters document for reproducibility

---

### STAGE 2: From 100+ to ~20 (Quick Filtering)

**FOR EACH GRANT PROSPECT:**

#### Filter 1: Funder's Giving Priorities
**PROMPT:** "Review funder overview. Does this feel like natural alignment?"
- [ ] Strong alignment - language matches our mission
- [ ] Possible alignment - could work with adjustments
- [ ] Weak alignment - feels like a stretch
- [ ] No alignment - CUT

**AUTOMATED CHECK:**
- Flag generic language vs. specific priorities
- Highlight keywords matching project description

#### Filter 2: Eligible Use of Funds
**PROMPT:** "What do you want to get funded?"
- [ ] Personnel/staffing
- [ ] Equipment
- [ ] Programming/services
- [ ] Capital improvements/construction
- [ ] Operating expenses
- [ ] Planning activities
- [ ] Other: _______

**AUTOMATED ACTIONS:**
- Cross-reference against funder's eligible expenses
- Flag common ineligible items (indirect costs, existing deficits, etc.)
- Mark as ELIGIBLE or INELIGIBLE

#### Filter 3: Funding History
**AUTOMATED ACTIONS:**

**For Foundations:**
- Generate 990 lookup instructions
- Prompt for key data points:
  * Total annual giving: $______
  * Average award size: $______
  * Geographic distribution: ______
  * Similar organizations funded: Y/N
  * Projects similar to yours: (list)

**Decision Matrix:**
- Total giving < $1M → CUT (unless exceptional fit)
- No grants in your geography → CUT
- No similar organizations funded → CUT
- All checks pass → KEEP for Stage 3

**For Government Grants:**
- Locate past awardees list URL
- Extract: award amounts, project types, geographic distribution
- Compare against your project

**OUTPUT:**
- `[project]_stage2_filtered.csv` with ~20 grants
- Cut grants moved to `[project]_eliminated.csv` with reasons
- Summary report: "Filtered [X] grants to [Y] based on [Z] criteria"

---

### STAGE 3: From ~20 to Top Pursuits (Deep Evaluation)

**FOR EACH REMAINING GRANT:**

#### STEP 1: Calculate Competitiveness
**AUTOMATED EMAIL GENERATOR:**
```
Subject: Quick question on [Program Name]

Hi [Contact Name],

We are interested in [Program Name] and gauging competitiveness.

Could you share:
- How many applicants applied last year?
- What percent of those were successful?

Thank you!

[Your Name]
[Organization]
```

**PROMPT USER:**
- Awards made last year: ______
- Total applicants: ______

**AUTOMATED CALCULATION:**
- Success Rate = Awards ÷ Applicants × 100
- 20%+ → GREEN (pursue)
- 15-19% → YELLOW (consider if strategic)
- <15% → RED (low priority unless exceptional)

**ADD TO TRACKING:**
- Competitiveness %
- Date contacted
- Response received: Y/N

#### STEP 2: Review Funding Guidelines
**AUTOMATED CHECKLIST GENERATOR:**

Downloads guidelines and creates checklist:
- [ ] Eligibility requirements (list all)
- [ ] Required attachments (count: ___)
- [ ] Page limits/word counts
- [ ] Match requirements (%: ___)
- [ ] Indirect costs allowed? Y/N (rate: ___)
- [ ] Letter of inquiry required first? Y/N
- [ ] Deadline date: ______
- [ ] Anticipated workload hours: ______

**COMPLEXITY ASSESSMENT:**
- Pages of narrative required: ___
- Number of attachments: ___
- Specialized requirements: (list)
- Time estimate for completion: ___ hours

**ROI CALCULATION:**
- Award amount: $______
- Estimated hours: ______
- $ per hour: $______ (should be $500+)

#### STEP 3: Contact Past Applicants
**AUTOMATED TEMPLATE GENERATOR:**
```
Subject: Request - [Program Name] Application Example

Hi [Name],

I noticed your organization received funding from [Program Name] in [year]. Congratulations!

We are considering applying this year and would greatly appreciate seeing an example of a successful application, if you're willing to share.

Additionally, I'd love to hear:
- How did you fund the rest of your project?
- Were the reporting requirements reasonable?
- Would you pursue this grant again?

Any insights would be tremendously helpful. Thank you for considering this request!

Best regards,
[Your Name]
```

**TRACKING:**
- Past awardee contacted: (name)
- Date contacted: ______
- Response received: Y/N
- Application received: Y/N
- Key insights: (notes)

#### STEP 4: Contact the Funder
**AUTOMATED PROJECT PROSPECTUS GENERATOR:**

Creates one-page overview with:
- Organization name and mission
- Project description (2-3 paragraphs)
- Beneficiary population and numbers served
- Total project budget
- Funding requested from this grant
- Timeline for implementation
- Key project partners
- Contact information

**MEETING PREPARATION CHECKLIST:**
- [ ] Prospectus sent 2-3 days before call
- [ ] Questions prepared (see below)
- [ ] Project team member assigned to call
- [ ] Calendar reminder set
- [ ] Follow-up thank you email drafted

**KEY QUESTIONS TO ASK:**
1. Would your organization fund a project like ours?
   - If yes: What would make it more appealing?
   
2. Is our project eligible?
   - Get confirmation in writing
   
3. Why would this project NOT get funded?
   - Identify weaknesses to address
   
4. When is the best time to apply?
   - Strategic timing considerations
   
5. What must be in place before applying?
   - Hidden prerequisites
   
6. Who can we partner with for success?
   - Recommended collaborators
   
7. What was the average award size?
   - Set realistic request amount
   
8. What distinguishes successful applicants?
   - Common success factors

**CALL NOTES TEMPLATE:**
- Funder contact: (name, title)
- Date of call: ______
- Key takeaways: (bullet points)
- Red flags identified: (if any)
- Green lights received: (if any)
- Action items: (numbered list)
- Next steps: ______

**AUTOMATED DECISION MATRIX:**

After completing Steps 1-4, score each grant:
- Competitiveness (20%+): __/5 points
- Natural fit: __/5 points
- Funder endorsement: __/5 points
- ROI ($/hour): __/5 points
- Strategic timing: __/5 points

**TOTAL SCORE: __/25**
- 20-25 points: TOP PURSUIT (include in funding strategy)
- 15-19 points: BACKUP PURSUIT (keep on radar)
- <15 points: LOW PRIORITY (eliminate or defer)

---

## FINAL STAGE 3 OUTPUT

**DELIVERABLES:**
1. `[project]_top_pursuits.csv` - Ranked list of best grants
2. `[project]_backup_pursuits.csv` - Secondary options
3. `[project]_research_summary.md` - Complete findings report
4. `[project]_funder_contacts.csv` - Contact information database
5. `[project]_action_items.md` - Prerequisites before applying

**SUMMARY REPORT INCLUDES:**
- Total grants researched: ___
- Grants eliminated in Stage 2: ___
- Grants evaluated in Stage 3: ___
- Top pursuits identified: ___
- Total potential funding: $______
- Timeline to secure funding: ___ months

---

## USAGE EXAMPLES

### Example 1: Commercial Fishing Grant Research
```bash
claude research_funnel \
  --project "Bristol_Bay_Processors" \
  --type "commercial_fishing,nonprofit" \
  --location "Alaska" \
  --keywords "fisheries,value-added,processing,infrastructure"
```

### Example 2: Community Development Project
```bash
claude research_funnel \
  --project "Downtown_Revitalization" \
  --type "local_government" \
  --location "California,multi-county" \
  --keywords "economic_development,main_street,tourism"
```

---

## AUTOMATION FEATURES

This command automates:
- ✅ Spreadsheet generation and formatting
- ✅ Email template creation
- ✅ Checklist generation
- ✅ Scoring matrices
- ✅ ROI calculations
- ✅ Timeline estimates
- ✅ Summary report writing
- ✅ File organization
- ✅ Decision tracking

**TIME SAVINGS:**
- Manual process: 40-60 hours
- With automation: 15-25 hours
- **Efficiency gain: 60%+**

---

## NOTES FOR USERS

**Best Practices:**
1. Don't skip Stage 2 filtering - speed is essential here
2. Calculate competitiveness for EVERY Stage 3 grant
3. Contact funders even if intimidating - they want to help
4. Request past applications when possible
5. Save all email confirmations of eligibility
6. Update tracking spreadsheet in real-time

**Common Mistakes to Avoid:**
- Trying to convince yourself of alignment (trust your gut)
- Not calculating competitiveness (wastes time)
- Skipping funder contact (misses critical feedback)
- Pursuing <15% success rates (low ROI)
- Not organizing files systematically (creates chaos)

---

**Related Commands:**
- `funding_strategy` - Create funding strategy from top pursuits
- `competitiveness_calc` - Quick calculator for success rates
- `funder_outreach` - Generate customized outreach emails
- `990_lookup` - Automated foundation research

**Version 1.0** | **Based on:** Meredith Noble's Grant Research Funnel
