# Assignment 5.1 - Coupon Acceptance Summary

## Jupyter Notebook
[View the Analysis Notebook](prompt.ipynb)

GitHub Repository: https://github.com/jtie/Module5_Assignment5_1

---

## Problem Statement

This analysis investigates **what factors influence drivers to accept mobile coupons** delivered while they are driving. The study focuses on understanding the characteristics and behaviors of drivers who accept coupons versus those who reject them.

Specifically, this analysis examines two coupon categories:
1. **Bar Coupons**: What driver demographics and behavioral patterns predict acceptance of bar-related offers?
2. **Coffee House Coupons**: How do passenger types influence acceptance of coffee house coupons among regular coffee house visitors?

Understanding these acceptance patterns enables targeted marketing strategies and improved coupon delivery systems that maximize redemption rates.

---

## Data Overview

**Source**: UCI Machine Learning Repository (collected via Amazon Mechanical Turk survey)

**Dataset**: 12,684 driving scenarios with coupon offers

**Key Variables**:
- **User Attributes**: Gender, age, marital status, income, occupation, venue visit frequency (bars, coffee houses, restaurants)
- **Contextual Attributes**: Destination, passenger type, weather, temperature, time of day
- **Coupon Attributes**: Type (Bar, Coffee House, Restaurant <$20, Restaurant $20-50, Carry out), expiration time
- **Outcome**: Acceptance (Y=1) or Rejection (Y=0)

**Overall Acceptance Rate**: 56.84% of all coupons were accepted

### Data Distribution

![Coupon Distribution](images/coupon_distribution.png)

*Figure 1: Distribution of coupon types in the dataset. Coffee House and Restaurant (<$20) coupons comprise the majority of offers.*

![Temperature Distribution](images/temperature_distribution.png)

*Figure 2: Distribution of temperatures during coupon delivery scenarios.*

---

## Data
The analysis is based on the `coupons.csv` dataset located in the `data/` directory.
