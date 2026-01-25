# Module 01: Music of Big Cities

## Overview

This project analyzes user behavior data from Yandex.Music to compare music listening patterns between Moscow and St. Petersburg. The analysis tests common cultural stereotypes about these two major Russian cities and their musical preferences.

## Objectives

The research aims to test three hypotheses:

1. **User activity patterns**: User activity depends on the day of the week, and this pattern differs between Moscow and St. Petersburg.
2. **Genre preferences by time**: On Monday mornings, different music genres dominate in Moscow compared to St. Petersburg. Similarly, on Friday evenings, genre preferences vary by city.
3. **Overall genre preferences**: Moscow and St. Petersburg have distinct genre preferences: pop music is more popular in Moscow, while Russian rap is more common in St. Petersburg.

## Data Description

The dataset `yandex_music_project.csv` contains user behavior data from Yandex.Music, including:

- User listening activity by day of week
- Music genre preferences
- City location (Moscow vs St. Petersburg)
- Time-based listening patterns

**Data Quality**: The quality of the data was unknown initially, requiring thorough data exploration and preprocessing to identify and correct critical issues.

## Methodology

### 1. Data Overview
- Initial examination of dataset structure
- Identification of data types and missing values
- Assessment of data quality issues

### 2. Data Preprocessing
- Handling missing values
- Correcting data type inconsistencies
- Standardizing column names
- Removing duplicates and outliers

### 3. Hypotheses Testing
- **Hypothesis 1**: Comparison of user activity across weekdays (Monday, Wednesday, Friday) between the two cities
- **Hypothesis 2**: Analysis of genre preferences during specific time periods (Monday mornings, Friday evenings)
- **Hypothesis 3**: Overall genre popularity comparison between cities

## Key Findings

### Hypothesis 1: User Activity Patterns
- **Confirmed**: The day of the week affects user activity differently in Moscow and St. Petersburg
- In Moscow: Peak listening activity occurs on Monday and Friday, with a noticeable decline on Wednesday
- In St. Petersburg: Music is listened to more on Wednesdays, with Monday and Friday showing almost equally lower activity

### Hypothesis 2: Genre Preferences by Time
- **Partially Confirmed**: Musical preferences do not change significantly during the week in either city
- Small differences are noticeable on Mondays:
  - Moscow: "World" genre is popular
  - St. Petersburg: Jazz and classical music are preferred
- Note: Missing data may have affected the reliability of this analysis

### Hypothesis 3: Overall Genre Preferences
- **Not Confirmed**: The music tastes of users in Moscow and St. Petersburg are more similar than different
- Contrary to expectations, St. Petersburg's genre preferences resemble those of Moscow
- If differences exist, they are not noticeable for the majority of users

### Additional Insights
- Pop is the most popular genre overall (5,409 listens), followed by dance (4,126) and rock (3,754)
- Moscow shows higher listening activity overall, with strong preferences for pop, dance, and electronic genres
- St. Petersburg has notable engagement with classical and jazz, reflecting more diverse musical taste
- The "unknown" genre ranks relatively high, indicating significant missing or unclassified data

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
Module_01/
├── project_1.ipynb          # Main project notebook
└── README.md                 # This file
```

## Results

The analysis revealed that while some stereotypes about Moscow and St. Petersburg hold true (particularly regarding activity patterns), the cities' musical preferences are more similar than different. The research demonstrates the importance of data-driven analysis over assumptions and highlights the need for statistical hypothesis testing to validate findings based on available data.

**Note**: In practice, research involves statistical hypothesis testing. Data from a single service does not always provide conclusions about all residents of a city. Statistical hypothesis testing can show the reliability of results based on available data.
