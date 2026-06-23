## Hypothesis Testing Notes

## Metric Being Tested

The metric selected for testing is **Paid Conversion Rate**.

Paid Conversion Rate shows the percentage of users who became paying customers after using the onboarding experience. This is the most important metric because the main goal of the campaign is to increase conversions.

---

## Null Hypothesis (H0)

There is no difference in the Paid Conversion Rate between the Control group and the Treatment group.

H0: The new onboarding campaign does not improve conversions.

---

## Alternative Hypothesis (H1)

The Treatment group has a higher Paid Conversion Rate than the Control group.

H1: The new onboarding campaign improves conversions.

---

## Type of Test

A **one-tailed test** is used because we only want to check whether the new onboarding experience performs better than the current one.

---

## Significance Level

The significance level used is **0.05 (5%)**.

If the p-value is less than 0.05, the result will be considered statistically significant.

---

## Why This Metric Was Chosen

Paid Conversion Rate was selected because it directly measures how many users become paying customers. Since the company wants to increase subscriptions and revenue, this metric is the best indicator of success.

---

## Decision Rule

* If p-value < 0.05, reject the null hypothesis.
* If p-value ≥ 0.05, fail to reject the null hypothesis.

---

## Interpretation

If the Treatment group has a significantly higher Paid Conversion Rate, it means the new onboarding campaign is performing better than the existing onboarding experience.

If there is no significant difference, there is not enough evidence to recommend launching the new campaign to all users.

---

## Business Decision

The result of this test will help determine whether the company should launch the new onboarding campaign to all users. The final decision will also consider guardrail metrics such as refund rate, support ticket rate, engagement score, and days to convert.

## ## Hypothesis Test Results

### Test Inputs

To compare the performance of the Control and Treatment groups, a Pivot Table was created using the **experiment_group** and **converted_to_paid** fields.

| Experiment Group | User Count | Converted Users |
| ---------------- | ---------- | --------------- |
| Control          | 693        | 22              |
| Treatment        | 715        | 50              |

The Paid Conversion Rate was calculated as:

**Paid Conversion Rate = Converted Users / Total Users**

| Experiment Group | Paid Conversion Rate |
| ---------------- | -------------------- |
| Control          | 3.17%                |
| Treatment        | 6.99%                |

---

### Test Output

A two-proportion A/B test was performed to compare the Paid Conversion Rates of the Control and Treatment groups.

**P-value = 0.0006**

---

### Decision Rule

* If the p-value is less than 0.05, reject the null hypothesis.
* If the p-value is greater than or equal to 0.05, fail to reject the null hypothesis.

---

### Result

The p-value (0.0006) is less than the significance level of 0.05.

Therefore, the null hypothesis is rejected.

This means there is statistical evidence that the Treatment group performed better than the Control group in terms of Paid Conversion Rate.

---

### Business Interpretation

The Treatment group achieved a Paid Conversion Rate of 6.99%, while the Control group achieved a Paid Conversion Rate of 3.17%.

The results suggest that the new onboarding campaign was more effective at converting users into paying customers. Based on the hypothesis test, the Treatment experience shows a meaningful improvement over the existing onboarding process.

However, before making a final rollout decision, guardrail metrics such as refund rate, support ticket rate, engagement score, and days to convert should also be reviewed to ensure there are no negative impacts on user experience.


##  Guardrail Metrics Evaluation

Although the Treatment group showed a higher Paid Conversion Rate, the decision should not be based only on conversion improvement. Additional guardrail metrics were reviewed to identify any potential risks.

### Refund Rate

The Treatment group showed a slightly higher refund rate compared to the Control group. This could indicate that some users were not fully satisfied after converting. However, the increase was relatively small and does not currently appear to be a major concern.

### Support Ticket Rate

The support ticket rate was higher in the Treatment group. This suggests that some users may have experienced confusion or needed additional help while using the new onboarding experience. This metric should continue to be monitored if the campaign is launched.

### Average Days to Convert

Users in the Treatment group converted faster than users in the Control group. A lower number of days to convert is a positive outcome because users are reaching the paid stage more quickly.

### Engagement Score

The Treatment group achieved a higher average engagement score than the Control group. This indicates that users were more active and engaged with the platform after experiencing the new onboarding process.

### Revenue Quality

Average revenue per user and average revenue per converted user were reviewed. The Treatment group generated higher revenue overall, suggesting that the conversion improvement also resulted in stronger business value.

### Segment-Level Review

Segment analysis was performed using Region, Device Type, and Traffic Source. No major segment showed a significant decline in performance. The Treatment group generally performed as well as or better than the Control group across most segments.

### Risk Assessment

The main risk identified during the analysis was the increase in support ticket rate and the slight increase in refund rate. While these metrics do not currently outweigh the conversion improvement, they should be monitored closely if the new onboarding campaign is rolled out to all users.
