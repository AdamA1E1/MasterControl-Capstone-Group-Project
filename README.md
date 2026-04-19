# MasterControl-Capstone-Group-Project
MasterControl Capstone Group Project

## Project Overview

MasterControl provides quality (Qx) and manufacturing (Mx) management software to life sciences companies. The Mx product, launched ~4 years ago, significantly underperforms the established Qx product (12.7% vs 19.7% lead progression). With limited sales resources, the company needs a data-driven way to identify which leads are most likely to progress, especially for Mx.

This project builds predictive models to help sales teams prioritize high-potential opportunities and close the performance gap between products.

## Business Problem

**Challenge:** Mx leads convert at only 12.7% compared to Qx at 19.7%. Sales teams waste time on low-potential leads while missing opportunities that could convert.

**Goal:** Build a model that identifies leads most likely to progress (SQL, SQO, or Won), enabling targeted outreach and improved resource allocation.

## Key Findings

### What Works Best
- **High-intent actions drive conversion:** Pricing page visits (58% for Mx, 50% for Qx) and demo requests (25–32%) are the strongest signals. Call these leads first.

- **Mx has a clear target profile:** Small-to-mid-sized Medical Device and Biologics companies in the Americas, with Quality or Engineering roles, show the highest conversion (~16%).

- **Organic channels outperform paid:** SEO and Direct/Inbound convert at 24–31% for both products. Online Ads for Mx lag at 19%.

### The Performance Gap
Qx outperforms Mx by 55% (7 percentage points). This gap reflects Mx's newer market presence, but targeted outreach can close it.

### Data Quality Opportunity
40% of records are missing critical fields such as job titles and site function. Leads with missing data convert at much lower rates. Making these fields required at sign-up would have an immediate impact.

## Model Performance

| Model | Test AUC | Business Value |
|-------|----------|----------------|
| Random Forest | 0.855 | **Selected: **  best overall performance |
| XGBoost | 0.838 | Strong alternative |
| Logistic Regression | 0.829 | Solid baseline |

At the recommended threshold (0.60), the model captures **72% of leads that would progress:** meaning the sales team can focus on the most promising opportunities without missing most real converts.

## Recommendations

1. **Prioritize by intent** — Route pricing page visitors and demo requesters to sales immediately. These convert far above average.

2. **Target Mx specifically** — Focus on Medical Device/Biologics companies in the Americas, targeting Quality and Engineering roles.

3. **Shift channel investment** — Reallocate budget from Online Ads to SEO and Direct/Inbound for better Mx ROI.

4. **Fix data collection** — Make job title and site function required fields at lead capture to improve future model performance.

## Repository Structure

```
├── README.md                                    # This file
├── MasterControl_Modeling_Final.html            # Exploratory data analysis, Modeling, and evaluation
├── MasterControl_Presentation.pdf               # Final slide deck
└── data/                                        # Not included (data not shared publicly)
```

## Team

Adam Edwards, An Lee, Brian Frerichs, Kun Joo Cho

## Sponsor

MasterControl — quality and manufacturing management software for life sciences
