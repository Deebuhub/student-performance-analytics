# Student Performance Analytics System
A data analytics internship project analyzing academic performance for 15,000 students to identify what actually drives outcomes — and to flag at-risk students for early intervention.

**Built for:** Data Analytics Internship · **Institute:** Sipalaya Infotech
**Dataset source:** [Student Performance Dataset — Kaggle](https://www.kaggle.com/)
**By:** Dibesh Shrestha

## Objective
Analyze student academic performance and identify the factors affecting grades, attendance, and outcomes, in order to flag at-risk students early.

## Project Phases

Raw file: 25,000 rows × 16 columns. After cleaning: **15,000 unique students**.

- **Phase 1:** Data Cleaning (duplicates, nulls, outliers, format fixes)
[
- Removed 10,000 exact duplicate student records
- Standardized inconsistent text casing across categorical columns
- Enforced correct data types
- Checked for outliers using the IQR method (none required removal — scores already bounded 0–100)
- Confirmed zero missing values
]

- **Phase 2:** EDA (visualizations — heatmaps, pairplots, boxplots)
[
Investigated:
- Does attendance affect marks? *(weak-moderate positive relationship, r ≈ 0.29)*
- Does family/parental background affect performance? *(minimal impact, <1 point difference between groups)*
- Does internet access improve scores? *(negligible difference)*
- Which students are at risk? *(11.9% flagged)*

Visualizations: correlation heatmap, histograms, pairplot, boxplots, regression scatter plots — all in `reports
]

- **Phase 3:** Feature Engineering (average score, risk category, performance level)
[
New columns created:
- `average_score` — mean of the three subject scores
- `risk_category` — At Risk / Needs Improvement / Safe
- `performance_level` — Low / Medium / High
]

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Deliverables

| Deliverable | Location |
|---|---|
| Cleaned dataset | `data/cleaned_data.csv` |
| Chart images | `reports/` |

## Key Findings
- Higher attendance correlates positively with final marks

## How to Run
1. Clone this repo
2. Install requirements: `pip install pandas numpy matplotlib seaborn jupyter`
3. Open `notebooks/student_analysis.ipynb` in Jupyter

## Project Structure

```
student-performance-analytics/
├── data/
│   ├── Student_Performance.csv
│   └── cleaned_data.csv
├── notebooks/
│   └── student_analysis.ipynb
├── reports
└── README.md
```

*Submitted as part of the Data Analytics Internship program at Sipalaya Infotech.*
