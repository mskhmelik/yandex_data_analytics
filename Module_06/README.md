# Module 06: Procrastinate Pro+ Business Analytics

## Overview

This project analyzes business data for Procrastinate Pro+, a mobile application that has been experiencing losses despite significant investment in user acquisition. The analysis investigates user behavior, retention, lifetime value (LTV), return on investment (ROI), and factors negatively affecting user acquisition.

## Objectives

- Understand how users interact with the product
- Analyze when users start making purchases
- Calculate how much money each customer brings (LTV - Lifetime Value)
- Determine when customers pay back their acquisition costs (payback period)
- Identify factors negatively affecting user acquisition
- Analyze user retention and cohort behavior

## Data Description

The analysis uses three main datasets:

### Visits Log (`visits_log_short`)
Server log with information about app visits by new users registered between 2019-05-01 and 2019-10-27:

1. `User Id` — unique user identifier
2. `Device` — user device category
3. `Session start` — date and time of session start
4. `Session End` — date and time of session end
5. `Channel` — advertising source identifier
6. `Region` — user's country

### Orders Log (`orders_log_short`)
Information about purchases from December 7, 2020, to January 4, 2021:

1. `User Id` — unique identifier of the user who made the purchase
2. `Event Dt` — date and time of purchase
3. `Revenue` — purchase revenue

### Costs (`costs_short`)
Marketing costs data:

1. `Channel` — advertising source identifier
2. `Dt` — date
3. `Costs` — costs for this advertising source on this day

**Note**: The analysis assumes the perspective of November 1, 2019, and the company considers payback should occur no later than 2 weeks after user acquisition.

## Methodology

### 1. Data Preprocessing
- Data loading and initial exploration
- Handling missing values and data types
- Date and time conversions
- Data quality assessment
- Merging datasets for comprehensive analysis

### 2. User Behavior Analysis
- Session analysis and user engagement patterns
- Device category impact on behavior
- Regional differences in user behavior
- Time-to-first-purchase analysis

### 3. Financial Metrics
- **LTV (Lifetime Value)**: Total revenue per user
- **CAC (Customer Acquisition Cost)**: Cost per acquired user by channel
- **ROI**: Return on investment by channel
- **Payback Period**: Time to recover acquisition costs
- Revenue analysis by user cohorts

### 4. Retention Analysis
- Cohort analysis of user retention
- Retention rates by acquisition channel
- Retention rates by region and device
- Long-term user value assessment

### 5. Channel Performance
- Comparison of acquisition channels
- Cost efficiency analysis
- User quality by channel
- Identification of underperforming channels

## Key Findings

### User Behavior
- Patterns in how users interact with the application
- Time to first purchase analysis
- Engagement levels by device and region
- Session frequency and duration patterns

### Financial Performance
- LTV calculations reveal user value over time
- CAC varies significantly by channel
- ROI analysis identifies profitable vs. unprofitable channels
- Payback period analysis shows which channels meet the 2-week requirement

### Retention Insights
- Cohort retention rates over time
- Factors affecting user retention
- Long-term value of retained users
- Drop-off patterns and critical retention points

### Channel Analysis
- Identification of high-performing acquisition channels
- Discovery of channels with poor ROI
- Recommendations for channel optimization
- Cost allocation insights

### Business Recommendations
- Channels to increase investment in
- Channels to reduce or eliminate
- Optimization strategies for user acquisition
- Focus areas for improving retention

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualization
- **SciPy**: Statistical analysis
- **Datetime**: Date and time handling
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_06/
├── 220616_mk_project_6_vChecked.ipynb    # Main project notebook (checked version)
├── 220616_mk_project_6_vF.ipynb          # Final version
├── Code examples/                          # Additional code examples
│   ├── yandex_cac_roi.ipynb
│   ├── yandex_cohort_visualization.ipynb
│   ├── yandex_ltv.ipynb
│   ├── yandex_retention_and_lifetime.ipynb
│   ├── yandex_share_y_visuallization.ipynb
│   ├── yandex_subplot.ipynb
│   └── yandex_variable_retention.ipynb
├── _old/                                   # Previous versions
└── README.md                               # This file
```

## Results

The analysis provides critical business insights for Procrastinate Pro+:

1. **Financial Health**: Clear picture of which channels are profitable and which are causing losses
2. **User Value**: Understanding of LTV and how it varies by acquisition channel
3. **Retention Patterns**: Identification of retention issues and opportunities
4. **Optimization Opportunities**: Specific recommendations for improving business performance

**Key Business Impact**:
- Identification of loss-making channels that should be discontinued
- Recognition of profitable channels for increased investment
- Understanding of user behavior patterns that affect revenue
- Data-driven recommendations for marketing budget reallocation

The project demonstrates the importance of comprehensive business analytics in identifying the root causes of business losses and providing actionable recommendations for improvement.
