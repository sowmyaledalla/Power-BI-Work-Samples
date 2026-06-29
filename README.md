# Student Education Analytics — Power BI Dashboard

> A 3-page Power BI report analyzing student enrollments, graduation rates, and credits earned across Michigan, Ohio, and Washington from January 2019 to February 2021 — built to surface geographic and temporal patterns in student outcomes for education operations stakeholders.

---

## 📌 Project Summary

This dashboard was built to help education administrators monitor the full student journey across three U.S. states (MI, OH, WA) — from enrollment through graduation and academic credit completion. Each of the three report pages answers a distinct business question, using interactive visuals and embedded data narratives to surface actionable insights without requiring any SQL or data extraction.

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

### Page 1 — Student Enrollments
*Answers: Where are students enrolling, when, and how many?*

![Enrollments](./screenshots/Enrollments.png)

| Visual | Type | Purpose |
|--------|------|---------|
| Monthly Student Enrollments by State | Stacked Area Chart | Time-series enrollment trend broken down by MI, OH, WA |
| Total Enrollments by State | Donut Chart | State share of overall enrollment — WA 4,386 · MI 3,093 · OH 305 |
| Average Enrollment by Month (2019–21) | Clustered Column Chart | Seasonal patterns across all 12 months |
| Total Students Enrolled | KPI Card | **7,784** total enrollments |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **Washington (WA)** has the highest enrollments at **4,386**; **Ohio (OH)** has the lowest at **305**
- **June (414) and September (402)** record the highest average enrollment volumes
- **July (132) and August (165)** are the slowest months — reflecting academic calendar gaps
- Peak single month: **September 2019** at **511 students**

---

### Page 2 — Student Graduations
*Answers: How many students complete the program, and which states are most efficient?*

![Graduations](./screenshots/Graduations.png)

| Visual | Type | Purpose |
|--------|------|---------|
| Monthly Graduates by State | Stacked Area Chart | Graduation volume trend over time |
| Graduation Ratio by State | Column Chart | Graduates ÷ Enrollments — efficiency comparison across states |
| Total Graduations | Gauge | **109** shown (OH filtered) out of **1,730** total |
| Graduation Ratio Trend | Line Chart | Monthly ratio movement — reveals declining trajectory |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **1,730 graduates** from **7,784 enrollments** = **22% overall graduation ratio**
- Monthly graduations show a **declining trend** from Jan 2019 to Nov 2020
- **Washington** has the highest absolute graduation count
- **Ohio**, despite the lowest enrollment, has the highest graduation efficiency at **36%** — highest of all 3 states

---

### Page 3 — Credits Earned
*Answers: How much academic output are students producing, and where?*

![Credits Earned](./screenshots/Credits_Earned.png)

| Visual | Type | Purpose |
|--------|------|---------|
| Credits Earned by State | Area Chart | Monthly credit accumulation — WA dominates at 61% |
| Credits Earned by State | Donut Chart | WA 19.5K (61%) · MI 11.2K (35%) · OH 1.2K (4%) |
| Average Credits Earned per Student | Bar Chart | WA 4.7 · OH 4.0 · MI 3.9 |
| Credits Earned / Courses / Students | KPI Cards | **31.83K** credits · **340** courses · **7,279** students |
| State Postal Code | Slicer | Cross-filters all visuals dynamically |

**Key Findings:**
- **31,830 total credits** earned by **7,279 students** across **340 courses** (Jan 2019 – Feb 2021)
- **March 2020** recorded the highest aggregate credits earned in a single month
- **Washington** leads in average credits per student at **4.7**; Michigan at 3.9 and Ohio at 4.0

---

## 🧮 DAX Measures

| Measure | Logic | Business Use |
|---------|-------|--------------|
| `average Enrollment` | Average of monthly enrollment counts | Smooths volatility for seasonal comparison |
| `graduates` | Count of students who completed the program | Core graduation KPI |
| `Graduation Ratio` | `DIVIDE([graduates], [total enrollments])` | Efficiency metric — comparable across states regardless of size |
| `Credits earned per student` | `DIVIDE([total credits], [distinct students])` | Academic output benchmark per student |

---

## 💡 Skills Demonstrated

| Skill | Evidence in This Report |
|-------|------------------------|
| Multi-page report design | 3 pages with consistent layout, color theme, and navigation |
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
├── screenshots/
│   ├── Enrollments.png                  # Page 1 screenshot
│   ├── Graduations.png                  # Page 2 screenshot
│   └── Credits_Earned.png               # Page 3 screenshot
├── docs/
│   └── data_dictionary.md               # Field and measure definitions
└── README.md
```

---

## ⚙️ How to Open

1. Download `SowmyaLedalla_-_PowerBI_demo.pbix`
2. Open in **Power BI Desktop** (free — [download here](https://powerbi.microsoft.com/desktop/))
3. Navigate pages via the tab bar: **Enrollments → Graduations → Credits Earned**
4. Use the **State Postal Code slicer** to cross-filter all visuals by state (MI / OH / WA)

---

## 🛠️ Tech Stack

- **Tool:** Microsoft Power BI Desktop
- **Visuals:** Stacked area · Donut · Clustered column · Gauge · Line · Bar · Card · Slicer
- **Data Grain:** Monthly, by state
- **States:** Michigan (MI) · Ohio (OH) · Washington (WA)
- **Period:** January 2019 – February 2021
- **Domain:** Higher Education Analytics

---

## 👤 Author

**Sowmya Ledalla** — Senior Data Analyst | Power BI · SQL · Healthcare & Insurance Analytics  
[LinkedIn](#) | [Portfolio](https://neema-madayi-veetil-o7wk4b5.gamma.site/)
