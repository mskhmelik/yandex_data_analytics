# Module 13: Data Science Gym - Customer Churn Prediction

## Overview

This project analyzes customer data for "Bodybuilder-Data Scientist," a fitness center network, to predict customer churn and develop strategies for customer retention. A customer is considered to have churned if they haven't visited the gym at least once in the last month. The project involves building predictive models, creating customer profiles through clustering, and developing actionable recommendations.

## Objectives

1. **Churn Prediction**: Build models to predict the probability of customer churn for the following month
2. **Customer Segmentation**: Create typical user profiles by identifying prominent groups and characterizing their attributes
3. **Feature Analysis**: Analyze main features that have the greatest impact on churn
4. **Business Recommendations**: Develop recommendations for improving customer relationship management:
   - Identifying target customer groups
   - Proposing measures to reduce churn
   - Determining other nuances of customer interactions

## Data Description

The dataset `gym_churn.csv` contains information about the month prior to churn and the fact of churn for a specific month:

### Target Variable
1. `Churn` - whether the customer churned in the current month

### Customer Demographics (Month Prior to Churn)
2. `Gender` - customer's gender
3. `Near_Location` - whether customer lives or works near the fitness center
4. `Partner` - whether customer is an employee of a club partner company
5. `Promo_friends` - whether customer registered under "bring a friend" promotion
6. `Phone` - whether customer provided a contact phone number
7. `Age` - customer's age
8. `Lifetime` - time since customer's first visit (in months)

### Visit and Subscription Data
9. `Contract_period` - duration of current active subscription (month, 3 months, 6 months, or year)
10. `Month_to_end_contract` - time until end of current active subscription (in months)
11. `Group_visits` - whether customer attends group classes
12. `Avg_class_frequency_total` - average frequency of visits per week for entire subscription duration
13. `Avg_class_frequency_current_month` - average frequency of visits per week for previous month
14. `Avg_additional_charges_total` - total revenue from other services (cafe, sports goods, beauty, massage salon)

## Methodology

### 1. Data Loading and Exploration
- Dataset loading and initial inspection
- Data type verification
- Missing value analysis
- Basic statistical summaries

### 2. Exploratory Data Analysis (EDA)

#### 2.1 Dataset Overview
- Examination of missing features
- Study of mean values and standard deviations
- Data distribution analysis

#### 2.2 Churn vs. Non-Churn Comparison
- Mean values of features in two groups (churned vs. stayed)
- Statistical comparison of groups
- Identification of significant differences

#### 2.3 Visualization
- Bar charts for categorical features
- Feature distributions for churned vs. stayed customers
- Correlation matrix visualization
- Pattern identification

### 3. Binary Classification Models

#### 3.1 Data Preparation
- Train-test split
- Feature preparation
- Target variable encoding

#### 3.2 Model Training
- **Logistic Regression**:
  - Model training
  - Hyperparameter tuning
  - Feature importance analysis

- **Random Forest**:
  - Model training
  - Hyperparameter tuning
  - Feature importance analysis

#### 3.3 Model Evaluation
- Accuracy calculation
- Precision and recall metrics
- Model comparison
- Selection of best-performing model

### 4. Customer Clustering

#### 4.1 Data Standardization
- Feature scaling
- Preparation for clustering algorithms

#### 4.2 Hierarchical Clustering
- Distance matrix construction
- Dendrogram visualization
- Cluster identification

#### 4.3 K-Means Clustering
- Model training with n=5 clusters
- Cluster prediction
- Cluster characterization

#### 4.4 Cluster Analysis
- Mean values of features for each cluster
- Feature distributions by cluster
- Churn rate calculation for each cluster
- Identification of churn-prone vs. reliable clusters

### 5. Recommendations Development
- Target customer group identification
- Churn reduction strategies
- Customer interaction guidelines
- Business action plans

## Key Findings

### Churn Prediction
- **Model Performance**: Comparison of Logistic Regression vs. Random Forest
- **Best Model**: Identification of model with highest accuracy, precision, and recall
- **Key Predictors**: Features most important for churn prediction
- **Prediction Accuracy**: Model performance metrics

### Customer Segmentation
- **Cluster Profiles**: Five distinct customer segments identified
- **Cluster Characteristics**: Key attributes of each cluster
- **Churn Rates by Cluster**: Which clusters are most prone to churn
- **Reliable Clusters**: Identification of customer groups with low churn risk

### Feature Importance
- **Demographic Factors**: Impact of age, gender, location
- **Engagement Factors**: Impact of visit frequency, group classes
- **Contract Factors**: Impact of contract period and time to end
- **Behavioral Factors**: Impact of additional service usage

### Business Insights
- **High-Risk Groups**: Customer segments most likely to churn
- **Retention Opportunities**: Segments that could be retained with intervention
- **Target Segments**: Most valuable customer groups to focus on
- **Action Items**: Specific recommendations for each segment

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Plotly**: Interactive data visualization
  - `plotly.graph_objects` for custom charts
  - `plotly.figure_factory` for statistical visualizations
  - `plotly.subplots` for multi-panel charts
- **Scikit-learn**: Machine learning
  - `train_test_split` for data splitting
  - `LogisticRegression` for classification
  - `RandomForestClassifier` for ensemble learning
  - `KMeans` for clustering
- **SciPy**: Scientific computing
  - `scipy.cluster.hierarchy` for hierarchical clustering
- **IPython.display**: Enhanced display capabilities

## Project Structure

```
Module_13/
├── prj_data_science_gym.ipynb    # Main project notebook
└── README.md                       # This file
```

## Results

The project successfully provides:

1. **Predictive Models**: Accurate churn prediction models with quantified performance
2. **Customer Understanding**: Clear segmentation of customer base into actionable groups
3. **Feature Insights**: Understanding of which factors most influence churn
4. **Actionable Recommendations**: Specific strategies for customer retention

**Key Business Impact**:
- **Churn Reduction**: Strategies to reduce customer churn
- **Target Marketing**: Identification of customer segments for focused efforts
- **Resource Allocation**: Data-driven guidance for retention investments
- **Customer Understanding**: Deep insights into customer behavior patterns

**Model Performance**:
- Comparison of Logistic Regression and Random Forest models
- Selection of best-performing model based on accuracy, precision, and recall
- Feature importance rankings for business understanding

**Clustering Insights**:
- Five distinct customer segments with unique characteristics
- Churn rate analysis by segment
- Identification of reliable vs. at-risk customer groups

The project demonstrates advanced data science skills including machine learning, clustering, and business analytics, providing a comprehensive solution for customer retention in the fitness industry.
