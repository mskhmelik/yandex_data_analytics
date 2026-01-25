# Module 02: Investigating Borrower Reliability

## Overview

This project analyzes client data from a bank's credit department to determine whether a client's marital status and number of children impact timely loan repayment. The results inform the development of a credit scoring model—a specialized system that evaluates a potential borrower's ability to repay a loan.

## Objectives

The research aims to test four hypotheses:

1. **Children and loan repayment**: Is there a correlation between having children and repaying a loan on time?
2. **Marital status and loan repayment**: Is there a correlation between marital status and repaying a loan on time?
3. **Income level and loan repayment**: Is there a correlation between income level and repaying a loan on time?
4. **Loan purpose and repayment**: How do different loan purposes affect the timely repayment of loans?

## Data Description

The dataset consists of 12 columns with information about bank clients:

1. `children` — the number of children in the family
2. `days_employed` — total employment history in days
3. `dob_years` — client's age in years
4. `education` — client's education level
5. `education_id` — identifier for the education level
6. `family_status` — marital status
7. `family_status_id` — identifier for the marital status
8. `gender` — client's gender
9. `income_type` — type of employment
10. `debt` — whether the client had debt related to loan repayment (yes/no)
11. `total_income` — monthly income
12. `purpose` — purpose of the loan

Each row represents a client. The data includes both categorical variables (education, income_type) and quantitative variables (total_income, children).

## Methodology

### 1. Data Preprocessing
- Standardization of data formats
- Handling missing values
- Removing duplicates
- Creating distinct categories for analysis
- Data type conversions
- Identification and correction of data artifacts

### 2. Hypothesis Testing
For each hypothesis, the analysis:
- Creates pivot tables comparing categories
- Calculates repayment rates by category
- Compares proportions across different segments
- Uses a 3% threshold to determine statistical significance (difference between categories)

### 3. Analysis Approach
- Categorical analysis of repayment rates
- Comparison of repayment probabilities across different client segments
- Identification of patterns and dependencies

## Key Findings

### Hypothesis 1: Children and Loan Repayment
- **Weak relationship**: The number of children has a weak influence on loan repayment probability
- Slight trend: Higher number of children corresponds to a lower repayment probability
- Overall repayment rate remains around 90% across all categories
- **Conclusion**: No significant relationship found based on the 3% threshold criteria

### Hypothesis 2: Marital Status and Loan Repayment
- **Significant impact**: Marital status has a notable effect on repayment rates
- Registered partnerships show higher repayment rates (around 93%)
- Civil partnerships and single individuals show lower rates (around 90%)
- Widowed individuals show the highest reliability (though sample size is relatively small)
- **Conclusion**: Dependency confirmed - marital status affects repayment probability

### Hypothesis 3: Income Level and Loan Repayment
- **Moderate relationship**: Income level plays a role in loan repayment probability
- Lower income levels generally associated with lower likelihood of repayment
- Category 'D' stands out as the most reliable, despite uneven income distribution
- **Conclusion**: Dependency confirmed - income level affects repayment rates

### Hypothesis 4: Loan Purpose and Repayment
- **Unexpected result**: Loans for real estate operations and wedding expenses have lower repayment rates
- Loans for education and car-related operations show higher repayment rates
- Difference is around 2%, which is noticeable but not dramatic
- **Conclusion**: Loan purpose influences repayment probability

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Plotly**: Interactive data visualization
  - `plotly.express` for quick visualizations
  - `plotly.graph_objects` for custom charts
  - `plotly.subplots` for multi-panel visualizations
- **Caseconverter**: String case conversion utilities
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_02/
├── prj_credit_score.ipynb    # Main project notebook
└── README.md                  # This file
```

## Results

The analysis successfully completed the entire data analysis cycle, from data loading to hypothesis testing. Key conclusions:

1. **Children**: Weak influence on repayment, with slight negative correlation
2. **Marital Status**: Significant impact - registered partnerships are more reliable
3. **Income Level**: Moderate relationship - higher income generally correlates with better repayment
4. **Loan Purpose**: Unexpected patterns - education and car loans show better repayment than real estate and wedding loans

These findings provide valuable insights for financial institutions in:
- Assessing loan applications
- Managing credit risk
- Developing credit scoring models
- Understanding factors that influence borrower reliability

The analysis demonstrates the importance of data-driven decision making in credit risk assessment, moving beyond assumptions to identify actual patterns in borrower behavior.
