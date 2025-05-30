CHURN ANALYSIS — SUBSCRIPTION RETENTION CASE STUDY  
Author: Ale Garay  
Project Type: Exploratory Data Analysis (EDA) • Strategic Insight Report  
Stack: Pandas • Matplotlib • Seaborn • SQL-ready logic • Markdown Narrative  
Use Case: Internal-style churn report for a fictional SaaS business. Focused on cohort analysis, segmentation, and actionable hypotheses.  
Status: Static analysis for portfolio. No modeling.
________________

TABLE OF CONTENTS
* Project Purpose  
* Dataset Overview  
* Analysis Flow  
* Segment Definitions  
* Cohort Logic  
* Strategic Insights  
* Reproducibility  
* Status and Limitations  
* Design Principles  
________________

PROJECT PURPOSE  
This is a production-minded churn analysis designed to simulate what a real Data Analyst might deliver to a Product or Strategy team.  
The goal is not prediction — it’s explanation. What user segments churn more? What patterns emerge by plan, tenure, or geography?  
The final output is a clear, insight-driven narrative built from SQL-style thinking and EDA.

________________

DATASET OVERVIEW  
Dataset: Telco Customer Churn (public source)  
Rows: ~7000  
Key fields:
* `customerID`, `tenure`, `Contract`, `MonthlyCharges`, `TotalCharges`, `PaymentMethod`
* Categorical features around internet service, online security, add-ons
* Binary churn indicator: `Churn`

This dataset mimics a subscription SaaS product with monthly vs annual contracts and varied usage profiles.

________________

ANALYSIS FLOW  
1. Define churn logic and segment the user base  
2. Analyze churn by plan type, tenure, and customer behavior  
3. Explore cohort patterns and visualize churn over time  
4. Extract hypotheses about root causes  
5. Draft strategic suggestions for product or growth decisions

________________

SEGMENT DEFINITIONS  
Key segments explored:
* Contract type (Monthly / One / Two Year)
* Tenure buckets (0–6, 6–12, 12–24, 24+ months)
* Add-on services (Online Security, Tech Support, etc.)
* Payment method and paperless billing
* Demographics (SeniorCitizen, Partner, etc.)

________________

COHORT LOGIC  
Cohorts based on `tenure` as a proxy for account age  
Retention curves and churn rates calculated across tenure bins

________________

STRATEGIC INSIGHTS  
Sample findings:
* Monthly contracts show 3x higher churn than annual ones  
* Users with no add-ons churn significantly more  
* Paperless billing users have marginally higher retention  
* Senior users on two-year contracts show the highest stickiness  

All insights are supported with visual evidence and written as stakeholder-facing hypotheses.

________________

REPRODUCIBILITY  
Notebook contains:
* Clean loading and preprocessing steps  
* Inline commentary and assumptions  
* Deterministic outputs (no random seed dependency)  
* SQL-ready transformations when applicable

No modeling, pipelines or automation — this is a static EDA artifact.

________________

STATUS AND LIMITATIONS  
This project is not meant to be predictive  
No causal inference or modeling is performed  
Simulated business framing over a public dataset  
Assumptions are made for clarity and communication

________________

DESIGN PRINCIPLES  
* Insight > Technique  
* Communication > Code  
* Every cell should justify its place  
* Notebooks are for stakeholders, not just analysts  
* Code clarity and visual storytelling are treated as first-class concerns
