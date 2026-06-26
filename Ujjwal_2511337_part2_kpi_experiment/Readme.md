# Task 1: Business Problem Understanding

## Background

The company operates a subscription-based digital product and wants to bring in more users who sign up and start using the platform successfully. To improve the onboarding experience, a new onboarding and activation campaign has been developed and tested.

Users were randomly divided into two groups:

* Control Group: Existing onboarding experience
* Treatment Group: New onboarding and activation campaign

The experiment was conducted to check whether the new onboarding experience creates measurable business value compared to the current experience.

## Business Decision

The key decision is whether the company should roll out the new onboarding campaign to all users or continue using the existing onboarding process.

This decision must be based on data rather than assumptions because a full rollout will affect future user growth, engagement, and subscription revenue.

## Stakeholders Impacted

The outcome of this decision impacts multiple stakeholders:

### Users

Will directly experience the onboarding flow selected for deployment.

### Growth and Marketing Team

Focused on increasing user activation and conversion efficiency.

### Product Team

Responsible for designing and improving the onboarding experience.

### Stakeholders

Use experiment results to make strategic investment and rollout decisions.

## Desired Business Outcome

The primary goal of the experiment is to improve user conversion and early-stage engagement.

A successful onboarding experience should help users understand product value quickly, complete important activation actions, and progress toward becoming long-term paying customers.

The experiment should show that the Treatment Group performs better than the Control Group on the primary success metric.

## Risks That Must Be Monitored

A higher conversion rate alone is not sufficient to justify a rollout decision.

The company must also monitor guardrail metrics to ensure that improvements are sustainable and do not negatively affect user experience.

Potential risks include:

* Lower user retention
* Reduced engagement quality
* Higher cancellation rates
* User frustration caused by aggressive onboarding tactics
* Short-term gains that do not translate into long-term value

If these risks increase significantly, the treatment should not be launched even if conversion improves.

## Evidence Required Before Making a Recommendation

Before recommending a full rollout, the following evidence is required:

1. The Treatment Group must do better than the Control Group on the primary success metric.
2. Guardrail metrics should remain stable or improve.
3. The overall business impact should be positive and aligned with long-term growth objectives.
4. The expected benefits should outweigh any identified risks.

Only after validating these conditions can a recommendation be made to launch, modify, or reject the new onboarding campaign.

## Success Criteria

The experiment will be considered successful if:

- Conversion rate improves meaningfully.
- Early user engagement increases.
- Retention and user quality metrics remain healthy.
- Statistical analysis confirms the reliability of results.
- The treatment generates positive business value without introducing significant risks.

Based on these findings, a final recommendation will be provided regarding the rollout of the new onboarding campaign.

# Task 2: North Star Metric

## Selected North Star Metric

### Paid Conversion Rate

**Definition:**

Paid Conversion Rate measures the percentage of users who successfully convert into paying customers after experiencing the onboarding process.

Formula:

Paid Conversion Rate = (Number of Users Converted to Paid ÷ Total Users) × 100

## Why Paid Conversion Rate is the North Star Metric

The primary objective of this experiment is to determine whether the new onboarding and activation campaign creates measurable business value. Since the company operates on a subscription-based model, business growth ultimately depends on converting users into paying customers.

Paid Conversion Rate directly measures whether the treatment experience is more effective than the existing onboarding process at generating revenue-producing users. Unlike intermediate metrics, it reflects the final outcome that leadership cares about when deciding whether the new onboarding campaign should be launched to all users.

For this reason, Paid Conversion Rate is the most appropriate North Star Metric for evaluating experiment success.

## Why Other Metrics Are Supporting Metrics

Several other metrics provide valuable insights into user behavior but do not directly measure the primary business outcome.

### Started Trial

This metric indicates initial user interest in the product. However, starting a trial does not guarantee that a user will eventually become a paying customer.

### Completed Onboarding

This measures how effectively users move through the onboarding process. While important, onboarding completion alone does not create business value unless it leads to paid conversion.

### Engagement Score

Engagement Score reflects how actively users interact with the product. Higher engagement is generally positive, but engaged users may still choose not to purchase a subscription.

### Revenue 30 Days

Revenue is closely related to business growth, but it is influenced by pricing plans and spending patterns. Paid Conversion Rate provides a cleaner measure of whether the onboarding campaign successfully converts users.

Therefore, these metrics should be treated as supporting or diagnostic metrics rather than the primary success metric.

## Connection to Business Growth

Paid Conversion Rate is directly connected to business growth because an increase in paying customers leads to:

* Higher subscription revenue
* Improved customer acquisition efficiency
* Better return on marketing investment
* Growth in the active customer base
* Increased customer lifetime value

If the treatment group achieves a higher Paid Conversion Rate than the control group, the company can generate more revenue from the same volume of acquired users. This makes Paid Conversion Rate a strong indicator of sustainable business growth.

## Risks of Optimizing Paid Conversion Rate in Isolation

Although Paid Conversion Rate is the most important success metric, optimizing it without considering other metrics may create unintended consequences.

Potential risks include:

* Aggressive onboarding tactics that pressure users into converting.
* Increased refund requests after conversion.
* Higher support ticket volumes due to user confusion.
* Lower long-term engagement and retention.
* Reduced customer satisfaction despite higher conversion rates.

For this reason, Paid Conversion Rate should be evaluated together with guardrail metrics such as Engagement Score, Refund Requests, Support Tickets, and Days to Convert before making a rollout decision.

## Conclusion

Paid Conversion Rate is selected as the North Star Metric because it directly measures the experiment's ability to convert users into paying customers and generate business value. Supporting and guardrail metrics will be analyzed alongside it to ensure that any observed improvement is sustainable and beneficial for both users and the business.

# Task 4: Data Cleaning and Preparation

Before performing the experiment analysis, the dataset was reviewed to assess its quality and ensure that it was suitable for KPI calculations and experiment evaluation. The following data validation checks were performed.

## 1. Missing Values

The dataset was checked for missing values across all columns.

| Column           | Missing Values |
| ---------------- | -------------: |
| Device Type      |             18 |
| Traffic Source   |             23 |
| Engagement Score |             14 |
| Days to Convert  |           1322 |

**Handling:**

* Missing values in **Device Type**, **Traffic Source**, and **Engagement Score** were documented and retained because there was no reliable basis for imputing these values.
* The missing values in **Days to Convert** were considered expected, as this metric is applicable only to users who successfully converted to a paid subscription. Therefore, these missing values were retained.

---

## 2. Experiment Group Counts

The number of users in each experiment group was verified.

| Experiment Group | User Count |
| ---------------- | ---------: |
| Control          |        693 |
| Treatment        |        715 |

**Handling:**

The Control and Treatment groups are reasonably balanced in size, making them suitable for comparison during the experiment analysis.

---

## 3. Duplicate User IDs

The `user_id` column was checked to verify that each user appeared only once in the dataset.

**Finding:**

* Duplicate User IDs identified: **8**

**Handling:**

The duplicate user IDs were identified and documented during the data validation process. No records were removed because the objective of this task was to assess and prepare the dataset for analysis. The duplicates were flagged as a potential data quality concern and considered during the interpretation of results.

---

## 4. Binary Variable Validation

The following binary variables were validated:

* `visited_landing_page`
* `started_trial`
* `completed_onboarding`
* `converted_to_paid`
* `refund_requested`

**Finding:**

All binary variables contained only valid values (**0** and **1**).

**Handling:**

No corrections were required, and all binary fields were considered valid for analysis.

---

## 5. Revenue Outlier Check

The `revenue_30d` column was reviewed for unusually high or unexpected values before analysis.

**Handling:**

No revenue records were removed from the dataset, as there was no clear evidence of data entry errors. All observations were retained to preserve the integrity of the experiment analysis.

---

## 6. Segment Distribution Across Groups

The distribution of users across key customer segments was examined using Pivot Tables.

The following segments were reviewed:

* Region
* Device Type
* Traffic Source
* Plan Type

**Finding:**

The Control and Treatment groups showed a broadly similar distribution across all four segments. Minor differences were observed in some categories; however, no substantial imbalance was identified that would significantly affect the comparison between the two groups.

**Handling:**

Since the segment distribution was reasonably balanced, no adjustments were required before proceeding with the experiment analysis.

---

# Dataset Preparation for Analysis
After completing the data validation process, the dataset was prepared for analysis by:

* Reviewing and documenting missing values.
* Verifying the distribution of users across the Control and Treatment groups.
* Identifying duplicate user IDs and flagging them for review.
* Validating that all binary variables contained only valid values (0 and 1).
* Reviewing the revenue column for unusual values without removing any records.
* Comparing the distribution of users across Region, Device Type, Traffic Source, and Plan Type to ensure that the experiment groups were reasonably balanced.

Based on these validation checks, the dataset was considered suitable for KPI calculation, experiment summary, and hypothesis testing. While a small number of missing values and duplicate user IDs were identified, these issues were documented and taken into consideration during the analysis.


# KPI Tree Summary
The KPI Tree was designed using **Paid Conversion Rate** as the North Star Metric.

### Primary KPI Drivers
- Landing Page Visit Rate
- Trial Start Rate
- Onboarding Completion Rate

### Supporting Drivers
- User Engagement
- Revenue per User
- Conversion Speed

### Guardrail Metrics
- Refund Request Rate
- Support Tickets per User
- Average Days to Convert

The KPI Tree illustrates how improvements in user acquisition and activation contribute to Paid Conversion Rate while ensuring that customer experience and business quality remain protected through guardrail metrics.


# Experiment Analysis Approach

The experiment analysis was completed in the following stages:

1. Defined the business problem and experiment objective.
2. Selected Paid Conversion Rate as the North Star Metric.
3. Created a KPI Tree to identify drivers and guardrail metrics.
4. Validated and prepared the dataset for analysis.
5. Compared Control and Treatment groups using key business KPIs.
6. Performed hypothesis testing on the Paid Conversion Rate.
7. Evaluated guardrail metrics to identify potential business risks.
8. Interpreted the results and prepared the final recommendation.


# Hypothesis Test Summary

The hypothesis test was conducted to determine whether the difference in Paid Conversion Rate between the Control and Treatment groups was statistically significant.

- **Null Hypothesis (H₀):** There is no significant difference in Paid Conversion Rate between the Control and Treatment groups.
- **Alternative Hypothesis (H₁):** There is a significant difference in Paid Conversion Rate between the Control and Treatment groups.

Based on the hypothesis test results, the null hypothesis was rejected, indicating that the improvement in Paid Conversion Rate observed in the Treatment group was statistically significant.


# Guardrail Metrics Considered

The following guardrail metrics were evaluated to ensure that the improvement in Paid Conversion Rate did not negatively impact customer experience or business performance.

| Metric | Control | Treatment |
|---------|---------:|----------:|
| Refund Request Rate | 0.00% | 0.42% |
| Support Tickets per User | 14.72% | 24.76% |
| Average Days to Convert | 8.86 | 6.40 |

The analysis showed that users in the Treatment group converted faster, but the increase in support tickets and the slight increase in refund requests indicate areas that require further improvement.


# Final Recommendation

**Recommendation: Continue Testing**

The Treatment group significantly improved the Paid Conversion Rate (6.99% vs. 3.17%), along with better engagement and faster conversions.

However, the increase in Support Tickets per User and the decline in Average Revenue per Converted User indicate that additional optimization is required before deploying the new onboarding campaign to all users.

A phased rollout or an additional round of A/B testing is recommended before full implementation.


# Assumptions and Limitations

- Duplicate User IDs were identified but not removed.
- Missing values were retained where appropriate.
- Days to Convert is applicable only to users who converted to paid.
- Revenue values were reviewed and retained.
- The analysis is based only on the available experiment dataset and may not fully represent future user behaviour.


# Screenshots Included

The repository includes the following screenshots:

- summary_metrics.png
- hypothesis_test_output.png
- kpi_tree_preview.png