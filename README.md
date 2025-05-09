# Sql-Product-Analyst

## Introduction
With this dataset, I want to perform various analyses such as trend changes over time, customer performance segments, products, and etc. Also, I aim to answer key business questions like identifying trends over time and comparing performance across different data segments.
The dataset consists of two dimension tables and one fact table, which provide comprehensive information about customer features and specifications, products, and purchase amounts.

##### Dimension tables:
 * gold.dim_customers (customer_key, customer_id, customer_number, first_name, last_name, 
                       country, marital_status, gender, birthdate, create_date)
 * gold.dim_products (product_key, product_id, product_number, product_name, category_id, 
                      category, subcategory, maintenance, cost, product_line, start_date)
   
##### Fact table:
 * gold.fact_sales (columns name: order_number, product_key, order_date, shipping_date, 
                    due_date, sales_amount, quantity, price )

## Objectives
•	Test SQL querying skills

•	Data analysis to address the problem statement

•	Provide business recommendations with stakeholders

## Business Qeustions

#### 1) Date Range Exploration
Purpose:

•	To determine the temporal boundaries of key data points.	                                 
•	To understand the range of historical data.                                            

#### 2) Magnitude Analysis
Purpose:

•	To quantify data and group results by specific dimensions.	    
•	For understanding data distribution across categories.

#### 3) Ranking Analysis
Purpose:

•	To rank items (e.g., products, customers) based on performance or other metrics.	    
•	To identify top performers or laggards.	                                                 

#### 4) Change Over Time Analysis
Purpose:

•	To track trends, growth, and changes in key metrics over time.	    
•	For time-series analysis and identifying seasonality.	    
•	To measure growth or decline over specific periods.
   
#### 5) Cumulative Analysis
Purpose:

•	To calculate running totals or moving averages for key metrics.             
• 	To track performance over time cumulatively.                              
• 	Useful for growth analysis or identifying long-term trends.

#### 6) Performance Analysis (Year-over-Year, Month-over-Month)
Purpose:

•	To measure the performance of products, customers, or regions over time.         
•	For benchmarking and identifying high-performing entities.                  
•	To track yearly trends and growth.

#### 7) Data Segmentation Analysis

Purpose:

•	To group data into meaningful categories for targeted insights.                      
•	For customer segmentation, product categorization, or regional analysis.

#### 8) Part-to-Whole Analysis

Purpose:

•	To compare performance or metrics across dimensions or time periods.                  
•	To evaluate differences between categories.                                         
•	Useful for A/B testing or regional comparisons.

## Reports
At the end of my code, i create two reports.                                            

#### Customer Report

Purpose:
     This report consolidates key customer metrics and behaviors

Highlights:

1. Gathers essential fields such as names, ages, and transaction details.               
2. Segments customers into categories (VIP, Regular, New) and age groups.                
3. Aggregates customer-level metrics:                                                  
•	total orders                                                            
•	total sales                                                                    
•	total quantity purchased                                                        
•	total products                                                                 
•	lifespan (in months)       

4. Calculates valuable KPIs:                                                          
•	recency (months since last order)                                                  
•	average order value                                                                
•	average monthly spend                                                               

#### Product Report

Purpose:
     This report consolidates key product metrics and behaviors.

Highlights:

1. Gathers essential fields such as product name, category, subcategory, and cost.          
2. Segments products by revenue to identify High-Performers, Mid-Range, or Low-Performers.   
3. Aggregates product-level metrics:                                                  
•	total orders                                                                        
•	total sales                                                                        
•	total quantity sold                                                                
•	total customers (unique)                                                           
•	lifespan (in months)
                                                          
5. Calculates valuable KPIs:                                                                 
•	recency (months since last sale)                                                  
•	average order revenue (AOR)                                                          
•	average monthly revenue                                                             

## Recommendations

#### Life Time Value
To measure if retention or lifetime value (LTV) increased, we need to understand what drives LTV. In a business sense.
We can broke it down:                                                                 
• Has Average Order Value (AOV) increased?                                                   
• Has the number of purchases per client increased?                                     
• Over what time window?                                                                
In this way, we can identify the demographic and psychographic characteristics of customers whose LTV increased during our considered period.                                          
•	Customers buying product X (Y% higher LTV) respond well to bundled deals. Upsell accessories to this group.                                                                         

#### Churn Rate Reduction
For this purpose, using customer segmentation techniques such as RFM or COHORT can help us a lot.                                                                                       
•	By identifying high-risk customers, strategies such as giving early discounts can reduce their churn rate.                                                                          
•	Creating VIP customers who receive personalized discounts can drastically reduce churn rates, which can prevent wasted marketing budgets.                                                 
