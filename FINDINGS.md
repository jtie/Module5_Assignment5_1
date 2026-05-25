# Assignment 5.1 - Coupon Acceptance Analysis

## Analysis & Findings

### 1. Bar Coupons Analysis

**Dataset**: 2,017 bar coupon observations (41.00% overall acceptance rate)

#### Key Statistical Findings

**Finding 1: Visit Frequency is the Strongest Predictor**
- **High-frequency bar visitors (>3 times/month)**: 76.88% acceptance rate
- **Low-frequency bar visitors (≤3 times/month)**: 37.07% acceptance rate
- **Difference**: +39.81 percentage points (**statistically significant**)

**Interpretation**: Past behavior is the strongest predictor of coupon acceptance. Drivers who already frequent bars are more than twice as likely to accept bar coupons, demonstrating strong behavioral consistency.

**Finding 2: Age and Social Context Matter**
| Driver Profile | Acceptance Rate |
|----------------|-----------------|
| Visits bars >1/month AND age <30 | 72.17% |
| Visits bars >1/month AND age >25 | 69.52% |
| Visits bars >1/month, no kids, non-farming occupation | 71.32% |
| Visits bars >1/month, no kids, not widowed | 71.32% |
| Frequent cheap restaurant visitors (<$50K income) | 45.76% |

**Interpretation**: Among bar visitors, younger drivers and those in social contexts (no children present, not widowed) show consistently high acceptance rates above 69%. This suggests bar coupon acceptance is associated with a social, leisure-oriented profile rather than family-focused activities.

---

### 2. Coffee House Coupons Analysis

**Dataset**: 3,996 coffee house coupon observations (49.92% overall acceptance rate)

#### Key Statistical Findings

**Finding 1: Passenger Type Dramatically Affects Acceptance**

![Coffee House Acceptance by Passenger](images/coffee_house_coupon_acceptance_rate.png)

*Figure 3: Acceptance rates for coffee house coupons by passenger type among regular coffee house visitors.*

| Passenger Type | Acceptance Rate | Difference from Baseline |
|----------------|-----------------|-------------------------|
| Friends / Partner | 76.66% | +26.74 percentage points |
| Alone / Kids | 59.60% | +9.68 percentage points |
| **Overall** | **49.92%** | **(baseline)** |

**Interpretation**: Among drivers who already visit coffee houses regularly (≥1 time/month):
- **Social trips (with friends/partner)** have the highest acceptance at 76.66% — a **28.8% relative increase** over being alone or with kids (59.60%)
- **The gap of 17.06 percentage points** between social and non-social contexts indicates that coffee house coupons resonate most strongly when the driver is already engaged in a social outing
- Even drivers alone or with kids show elevated acceptance (59.60%) compared to the overall rate, suggesting visit frequency still matters

![Coffee House Coupon Acceptance Detailed Analysis](images/coffee_house_coupon_acceptance_subplot.png)

*Figure 4: Detailed breakdown of coffee house coupon acceptance patterns by passenger type and income level.*

---

## Next Steps & Recommendations

### Immediate Actions

1. **Implement Behavioral Segmentation**
   - Build targeting models based on venue visit frequency (primary variable)
   - Create audience segments: "Frequent Bar Visitors" (>3/month) and "Regular Coffee House Visitors" (≥1/month)
   - Deploy coupons preferentially to high-frequency visitors for each venue type

2. **Context-Aware Delivery**
   - Integrate passenger detection (if technically feasible) to optimize coffee house coupon timing
   - Suppress bar coupons when children are passengers
   - Time bar coupon delivery toward younger demographics and evening/social hours

### Future Research Directions

1. **Expand Analysis to Other Coupon Types**
   - Conduct similar investigations for Restaurant (<$20), Restaurant ($20-50), and Carry Out coupons
   - Identify unique acceptance drivers for each category

2. **Temporal and Weather Analysis**
   - Analyze acceptance patterns by time of day, day of week, and weather conditions
   - Determine optimal delivery windows for each coupon type

3. **Income and Occupation Deep-Dive**
   - Explore whether income brackets and occupation types show significant acceptance differences
   - Understand the relationship between financial factors and coupon appeal

4. **Geographic and Distance Factors**
   - Examine how proximity to venue (5min/15min/25min drive) affects acceptance
   - Analyze whether same-direction vs. opposite-direction routing impacts decisions
