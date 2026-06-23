# Task 1: Business Problem Statement

The company has introduced a new onboarding and activation campaign for new users. The main decision is whether this new campaign should be launched for all users or continue only as a test.

This decision can affect both users and the business. If the campaign helps users complete onboarding and become active more quickly, it may improve overall business performance. However, if the new experience creates confusion or reduces engagement, it could negatively impact user satisfaction.

The primary metric that should improve is the user activation rate because the goal of the campaign is to encourage more users to complete the onboarding process and start using the product.

Before making a final recommendation, it is important to monitor possible risks such as lower retention, reduced revenue, higher churn, or any decline in user engagement.

A recommendation should only be made after comparing the performance of the treatment group with the control group and confirming that the new campaign produces better results without causing negative effects on other important business metrics.

# Dataset Description

The dataset contains information from an onboarding and activation experiment conducted on new users. Each row represents a single user who participated in the experiment.

The data includes user details such as experiment group (Control or Treatment), region, device type, traffic source, and plan type. It also contains outcome metrics such as activation status, trial completion, revenue, engagement score, retention indicators, refund information, and churn-related metrics.

The dataset is used to compare the performance of the existing onboarding experience against the new onboarding campaign and to understand its impact on user activation and business outcomes.


# Task 2: North Star Metric

## Selected North Star Metric

**User Activation Rate**

### Why this is the main success metric

User Activation Rate is the most important metric for this experiment because the purpose of the new onboarding campaign is to help more users complete the onboarding process and start using the product successfully. If more users become active, the campaign can be considered effective.

### Why other metrics are supporting metrics

Other metrics such as revenue, retention rate, engagement rate, and churn rate are important, but they are supporting metrics. These metrics help us understand the overall impact of the campaign after users become active. They do not directly measure whether the onboarding experience is successful.

### How this metric connects to business growth

A higher activation rate means more users are successfully reaching the value of the product. Active users are more likely to remain engaged, continue subscriptions, and generate revenue for the company. Therefore, improving activation rate can contribute to long-term business growth.

### What could go wrong if this metric is optimized blindly

If the company focuses only on activation rate, users may be pushed through onboarding too quickly without a good experience. This could increase short-term activation while reducing user satisfaction, retention, or long-term revenue. For this reason, guardrail metrics should also be monitored.


# Task 3: KPI Tree Summary

## North Star Metric

User Activation Rate

## Supporting Metrics

* Trial Completion Rate
* Revenue per User
* Engagement Score
* Retention Rate

## Guardrail Metrics

* Refund Rate
* Churn Rate
* User Experience Metrics

The KPI tree shows how the primary goal of improving user activation is connected to other business metrics. While activation rate is the main success metric, supporting metrics help measure overall business impact and guardrail metrics ensure that the experiment does not negatively affect users or business performance.


# Task 4: Data Quality Checks

The dataset was reviewed before analysis.

- No duplicate user IDs were found.
- No missing values were detected.
- Control and Treatment groups were available for comparison.
- Binary columns contained only valid values (0 and 1).
- No significant revenue outliers required removal.
- Segment distribution appeared balanced across groups.

All checks were documented in analysis/experiment_analysis.xlsx.


# Task 5: Experiment Summary

An experiment summary was prepared by comparing the Control and Treatment groups across key business metrics. The analysis included user count, landing page visit rate, trial start rate, onboarding completion rate, paid conversion rate, average revenue per user, average revenue per converted user, refund rate, support ticket rate, average engagement score, and average days to convert.

The Treatment group showed stronger performance in user activation, trial starts, onboarding completion, paid conversions, revenue generation, and engagement score compared to the Control group. The average time required for users to convert was also slightly lower in the Treatment group, indicating a more effective onboarding experience.


## Task 6: Frame Hypotheses

Created `analysis/hypothesis_test_notes.md` containing:

* Null Hypothesis (H0)
* Alternative Hypothesis (H1)
* Test type (one-tailed)
* Significance level (α = 0.05)
* Metric selected: Paid Conversion Rate
* Reason for selecting the metric
* Interpretation logic for hypothesis testing
* Business decision criteria based on statistical significance

The hypothesis is designed to evaluate whether the Treatment group improves paid conversion rate compared to the Control group.


## Task 7: A/B Test Analysis

Performed hypothesis testing on Paid Conversion Rate.

Results:

* Control Conversion Rate: 3.17%
* Treatment Conversion Rate: 6.99%

The Treatment group showed a meaningful improvement over the Control group.

Evidence saved in:

* screenshots/hypothesis_test_output.png

Analysis documented in:

* analysis/hypothesis_test_notes.md


## Task 8: Guardrail Metrics

Evaluated key guardrail metrics including:
- Refund Rate
- Support Ticket Rate
- Engagement Score
- Days to Convert

Findings:
- Refund rate remained stable.
- Engagement score improved.
- Days to convert decreased.
- Support ticket rate increased and should be monitored.


## Task 9: Recommendation

Based on the experiment results, the Treatment group achieved a higher conversion rate (6.99%) than the Control group (3.17%).

Recommendation: Launch the Treatment version while monitoring support ticket rates after rollout.
