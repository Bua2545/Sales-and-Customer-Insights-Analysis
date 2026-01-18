# Sales and Customer insights analysis

## Project Overview
This synthetic retail transaction dataset contains sales, product and customer data with common data quality issues. It is designed for practicing data cleaning, analysis and visualization to uncover sales and customer insights.
## Data Structure
The structure as seen below consists of 3 tables: customer_info, production_info and sales_data with a total record of 2997 after cleaning.

<p align="center"><img width="40%" src="https://github.com/user-attachments/assets/def4fdc4-8d66-4a4a-bdc4-cd83a0095358" /></p>

### Data cleaning
*Customer_info dataset*
-  Filled missing customer_id with sequential values
- Standardized inconsistent gender and loyalty_tier
- Filled missing gender and loyalty_tier with “Unknown”
- Removed email and region (seem to be home address) columns

*Product_info dataset*
- Remove launch_data and supplier_code columns

*Sales_data dataset*
- Regenerated order_date with the help of AI to be able to analyze sales trend
- Filled order_id, customer_id, product_id, delivery_status and payment_method with “Unknown”
- Standardized inconsistent quantity and delivery_status values and remove missing quantity records
- Filled missing unit_price with base_price
- Converted order_date to date format
- Filled empty discount_applied with 0
- Added price_paid column calculated by (quantity x unit_price) – (quantity x unit_price x discount_applied)
### Tools used
Excel and Power BI (Desktop)
## Key Findings

<img width="49%" src="https://github.com/user-attachments/assets/2e680321-1803-49cd-a026-c5f92a5b1bab" /><img width="49%" src="https://github.com/user-attachments/assets/87fed3c9-1a22-4aef-a802-5e162f2cadc4" />

*All the sales visualizations were sales from complete deliveries, which included delivered and delayed status.*
- Sales trend rose from July to August 2024 and continued steadily until February 2025. The trend peaked in March 2025 and gradually dropped.
- By category, the highest sales were cleaning of 77681.69 (40.22%) and the lowest were personal care of 20388.47 (10.56%).
- There were 2403 orders with complete delivery. The region with the most complete delivery status was East with 503 orders and the least was West with 459 orders.
- There were 594 orders with incomplete delivery. The region with the least incomplete deliveries was East with 99 orders and the most was West with 134 orders – the more incomplete deliveries, the more sales lost. Noted that incomplete deliveries combine cancelled and unknown delivery status.
- There was no one-time buyer. The top 10 customers based on sales were C00108, C00191, C00385, C00062, C00301, C00362, C00371, C00500, C00479, and C00040.
- Most of the sales were from the gold loyalty tier of 109.143.07 (56.39%) with a contribution of 265 customers (53%). However, the highest average sales were from the unknown tier of 90.99 (27.5%), followed by the gold tier of 81.69 (24.69%)
- Female customers purchased the most in all categories, particularly in the cleaning category, which showed higher quantity purchased. 
## Conclusion
The analysis illustrates an overall upward trend from July 2024 until March 2025, followed by a downward trend until September 2025. With no one-time buyer, sales were primarily driven by the gold tier customers, the cleaning category, female customers. While the incomplete deliveries including cancelled and unknown status were found to have an impact on sales loss.
### Recommendations
- According to the loyalty tier, the highest sales and the majority of customers were in the gold tier. However, the average sales of the gold tier fell on the second. Based on these findings, the store can provide more discounts or promotions to encourage gold tier to purchase more.
- Based on incomplete deliveries, improving delivery will increase the total sales of the store.
## Data Source
https://www.kaggle.com/datasets/ajinkyachintawar/sales-and-customer-behaviour-insights
