# Module 07: Hypothesis Prioritization and A/B Testing

## Overview

This project focuses on prioritizing hypotheses for increasing revenue at a large online store and analyzing the results of an A/B test. Working with the marketing department, hypotheses are prioritized using frameworks like ICE (Impact, Confidence, Effort) or RICE (Reach, Impact, Confidence, Effort), then an A/B test is launched and analyzed.

## Objectives

1. **Prioritize hypotheses** using a structured framework (ICE or RICE)
2. **Launch an A/B test** based on prioritized hypotheses
3. **Analyze A/B test results** to determine statistical significance
4. **Make data-driven recommendations** about implementing changes

## Data Description

### Hypotheses Table (`hypothesis.csv`)
Contains hypotheses prepared by the marketing department:

1. `Hypothesis` — brief description of the hypothesis
2. `Reach` — user reach on a 10-point scale
3. `Impact` — impact on users on a 10-point scale
4. `Confidence` — confidence in the hypothesis on a 10-point scale
5. `Efforts` — resource costs to test the hypothesis on a 10-point scale (higher = more expensive)

### Orders Table (`orders.csv`)
Information about orders:

1. `transactionId` — order identifier
2. `visitorId` — identifier of the user who made the order
3. `date` — date when the order was made
4. `revenue` — order revenue
5. `group` — A/B test group (A or B)

### Visitors Table (`visitors.csv`)
Information about visitors:

1. `date` — date
2. `group` — A/B test group (A or B)
3. `visitors` — number of users on the specified date in the specified A/B test group

## Methodology

### 1. Hypothesis Prioritization
- Application of ICE framework: Impact × Confidence / Effort
- Application of RICE framework: Reach × Impact × Confidence / Effort
- Ranking of hypotheses by priority score
- Identification of top hypotheses for testing

### 2. A/B Test Analysis
- **Data Quality Check**:
  - Verification of test duration
  - Check for overlapping users between groups
  - Analysis of visitor distribution
  - Identification of anomalies

- **Statistical Analysis**:
  - Calculation of conversion rates by group
  - Statistical significance testing
  - Analysis of revenue per visitor
  - Cumulative metrics analysis

- **Visualization**:
  - Conversion rate trends over time
  - Revenue comparison charts
  - Statistical significance indicators

### 3. Statistical Testing
- Z-test for proportions (conversion rates)
- T-test for means (revenue per visitor)
- Confidence intervals
- P-value interpretation
- Effect size calculation

## Key Findings

### Hypothesis Prioritization
- Top hypotheses identified using ICE/RICE frameworks
- Clear ranking of hypotheses by potential impact
- Resource allocation recommendations
- Testing sequence suggestions

### A/B Test Results
- **Conversion Rate Analysis**:
  - Comparison of conversion rates between groups A and B
  - Statistical significance of differences
  - Trend analysis over time

- **Revenue Analysis**:
  - Average revenue per visitor comparison
  - Total revenue impact
  - Revenue distribution analysis

- **Statistical Conclusions**:
  - Whether the test shows statistically significant results
  - Confidence level in the findings
  - Recommendations for implementation

### Business Recommendations
- Whether to implement the tested changes
- Expected impact on key metrics
- Risk assessment
- Next steps for further testing

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualization
- **SciPy**: Statistical testing (z-tests, t-tests)
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_07/
├── 220731_mk_project_7_vChecked.ipynb    # Main project notebook (checked version)
├── 220731_mk_project_7_vF.ipynb          # Final version
├── _old/                                   # Previous versions
└── README.md                               # This file
```

## Results

The project successfully demonstrates:

1. **Structured Prioritization**: Use of frameworks to objectively rank hypotheses
2. **Rigorous Testing**: Proper A/B test design and execution
3. **Statistical Approach**: Appropriate use of statistical tests to validate results
4. **Business Impact**: Clear recommendations based on data analysis

**Key Learnings**:
- Importance of hypothesis prioritization before testing
- Need for proper statistical analysis in A/B testing
- Value of cumulative metrics in understanding test results
- Critical role of data quality checks before analysis

The analysis provides actionable insights for the marketing department to make data-driven decisions about which changes to implement, ultimately improving the online store's revenue and user experience.
