# Online-Shopping-Intention-Data-Analyst
A data analytics project exploring what separates purchasing sessions from non-purchasing sessions on an e-commerce site, and translating those differences into evidence-based UX and conversion-rate strategy.

Business Question
What behavioral patterns distinguish purchasing sessions from non-purchasing sessions, and which factors represent the greatest opportunity to improve conversion?

Dataset
Online Shoppers Purchasing Intention Dataset (UCI Machine Learning Repository)


12,330 rows · 19 columns
Session-level browsing behavior (Administrative, Informational, ProductRelated pages/durations), website metrics (BounceRates, ExitRates, PageValues), visitor/traffic attributes (VisitorType, TrafficType, Region, Month), and the outcome variable Revenue (purchase completed: True/False).


Project Structure
├── README.md                                  → this file
├── online_shoppers_conversion_report.md       → full written analysis: business understanding,
│                                                 EDA approach, executive summary, cross-dashboard
│                                                 synthesis, strategic recommendations, limitations
├── bounceRate_vs_exitRate.html                 → dashboard: bounce rate vs. exit rate by purchase outcome
├── visitor_type_dashboard.html                 → dashboard: visitor type composition, purchase vs. no purchase
├── productType_dashboard.html                  → dashboard: page-type engagement and the conversion "dead zone"
└── online_shoppers_conversion_dashboard.html   → dashboard: integrated purchase vs. non-purchase comparison
                                                   across all five behavioral metrics, ranked by Gap Index

Methodology
Data cleaning — validated data types, checked for missing/duplicate records (none found), reordered Month chronologically.
Comparative analysis — compared purchasing vs. non-purchasing sessions across four dimensions: Page Type, Bounce Rate vs. Exit Rate, Visitor Type, and an integrated cross-metric comparison.
Gap Index — a custom normalized score (100 − min/max × 100) used to rank every metric by how strongly it separates the two outcome groups, independent of each metric's original unit.
Dashboards — four interactive HTML dashboards built to visualize each dimension and support the written recommendations.


Key Findings
Page Value shows the widest gap between purchasing and non-purchasing sessions (13.8×), but — because it's calculated from completed transactions — it's a diagnostic signal, not an independent lever.
Conversion is threshold-gated: purchase rate stays near 0% through Low/Medium ProductRelated engagement and only rises sharply (~16–17%) once sessions reach the High-engagement band.
Bounce/Exit Rate separate the groups clearly (0.07 vs. up to 0.20), though part of that gap is structural rather than purely behavioral.
Returning Visitors drive ~77% of purchases (the volume opportunity); New Visitors convert disproportionately well relative to their traffic share (the efficiency opportunity) — the two segments need different interventions.


See online_shoppers_conversion_report.md for the full write-up, including caveats on causality and a prioritized recommendation table.

Limitations
The dataset is static, session-level (not customer-level), and purely observational — all relationships are correlational and should be validated through A/B testing before being treated as proven drivers of conversion. See the report's Limitations section for the full list.

Tools

HTML / CSS / Chart.js for dashboards · Markdown for the written report.
