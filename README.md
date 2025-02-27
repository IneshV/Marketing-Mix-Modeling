# Marketing-Mix-Modeling

1. Project Background

This project is an attempt to gain experience in data science consulting by exploring Marketing Mix Modeling. The goal is to understand how advertising spend across various channels impacts overall sales. Finding a suitable dataset was challenging; I discovered a realistic dataset on Kaggle, although much of the meta-information is missing. We don’t know whether the data is real or synthetic, or even what specific product is being sold. However, we do have information on the marketing budget and total sales, which is enough to get started practicing and refining our analytical skills.

2. Datastructure and Overview

The dataset consists of 5 columns:

Date: The date of each observation.
TikTok: Advertising spend on TikTok (in dollars).
Facebook: Advertising spend on Facebook (in dollars).
Google Ads: Advertising spend on Google Ads (in dollars).
Sales: Total sales revenue (in dollars).
All monetary values are assumed to be in dollars. The data is organized over time, allowing us to investigate trends and relationships between ad spend and sales.

3. Executive Summary

The analysis aims to quantify how advertising spend on TikTok, Facebook, and Google Ads affects overall sales.
Key findings include:

Google Ads appears to have the strongest effect on sales per dollar spent.
Facebook also shows a significant impact, while TikTok has a comparatively smaller effect.
The overall model explains a significant portion of the variance in sales, providing actionable insights for marketing budget allocation.
Below is the graph summarizing these insights:



For further details, review the code in the following files:

main.py
graph.py
4. Insights Deep Dive

Modeling Approach:
Both Linear Regression and Bayesian Ridge Regression were applied to understand the direct effect of ad spend on sales.
The regression coefficients indicate that a unit increase in Google Ads spend yields a higher sales increase compared to Facebook and TikTok.
Time-series cross-validation ensured that model evaluation respected the chronological order, though for this analysis we assume direct effects without temporal dependencies.
Data Trends:
Exploratory analysis revealed that sales generally follow changes in marketing spend. Seasonal or sporadic variations exist, but the overall trends support the regression findings.
Statistical Inference:
The regression analysis provides p-values and confidence intervals (available in the detailed model outputs), offering insights into the significance and reliability of each channel’s impact.
5. Recommendations

Budget Reallocation:
Given that Google Ads exhibits the strongest effect on sales, consider increasing the budget allocation to Google Ads while monitoring the impact on overall sales.
Data Enrichment:
Future projects should consider adding more granular data (e.g., lagged effects, additional marketing channels, external economic indicators) to refine the model and capture delayed effects.
Further Analysis:
Explore advanced techniques such as causal inference methods and alternative time-series models if more detailed temporal dynamics need to be captured.
Continued Monitoring:
Maintain and update the model as more data becomes available to ensure the insights remain valid over time.
