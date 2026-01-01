# olist-ecommerce-sql-analysis
SQL-based exploratory analysis of the Brazilian Olist e-commerce dataset using Google BigQuery.
## 1. Project Overview

This project performs an exploratory data analysis (EDA) on the Brazilian Olist e-commerce dataset using SQL in Google BigQuery. The goal is to analyze customer behavior, sales performance, delivery efficiency, and customer satisfaction through structured SQL queries.

The project focuses on applying core SQL concepts such as joins, aggregations, and time-based analysis to extract meaningful business insights from a real-world relational dataset. It was developed as a portfolio project to demonstrate practical SQL and analytical skills.

## 2. Dataset Description

The analysis is based on the Brazilian Olist e-commerce public dataset, which contains real transactional data from an online marketplace.

The dataset includes multiple relational tables covering different aspects of the e-commerce process, such as:
- Customers and their geographic information
- Orders and order status lifecycle
- Order items and product details
- Sellers and seller locations
- Payments and payment methods
- Customer reviews and satisfaction scores

The data spans from 2016 to 2018 and represents thousands of orders placed across Brazil, making it suitable for analyzing customer behavior, sales performance, delivery efficiency, and customer satisfaction.

## 3. Tools & Technologies

- **SQL** – Used for data querying, aggregation, joins, and analytical calculations  
- **Google BigQuery** – Cloud-based data warehouse used to query and analyze large-scale e-commerce data  
- **GitHub** – Version control and project documentation  
- **Markdown** – Used for writing and structuring project documentation

## 4. Analysis Scope

The analysis focuses on answering key business questions related to the performance of an e-commerce platform using SQL. The scope of the analysis includes:

- Understanding overall order volume and customer distribution

- Analyzing sales performance across product categories

- Identifying high-spending customers and top-performing sellers

- Evaluating delivery performance, including delivery times and late delivery rates

- Assessing customer satisfaction through review score analysis

- Examining the relationship between delivery performance and customer reviews

The analysis is structured step by step, starting from high-level metrics and gradually moving toward more detailed, insight-driven queries to reflect a real-world analytical workflow.

## 5. Key SQL Analyses

The project includes a set of structured SQL analyses designed to address core e-commerce business questions:

- Data validation and baseline metrics: row counts, basic distributions, and order status checks to ensure data consistency

- Time-based analysis: monthly order trends using purchase timestamps to observe growth patterns

- Product and category analysis: sales volume and average price analysis across product categories

- Customer analysis: identification of high-spending customers through aggregated order values

- Delivery performance analysis: calculation of delivery durations and late delivery rates

- Customer satisfaction analysis: review score distribution and comparison between on-time and late deliveries

These analyses leverage core SQL concepts such as multi-table joins, aggregations, CASE statements, and date functions to transform raw transactional data into business-relevant insights.

## 6. Key Insights

The analysis revealed several important insights regarding the performance of the e-commerce platform:

- The majority of orders were delivered on time, indicating generally strong logistics performance; however, a noticeable portion of orders experienced delivery delays.  
- Late deliveries were strongly associated with lower customer satisfaction, with average review scores dropping significantly compared to on-time deliveries.  
- Customer spending was highly concentrated, with a small group of customers contributing disproportionately to total revenue.  
- Certain product categories generated high order volumes but differed significantly in average price, suggesting varying revenue strategies across categories.  
- Review score distribution showed that while most customers provided positive feedback, delivery performance played a critical role in negative reviews.

These findings highlight the importance of delivery efficiency and customer experience as key drivers of overall platform performance.

## 7. Limitations

## 8. Next Steps
