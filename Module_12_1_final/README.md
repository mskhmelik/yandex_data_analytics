# Module 12.1: Space Brothers - Game Analytics Final Project

## Overview

This project analyzes user acquisition data for "Space Brothers," a new game where users can build different buildings and fight other users. The marketing department needs to understand which traffic sources work well and which work poorly to optimize advertising costs in the long term. Since monetization is not yet implemented, intermediate metrics like time in game, number of buildings constructed, and completion of the first level are used to evaluate channel effectiveness.

## Objectives

- Analyze user acquisition sources and their effectiveness
- Calculate key metrics for each traffic source:
  - User acquisition costs
  - User retention and engagement
  - Time in game
  - Building construction activity
  - Level completion rates
- Identify which sources are performing well vs. poorly
- Provide recommendations for optimizing advertising spend
- Test specific hypotheses about user behavior

## Data Description

### Game Actions Dataset (`game_actions.csv`)
Contains data about user actions on the first level. Completing the first level requires either:
1. Defeating the first enemy (PvP)
2. Completing a project - developing an orbital satellite assembly (PvE)

The dataset contains data for the first user cohort (users who started using the app between May 4-10, inclusive). The day a user opens the app is considered the day they saw the advertisement.

1. `event_datetime` — event timestamp
2. `event` — one of three event types
3. `building_type` — one of three building types
4. `user_id` — user identifier
5. `project_type` — type of completed project

### Ad Costs Dataset (`ad_costs.csv`)
Contains costs for attracting users by day and source. To attract users on May 4, advertising was paid on May 3, etc.

1. `day` — day when the ad click occurred
2. `source` — traffic source
3. `cost` — cost of clicks

### User Source Dataset (`user_source.csv`)
Contains user-source mapping:

1. `user_id` — user identifier
2. `source` — source from which the user who installed the app came

## Methodology

### 1. Data Preprocessing
- Data loading and initial exploration
- Handling missing values and data types
- Date and time conversions
- Merging datasets
- Data quality assessment

### 2. Exploratory Data Analysis
- **User Metrics**:
  - Total number of users by source
  - Users who completed the game
  - Time spent in game
  - User retention patterns

- **Event Analysis**:
  - Total events by period
  - Completed projects
  - Buildings constructed
  - Event distribution by source

- **Source Analysis**:
  - User distribution by traffic source
  - Acquisition costs by source
  - Cost per user calculations
  - Source performance comparison

### 3. Hypothesis Testing
- **Hypothesis 1**: Time to complete level differs depending on completion method (PvP vs PvE)
- **Hypothesis 2**: Number of buildings constructed differs between Yandex and Facebook sources
- Statistical testing using appropriate methods
- Interpretation of results

### 4. Financial Analysis
- Cost per acquisition (CAC) by source
- User lifetime value indicators
- Return on investment (ROI) calculations
- Cost efficiency rankings

### 5. Recommendations
- Sources to increase investment in
- Sources to reduce or eliminate
- Optimization strategies
- Focus areas for improvement

## Key Findings

### User Acquisition Performance
- Identification of high-performing traffic sources
- Discovery of underperforming sources
- Cost efficiency analysis
- User quality by source

### User Behavior Patterns
- Completion method preferences (PvP vs PvE)
- Time to completion analysis
- Engagement levels by source
- Building construction patterns

### Hypothesis Results
- **Hypothesis 1**: Results regarding completion time differences
- **Hypothesis 2**: Results regarding building construction differences
- Statistical significance of findings
- Business implications

### Financial Insights
- Cost per user by source
- User value indicators
- ROI calculations
- Budget allocation recommendations

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Plotly**: Interactive data visualization
- **SciPy**: Statistical testing
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_12_1_final/
├── prj_space_brothers.ipynb    # Main project notebook
├── ppt_space_brothers.pptx      # Presentation
└── README.md                     # This file
```

## Results

The analysis provides critical insights for optimizing user acquisition:

1. **Source Performance**: Clear ranking of traffic sources by effectiveness
2. **Cost Optimization**: Identification of cost-efficient acquisition channels
3. **User Quality**: Understanding of which sources bring better users
4. **Behavioral Insights**: Patterns in how users from different sources engage

**Key Business Impact**:
- Data-driven budget reallocation recommendations
- Identification of profitable vs. unprofitable sources
- Understanding of user behavior patterns
- Foundation for scaling successful channels

**Presentation**: The project includes a comprehensive presentation summarizing findings and recommendations for stakeholders.

The project demonstrates advanced analytics skills in game analytics, combining user behavior analysis, financial metrics, and statistical testing to provide actionable business recommendations.
