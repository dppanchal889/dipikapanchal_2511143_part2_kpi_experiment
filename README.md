# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company introduced a new onboarding campaign to help more users become paying customers. To measure its impact, users were divided into two groups:

* Control Group: Existing onboarding experience
* Treatment Group: New onboarding experience

The goal of this analysis is to determine whether the new onboarding campaign should be launched to all users.

---

## Dataset Description

The dataset contains experiment data for users in both the Control and Treatment groups.

The dataset includes information such as:

* User ID
* Experiment Group
* Region
* Device Type
* Traffic Source
* Plan Type
* Landing Page Visit
* Trial Start
* Onboarding Completion
* Paid Conversion
* Revenue
* Refund Requests
* Support Tickets
* Engagement Score
* Days to Convert

The data was reviewed and checked before starting the analysis.

---

## Business Problem Statement

The company wants to know if the new onboarding campaign performs better than the current onboarding process.

The decision affects product teams, marketing teams, customer support teams, and future users of the platform.

The main goal is to improve the number of users who become paying customers while making sure the user experience is not negatively affected.

The final recommendation should be based on experiment results, hypothesis testing, and guardrail metrics.

---

## North Star Metric

### Selected Metric: Paid Conversion Rate

Paid Conversion Rate was selected as the North Star Metric because it directly measures how many users become paying customers.

This metric is important because an increase in paid conversions can lead to higher revenue and business growth.

Other metrics such as onboarding completion rate, engagement score, and trial start rate are useful for understanding user behavior, but they do not directly measure business success.

---

## KPI Tree Summary

The KPI tree was created using Paid Conversion Rate as the main metric.

### Main Drivers

#### Acquisition Quality

* Landing Page Visit Rate
* Traffic Source Quality

#### Activation Success

* Trial Start Rate
* Onboarding Completion Rate

#### User Engagement and Experience

* Engagement Score
* Days to Convert

#### Revenue Quality

* Average Revenue Per User
* Average Revenue Per Converted User

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Segment-Level Performance

---

## Data Cleaning and Preparation

Before analyzing the experiment results, several data quality checks were performed.

### Missing Values

The dataset was checked for missing values. Missing values were found in some columns such as device type, traffic source, engagement score, and days to convert.

### Group Counts

The number of users in both groups was reviewed to make sure the Control and Treatment groups were suitable for comparison.

### Duplicate User IDs

Duplicate user IDs were identified and reviewed to avoid counting the same user more than once.

### Binary Value Validation

Columns containing binary values were checked to confirm that they only contained valid values of 0 and 1.

### Revenue Outlier Analysis

Revenue values were reviewed using the IQR method. Positive revenue values were treated as valid customer purchases and were not removed from the dataset.

### Segment Distribution

The distribution of users across Region, Device Type, Traffic Source, and Plan Type was reviewed to ensure that both groups were reasonably balanced.

---

## Experiment Analysis Approach

The Control and Treatment groups were compared using Paid Conversion Rate as the primary metric.

Additional metrics such as engagement score, revenue, refund rate, support ticket rate, and days to convert were also analyzed.

Segment-level analysis was performed to understand whether the campaign performed differently across user groups.

---

## Hypothesis Test Summary

### Null Hypothesis (H0)

There is no difference in Paid Conversion Rate between the Control and Treatment groups.

### Alternative Hypothesis (H1)

The Treatment group has a higher Paid Conversion Rate than the Control group.

### Test Type

One-tailed test

### Significance Level

0.05

### Result

The hypothesis test showed that the Treatment group achieved a higher Paid Conversion Rate than the Control group.

The p-value was lower than 0.05, so the null hypothesis was rejected.

This means the improvement in conversion rate is statistically significant.

---

## Guardrail Metrics Considered

The following guardrail metrics were reviewed:

### Refund Rate

Refund rates increased slightly in the Treatment group and should continue to be monitored.

### Support Ticket Rate

Support ticket rates were higher in the Treatment group, which may indicate that some users required additional support.

### Engagement Score

The Treatment group showed higher engagement scores compared to the Control group.

### Days to Convert

Users in the Treatment group converted faster than users in the Control group.

### Segment-Level Performance

No major segment showed a significant decline in performance.

---

## Final Recommendation

### Launch

Based on the analysis, I recommend launching the new onboarding campaign.

The Treatment group achieved better conversion results and higher engagement. The hypothesis test also showed that the improvement was statistically significant.

Although some guardrail metrics increased slightly, the overall results suggest that the new onboarding campaign performs better than the current onboarding experience.

---

## Assumptions and Limitations

* The analysis is based only on the provided dataset.
* Long-term customer retention was not included in the analysis.
* User behavior may change after a full rollout.
* Future monitoring will still be required after launch.

---

## Screenshots Included

The repository includes the following screenshots:

* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png

These screenshots provide supporting evidence for the analysis and findings.
