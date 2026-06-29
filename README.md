# Student Education Analytics — Power BI Dashboard

> A 3-page Power BI report analyzing student enrollments, graduation rates, and credits earned across U.S. states from January 2019 to February 2021 — built to surface geographic and temporal patterns in student outcomes for education operations stakeholders.

---

## 📌 Project Summary

This dashboard was built to help education administrators monitor the full student journey across three U.S. states — from enrollment through graduation and academic credit completion. Each of the three report pages answers a distinct business question, using interactive visuals and embedded data narratives to surface actionable insights without requiring any SQL or data extraction.

The report covers **7,784 student enrollments**, **1,730 graduates**, and **~32,000 credits earned** across **340 courses** over a two-year period, with state-level filtering throughout.

---

## 📌 Business Problem

Education administrators lack consolidated visibility into enrollment trends, graduation performance, and academic credit completion across states and time periods. Without a unified report:

- Seasonal enrollment patterns go undetected until capacity is strained
- Underperforming states on graduation rates are not flagged early
- Per-student academic output cannot be benchmarked across regions
- Reporting requires manual data pulls instead of self-service dashboards

---

## 📊 Report Pages

### Page 1 — Enrollments
*Answers: Where are students enrolling, when, and how many?*

| Visual | Type | Purpose |
|--------|------|---------|
| Monthly Student Enrollments by State | Stacked Area Chart | Time-series enrollment trend broken down by state |
| Total Enrollments by State | Donut Chart | State share of overall enrollment volume |
| Average Enrollment by Month (2019–21) | Clustered Column Chart | Seasonal patterns — which months peak and trough |
| Total Enrollment Count | KPI Card | Single top-line enrollment metric |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **Washington (WA)** has the highest enrollments; **Ohio (OH)** has the lowest
- **June and September** consistently record the highest average enrollment volumes
- **July and August** are the slowest months — likely reflecting academic calendar gaps
- Peak single month: **September 2019** at **511 students**

---

### Page 2 — Graduations
*Answers: How many students complete the program, and which states are most efficient?*

| Visual | Type | Purpose |
|--------|------|---------|
| Monthly Graduates by State | Stacked Area Chart | Graduation volume trend over time by state |
| Graduation Ratio by State | Column Chart | Graduates ÷ Enrollments — efficiency comparison across states |
| Total Graduations | Gauge | Actual graduation count vs. target benchmark |
| Graduation Ratio Trend | Line Chart | Monthly ratio movement — reveals declining trajectory |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **1,730 graduates** from **7,784 enrollments** = **22% overall graduation ratio**
- Monthly graduations show a **declining trend** from Jan 2019 to Nov 2020 — a signal worth investigating
- **Washington** has the highest absolute graduation count, consistent with its enrollment lead
- **Ohio**, despite the lowest enrollment, has the highest graduation efficiency at **36%** — a counterintuitive finding that suggests stronger program completion rates or a different student profile

---

### Page 3 — Credits Earned
*Answers: How much academic output are students producing, and where?*

| Visual | Type | Purpose |
|--------|------|---------|
| Credits Earned by State | Area Chart | Monthly credit accumulation trend by state |
| Credits Earned by State | Donut Chart | State share of total credits |
| Average Credits Earned per Student | Bar Chart | Per-student academic output benchmarked by state |
| Total Credits / Students / Courses | KPI Cards (3) | Top-line volume metrics at a glance |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **~32,000 total credits** earned by **7,279 students** across **340 courses** (Jan 2019 – Feb 2021)
- **March 2020** recorded the highest aggregate credits in a single month
- **Washington** leads in average credits per student at **4.7** — the highest of all states

---

## 🧮 DAX Measures

| Measure | Logic | Business Use |
|---------|-------|--------------|
| `average Enrollment` | Average of monthly enrollment counts | Smooths volatility for trend comparison |
| `graduates` | Count of students who completed the program | Core graduation KPI |
| `Graduation Ratio` | `DIVIDE([graduates], [total enrollments])` | Efficiency metric — comparable across states regardless of size |
| `Credits earned per student` | `DIVIDE([total credits], [distinct students])` | Academic output benchmark per student |

---

## 💡 Skills Demonstrated

| Skill | Evidence in This Report |
|-------|------------------------|
| Multi-page report design | 3 pages with consistent layout, color, and navigation |
| DAX measure development | 4 custom measures including ratio and average calculations |
| Visual selection judgment | 7 chart types chosen to match the analytical question per visual |
| Data storytelling | Embedded insight narratives on each page with specific data callouts |
| Interactivity | State slicer cross-filters all visuals on every page |
| Comparative analysis | State benchmarking across enrollment, graduation ratio, and credits per student |

---

## 🗂️ File Structure

```
Student_Education_Analytics/
├── SowmyaLedalla_-_PowerBI_demo.pbix   # Power BI report file
├── docs/
│   └── data_dictionary.md               # Field and measure definitions
├── screenshots/
│   └── (add page screenshots here)
└── README.md
```

---

## ⚙️ How to Open

1. Download `SowmyaLedalla_-_PowerBI_demo.pbix`
2. Open in **Power BI Desktop** (free — [download here](https://powerbi.microsoft.com/desktop/))
3. Navigate pages via the tab bar at the bottom: **Enrollments → Graduations → Credits Earned**
4. Use the **State Postal Code slicer** on any page to cross-filter all visuals

---

## 🛠️ Tech Stack

- **Tool:** Microsoft Power BI Desktop
- **Visuals:** Stacked area · Donut · Clustered column · Gauge · Line · Bar · Card · Slicer
- **Data Grain:** Monthly, by state
- **Period:** January 2019 – February 2021
- **Domain:** Higher Education Analytics

---

## 👤 Author

**Sowmya Ledalla** — Senior Data Analyst | Power BI · SQL · Healthcare & Insurance Analytics  
[LinkedIn](#) | [Portfolio](https://neema-madayi-veetil-o7wk4b5.gamma.site/)
