# Module 12.2: A/B Testing Final Project

## Overview

This project evaluates the results of an A/B test for a recommender system. The analysis includes assessing the correctness of test implementation and analyzing test results. The project involves checking for issues like audience overlap with competing tests, alignment with marketing events, and temporal boundary problems.

## Objectives

1. **Test Implementation Assessment**:
   - Verify data compliance with technical specifications
   - Check test timing (no overlap with marketing events)
   - Validate test audience (no overlaps, correct group distribution)
   - Ensure proper test group formation

2. **Exploratory Data Analysis**:
   - Event distribution analysis
   - Funnel conversion analysis
   - Data quality assessment
   - Identification of data peculiarities

3. **A/B Test Results Evaluation**:
   - Statistical significance testing
   - Conversion rate comparison
   - Revenue impact analysis
   - Business recommendations

## Technical Specification

- **Test Name**: `recommender_system_test`
- **Groups**: A (control) - old payment funnel, B (test) - new payment funnel
- **Launch Date**: December 7, 2020
- **Stop Collecting New Users**: December 21, 2020
- **End Date**: January 4, 2021
- **Audience**: 15% of new users from EU region
- **Objective**: Testing changes related to improved recommender system implementation
- **Expected Participants**: 6,000 users
- **Expected Effect**: Within 14 days from registration, users should show at least 10% improvement for each metric:
  - Conversion to product page views (event: `product_page`)
  - Views of product cart (event: `product_cart`)
  - Purchases (event: `purchase`)

## Data Description

### Marketing Events (`ab_project_marketing_events.csv`)
Calendar of marketing events for 2020:
1. `name` — marketing event name
2. `regions` — regions where the campaign takes place
3. `start_dt` — campaign start date
4. `finish_dt` — campaign end date

### New Users (`final_ab_new_users.csv`)
Users who registered from December 7 to December 21, 2020:
1. `user_id` — user identifier
2. `first_date` — registration date
3. `region` — user's region
4. `device` — device used for registration

### Events (`final_ab_events.csv`)
Actions of new users from December 7, 2020, to January 4, 2021:
1. `user_id` — user identifier
2. `event_dt` — date and time of event
3. `event_name` — event type
4. `details` — additional event data (for purchases, contains cost in dollars)

### Test Participants (`final_ab_participants.csv`)
Table of test participants:
1. `user_id` — user identifier
2. `ab_test` — test name
3. `group` — user group (A or B)

## Methodology

### 1. Data Exploration
- Type conversions
- Identification of missing values
- Duplicate detection
- Data quality assessment

### 2. Test Implementation Assessment

#### 2.1 Technical Specification Compliance
- Verification of all specification points
- Group distribution check
- Audience size validation
- Date range verification

#### 2.2 Test Timing
- Check for overlap with marketing events
- Verification of test period boundaries
- Identification of external factors

#### 2.3 Test Audience
- Check for overlaps with competing tests
- Verification of no users in both groups
- Uniform distribution check
- Correct group formation validation

### 3. Exploratory Data Analysis

#### 3.1 Event Distribution
- Are events per user evenly distributed in samples?
- Event distribution over days
- User activity patterns

#### 3.2 Funnel Analysis
- Conversion at different funnel stages
- Comparison between groups
- Drop-off analysis

#### 3.3 Data Quality
- Identification of data peculiarities
- Issues to consider before A/B testing
- Data cleaning requirements

### 4. A/B Test Results Evaluation

#### 4.1 Statistical Analysis
- Z-test for proportions (conversion rates)
- Statistical significance testing
- Confidence intervals
- Effect size calculation

#### 4.2 Business Metrics
- Conversion rate comparison
- Revenue impact
- User behavior changes
- Expected vs. actual results

### 5. Conclusions
- Overall assessment of test implementation
- Validity of test results
- Business recommendations
- Next steps

## Key Findings

### Test Implementation
- **Compliance**: Assessment of technical specification adherence
- **Timing**: Evaluation of test period appropriateness
- **Audience**: Validation of group formation and distribution

### Data Quality
- Event distribution patterns
- Data completeness
- Issues affecting analysis

### Test Results
- **Statistical Significance**: Whether differences are statistically significant
- **Conversion Impact**: Effect on key conversion metrics
- **Business Impact**: Quantified impact on business metrics
- **Expected vs. Actual**: Comparison with expected 10% improvement

### Recommendations
- Whether to implement the new recommender system
- Risk assessment
- Next steps for further testing or implementation

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Math**: Mathematical functions
- **Plotly**: Interactive data visualization
- **SciPy**: Statistical testing (z-tests)
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_12_2_final/
├── prj_ab_test.ipynb    # Main project notebook
└── README.md             # This file
```

## Results

The comprehensive analysis provides:

1. **Test Validity**: Assessment of whether the test was properly conducted
2. **Statistical Results**: Rigorous statistical analysis of test outcomes
3. **Business Impact**: Quantified impact on key business metrics
4. **Implementation Guidance**: Clear recommendations for next steps

**Key Learnings**:
- Importance of proper test design and implementation
- Critical role of data quality checks
- Need for comprehensive test validation
- Value of statistical rigor in A/B testing

**Business Impact**:
- Evidence-based decision on recommender system implementation
- Understanding of test validity and reliability
- Identification of potential issues in test execution
- Foundation for future A/B testing practices

The project demonstrates advanced skills in A/B testing, including test design validation, statistical analysis, and business interpretation of results.
