# Module 11: Yandex Zen Data Pipeline

## Overview

This project creates a data pipeline to import and process data from Yandex servers. The data covers visits to various Yandex Zen pages by users. This is a data engineering project focused on extracting, transforming, and loading (ETL) data for analytics purposes.

## Objectives

- Connect to Yandex database server
- Extract visit data from the database
- Transform data as needed for analysis
- Save data in a format suitable for further analysis (CSV)
- Create a reusable pipeline for regular data updates

## Data Description

The pipeline extracts data from the `dash_visits` table in the Yandex database, which contains information about:
- User visits to Yandex Zen pages
- Visit timestamps
- Page information
- User identifiers
- Other relevant visit metrics

## Methodology

### 1. Database Connection
- Configuration of database connection parameters
- Connection string setup using SQLAlchemy
- Secure credential management
- Connection testing and validation

### 2. Data Extraction
- SQL query execution to retrieve data
- Data retrieval from `dash_visits` table
- Handling of large datasets efficiently
- Error handling for connection issues

### 3. Data Transformation
- Data type conversions if needed
- Column renaming or standardization
- Data quality checks
- Preparation for export

### 4. Data Loading
- Export to CSV format
- File naming conventions
- Data validation after export
- Documentation of output format

## Database Configuration

The project connects to a PostgreSQL database:

```python
db_config = {
    'user': 'praktikum_student',
    'pwd': '',
    'host': '',
    'port': 6432,
    'db': 'data-analyst-zen-project-db'
}
```

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **SQLAlchemy**: Database connection and query execution
- **PostgreSQL**: Database system
- **Jupyter Notebook**: Interactive development environment

## Project Structure

```
Module_11/
├── pipe_yandex_zen.ipynb       # Main pipeline notebook
├── dash_visits.hyper           # Tableau data file (if applicable)
├── CA.pem                      # SSL certificate for secure connection
├── tableau_link.txt            # Tableau connection information
├── 221127_mk_project_11_vF.zip # Final project archive
├── 221127_mk_project_11_vF.pptx # Presentation
├── 221127_yandex_zen_vShared.twb # Tableau workbook
└── README.md                    # This file
```

## Pipeline Workflow

1. **Connection Setup**: Establish secure connection to Yandex database
2. **Query Execution**: Execute SQL query to retrieve visit data
3. **Data Retrieval**: Load data into pandas DataFrame
4. **Data Processing**: Apply any necessary transformations
5. **Export**: Save processed data to CSV file
6. **Validation**: Verify data integrity and completeness

## Results

The pipeline successfully:

1. **Data Access**: Provides reliable access to Yandex Zen visit data
2. **Automation**: Creates a repeatable process for data extraction
3. **Data Format**: Produces CSV files ready for analysis
4. **Documentation**: Includes clear documentation for future use

**Key Benefits**:
- Automated data extraction process
- Consistent data format for analysis
- Foundation for regular reporting
- Integration with analytics tools (Tableau)

**Use Cases**:
- Regular data updates for dashboards
- Historical data analysis
- User behavior tracking
- Performance monitoring

The project demonstrates practical data engineering skills, creating a pipeline that can be scheduled for regular execution to keep analytics data up-to-date.
