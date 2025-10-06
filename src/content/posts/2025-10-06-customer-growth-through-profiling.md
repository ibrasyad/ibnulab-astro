---
title: Customer Growth through Profiling
published: 2024-11-17T09:00:00
updated: ''
draft: false
description: This is a clustering analysis focusing on understanding our customer. It was using a public dataset from BigQuery as a learning project.
image: /assets/images/cover profiling.jpg
tags:
  - Project, Python, Analysis, Customer Segmentation, K-Means, Ecommerce
category: Project
lang: ''
pinned: false
author: M. Ibnu Rasyad
sourceLink: ''
licenseName: CC BY 4.0
licenseUrl: https://creativecommons.org/licenses/by/4.0/
encrypted: false
password: ''
---
## Introduction

In 2023, TheLook Ecommerce experienced remarkable growth in gross merchandise value (GMV), reaching nearly $3 million, a fivefold increase from the previous year. This success was reflected in the exponential rise in the number of transactions and customer base expansion. However, this growth masked a concerning trend—customer acquisition was slowing down. By the end of 2023, the company saw a 24.43% decline in customer acquisition, with the second half of the year showing a sharp drop of up to 50%. This alarming trend posed a significant challenge: how to sustain business growth when the influx of new customers was dwindling.

Read the summary below or visit the full report [here](https://docs.google.com/presentation/d/1G_4Q6J5wm3tIFckUGJes5LKb_MupIr_t71eNmy4eQmM/edit?usp=sharing)

## Segmenting the Customer Base

To address this challenge, the analysis focused on understanding customer profile and behavior through segmentation. Four distinct customer groups were identified:

- **VVIP:** This group, representing only 5% of the customer base, contributed a significant 23% of the total GMV. These top spenders are the most valuable customers.
- **Premier:** Comprising 22% of customers, this group had better spending power than average customers and accounted for 38% of the GMV.
- **Majority:** The largest segment, making up 49% of the customer base, contributed 25% of the GMV. This group had high transaction volumes but lower average revenue per user (ARPU).
- **Churned:** These customers, who had not made a purchase in over a year, represented 22% of the customer base and contributed 12% of the GMV.

The segmentation was achieved through clustering analysis, considering metrics such as GMV, ARPU, transaction history, and other behavioral data. The goal was to identify patterns within these groups to tailor strategies that could boost customer retention and acquisition.

## Key Findings and Behavioral Insights

The analysis revealed significant behavioral shifts in 2023. The "Majority" group saw a spike in activity and GMV, while the "Churned" group continued to decline. It was hypothesized that a business change in late 2022 or early 2023 might have contributed to these shifts—attracting more activity from the "Majority" while losing interest from the "Churned."

The impact analysis showed that focusing on specific customer groups could lead to measurable improvements in GMV. Targeting the VVIP and Premier segments was projected to increase GMV by 3.11%, while efforts to engage the Majority and Churned groups could yield additional increases of 1.27% and 0.63%, respectively.

## Strategic Focus Areas

Given these findings, the analysis recommends a multi-faceted approach to drive growth:

- **Prioritize Top Customers:** Focus on the VVIP and Premier groups to secure a substantial portion of GMV with relatively low effort. These customers are already high spenders, and nurturing their loyalty could yield significant returns.
- **Engage the Majority:** While they contribute less per transaction, the Majority group is large and active. Maintaining their engagement and encouraging incremental spending could provide steady growth.
- **Reactivate Churned Customers:** Though they currently represent a smaller portion of GMV, re-engaging Churned customers could be worthwhile. Even a small percentage of reactivation could lead to a meaningful increase in revenue.

## Conclusion

In conclusion, while TheLook Ecommerce has enjoyed substantial growth, the slowing rate of customer acquisition requires immediate attention. By understanding and segmenting the customer base, the company can implement targeted strategies that not only retain high-value customers but also re-engage those who have lapsed.
