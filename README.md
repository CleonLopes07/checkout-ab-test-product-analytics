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
