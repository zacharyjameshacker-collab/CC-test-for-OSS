# BUDGET PREP - Automated Grant Budget Development

## USAGE
```bash
claude budget_prep --project "[project_name]" --template "sf424a" --duration "[months]"
```

## PURPOSE
Generates comprehensive grant budgets in SF-424A format with automated calculations, match tracking, and multi-year projections.

---

## WORKFLOW EXECUTION

### INITIAL PROJECT SETUP

**PROMPT USER FOR:**
1. Project duration: ___ months/years
2. Project start date: ______
3. Total project scope: $______ (estimate)
4. Match requirement: ___% (if known)
5. Your organization's indirect rate: ___%
6. Are indirect costs allowed in this grant? Y/N

**AUTOMATED ACTIONS:**
- Create budget workbook with 10 tabs
- Set up formulas for automatic calculations
- Generate inflation projections (3-5% annually)
- Create summary dashboard

---

## BUDGET CATEGORY WORKFLOWS

### 1. PERSONNEL TAB

**PROMPT FOR EACH POSITION:**
```
Position Title: ______
Hours per week on project: ___
Weeks of project involvement: ___
Hourly rate: $___/hour
```

**AUTOMATED CALCULATIONS:**
- Total hours = hours/week × weeks
- Total cost = total hours × hourly rate
- Year 1, Year 2, Year 3 breakdown (if multi-year)
- Inflation adjustments for future years

**TEMPLATE GENERATION:**
```
| Position          | Hours/Week | Weeks | Total Hours | Rate   | Year 1  | Year 2  | Total    |
|-------------------|-----------|-------|-------------|--------|---------|---------|----------|
| Program Director  | 10        | 52    | 520         | $45.00 | $23,400 | $24,102 | $47,502  |
| Project Coordinator| 20       | 52    | 1,040       | $28.00 | $29,120 | $29,986 | $59,106  |
```

**VALIDATION CHECKS:**
- ⚠️ Hours exceed 2,080/year (full-time equivalent)
- ✅ Reasonable hourly rates for positions
- ✅ Time commitment aligns with project scope

---

### 2. FRINGE BENEFITS TAB

**PROMPT:**
- Organizational fringe rate: ___%
- Is rate consistent across all staff? Y/N
- If no, specify rates by position: ______

**AUTOMATED CALCULATIONS:**
- Fringe for each position = Personnel cost × Fringe %
- Total fringe benefits
- Multi-year projections

**COMMON RATES:**
- Entry level: 10-15%
- Mid-level: 20-25%
- Senior level: 25-30%

---

### 3. TRAVEL TAB

**FOR EACH TRIP:**
```
Trip Purpose: ______
Destination: ______
Number of travelers: ___
Trip duration (days): ___
Departure date: ______
```

**AUTOMATED GSA RATE LOOKUP:**
- Per diem rate for destination: $___
- Lodging rate for destination: $___
- Current year rates + inflation buffer

**COST BREAKDOWN:**
```
Transportation:
- Airfare: $_______ × ___ travelers = $_______
- Ground transportation: $_______
- Vehicle rental: $_______

Lodging:
- Nights: ___ × GSA rate $___× ___ travelers = $_______

Meals & Incidentals:
- Days: ___ × M&IE rate $___× ___ travelers = $_______
```

**TOTAL TRIP COST:** $_______

**VALIDATION:**
- ✅ Rates align with current GSA tables
- ✅ 3-5% inflation buffer included
- ✅ Purpose aligns with project goals

---

### 4. EQUIPMENT TAB (>$5,000, >1 year useful life)

**FOR EACH EQUIPMENT ITEM:**
```
Item description: ______
Vendor: ______
Quote date: ______
Base cost: $_______
Inflation buffer (3-5%): $_______
Total estimated cost: $_______
```

**REQUIRED DOCUMENTATION:**
- [ ] Vendor quote saved in project folder
- [ ] Equipment specification sheet
- [ ] Justification narrative (why needed)

**AUTOMATED TRACKING:**
- Equipment total
- Quote expiration dates
- Vendor contact information

---

### 5. SUPPLIES TAB (<$5,000 or consumable)

**SUPPLY CATEGORIES:**
```
Office Supplies:
- Item: _______ | Quantity: ___ | Unit Cost: $___ | Total: $_____

Program Materials:
- Item: _______ | Quantity: ___ | Unit Cost: $___ | Total: $_____

Software/Subscriptions:
- Item: _______ | Duration: ___ months | Monthly: $___ | Total: $_____
```

**AUTOMATED CALCULATIONS:**
- Category subtotals
- Grand total for supplies
- Cost per beneficiary (if applicable)

---

### 6. CONTRACTUAL TAB

**FOR EACH CONTRACTOR/VENDOR:**
```
Contractor name: ______
Service provided: ______
Contract duration: ___ months
Rate structure: $___/hour or $___/project
Total estimated cost: $_______
```

**COMMON CONTRACTUAL SERVICES:**
- Third-party evaluators
- Training consultants
- Design/marketing services
- IT/database development
- Grant writing services
- Legal counsel
- Audit services

**REQUIRED DOCUMENTATION:**
- [ ] Cost estimate/proposal saved
- [ ] Scope of work defined
- [ ] Selection process documented

---

### 7. CONSTRUCTION TAB

**PROJECT COMPONENTS:**
```
Construction Type:
[ ] New construction
[ ] Renovation
[ ] Site improvements

Cost Elements:
- Architectural/Engineering fees: $_______
- Permits and inspections: $_______
- General contractor: $_______
- Materials: $_______
- Labor: $_______
- Contingency (10-15%): $_______
```

**AUTOMATED CALCULATIONS:**
- Total construction costs
- Cost per square foot
- Contingency buffer

---

### 8. OTHER DIRECT COSTS TAB

**MISCELLANEOUS EXPENSES:**
```
Communications:
- Phone/internet: $_______
- Postage/shipping: $_______

Printing/Copying:
- Marketing materials: $_______
- Reports/documents: $_______

Space Rental:
- Meeting space: $_______
- Storage: $_______

Insurance:
- Liability: $_______
- Property: $_______
```

---

### 9. INDIRECT COSTS TAB

**AUTOMATED CALCULATIONS:**

**Method 1: De Minimis Rate (10%)**
- Modified Total Direct Costs (MTDC): $_______
- Indirect = MTDC × 10%
- **Total Indirect: $_______**

**Method 2: Negotiated Rate**
- Indirect cost base: $_______
- Your organization's rate: ___%
- **Total Indirect: $_______**

**VALIDATION:**
- ✅ Verify allowability in funding guidelines
- ⚠️ Reduces funds available for direct costs
- ✅ May be requirement for smaller organizations

---

### 10. COST SHARE/MATCH TAB

**CRITICAL RULE:** Every match item MUST appear in main budget!

**AUTOMATED TRACKING:**
```
| Budget Line Item    | Total Cost | Grant Request | Cost Share | Source        |
|---------------------|-----------|---------------|------------|---------------|
| Program Director    | $47,502   | $0            | $47,502    | In-kind time  |
| Equipment - Computer| $5,200    | $0            | $5,200     | Cash donation |
| Office Space        | $12,000   | $0            | $12,000    | In-kind rent  |
```

**AUTOMATED CALCULATIONS:**
- Total cost share amount: $_______
- Total project budget: $_______
- Cost share percentage: ___% (Cost Share ÷ Total Budget)
- **Does it meet requirement? Y/N**

**MATCH VALIDATION:**
- ✅ All cost share items in main budget
- ⚠️ Match percentage meets requirement
- ✅ Match sources documented
- ✅ Letters of commitment for cash match

**TYPES OF MATCH:**
- Cash (requires donor commitment letters)
- In-kind personnel (use actual hourly rates)
- In-kind space (use fair market value)
- In-kind equipment/materials (use purchase price)
- Volunteer time (use volunteer rate guidelines)

---

## BUDGET SUMMARY DASHBOARD

**AUTOMATED GENERATION:**

```
PROJECT BUDGET SUMMARY
Project: [Name]
Duration: [X] months/years
Grant: [Funder Name]

COST BREAKDOWN:
1. Personnel                    $_______ (___%)
2. Fringe Benefits              $_______ (___%)
3. Travel                       $_______ (___%)
4. Equipment                    $_______ (___%)
5. Supplies                     $_______ (___%)
6. Contractual                  $_______ (___%)
7. Construction                 $_______ (___%)
8. Other Direct Costs           $_______ (___%)
9. Subtotal Direct Costs        $_______

10. Indirect Costs (__%)        $_______

TOTAL PROJECT COST              $_______

FUNDING SOURCES:
Grant Request                   $_______ (___%)
Cost Share/Match                $_______ (___%)
Other Sources                   $_______ (___%)

TOTAL FUNDING                   $_______

MATCH REQUIREMENT:
Required: ___%
Provided: ___%
Status: ✅ MEETS / ⚠️ DEFICIT $_____
```

---

## MULTI-YEAR BUDGET PROJECTION

**AUTOMATED FOR YEARS 2-3:**

```
YEAR 1 | YEAR 2 | YEAR 3 | TOTAL

Apply inflation rates:
- Personnel: 3% annual increase
- Fringe: matches personnel increase
- Travel: 4% annual increase  
- Equipment: 3% annual increase
- Supplies: 3% annual increase
- Contractual: per contract terms
- Other: 3% annual increase
```

**AUTOMATED GRAPHS:**
- Cost distribution pie chart
- Multi-year spending timeline
- Cost share visualization

---

## BUDGET NARRATIVE GENERATOR

**AUTOMATED SECTIONS:**

### Personnel Justification:
```
[Position Title] will dedicate [X] hours per week to [specific duties]. This position is essential because [justification]. The hourly rate of $[X] reflects [market rate/organizational pay scale].
```

### Travel Justification:
```
Travel to [destination] is necessary for [purpose]. This aligns with project goal of [objective]. Costs are based on current GSA rates plus a 3-5% inflation buffer.
```

### Equipment Justification:
```
[Equipment name] is required to [purpose/function]. This equipment will be used for [duration] and will serve [number] beneficiaries. Cost estimate based on [vendor] quote dated [date].
```

**FULL NARRATIVE OUTPUT:**
- `[project]_budget_narrative.docx`
- Formatted, ready to attach
- Cross-referenced to budget spreadsheet

---

## VENDOR QUOTE TRACKING

**AUTOMATED SYSTEM:**
```
| Item         | Vendor      | Quote Date | Amount  | Valid Until | Status  | File Location |
|--------------|-------------|-----------|---------|-------------|---------|---------------|
| Server       | Dell        | 1/15/26   | $8,500  | 4/15/26     | Current | quotes/dell.pdf|
| Furniture    | Steelcase   | 12/20/25  | $12,400 | 3/20/26     | Expiring| quotes/steel.pdf|
```

**ALERTS:**
- ⚠️ Quote expiring within 30 days
- ⚠️ No quote on file for item >$5,000
- ✅ All quotes current and saved

---

## FUNDER-SPECIFIC FORMATTING

**AUTOMATED CONVERSION:**
```bash
claude budget_prep --convert-to "funder_format"
```

Supports conversion to:
- SF-424A (federal standard)
- SF-424C (construction)
- Foundation custom templates
- State agency formats
- Corporate foundation formats

**PRESERVES:**
- All calculations
- Cost share tracking
- Narrative justifications
- Supporting documentation links

---

## BUDGET REVIEW CHECKLIST

**AUTOMATED GENERATION:**
```
BUDGET COMPLETENESS:
[ ] All personnel positions included
[ ] Fringe rates verified with accounting
[ ] Travel costs based on GSA rates + buffer
[ ] Equipment quotes obtained and saved
[ ] Contractual scopes of work defined
[ ] Indirect costs calculated correctly
[ ] Match appears in main budget AND cost share
[ ] Match percentage meets requirement
[ ] Budget total matches narrative request amount
[ ] Multi-year budgets include inflation
[ ] Budget narrative drafted for each category
[ ] All vendor quotes saved in project folder
[ ] Cash match commitment letters obtained

VALIDATION:
[ ] Math checks out (all formulas working)
[ ] Subtotals match category totals
[ ] Grand total is sum of all categories
[ ] Percentages add to 100%
[ ] Cost per beneficiary is reasonable
[ ] Hourly rates are defensible
[ ] No unallowable costs included
```

---

## ERROR DETECTION

**AUTOMATED WARNINGS:**

🔴 **CRITICAL ERRORS:**
- Match in cost share but NOT in main budget
- Match percentage below requirement
- Indirect costs included when not allowed
- Budget total ≠ sum of categories
- Equipment <$5,000 in equipment tab
- Supplies >$5,000 in supplies tab

🟡 **WARNINGS:**
- Personnel >2,080 hours/year
- Quote older than 90 days
- Travel without GSA rate reference
- Contractual without scope of work
- Missing vendor quote for equipment
- Inflation buffer not applied

---

## COLLABORATION FEATURES

**AUTOMATED SHARING:**
```bash
claude budget_prep --export-for-review --recipients "finance@org.com,director@org.com"
```

**GENERATES:**
- Read-only spreadsheet link
- PDF summary report
- Change log
- Comment threads

**VERSION CONTROL:**
- `budget_v1.0_draft.xlsx`
- `budget_v2.0_finance_review.xlsx`
- `budget_v3.0_final.xlsx`

---

## BUDGET TO NARRATIVE INTEGRATION

**AUTOMATED CROSS-REFERENCING:**
```
Narrative mentions: "10 hours/week of program director time"
Budget shows: Program Director - 10 hours/week

Status: ✅ ALIGNED

Narrative mentions: "$45,000 for contractual evaluator"  
Budget shows: Contractual - Evaluator: $42,000

Status: ⚠️ MISMATCH - Needs correction
```

---

## USAGE EXAMPLES

### Example 1: Simple One-Year Project
```bash
claude budget_prep \
  --project "Youth_Mentoring_Program" \
  --duration "12_months" \
  --match "25%" \
  --indirect_rate "15%"
```

### Example 2: Multi-Year Capital Project
```bash
claude budget_prep \
  --project "Community_Center_Renovation" \
  --duration "36_months" \
  --type "construction" \
  --match "50%" \
  --indirect "not_allowed"
```

### Example 3: Federal Grant (SF-424A)
```bash
claude budget_prep \
  --project "USDA_Rural_Development" \
  --template "sf424a" \
  --duration "24_months" \
  --match "20%" \
  --indirect_rate "de_minimis"
```

---

## DELIVERABLES

**GENERATED FILES:**
1. `[project]_budget_master.xlsx` - Full budget workbook
2. `[project]_budget_summary.pdf` - One-page overview
3. `[project]_budget_narrative.docx` - Justifications
4. `[project]_match_tracking.xlsx` - Cost share detail
5. `[project]_vendor_quotes/` - Supporting documents folder
6. `[project]_budget_checklist.md` - Quality assurance

---

## TIME SAVINGS

**Manual Process:**
- Budget development: 8-12 hours
- Narrative writing: 3-5 hours
- Review and corrections: 2-4 hours
- **Total: 13-21 hours**

**Automated Process:**
- Budget setup: 2-3 hours
- Data entry: 3-4 hours
- Review: 1-2 hours
- **Total: 6-9 hours**

**TIME SAVED: 57%+**

---

## RELATED COMMANDS
- `match_calculator` - Quick cost share percentage tool
- `inflation_adjuster` - Multi-year cost projections
- `quote_tracker` - Vendor quote management
- `budget_compare` - Compare budgets across grants
- `narrative_sync` - Verify budget/narrative alignment

**Version 1.0** | **Based on:** Meredith Noble Ch. 12 & SF-424A Standards
