# Module 10: Mobile App Font Experiments (A/A/B Testing)

## Overview

This project analyzes user behavior in a mobile food delivery app and investigates the results of an A/A/B experiment. The design team wanted to change fonts throughout the app, but managers were concerned about user unfamiliarity. The decision was made to conduct an A/A/B test with users split into 3 groups: 2 control groups (246 and 247) with old fonts and one experimental group (248) with new fonts.

## Objectives

1. **Funnel Analysis**: Understand the sales funnel and identify where users drop off
2. **A/A/B Test Analysis**: Determine if the new font design improves user experience
3. **Statistical Testing**: Validate test results using appropriate statistical methods
4. **Business Recommendations**: Provide data-driven recommendations about font implementation

## Data Description

The dataset `logs_exp.csv` contains event logs from the mobile application:

1. `EventName` — event name
2. `DeviceIDHash` — unique user identifier
3. `EventTimestamp` — event timestamp
4. `ExpId` — experiment number (246, 247, or 248)

### Event Types
The funnel typically includes events such as:
- `MainScreenAppear` — user opened the app
- `OffersScreenAppear` — user viewed offers
- `CartScreenAppear` — user viewed cart
- `PaymentScreenSuccessful` — user completed payment
- `Tutorial` — user completed tutorial

## Methodology

### 1. Data Preprocessing
- Data loading and initial exploration
- Timestamp conversion and handling
- Data filtering (removing development/testing periods)
- Identification of the analysis period
- Data quality assessment

### 2. Funnel Analysis
- **Funnel Construction**:
  - Identification of funnel steps
  - Calculation of conversion rates at each step
  - Drop-off analysis between steps
  - Visualization of the funnel

- **Funnel Metrics**:
  - Overall conversion rate
  - Step-by-step conversion rates
  - Drop-off percentages
  - User flow analysis

### 3. A/A/B Test Analysis
- **Data Filtering**:
  - Selection of relevant time period
  - Removal of development/testing data
  - Focus on production user behavior

- **Group Comparison**:
  - Comparison of control groups (246 vs 247) to validate A/A test
  - Comparison of experimental group (248) vs control groups
  - Event-level analysis
  - Conversion rate comparison

- **Statistical Testing**:
  - Z-test for proportions (conversion rates)
  - Chi-square tests for categorical data
  - Multiple comparison correction (if needed)
  - Confidence intervals
  - P-value interpretation

### 4. Event Analysis
- Analysis of each event type separately
- Understanding of user behavior patterns
- Identification of events affected by font change
- Time-based analysis of events

## Key Findings

### Funnel Analysis
- **Conversion Funnel**: Clear visualization of user journey
- **Drop-off Points**: Identification of steps where users most frequently drop off
- **Conversion Rates**: Quantification of conversion at each funnel stage
- **Bottlenecks**: Steps that need optimization

### A/A Test Validation
- **Control Group Comparison**: Validation that groups 246 and 247 show no significant differences
- **Test Validity**: Confirmation that the A/A test setup is correct
- **Baseline Establishment**: Understanding of normal variation between groups

### A/B Test Results
- **Font Impact**: Whether the new font (group 248) shows significant differences
- **Event-Level Analysis**: Which specific events are affected
- **User Experience**: Overall impact on user behavior
- **Statistical Significance**: Confidence in the results

### Business Recommendations
- **Implementation Decision**: Whether to implement the new font
- **Expected Impact**: Quantified impact on key metrics
- **Risk Assessment**: Potential risks and benefits
- **Next Steps**: Recommendations for further testing or implementation

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualization
- **SciPy**: Statistical testing (z-tests, chi-square tests)
- **Math**: Mathematical functions
- **Datetime**: Date and time handling
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_10_mix/
├── 221103_mk_project_10_vChecked.ipynb    # Main project notebook (checked version)
├── 221017_mk_project_10_v01.ipynb         # Initial version
└── README.md                                # This file
```

## Results

The analysis provides clear insights for decision-making:

1. **Funnel Understanding**: Complete picture of user journey and conversion points
2. **Test Validity**: Confirmation that the A/A/B test was properly conducted
3. **Font Impact**: Data-driven assessment of whether new fonts improve user experience
4. **Statistical Confidence**: Rigorous statistical validation of results

**Key Business Impact**:
- Evidence-based decision on font implementation
- Understanding of user behavior patterns
- Identification of optimization opportunities in the funnel
- Foundation for future A/B testing practices

**Key Learnings**:
- Importance of proper test design (A/A/B vs A/B)
- Need for statistical rigor in test analysis
- Value of funnel analysis in understanding user behavior
- Critical role of data filtering (removing development periods)

The project demonstrates the importance of proper experimental design and statistical analysis in making product decisions, ensuring that changes are based on data rather than assumptions.
