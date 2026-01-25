# Module 04: Mobile Operator Tariff Plans Research

## Overview

This project analyzes customer behavior data for "Megaline," a federal mobile operator offering two tariff plans: "Smart" and "Ultra." The commercial department wants to understand which tariff generates more revenue to adjust the advertising budget accordingly.

## Objectives

The analysis aims to:
1. Describe customer behavior based on the sample data
2. Test two hypotheses:
   - The average revenue of "Ultra" and "Smart" tariff users differs
   - The average revenue of users from Moscow differs from users in other regions

## Tariff Plans Description

### Smart Tariff
- **Monthly fee**: 550 rubles
- **Included services**:
  - 500 minutes of calls
  - 50 messages
  - 15 GB of internet traffic
- **Overage charges**:
  - Call minute: 3 rubles
  - Message: 3 rubles
  - 1 GB of internet: 200 rubles

### Ultra Tariff
- **Monthly fee**: 1,950 rubles
- **Included services**:
  - 3,000 minutes of calls
  - 1,000 messages
  - 30 GB of internet traffic
- **Overage charges**:
  - Call minute: 1 ruble
  - Message: 1 ruble
  - 1 GB of internet: 150 rubles

## Data Description

The dataset contains information about 500 Megaline users, including:

### Users Table
1. `user_id` — unique user identifier
2. `first_name` — user's first name
3. `last_name` — user's last name
4. `age` — user's age (years)
5. `reg_date` — date of tariff connection (day, month, year)
6. `churn_date` — date of tariff termination (if missing, tariff was still active at data extraction)
7. `city` — user's city of residence
8. `tariff` — tariff plan name

### Calls Table
1. `id` — unique call identifier
2. `call_date` — call date
3. `duration` — call duration in minutes
4. `user_id` — identifier of the user who made the call

### Messages Table
1. `id` — unique message identifier
2. `message_date` — message date
3. `user_id` — identifier of the user who sent the message

### Internet Table
1. `id` — unique session identifier
2. `session_date` — session date
3. `mb_used` — data volume used in megabytes
4. `user_id` — identifier of the user who used the internet

## Methodology

### 1. Data Preprocessing
- Data loading and initial exploration
- Handling missing values
- Data type conversions
- Rounding values according to tariff rules (seconds to minutes, MB to GB)
- Merging data from multiple tables

### 2. Revenue Calculation
- Calculation of monthly revenue per user
- Consideration of:
  - Base monthly fee
  - Overage charges for calls (beyond included minutes)
  - Overage charges for messages (beyond included messages)
  - Overage charges for internet (beyond included GB)

### 3. Statistical Analysis
- Descriptive statistics for each tariff group
- Comparison of average revenues
- Statistical hypothesis testing using t-tests
- Analysis by geographic region (Moscow vs. other regions)

## Key Findings

### Hypothesis 1: Revenue Difference Between Tariffs
- **Result**: The average revenue of "Ultra" and "Smart" tariff users differs significantly
- Statistical test (t-test) confirms the difference with p-value < 0.05
- The analysis reveals which tariff generates more revenue per user

### Hypothesis 2: Revenue Difference by Region
- **Result**: Analysis of Moscow vs. other regions
- Comparison of average revenue between Moscow users and users from other regions
- Statistical testing to confirm or reject the hypothesis

### Customer Behavior Insights
- Usage patterns for calls, messages, and internet
- Distribution of users across tariff plans
- Regional differences in service usage
- Overage patterns and their impact on revenue

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualization
- **SciPy**: Statistical testing (t-tests)
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_04/
├── 220331_mk_project_4_vChecked.ipynb    # Main project notebook (checked version)
├── 220316_mk_project_4_vShared.ipynb      # Shared version
├── _old/                                   # Previous versions
└── README.md                               # This file
```

## Results

The analysis provides actionable insights for the commercial department:

1. **Revenue Comparison**: Clear understanding of which tariff generates more revenue
2. **Regional Insights**: Identification of revenue differences between Moscow and other regions
3. **Customer Behavior**: Understanding of how customers use services and generate overage charges
4. **Business Recommendations**: Data-driven guidance for advertising budget allocation

The project demonstrates the importance of:
- Proper data preprocessing and merging
- Accurate revenue calculation based on tariff rules
- Statistical hypothesis testing for business decisions
- Understanding customer behavior patterns

These findings enable Megaline to make informed decisions about marketing strategies and tariff plan optimization.
