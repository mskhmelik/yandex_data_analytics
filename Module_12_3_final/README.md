# Module 12.3: SQL Database Connection Project

## Overview

This project demonstrates database connectivity and SQL query execution using Python. It focuses on establishing secure connections to PostgreSQL databases, executing queries, and working with database results in a Python environment.

## Objectives

- Establish secure database connections
- Execute SQL queries from Python
- Handle database credentials securely
- Process query results in pandas DataFrames
- Demonstrate best practices for database connectivity

## Database Configuration

The project connects to a PostgreSQL database using SQLAlchemy:

```python
db_config = {
    'user': 'praktikum_student',
    'pwd': '',
    'host': '',
    'port': 6432,
    'db': 'data-analyst-final-project-db'
}
```

## Methodology

### 1. Connection Setup
- Database configuration
- Connection string construction
- SSL certificate handling (CA.pem)
- Secure credential management

### 2. Query Execution
- SQL query writing
- Query execution using SQLAlchemy
- Result retrieval
- Error handling

### 3. Data Processing
- Conversion to pandas DataFrames
- Data manipulation and analysis
- Result visualization
- Export capabilities

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **SQLAlchemy**: Database connection and ORM
- **PostgreSQL**: Database management system
- **Jupyter Notebook**: Interactive development environment

## Project Structure

```
Module_12_3_final/
├── prj_connect_to_sql_db.ipynb    # Main project notebook
├── CA.pem                          # SSL certificate for secure connection
└── README.md                        # This file
```

## Key Features

### Secure Connection
- SSL/TLS encryption support
- Certificate-based authentication
- Secure credential handling

### Query Execution
- Direct SQL query execution
- Parameterized queries support
- Transaction management

### Data Integration
- Seamless integration with pandas
- DataFrame operations on query results
- Data export capabilities

## Results

The project successfully demonstrates:

1. **Database Connectivity**: Reliable connection to remote PostgreSQL databases
2. **Query Execution**: Efficient execution of SQL queries from Python
3. **Data Processing**: Integration of database results with pandas workflows
4. **Best Practices**: Secure and efficient database interaction patterns

**Key Benefits**:
- Foundation for database-driven analytics
- Reusable connection patterns
- Secure credential management
- Integration with Python data science stack

This project provides the technical foundation for working with databases in data analysis workflows, demonstrating essential skills for data analysts working with SQL databases.
