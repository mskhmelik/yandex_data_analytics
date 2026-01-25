# Module 09: SQL Database Analysis - Book Subscription Service

## Overview

This project analyzes a database for a book subscription service that was acquired during the COVID-19 pandemic when reading became more popular. The database contains information about books, publishers, authors, and user reviews. The analysis helps formulate a value proposition for the new product.

## Objectives

- Analyze the database structure and relationships
- Answer specific business questions using SQL queries
- Understand user preferences and behavior
- Identify popular authors, publishers, and books
- Provide insights for product development and marketing

## Database Schema

The database consists of five main tables:

### Books Table (`books`)
Contains data about books:
- `book_id` — book identifier
- `author_id` — author identifier
- `title` — book title
- `num_pages` — number of pages
- `publication_date` — book publication date
- `publisher_id` — publisher identifier

### Authors Table (`authors`)
Contains data about authors:
- `author_id` — author identifier
- `author` — author name

### Publishers Table (`publishers`)
Contains data about publishers:
- `publisher_id` — publisher identifier
- `publisher` — publisher name

### Ratings Table (`ratings`)
Contains user ratings of books:
- `rating_id` — rating identifier
- `book_id` — book identifier
- `username` — username who gave the rating
- `rating` — book rating

### Reviews Table (`reviews`)
Contains user reviews of books:
- `review_id` — review identifier
- `book_id` — book identifier
- `username` — username who wrote the review
- `text` — review text

## Tasks and Queries

### Task 1: Books Published After 2000
Count how many books were published after January 1, 2000.

### Task 2: Reviews and Average Rating per Book
For each book, calculate:
- Number of reviews
- Average rating

### Task 3: Publisher with Most Books Over 50 Pages
Identify the publisher that released the most books with more than 50 pages (excluding brochures).

### Task 4: Author with Highest Average Rating
Find the author with the highest average book rating, considering only books with 50 or more ratings.

### Task 5: Average Reviews from Active Users
Calculate the average number of reviews from users who have given more than 50 ratings.

## Methodology

### 1. Database Exploration
- Examination of table structures
- Understanding relationships between tables
- Data type verification
- Initial data quality assessment

### 2. SQL Query Development
- Writing queries for each task
- Using JOINs to combine data from multiple tables
- Aggregation functions (COUNT, AVG, SUM)
- Filtering and grouping data
- Subqueries and CTEs where necessary

### 3. Query Optimization
- Ensuring query efficiency
- Proper indexing considerations
- Query readability and maintainability

### 4. Results Analysis
- Interpretation of query results
- Business insights extraction
- Validation of findings

## Key Findings

### Publication Trends
- Number of books published after 2000
- Publishing activity trends
- Market growth indicators

### User Engagement
- Review activity patterns
- Rating distributions
- Most reviewed books
- User engagement levels

### Publisher Performance
- Leading publishers by volume
- Publisher focus areas
- Market share insights

### Author Performance
- Top-rated authors
- Author popularity metrics
- Quality indicators

### User Behavior
- Active user patterns
- Review writing habits
- Engagement levels of different user segments

## Technologies Used

- **SQL**: Database querying language
- **PostgreSQL**: Database management system
- **Python**: For data analysis and visualization
- **Pandas**: Data manipulation
- **SQLAlchemy**: Database connection and query execution
- **Jupyter Notebook**: Interactive development environment

## Database Connection

The project connects to a PostgreSQL database using SQLAlchemy:

```python
db_config = {
    'user': 'praktikum_student',
    'pwd': '',
    'host': '',
    'port': 6432,
    'db': 'data-analyst-advanced-sql'
}
```

## Project Structure

```
Module_09/
├── 220925_test_v01.ipynb      # Main project notebook
├── online_store.sql            # SQL queries (if exported)
├── tools_shop.sql              # Additional SQL queries
└── README.md                    # This file
```

## Results

The SQL analysis provides valuable insights for the book subscription service:

1. **Content Strategy**: Understanding of publication trends and popular content
2. **User Insights**: Patterns in user engagement and behavior
3. **Publisher Relationships**: Identification of key publishers for partnerships
4. **Author Discovery**: Recognition of highly-rated authors for promotion
5. **Product Development**: Data-driven guidance for service features

**Key Business Impact**:
- Informed content acquisition strategy
- Understanding of user preferences
- Identification of marketing opportunities
- Foundation for value proposition development

The project demonstrates proficiency in SQL for business analysis and provides actionable insights for launching and growing the book subscription service in a competitive market.
