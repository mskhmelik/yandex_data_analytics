# Module 05: Computer Game Sales Analysis

## Overview

This project analyzes historical data about game sales, user and expert reviews, genres, and platforms (e.g., Xbox or PlayStation) to identify patterns that determine game success. This analysis helps make informed decisions about potentially popular products and plan advertising campaigns.

## Objectives

- Identify patterns that determine game success
- Analyze sales trends across different platforms, genres, and regions
- Understand the relationship between game characteristics and sales performance
- Provide recommendations for game development and marketing strategies
- Analyze regional preferences (North America, Europe, Japan, Other regions)

## Data Description

The dataset contains information about games with the following columns:

1. `Name` — game title
2. `Platform` — gaming platform
3. `Year_of_Release` — year of release
4. `Genre` — game genre
5. `NA_sales` — sales in North America (millions of copies sold)
6. `EU_sales` — sales in Europe (millions of copies sold)
7. `JP_sales` — sales in Japan (millions of copies sold)
8. `Other_sales` — sales in other countries (millions of copies sold)
9. `Critic_Score` — critics' rating (maximum 100)
10. `User_Score` — users' rating (maximum 10)
11. `Rating` — ESRB rating (Entertainment Software Rating Board) - age category

## Methodology

### 1. Data Preprocessing
- Examination of column names and data types
- Handling missing values (NaNs)
- Identification and removal of duplicates
- Data type conversions (e.g., User_Score from object to numeric)
- Handling of artifacts and inconsistencies
- Standardization of column names

### 2. Exploratory Data Analysis
- Analysis of sales trends over time
- Platform popularity analysis
- Genre distribution and popularity
- Regional sales patterns (NA, EU, JP, Other)
- Relationship between ratings and sales
- ESRB rating distribution

### 3. Regional Analysis
- Comparison of platform preferences across regions
- Genre preferences by region
- Sales volume comparisons
- Identification of region-specific trends

### 4. Time Series Analysis
- Sales trends by year
- Platform lifecycle analysis
- Identification of peak sales periods
- Analysis of platform decline and growth

## Key Findings

### Sales Trends
- Significant drop in game sales in 2013-2014 (more than 50% decline from peak)
- Peak sales occurred in earlier years
- Market recovery patterns in subsequent years

### Platform Analysis
- **PS4** and **XOne** showed growth during the analyzed period
- PS4 sales increased almost 6 times
- XOne sales doubled
- Other platforms showed declining sales
- Platforms have a lifecycle with periods of growth and decline

### Regional Differences
- **North America and Europe**: Similar preferences for platforms and genres
  - Action genre dominates
  - Shooter genre shows high average sales
  - PS, Xbox, and PC are popular platforms
- **Japan**: Distinct market with different preferences
  - Strong preference for mobile platforms
  - RPG genre is highly popular (second only to Action)
  - Different platform preferences compared to Western markets
  - Younger demographic (reflected in ESRB rating analysis)

### Genre Analysis
- **Action** genre remains first in most regions
- **Shooter** genre has high average sales in North America and Europe
- **RPG** is particularly strong in Japan
- Genre preferences vary significantly by region

### Recommendations
- Focus on **Shooter** genre for North America and Europe markets
- Target platforms: **PS**, **Xbox**, and **PC** for Western markets
- Consider mobile platforms for Japanese market
- Account for platform lifecycle when planning releases
- Investigate the 2013-2014 sales decline to understand market dynamics

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Static data visualization
- **Seaborn**: Statistical data visualization
- **SciPy**: Statistical analysis
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_05_mix/
├── 220505_mk_project_5_vChecked.ipynb    # Main project notebook (checked version)
├── 220413_mk_project_5_vF.ipynb          # Final version
├── _old/                                   # Previous versions
└── README.md                               # This file
```

## Results

The analysis reveals critical insights for game development and marketing:

1. **Market Segmentation**: Clear differences between Western markets (NA/EU) and Japanese market
2. **Platform Strategy**: Understanding of platform lifecycles and regional preferences
3. **Genre Strategy**: Identification of high-performing genres by region
4. **Market Dynamics**: Recognition of significant sales decline that requires investigation

**Key Business Insights**:
- The market is highly regionalized with distinct preferences
- Platform choices should align with target regions
- Genre selection significantly impacts sales potential
- Market timing and platform lifecycle are crucial factors

The project demonstrates the importance of regional analysis in the gaming industry and provides actionable recommendations for game development and marketing strategies.
