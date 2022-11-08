# Enhance Trust with Machine Learning Model Error Analysis
## November 2, 2022
## Serg Masis
---
### Notes

- "Enough true negatives to cover those that were never readmitted, also willing to have as many false positives as those that were readmitted over 30 days, because eventually they will be readmitted." - how does this translate to my project? Toleration considerations.
- error_breakdown_by_group - custom function that shows how many of each type of error are in each group 
- RAIInsights has an error analysis dashboard. It shows the distribution of errors by feature. It also shows the distribution of errors by feature value. It also shows the distribution of errors by feature value and label.
- Error rate the the opposite of accuracy. It is the percentage of predictions that are incorrect. Error rate = (FP + FN) / (TP + TN + FP + FN)

### Investigate
- **Custom metrics for error analysis** 