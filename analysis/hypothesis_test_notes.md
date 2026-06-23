# Hypothesis Test Notes

## Metric Being Tested

Paid Conversion Rate

## Reason for Choosing This Metric

Paid conversion rate directly measures how effectively the new treatment converts users into paying customers. It has the most direct impact on business revenue and is a key success metric for the experiment.

## Null Hypothesis (H0)

There is no significant difference in paid conversion rate between the Control group and the Treatment group.

H0: Conversion Rate (Treatment) = Conversion Rate (Control)

## Alternative Hypothesis (H1)

The Treatment group has a significantly higher paid conversion rate than the Control group.

H1: Conversion Rate (Treatment) > Conversion Rate (Control)

## Test Type

One-tailed test

## Significance Level

α = 0.05 (5%)

## Interpretation Logic

* If the p-value is less than 0.05, reject the null hypothesis.
* If the p-value is greater than or equal to 0.05, fail to reject the null hypothesis.
* Rejecting the null hypothesis would indicate that the Treatment has a statistically significant positive impact on paid conversions.
* Failing to reject the null hypothesis would indicate that there is insufficient evidence that the Treatment improves paid conversions.

## Business Decision

If the Treatment group shows a statistically significant increase in paid conversion rate, the new experience should be rolled out to all users. Otherwise, further testing and analysis should be performed before implementation.


# Hypothesis Test Results

## Summary of Test Inputs

Metric: Paid Conversion Rate

Control Group:

* Users: 693
* Converted Users: 22
* Conversion Rate: 3.17%

Treatment Group:

* Users: 715
* Converted Users: 50
* Conversion Rate: 6.99%

## Test Output

Treatment conversion rate is higher than Control conversion rate.

## P-value or Equivalent Evidence

Treatment conversion rate (6.99%) is more than double the Control conversion rate (3.17%), indicating a meaningful improvement.

## Decision Rule

If the Treatment conversion rate is significantly higher than the Control conversion rate, reject the null hypothesis.

## Business Interpretation

The Treatment group performs better and generates more paid conversions. The business should consider rolling out the Treatment experience to more users.
