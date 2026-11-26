# CampusFest 2025 — Sponsorship Growth Center

**Shobhit Kumar** | 23HS10050 | IIT Kharagpur
**Challenge B:** Sponsorship Growth — Maximize sponsorship cash collected before the festival
**Live Product:** [shobhit-007.github.io/campusfest-2025-growth-center](https://shobhit-007.github.io/campusfest-2025-growth-center/)

---

## 1. Project Overview

CampusFest 2025 is a fictional two-day college festival (12-13 April 2025) set in **Bangalore**.

**Why Bangalore:**
- India's startup capital with 5,000+ active startups and major MNCs (Flipkart, Infosys, Wipro, Swiggy, Razorpay), giving the deepest pool of brands with dedicated marketing and sponsorship budgets.
- Highest density of young professionals and college students in a single metro — sponsors see direct access to their target demographic.
- Strong college fest culture (IISc, IIIT-B, PES, RVCE) means brands are already familiar with the sponsorship format and ROI expectations.
- Excellent air and rail connectivity makes it easy for national brands to send activation teams.

**The Product:** A single-page web application that serves as the sponsorship team's command center — combining analytics, campaign management, opportunity tracking, and an AI analyst in one interface. Every number on the dashboard is derived from the provided Sponsor Dataset.

---

## 2. Research and Assumptions

### Sourced from the dataset (facts)

| Metric | Value | Source |
|--------|-------|--------|
| Brands targeted | 180 | Brands sheet |
| Contacts reached | 270 | Sponsor Contacts sheet |
| Total interactions | 953 | Sponsor Interactions sheet |
| Acquisition campaigns | 6 | Sponsor Campaigns sheet |
| Qualified brands (latest status) | 60 | Brand Qualification History (latest per brand) |
| Opportunities created | 58 | Partner Opportunities sheet |
| Confirmed partnerships | 24 | Opportunity History (latest stage = partner_confirmed) |
| Total cash collected | ₹22,40,000 | Sum of confirmed_value_inr for confirmed deals |
| Average deal size | ₹93,333 | ₹22,40,000 / 24 |
| Deal range | ₹35,000 – ₹2,00,000 | Min/max of confirmed values |
| Revised target (Mar 15) | 55 qualified, 28 confirmed | Targets sheet |

### Assumptions (clearly marked)

| Assumption | Rationale |
|------------|-----------|
| Negotiating deals close at ~60-70% | Industry benchmark for late-stage sponsorship; these brands have already attended meetings and are discussing terms |
| Proposal-sent deals close at ~35-50% | Proposals are out but no negotiation has started; drop-off is higher at this stage |
| Engaged brands can be fast-tracked to qualification at ~30% | 28 brands responded but are not yet qualified; with 10 days left, only well-fitting brands will convert |
| Lost deals can be partially recovered (~20%) with revised terms | 7 lost deals worth ₹7,80,000; a last-attempt outreach to the 2-3 highest-value ones is worthwhile |
| Campaign reply rates are representative of future performance | The dataset covers 87 days of outreach; channel-level patterns are stable enough to project |

---

## 3. Detailed Calculations

### Funnel conversion rates (actual)

```
180 brands targeted
 └─ 60 qualified          33.3%
     └─ 58 opportunities  96.7% of qualified
         └─ 24 confirmed  41.4% of opportunities
              = 13.3% end-to-end conversion
```

### Campaign-level funnel (actual)

| Campaign | Reach | Replies | Reply Rate | Meetings | Opportunities | Confirmed | Revenue |
|----------|-------|---------|------------|----------|---------------|-----------|---------|
| Brand Discovery Email | 224 | 38 | 17% | 7 | 11 | 7 | ₹6,05,000 |
| Warm Partner Introductions | 10 | 9 | 90% | 8 | 9 | 7 | ₹6,05,000 |
| Brand Leader LinkedIn | 55 | 33 | 61% | 10 | 12 | 5 | ₹4,35,000 |
| Partner Interest Form | 18 | 18 | 100% | 13 | 7 | 5 | ₹3,95,000 |
| Creator Network Referrals | 22 | 21 | 95% | 15 | 9 | 6 | ₹5,10,000 |
| Past Conversation Revival | 44 | 12 | 27% | 7 | 10 | 4 | ₹2,90,000 |

### Base case projection

| Source | Deals | Expected value |
|--------|-------|---------------|
| Already confirmed | 24 | ₹22,40,000 |
| Negotiating (8 × 60%) | ~5 | ~₹4,32,000 |
| Proposal sent (6 × 35%) | ~2 | ~₹1,10,000 |
| **Base case total** | **~31** | **~₹27,82,000** |

### Stretch target projection

| Source | Deals | Expected value |
|--------|-------|---------------|
| Base case | ~31 | ~₹27,82,000 |
| Aggressive negotiating close (80%) | +1-2 | ~₹1,50,000 |
| Aggressive proposal close (55%) | +1 | ~₹80,000 |
| Re-engage 2 high-value lost deals | +1-2 | ~₹2,00,000 |
| Convert engaged brands (28 × 30% qual × 50% close) | ~4 | ~₹3,00,000 |
| **Stretch total** | **~35+** | **~₹35,00,000+** |

---

## 4. Data Sources

| Source | Description | Usage |
|--------|-------------|-------|
| `Sponsor Dataset.xlsx` (provided by RISA Labs) | 12 sheets covering event metadata, targets, 180 brands, 270 contacts, 6 campaigns, 953 interactions, qualification history, 58 opportunities, opportunity stage history, and 3 sponsor activations | All dashboard metrics, funnel calculations, and chatbot data |
| Dataset "Read Me" sheet | Confirms all data is synthetic/fictional | Noted; no real brand claims made |
| Dataset "Field Guide" sheet | Column definitions and join keys | Used to correctly aggregate by latest status per entity |
| Simulated data | Task board items, campaign budget/status fields | Clearly marked as editable/simulated in the management tab |

Monthly cumulative cash trend was derived by sorting confirmed partnerships by their opportunity history `effective_at` date into Jan/Feb/Mar/Apr buckets.

---

## 5. Prioritization Framework

**Framework: ICE (Impact, Confidence, Ease)** — each scored 1-10, summed for a total out of 30.

| Rank | Strategy | Impact | Confidence | Ease | Total | Why prioritize / deprioritize |
|------|----------|--------|------------|------|-------|-------------------------------|
| 1 | **Close Negotiating Deals** | 10 | 9 | 9 | **28** | Highest probability revenue; 8 deals worth ₹7.2L already in final stage. Pure execution — no new outreach needed. |
| 2 | **Alumni & Warm Intro Expansion** | 9 | 8 | 7 | **24** | 90% reply rate on introductions; each warm touch is worth 5× a cold email. Requires activating alumni network. |
| 3 | **LinkedIn ABM Targeting** | 8 | 8 | 7 | **23** | 61% reply rate, 12 opportunities generated. Target decision-makers at brands already in the engaged/unreviewed pool. |
| 4 | **Win-Back Lost High-Value Deals** | 7 | 5 | 6 | **18** | ₹7.8L in lost pipeline. Low confidence (brands said no) but Daybreak Studio (₹1.25L) and Evergreen Collective (₹1.35L) are worth one final attempt with revised terms. |
| 5 | **Inbound Content + Partner Form** | 6 | 6 | 5 | **17** | 100% reply rate on inbound but only 18 submissions over 87 days. Improving the partner form page and promoting it could lift volume, but ROI timeline is tight. |

**Deprioritized:** Cold email volume expansion — the 17% reply rate and 7 opt-outs suggest diminishing returns on more sends. Budget is better spent on warm channels.

---

## 6. Setup Instructions

The product is a single self-contained HTML file. No build step, no dependencies, no API keys.

### Option 1: Live site (recommended)

Visit **[shobhit-007.github.io/campusfest-2025-growth-center](https://shobhit-007.github.io/campusfest-2025-growth-center/)**

### Option 2: Open locally

```bash
# Just open the file in any modern browser
start growth-center/index.html        # Windows
open growth-center/index.html         # macOS
xdg-open growth-center/index.html    # Linux
```

### Option 3: Local HTTP server

```bash
cd growth-center
python -m http.server 8000
# Visit http://localhost:8000
```

No environment variables, no `.env` files, no package installation required.

---

## 7. Tools Used

| Tool | Purpose | Cost |
|------|---------|------|
| Claude Code (Claude Opus 4.6) | AI-assisted development — data analysis, dashboard generation, chatbot logic | Used via existing subscription |
| HTML / CSS / JavaScript | Application code — vanilla, zero external libraries | Free |
| Inline SVG | All charts rendered as SVG with hover tooltips | Free |
| Python + openpyxl | Dataset extraction and aggregation from `.xlsx` | Free |
| GitHub + GitHub Pages | Version control, hosting, deployment | Free |
| GitHub CLI (`gh`) | Repository creation and Pages configuration | Free |

**What was reused vs. built:**
- The entire `index.html` application was built from scratch for this assignment.
- No templates, UI frameworks, or chart libraries were used.
- Claude Code assisted with data extraction from the Excel file, structuring the embedded dataset, generating chart rendering functions, and writing the chatbot pattern-matching logic. All outputs were reviewed and verified against the source data.

---

## 8. Product Features

### Tab 1: Analytics Dashboard
- **5 hero KPI cards** — Total Cash Collected (₹22.4L), Confirmed Partners (24/28), Qualified Brands (60/55), Active Pipeline (₹10.5L), Win Rate (41%)
- **Sponsorship funnel** — Horizontal bar chart: 180 prospects → 60 qualified → 58 opportunities → 24 confirmed
- **Pipeline by stage** — Bar chart showing deal count and value at each stage
- **Campaign performance table** — All 6 campaigns with reach, replies, reply rate, meetings, opportunities, confirmed deals, and revenue
- **Revenue by campaign** — Bar chart comparison
- **Industry breakdown** — Confirmed deals grouped by sponsor industry
- **Cumulative cash trend** — Line chart showing monthly collection trajectory (Jan–Apr 2025)
- **Target vs Actual meters** — Visual progress bars for qualified brands and confirmed partnerships against revised targets

### Tab 2: Campaign Management
- **Campaign table** — Editable status (Active/Paused/Completed), budget, and notes per campaign
- **Kanban task board** — Three columns (To Do / In Progress / Done) with 10 pre-populated tasks
- **Task cards** — Each has title, owner, priority (color-coded), deadline, and movable status
- **Add Task modal** — Create new tasks with owner, priority, deadline assignment
- **Persistence** — All edits saved to localStorage

### Tab 3: Opportunity Tracker
- **Full table** — All 58 opportunities with brand, stage badge, proposed/confirmed values, owner, campaign, industry
- **Filters** — Dropdown filters for stage, campaign, and owner
- **Sortable columns** — Click headers to sort by brand, stage, value, or owner
- **Inline editing** — Edit stage and values via modal; changes persist to localStorage and immediately update all dashboard analytics
- **Summary KPIs** — Total opportunities, pipeline value, confirmed count, average deal size

### Tab 4: AI Growth Analyst (Chatbot)
- **20+ question patterns** handled with data-driven responses:
  - Overall performance and status summary
  - Total cash collected and revenue breakdown
  - Campaign ranking and comparison (e.g., "Compare email vs LinkedIn")
  - Active pipeline analysis and closing potential
  - Specific brand lookup (e.g., "Tell me about Beardo")
  - Priority recommendations and action items
  - Bottleneck diagnosis
  - Target tracking and projections
  - Industry analysis
  - Team/owner breakdowns
  - Deal size statistics
  - Win rate by campaign
- **Rich HTML responses** with data highlights, inline tables, and stage badges
- **Suggested questions sidebar** — 18 pre-written questions for quick access
- **Uncertainty handling** — Acknowledges when data cannot answer a question and lists what it can help with
- **Dynamic data** — Chatbot reads from the same data store as the dashboard, including any edits made in the Opportunities tab

---

## 9. Known Limitations

| Limitation | Impact | Mitigation |
|------------|--------|------------|
| **Chatbot is rule-based** | Covers ~20 patterns; misses complex or heavily paraphrased questions | Suggested questions sidebar guides users to supported queries; fallback response lists capabilities |
| **No backend or database** | Data embedded in JS; edits persist only in browser localStorage | Sufficient for demo; production would use Supabase or Firebase |
| **Charts are static SVG** | No animation, zoom, or drill-down | Hover tooltips provide detail; layout is clear at a glance |
| **Single HTML file** | All logic in one file (~1,260 lines) | Intentional for portability and zero-dependency deployment; would modularize for maintenance |
| **Monthly trend is approximated** | Cumulative cash per month estimated from opportunity confirmation dates | Noted in the chart; actual payment receipt dates are not in the dataset |
| **No authentication** | Anyone with the link can view and edit data | Acceptable for assignment demo; production would add auth |
| **localStorage is browser-specific** | Edits made in one browser are not visible in another | A backend database would solve this |

---

## 10. What I Would Improve

1. **LLM-powered chatbot** — Replace pattern matching with a Claude or Gemini API call, using the full dataset as context via RAG. This would handle arbitrary questions, follow-ups, and multi-step analysis.
2. **Supabase backend** — Persistent, multi-user database so the team shares one source of truth. Real-time sync across browsers.
3. **Notification system** — Email or Slack alerts when a deal changes stage, a deadline approaches, or a KPI crosses a threshold.
4. **Predictive deal scoring** — ML model trained on interaction history and qualification signals to predict close probability per opportunity.
5. **A/B test tracking** — Track message variants per campaign to optimize reply rates (especially for the 17% email channel).
6. **Export and reporting** — CSV export, PDF report generation, and scheduled email digests for stakeholders.
7. **Mobile-responsive refinement** — The current layout adapts to small screens but would benefit from a dedicated mobile task view.

---

## Repository

- **Source:** [github.com/Shobhit-007/campusfest-2025-growth-center](https://github.com/Shobhit-007/campusfest-2025-growth-center)
- **Live:** [shobhit-007.github.io/campusfest-2025-growth-center](https://shobhit-007.github.io/campusfest-2025-growth-center/)
