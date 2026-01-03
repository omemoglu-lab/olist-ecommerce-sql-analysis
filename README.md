# olist-ecommerce-sql-analysis
SQL-based exploratory analysis of the Brazilian Olist e-commerce dataset using Google BigQuery.

## 1. 1. Project Vision & Business Context

I chose the Olist dataset because it represents the "messy" reality of Brazilian e-commerce between 2016 and 2018. My goal wasn't just to write SQL queries, but to understand how logistical bottlenecks and payment behaviors directly impact customer satisfaction. I wanted to experience the full lifecycle of data—from cleaning inconsistent timestamps to deriving actionable business strategies.

## 2. Exploring the Olist Ecosystem

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

## 4. Exploring the Olist Ecosystem

The analysis focuses on answering key business questions related to the performance of an e-commerce platform using SQL. The scope of the analysis includes:

- Understanding overall order volume and customer distribution

- Analyzing sales performance across product categories

- Identifying high-spending customers and top-performing sellers

- Evaluating delivery performance, including delivery times and late delivery rates

- Assessing customer satisfaction through review score analysis

- Examining the relationship between delivery performance and customer reviews

The analysis is structured step by step, starting from high-level metrics and gradually moving toward more detailed, insight-driven queries to reflect a real-world analytical workflow.

## 5. Technical Deep Dive: SQL Logic

To extract meaningful insights from the Olist ecosystem, I structured my analysis into three main pillars: Performance Metrics, Logistics Efficiency, and Customer Satisfaction.

A. Sales & Performance Metrics
Monthly Trends: I used DATE_TRUNC to observe order volumes over time, identifying seasonal growth patterns in the marketplace.

Top-Performing Categories: By joining order_items, products, and category_name_translation tables, I calculated total sales and revenue per category. I discovered significant differences in average product prices across different sectors.

High-Value Customers: I identified the "Top 20 Spenders" by aggregating price and freight values. Insight: I limited this to the top 20 to focus on high-value users, which is a common practice for targeted marketing strategies.

B. Logistics & Delivery Performance (The Critical Metric)
Average Delivery Speed: Using DATE_DIFF, I calculated the average delivery time in days. This served as my baseline for operational efficiency.

Late Delivery Analysis: I implemented CASE WHEN logic to flag orders where the order_delivered_customer_date exceeded the order_estimated_delivery_date.

Late Delivery Percentage: I calculated the overall percentage of delayed orders to quantify the impact of logistics failures on the platform.

C. Customer Satisfaction & Feedback Loop
The Impact of Delay: By joining orders and order_reviews, I analyzed the correlation between late deliveries and review scores.

Review Score Distribution: I used COUNT and GROUP BY to see the spread of ratings. Key Discovery: I found a direct correlation where "Late Delivery" status leads to a significantly lower average review score compared to on-time deliveries.

## 6. Technical Deep Dive: SQL Logic

The analysis revealed several important insights regarding the performance of the e-commerce platform:

- The majority of orders were delivered on time, indicating generally strong logistics performance; however, a noticeable portion of orders experienced delivery delays.  
- Late deliveries were strongly associated with lower customer satisfaction, with average review scores dropping significantly compared to on-time deliveries.  
- Customer spending was highly concentrated, with a small group of customers contributing disproportionately to total revenue.  
- Certain product categories generated high order volumes but differed significantly in average price, suggesting varying revenue strategies across categories.  
- Review score distribution showed that while most customers provided positive feedback, delivery performance played a critical role in negative reviews.

These findings highlight the importance of delivery efficiency and customer experience as key drivers of overall platform performance.

## 7. Limitations

This analysis is subject to several limitations:

- The dataset covers a fixed historical period (2016–2018), which limits the ability to reflect current market dynamics.  
- Some orders do not contain complete delivery or review information, which may slightly affect delivery and customer satisfaction analyses.  
- Revenue calculations are based on available order item prices and freight values and do not account for potential refunds or cancellations beyond recorded statuses.  
- The analysis focuses on quantitative data and does not include qualitative insights such as customer review text sentiment.

Despite these limitations, the dataset provides a reliable foundation for identifying overall trends and key relationships within the e-commerce workflow.

## 8. Next Steps

If extended further, this analysis could be enhanced in several ways:

- Incorporating text-based sentiment analysis on customer reviews to better understand qualitative feedback.  
- Performing cohort or retention analysis to evaluate repeat purchase behavior over time.  
- Building interactive dashboards (e.g., using BI tools) to visualize key metrics such as delivery performance and customer satisfaction.  
- Expanding the analysis to include predictive models for delivery delays or customer churn.  

These extensions would allow deeper insights and support more advanced, data-driven decision making.
