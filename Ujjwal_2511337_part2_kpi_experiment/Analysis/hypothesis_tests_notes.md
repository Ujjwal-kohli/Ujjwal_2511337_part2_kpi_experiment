# Hypothesis Test Notes

## Experiment Objective

The objective of this experiment is to determine whether the Treatment group performs better than the Control group and whether the new experience should be implemented for all users.

The business decision depends on whether the Treatment improves user conversion and generates better business outcomes.

---

# Hypothesis 1: Paid Conversion Rate

## Metric Being Tested

**Paid Conversion Rate**

Formula:

Paid Conversion Rate = Converted Users / Total Users

---

## Null Hypothesis (H0)

There is no significant difference in paid conversion rate between the Control group and Treatment group.

H0:
Treatment Conversion Rate = Control Conversion Rate

---

## Alternate Hypothesis (H1)

The Treatment group has a higher paid conversion rate compared to the Control group.

H1:
Treatment Conversion Rate > Control Conversion Rate

---

## Test Type

**One-tailed test**

Reason:
The business objective is specifically to check whether the Treatment improves conversion performance. We are only interested in detecting an increase, not a decrease.

---

## Significance Level

Significance level (α):

**0.05 (5%)**

Reason:
A 5% significance level is commonly used in business experiments to balance confidence and decision-making speed.

---

## Reason for Choosing This Metric

Paid conversion rate is selected as the primary metric because it directly measures whether the experiment successfully increases the number of users who become paying customers.

An improvement in conversion rate can directly impact revenue growth and business scalability.

---

## Interpretation Logic

- If p-value < 0.05:
  - Reject the null hypothesis.
  - The Treatment group has a statistically significant improvement in conversion rate.
  - The new experience can be considered for wider implementation.

- If p-value >= 0.05:
  - Fail to reject the null hypothesis.
  - There is not enough evidence that Treatment improves conversion.
  - Further testing or analysis may be required before rollout.

---

# Supporting Metrics

Additional metrics considered:

- Average Revenue Per User
- Engagement Score
- Refund Rate
- Support Ticket Rate

These metrics help evaluate whether the Treatment improves business performance without negatively affecting user experience.

---

# Business Decision

The final decision will be based on whether the Treatment group shows a statistically significant improvement in paid conversion rate while maintaining acceptable revenue, engagement, refund, and support metrics.

# Test Output

## Summary of Test Inputs

* Statistical Test: Two-Proportion Z-Test
* Primary Metric: Paid Conversion Rate
* Control Group:

  * Total Users: 693
  * Converted Users: 22
  * Conversion Rate: 3.17%
* Treatment Group:

  * Total Users: 715
  * Converted Users: 50
  * Conversion Rate: 6.99%
* Significance Level (α): 0.05

## Test Output

The Two-Proportion Z-Test was performed to compare the paid conversion rates of the Control and Treatment groups.

The resulting p-value was below the significance level of 0.05, indicating a statistically significant difference between the two groups.

## Decision Rule

* If p-value < 0.05: Reject the null hypothesis.
* If p-value ≥ 0.05: Fail to reject the null hypothesis.

## Decision

Since the p-value is less than 0.05, the null hypothesis is rejected.

## Business Interpretation

The Treatment group achieved a significantly higher paid conversion rate than the Control group. This suggests that the experimental change positively impacted user conversions. Based on this result, the Treatment can be considered for rollout, provided that other business metrics such as revenue, refunds, and support tickets remain acceptable.
