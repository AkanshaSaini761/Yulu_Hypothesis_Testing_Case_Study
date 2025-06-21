# 🚲 Yulu Bike Sharing Demand Analysis Case Study

## 🏢 About Yulu

**Yulu** is India’s leading micro-mobility service provider offering shared electric cycles for daily commute. With an app-based rental model and strategically placed Yulu Zones, the company aims to solve India's first and last-mile commute issues.

Recently, Yulu has experienced a dip in revenue and seeks to understand the factors influencing the demand for shared electric cycles in the Indian market.


## 📌 Business Objective

The consulting team was tasked with identifying:

- **Which variables significantly influence bike rental demand**
- **How well those variables predict rental patterns**
- **Actionable strategies to boost utilization and efficiency**


## 📁 Dataset Overview

**Dataset Name:** [bike_sharing.csv](https://github.com/AkanshaSaini761/Yulu_Hypothesis_Testing_Case_Study/blob/main/yulu_data.csv)

**Shape:** 10,886 rows × 12 columns 

**Time Range:** January 1, 2011 – December 19, 2012


| Column       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `datetime`   | Timestamp of rental record                                                  |
| `season`     | 1 = spring, 2 = summer, 3 = fall, 4 = winter                                |
| `holiday`    | Whether the day is a holiday                                                |
| `workingday` | 1 if working day, 0 if weekend or holiday                                   |
| `weather`    | Categorical (1: clear, 2: cloudy, 3: light snow/rain, 4: heavy rain/snow)   |
| `temp`       | Temperature in Celsius                                                      |
| `atemp`      | Perceived temperature                                                       |
| `humidity`   | Humidity level (%)                                                          |
| `windspeed`  | Wind speed                                                                  |
| `casual`     | Number of casual users                                                      |
| `registered` | Number of registered users                                                  |
| `count`      | Total rentals (casual + registered)                                         |


## 🔍 Exploratory Goals 

- **Descriptive & Inferential Statistics**  
  Understand distribution, central tendency, and variation of variables.

- **Univariate & Bivariate Analysis**  
  Analyze individual features and their relationship with `count`.

- **Hypothesis Testing**  
  - Is there a difference in bike rentals on **working** vs **non-working days**?
  - Does **season** or **weather** significantly impact **rental demand**?
  - Are **weather** and **season** dependent on each other?
  
- **Assumption Checks**

  Use **histograms, Q-Q plots, Levene’s test, and Shapiro-Wilk test** to check for normality and equal variance.


- **Visualization Techniques**

  Apply **boxplots, histograms, line plots, KDE plots, and heatmaps** to support statistical findings.


- **Inference Drawing**

  Based on test statistics and significance level, decide whether to **accept or reject null hypotheses**, and interpret the results in a business context.


## 📊 Key Insights

### 1. User Profile
- **Registered users account for 81%**, while **casual users are 19%**.
- Consistent rise in total rentals from 2011 to 2012 (↑65.4% YoY).

### 2. Temporal Trends
- **Peak demand months:** June, July, August.
- **Low demand months:** January, February, March.
- **Daily Pattern:** High usage during **8 AM** and **5–6 PM** (commute hours).
- **Weekly Pattern:** Highest demand on **Thursdays**, lowest on **Sundays**.

### 3. Environmental Factors
- Rentals drop sharply when:
  - Temperature < 10°C
  - Humidity < 20%
  - Wind speed > 35 km/h
- **Clear/cloudy weather** shows highest demand.

### 4. Statistical Hypothesis Testing
- **No significant difference** between rentals on working vs non-working days.
- **Significant difference** in rentals across weather types (Kruskal-Wallis).
- **Significant difference** in rentals across seasons (Kruskal-Wallis).
- Weather and season are **statistically dependent** (Chi-square test).


## 💡 Recommendations

1. **Seasonal Marketing:** Promote heavily in spring and summer.  
2. **Dynamic Pricing:** Charge more during rush hours; incentivize off-peak times.  
3. **Weather-based Promotions:** Target users on clear/cloudy days.  
4. **Focus on Registered Users:** Offer loyalty programs and perks.  
5. **Inventory Optimization:** Scale fleet based on monthly trends.  
6. **Enhanced Customer Comfort:** Provide seasonal kits (umbrellas, ponchos).  
7. **Collaborate with Weather Services:** Enable real-time weather-informed offers.  
8. **Regular Maintenance:** Plan seasonal checks pre-summer/winter.  
9. **Engagement Campaigns:** Use customer feedback for product and service refinement.


## 🛠️ Tools & Libraries Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scipy)
- **Statistical Tests** (t-test, ANOVA, Kruskal-Wallis, Chi-square)
- **Visualizations** (Boxplots, Histograms, Line charts, Heatmaps)


## 📄 Output Report

All visuals, hypothesis test results, and insights are documented in the PDF below:

📎 [`yulu_case_study_akansha_saini.pdf`](https://github.com/AkanshaSaini761/Yulu_Hypothesis_Testing_Case_Study/blob/main/yulu_case_study_akansha_saini.pdf)
