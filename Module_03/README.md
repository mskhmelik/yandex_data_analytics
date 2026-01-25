# Module 03: Market Value of Real Estate Properties

## Overview

This project analyzes data from the Yandex Real Estate service, which contains an archive of apartment sale listings in St. Petersburg and neighboring areas over several years. The objective is to determine parameters for accurately estimating the market value of real estate properties, enabling the development of an automated system to identify anomalies and fraudulent activities.

## Objectives

- Identify key factors that influence apartment prices
- Analyze the relationship between property characteristics and market value
- Detect anomalies and potential fraudulent listings
- Understand how location, property features, and other variables affect pricing
- Provide insights for automated property valuation systems

## Data Description

The dataset consists of 22 columns with information about apartment listings:

### Location Data
- `locality_name` - Name of the locality (city or town)
- `cityCenters_nearest` - Distance to the city center in meters
- `airports_nearest` - Distance to the nearest airport in meters
- `parks_nearest` - Distance to the nearest park in meters
- `parks_around3000` - Number of parks within a 3-kilometer radius
- `ponds_nearest` - Distance to the nearest body of water (pond) in meters
- `ponds_around3000` - Number of bodies of water within a 3-kilometer radius

### Property Characteristics
- `total_area` - Total area of the apartment in square meters
- `living_area` - Area of the living space in square meters
- `kitchen_area` - Area of the kitchen in square meters
- `rooms` - Number of rooms in the apartment
- `ceiling_height` - Height of the ceilings in meters
- `floor` - Floor on which the apartment is located
- `floors_total` - Total number of floors in the building
- `balcony` - Number of balconies in the apartment

### Property Type
- `is_apartment` - Indicates whether the property is an apartment (non-residential premises)
- `studio` - Indicates whether the apartment is a studio
- `open_plan` - Indicates whether the apartment has an open floor plan

### Listing Information
- `last_price` - Price of the apartment at the time of withdrawal from publication
- `first_day_exposition` - Date of the listing publication
- `days_exposition` - Duration in days for which the listing was active
- `total_images` - Number of photographs of the apartment included in the listing

**Note**: "Apartments" refer to non-residential premises that do not fall under the category of residential housing but have the necessary living conditions.

## Methodology

### 1. Data Preprocessing
- Examination of dataset structure and data types
- Identification of missing values and data quality issues
- Column renaming for consistency (snake_case format)
- Handling missing values appropriately
- Data type conversions (e.g., boolean types)
- Identification and handling of outliers and anomalies

### 2. Exploratory Data Analysis
- Statistical summaries of key variables
- Distribution analysis of prices and property characteristics
- Correlation analysis between variables
- Geographic analysis of property locations
- Time-based analysis of listing patterns

### 3. Feature Analysis
- Analysis of how each feature affects property prices
- Identification of most influential factors
- Detection of unusual patterns that might indicate fraud
- Price per square meter analysis
- Location premium analysis

## Key Findings

The analysis reveals several important patterns in the real estate market:

### Price Determinants
- **Location**: Distance to city center significantly impacts prices
- **Property Size**: Total area, living area, and number of rooms are key factors
- **Property Type**: Studios, apartments, and open-plan layouts have different pricing patterns
- **Building Characteristics**: Floor number, total floors, and ceiling height affect values

### Market Patterns
- Geographic distribution of listings across St. Petersburg and surrounding areas
- Seasonal or temporal trends in listing activity
- Relationship between listing duration and pricing
- Impact of property photos on listing success

### Anomaly Detection
- Identification of listings with unusual price-to-feature ratios
- Detection of potential data quality issues
- Flagging of properties that may require further investigation

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Static data visualization
- **Seaborn**: Statistical data visualization
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_03/
├── prj_property_pricing.ipynb    # Main project notebook
└── README.md                      # This file
```

## Results

The project successfully identifies key parameters that influence real estate property values in the St. Petersburg market. The analysis provides:

1. **Valuation Factors**: Clear understanding of which features most significantly impact property prices
2. **Market Insights**: Patterns in how properties are priced and listed
3. **Anomaly Indicators**: Methods to identify potentially fraudulent or problematic listings
4. **Data Quality Assessment**: Identification of data issues that need addressing

These findings enable the development of automated systems for:
- Property valuation
- Fraud detection
- Market analysis
- Pricing recommendations

The analysis demonstrates the importance of comprehensive data preprocessing and exploratory analysis in understanding complex real estate markets.
