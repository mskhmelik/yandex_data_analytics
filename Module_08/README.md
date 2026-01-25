# Module 08: Cafes in Moscow - Market Research

## Overview

This project conducts market research for investors from the "Shut Up and Take My Money" fund who want to open a food establishment in Moscow. The investors haven't decided on the type of establishment (cafe, restaurant, pizzeria, pub, or bar), location, menu, or pricing. The analysis identifies interesting market features and presents findings to help inform their decision.

## Objectives

- Analyze the Moscow food establishment market
- Identify market patterns and opportunities
- Provide insights on:
  - Establishment types and their distribution
  - Location patterns and optimal areas
  - Pricing strategies
  - Rating distributions
  - Chain vs. independent establishments
  - Seating capacity analysis
- Create visualizations including interactive maps
- Present actionable recommendations for investors

## Data Description

The dataset `moscow_places.csv` contains information about food establishments in Moscow:

1. `name` — establishment name
2. `address` — establishment address
3. `category` — establishment category (e.g., "cafe", "pizzeria", "coffee shop")
4. `hours` — information about days and hours of operation
5. `lat` — latitude of the geographic point
6. `lng` — longitude of the geographic point
7. `rating` — establishment rating based on Yandex Maps user reviews
8. `price` — price category (e.g., "average", "below average", "above average")
9. `avg_bill` — string containing average order cost as a range
10. `middle_avg_bill` — numeric estimate of average bill (only for values starting with "Average bill")
11. `middle_coffee_cup` — numeric estimate of one cup of cappuccino (only for values starting with "Price of one cup of cappuccino")
12. `chain` — number (0 or 1) indicating if the establishment is part of a chain
13. `district` — administrative district where the establishment is located
14. `seats` — number of seating places

**Additional Data**:
- `admin_level_geomap.geojson` — GeoJSON file with administrative boundaries for mapping

## Methodology

### 1. Data Preprocessing
- Data loading and initial exploration
- Handling missing values
- Data type conversions
- Standardization of categorical variables
- Geographic data preparation
- Price category normalization

### 2. Exploratory Data Analysis
- **Category Analysis**:
  - Distribution of establishment types
  - Popular categories
  - Category-specific characteristics

- **Geographic Analysis**:
  - Distribution across districts
  - Density mapping
  - Identification of high-traffic areas
  - Location patterns by category

- **Pricing Analysis**:
  - Price category distribution
  - Average bill analysis
  - Price vs. rating relationships
  - Category-specific pricing patterns

- **Rating Analysis**:
  - Rating distributions
  - Rating by category
  - Rating by district
  - Rating vs. price relationships

- **Chain Analysis**:
  - Chain vs. independent distribution
  - Performance comparison
  - Market share analysis

- **Capacity Analysis**:
  - Seating capacity distributions
  - Capacity by category
  - Optimal capacity insights

### 3. Visualization
- Interactive maps using Folium
- Heatmaps of establishment density
- Marker clusters for geographic visualization
- Bar charts and histograms for distributions
- Scatter plots for relationships
- District-level analysis maps

### 4. Market Insights
- Identification of market gaps
- Competitive landscape analysis
- Opportunity identification
- Risk assessment

## Key Findings

### Market Structure
- Distribution of establishment types across Moscow
- Dominant categories and market saturation
- Opportunities in underserved categories

### Geographic Patterns
- High-density areas for food establishments
- District-level preferences
- Location strategies for different establishment types
- Areas with growth potential

### Pricing Insights
- Price category distributions
- Relationship between price and ratings
- Optimal pricing strategies by category
- Market positioning opportunities

### Rating Analysis
- Rating distributions and patterns
- Factors affecting ratings
- Category-specific rating benchmarks
- Opportunities for quality improvement

### Chain vs. Independent
- Market share comparison
- Performance differences
- Advantages and disadvantages of each model

### Recommendations
- Suggested establishment type based on market analysis
- Recommended locations with justification
- Pricing strategy recommendations
- Capacity planning insights

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Static data visualization
- **Plotly**: Interactive data visualization
- **Folium**: Interactive mapping and geographic visualization
- **JSON**: GeoJSON data handling
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_08/
├── 221116_mk_project_8_vF.ipynb          # Main project notebook (final version)
├── 221115_mk_project_8_vF.pptx           # Presentation
├── admin_level_geomap.geojson             # Geographic data
├── Code examples/                          # Additional code examples
│   ├── 221104_geo_cluster_example.ipynb
│   ├── 221104_geo_custom_marker_example.ipynb
│   ├── 221104_geo_example.ipynb
│   ├── 221104_geo_heatmap_example.ipynb
│   ├── 221104_geo_marker_example.ipynb
│   └── 221104_plotly_example.ipynb
├── _old/                                   # Previous versions
└── README.md                               # This file
```

## Results

The analysis provides comprehensive market insights for investors:

1. **Market Overview**: Clear understanding of the Moscow food establishment landscape
2. **Location Strategy**: Data-driven recommendations for optimal locations
3. **Category Selection**: Insights on which establishment types have the best opportunities
4. **Pricing Strategy**: Recommendations for competitive pricing
5. **Competitive Analysis**: Understanding of market saturation and competition

**Key Business Impact**:
- Informed decision-making for establishment type
- Strategic location selection based on data
- Understanding of market dynamics and opportunities
- Risk mitigation through comprehensive analysis

The project demonstrates the value of data-driven market research in making critical business decisions, providing investors with actionable insights to maximize their chances of success in the competitive Moscow food market.
