# Exploratory Data Analysis of Digital Advertising Campaigns

## Dataset Overview

This project analyzes a comprehensive dataset containing information on digital video advertising campaigns from 26 advertiser accounts, spanning a one-year period between 2021 and 2022. The dataset consists of 237,409 records and 51 columns in Spanish, covering a wide array of campaign performance metrics such as impressions, clicks, conversions, costs, and revenue. The data was obtained from [Zenodo](https://zenodo.org/records/7965793).

Due to limited documentation, column meanings were inferred based on naming conventions, and additional columns—such as *ROAS_calculated*—were created to enrich the analysis. While the dataset is synthetic and features an uneven distribution, normalization techniques were applied to improve its quality and usability for analysis.

## Objective

The primary goal of this project is to extract actionable insights that help advertisers optimize their campaigns. By using exploratory data analysis (EDA), visualization, and basic statistical techniques, this study investigates how variables like time, investment, device, and location influence return on advertising spend (*ROAS*) and overall performance.

## Methodology

Data preparation included cleaning missing or irrelevant columns, converting data types, and generating new variables such as calculated ROAS. Outliers were filtered based on the 1st and 99th percentiles to improve the accuracy of trend identification. Key numerical and categorical variables were selected to answer strategic questions, such as:

- Which days yield the highest ROAS?  
- Is there a link between campaign investment and ROAS?  
- What devices drive the most conversions?  
- Do some product categories perform better in certain countries?

## Key Findings

One of the first insights derived from the analysis was the role of the *day of the week* in campaign performance. *Tuesdays and Wednesdays* consistently showed higher average ROAS values, suggesting that midweek may be more effective for digital advertising. However, an ANOVA test indicated that these differences were *not statistically significant*, implying that day-based trends should be interpreted with caution and not relied upon as a sole strategic factor.

When exploring the relationship between *final campaign cost and ROAS*, a counterintuitive pattern emerged. Higher investment did not necessarily lead to better returns. In fact, the data revealed a *weak negative correlation* between cost and ROAS, indicating that while expensive campaigns can generate high revenues, they don’t always produce proportionally higher returns. This highlights the importance of focusing not just on budget size but on the *efficiency and targeting quality* of the campaign.

Regarding *device usage*, *Desktop* emerged as the dominant device in terms of conversions, significantly outperforming Smartphones and Tablets. Despite this, the ROAS associated with Desktop conversions was generally lower, suggesting that high conversion volume doesn’t automatically translate to high profitability. Mobile devices, although less effective overall, showed sporadic high-performing campaigns, indicating that they may benefit from further optimization.

Geographical and categorical analysis showed that certain *product categories perform significantly better in specific countries*. For example, *HostedDataStorage* and *AttorneysLawFirms* in the United States demonstrated superior ROAS compared to the same categories in other countries. This finding underscores the importance of tailoring campaign strategies to specific markets, aligning product offerings with regional demand and behavior.

## Challenges

Several challenges were addressed during the analysis. First, many percentage-based metrics were stored as text strings, requiring conversion into decimal format for accurate computation. Additionally, inconsistencies in the *ROAS_f* column led to the development of a new variable, *ROAS_calculated*, which was computed using revenue and final cost. Outliers presented another issue, as extreme values distorted the distributions; this was resolved by filtering data outside the 1st and 99th percentiles, resulting in clearer and more reliable insights.

## References

- [Dataset Source (Zenodo, 2023)](https://zenodo.org/records/7965793)  
- Charalabides, S., National College of Ireland – Data Analysis & Visualization Lectures (2024)  
- Dholakia, R. R. & Bagozzi, K. M., *Journal of Interactive Marketing* (2020)  
- Google Think Insights: [Understand customer needs](https://www.thinkwithgoogle.com/consumer-insights/consumer-journey/understand-customer-needs/)
