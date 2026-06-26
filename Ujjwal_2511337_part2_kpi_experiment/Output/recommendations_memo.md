# Business Problem Summary

The company tested a new onboarding and activation campaign to determine whether it should replace the existing onboarding experience. Users were divided into Control and Treatment groups to evaluate the impact of the new campaign on user conversion and early engagement.

The decision affects users, product teams, growth and marketing teams, and business stakeholders. The primary objective is to improve conversion while maintaining a positive user experience and supporting long-term business growth.

Before recommending a full rollout, the experiment results must demonstrate that the Treatment Group performs better than the Control Group on the primary success metric. In addition, guardrail metrics such as retention, churn, and engagement quality should remain stable or improve to ensure that any gains are sustainable.

The final recommendation will be based on the overall business impact of the treatment, balancing potential benefits against associated risks.

# North Star Metric Summary

The selected North Star Metric for this experiment is **Paid Conversion Rate**, calculated as the percentage of users who convert into paying customers after experiencing the onboarding process. This metric was chosen because it directly measures the primary business objective of the experiment and reflects the company's ability to generate revenue from acquired users.

Metrics such as Trial Start Rate, Onboarding Completion Rate, Engagement Score, and Revenue are considered supporting metrics. These metrics help explain user behavior and identify factors influencing conversion, but they do not directly measure the experiment's core success.

Paid Conversion Rate is closely linked to business growth because higher conversion leads to more paying customers, increased subscription revenue, and improved customer acquisition efficiency. However, it should not be optimized in isolation. Guardrail metrics such as Engagement Score, Support Tickets, Refund Requests, and Days to Convert must also be monitored to ensure that any increase in conversions is sustainable and does not negatively impact the user experience.

# Task 8: Guardrail Metrics Evaluation

The Paid Conversion Rate improved from **3.17%** in the Control group to **6.99%** in the Treatment group. However, the campaign should not be evaluated based only on conversion improvement. Additional guardrail metrics were reviewed to identify any potential business risks.

### 1. Refund Rate

* **Control:** 0.00%
* **Treatment:** 0.42%

The refund rate increased slightly in the Treatment group. Although the increase is small, it indicates that a few users requested refunds after converting. This should be monitored during future rollouts.

### 2. Support Ticket Rate

* **Control:** 14.72%
* **Treatment:** 24.76%

The support ticket rate increased significantly after the new onboarding experience. This suggests that more users required assistance, which could increase customer support costs and negatively affect the overall user experience.

### 3. Average Days to Convert

* **Control:** 8.86 days
* **Treatment:** 6.40 days

Users in the Treatment group converted more quickly than those in the Control group. A shorter conversion time is a positive outcome because users reached the paid subscription stage faster.

### 4. Average Engagement Score

* **Control:** 57.03
* **Treatment:** 62.93

The Treatment group achieved a higher engagement score, indicating that users interacted more actively with the product after the new onboarding experience.

### 5. Revenue Quality

* **Average Revenue per User:** Increased from **51.75** to **53.88**
* **Average Revenue per Converted User:** Decreased from **1630.10** to **770.41**

Although overall revenue per user improved slightly, the revenue generated from each converted customer decreased substantially. This suggests that the increase in conversions did not translate into proportionally higher revenue from paying customers.

## Risk Assessment

The Treatment group delivered better conversion, engagement, and faster user activation. However, the increase in support ticket rate and the decline in average revenue per converted user indicate potential business risks. These guardrail metrics should be monitored and optimized before a full-scale rollout of the new onboarding campaign.


# Recommendation Memo

## Executive Summary

This report evaluates the performance of the new onboarding and activation campaign by comparing the Treatment group with the existing onboarding experience (Control group). The primary objective was to determine whether the new onboarding process should be launched to all users based on business performance, user behavior, and overall experiment results.

The Treatment group achieved a higher Paid Conversion Rate, better user engagement, and faster conversion. However, an increase in support tickets and a decline in average revenue per converted user indicate that further improvements are needed before a full rollout.

---

# North Star Metric

The North Star Metric for this experiment is **Paid Conversion Rate**.

This metric directly measures the percentage of users who become paying customers after experiencing the onboarding process. Improving paid conversion contributes directly to subscription growth and long-term business revenue.

**Results**

| Metric               | Control | Treatment |
| -------------------- | ------: | --------: |
| Paid Conversion Rate |   3.17% |     6.99% |

The Treatment group more than doubled the Paid Conversion Rate, indicating that the new onboarding campaign was effective in converting users into paying customers.

---

# KPI Tree Explanation

The KPI Tree was designed around the Paid Conversion Rate as the North Star Metric.

The primary KPI drivers included:

* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate

These drivers represent the key stages of the user journey that influence paid conversion.

The following guardrail metrics were monitored to ensure that higher conversions did not negatively affect business performance:

* Refund Request Rate
* Support Tickets per User
* Average Days to Convert

---

# Experiment Result Summary

The Treatment group outperformed the Control group across several key performance metrics.

| Metric                     | Control | Treatment |
| -------------------------- | ------: | --------: |
| Landing Page Visit Rate    |  63.64% |    72.59% |
| Trial Start Rate           |  25.11% |    29.09% |
| Onboarding Completion Rate |  15.58% |    21.26% |
| Paid Conversion Rate       |   3.17% |     6.99% |
| Average Revenue per User   |   51.75 |     53.88 |
| Average Engagement Score   |   57.03 |     62.93 |
| Average Days to Convert    |    8.86 |      6.40 |

These results indicate that the new onboarding campaign improved user activation, engagement, and conversion performance.

---

# Hypothesis Test Interpretation

The hypothesis test was conducted to evaluate whether the observed improvement in the Paid Conversion Rate was statistically significant.

* **Null Hypothesis (H₀):** There is no significant difference in Paid Conversion Rate between the Control and Treatment groups.
* **Alternative Hypothesis (H₁):** The Treatment group has a significantly different Paid Conversion Rate compared with the Control group.

Based on the hypothesis test results, the null hypothesis was rejected, indicating that the improvement in Paid Conversion Rate was statistically significant and was unlikely to have occurred by chance.

---

# Guardrail Analysis

Although the Treatment group achieved better conversion performance, additional guardrail metrics revealed some potential concerns.

| Guardrail Metric                   | Control | Treatment | Observation          |
| ---------------------------------- | ------: | --------: | -------------------- |
| Refund Request Rate                |   0.00% |     0.42% | Slight increase      |
| Support Tickets per User           |  14.72% |    24.76% | Significant increase |
| Average Days to Convert            |    8.86 |      6.40 | Improved             |
| Average Engagement Score           |   57.03 |     62.93 | Improved             |
| Average Revenue per Converted User | 1630.10 |    770.41 | Declined             |

The increase in Support Tickets per User represents the most important business risk, while the decline in Average Revenue per Converted User suggests that additional analysis is required to understand customer purchasing behaviour.

---

# Segment-Level Insight

Segment-level analysis was performed using Region, Device Type, and Traffic Source.

The Treatment group generally performed consistently across the analyzed segments without any major imbalance in user distribution. No single segment showed evidence of substantial performance decline, indicating that the onboarding campaign performed reasonably consistently across different customer groups.

---

# Final Recommendation

**Recommendation: Continue Testing**

The experiment successfully improved the North Star Metric (Paid Conversion Rate), user engagement, and conversion speed. However, the increase in Support Tickets per User and the reduction in Average Revenue per Converted User indicate that there are still usability and revenue quality concerns.

Instead of launching the campaign to all users immediately, it is recommended to continue testing and optimize the onboarding experience before a full-scale deployment.

---

# Risks and Limitations

* Duplicate User IDs were identified during data validation and were documented but not removed.
* Some missing values were present in Device Type, Traffic Source, Engagement Score, and Days to Convert.
* Days to Convert contained expected missing values for users who did not convert.
* Revenue quality declined despite higher overall conversion.
* Increased customer support requests may indicate onboarding usability issues.

---

# Next Steps

* Investigate the reasons behind the increase in support tickets.
* Analyze why Average Revenue per Converted User decreased.
* Optimize the onboarding flow to reduce user confusion.
* Conduct another A/B test after implementing improvements.
* Continue monitoring guardrail metrics before considering a full rollout.
