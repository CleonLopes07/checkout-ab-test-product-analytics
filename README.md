🧪 A/B Testing Analysis – Checkout Flow Optimization

📌 Project Overview

This project presents an end-to-end A/B testing analysis conducted to evaluate a redesigned checkout flow for a multi-category e-commerce platform. The goal was to determine whether simplifying the checkout experience could reduce user drop-off and increase completed purchases, while ensuring no negative impact on key business guardrails.

The project simulates a real-world product experimentation workflow using large-scale event data, statistical rigor, and business-focused insights.

🎯 Business Problem

A significant proportion of users enter the checkout flow but fail to complete their purchase, leading to lost revenue and inefficient conversion.

Hypothesis:
A simplified checkout flow with fewer steps and clearer UI will improve checkout completion rates compared to the existing flow.

🧪 Experiment Design Summary

Experiment Type: Controlled A/B Test

Variants:

Variant A (Control): Existing checkout flow

Variant B (Treatment): Redesigned, simplified checkout flow

Unit of Analysis: Session-level checkout sessions

Randomization: Deterministic hashing-based assignment

Sample Size:
~870,000+ checkout entries per variant

Power & MDE:
Powered to detect a +2 percentage point absolute uplift with 80% power at α = 0.05

📊 Metrics Used
Primary Metric

Checkout Conversion Rate
Completed Checkouts ÷ Entered Checkouts

Secondary Metrics

Funnel progression (views → cart → purchase)

Session engagement (events per session)

Guardrail Metrics

Revenue per session

Revenue per user

Bounce rate (approx.)

Sessions per user

📈 Key Results

Variant B achieved a statistically significant uplift in checkout conversion compared to Variant A.

The uplift was validated using:

Two-sample z-test for proportions

95% confidence intervals

Effect size estimation (Cohen’s h)

Sample Ratio Mismatch (SRM) checks confirmed valid randomization.

Guardrail metrics showed no material degradation in revenue or engagement.

Results were consistent across multiple segments:

Product categories

Price bands

Session duration buckets

New vs returning users

Logistic regression confirmed the treatment effect after controlling for key covariates.

💼 Business Impact

The redesigned checkout flow demonstrates a clear opportunity to:

Increase completed purchases

Improve conversion efficiency

Drive incremental revenue at scale without harming user experience

Recommendation:
Roll out the redesigned checkout flow (Variant B) to all users, with continued monitoring of guardrail metrics post-launch.

🛠️ Tools & Technologies

Languages: Python

Libraries: Pandas, NumPy, SciPy, Statsmodels, Matplotlib, Plotly

Environment: Google Colab

Storage: Parquet

Documentation: Word / PDF

Version Control: GitHub

🗂️ Repository Structure
checkout-ab-test-product-analytics/
│
├── notebooks/
│   └── AB_Testing.ipynb
│
├── figures/
│   └── *.png
│
├── docs/
│   ├── Feature_Documentation.docx
│   ├── Experiment_Design_Document.docx
│   ├── Data_Dictionary.docx
│   ├── Metric_Definitions.docx
    ├── Architecture workflow and diagram document.docx 
│   └── Executive_Summary.docx
│
├── data/
│   └── DataREADME.md
│
└── README.md

📂 Data Availability

The original raw event dataset (~8GB) is not included due to storage constraints.

Analysis is fully reproducible using the processed session-level dataset:

sessions_with_segments_fixed.parquet

All feature engineering, aggregation, and experiment logic are documented in the notebook.

▶️ How to Run the Analysis

Clone the repository:

git clone https://github.com/CleonLopes07/checkout-ab-test-product-analytics/


Open the notebook in Jupyter or Google Colab:

notebooks/AB_Testing_Checkout_Flow.ipynb


Ensure required Python libraries are installed.

Run cells sequentially to reproduce the analysis.

⚠️ Limitations

Experimental outcomes are simulated rather than generated from live production traffic.

Multiple sessions per user may introduce correlation.

External factors such as seasonality or promotions are not modeled.

🚀 Future Improvements

Validate results using a live production A/B test.

Explore personalized checkout flows by user segment.

Extend analysis to long-term retention and lifetime value (LTV).

👤 Author

Cleon
Aspiring Product Analyst / Data Analyst
Focused on experimentation, product metrics, and data-driven decision-making.

🏷️ Tags

ab-testing · product-analytics · experiment-design · statistics · python · data-analysis
