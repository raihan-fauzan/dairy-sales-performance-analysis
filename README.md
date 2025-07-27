# *Pratama Nusantara Dairy* - Sales Performance Analysis (Nov 2024 - Feb 2025)

## Project Background
### Company Info
**Pratama Nusantara Dairy (PND)** is an Indonesian dairy company with two main plants in Bekasi and Bandung. PND offers 90 SKUs and distributes through 70+ partners across Indonesia. This project focuses on analysis of sales data from November 2024 to February 2025 for one of the city in Sumatra. Recommendations will be provided to improve sales performance, mainly for Area Business Manager.

### Objectives
- **Analyze key sales metrics** *(total sales, returns, transactions, unique customers, & more)* to identify overall performance trends and fluctuation from November 2024 to February 2025.
- **Evaluate the performance of Salesman, Product, and Customer segments** to identify key points of sales success and also area of improvements.
- **Provide actionable recommendations** based on the findings and analysis to support Area Business Manager in optimizing strategies and improving overall sales performance.

### Deliverables
- Sales Performance Analysis Report (PDF)
- Sales Performance Dashboard (Tableau) *(On Progress)*
- Detailed Exploratory Data Analysis (Excel/Python Notebook) *(On Progress)*

## Executive Summary

## Technical Details

### Dataset

#### `sales_data`

The **`sales_data`** table tracks every transaction. It includes unique IDs for the **transaction**, **line item**, the **date** of sale, and quantities sold in both **boxes** and **pieces**. It also contains detail about **price per piece**, **total price** before and after discounts and taxes, and the **discount amount**. Each sale is linked to a **salesman**, **customer**, and **product**.

#### `customer_data`

The **`customer_data`** table stores information about each customer. It has a unique **customer ID** and notes their linked **salesman ID**. Customers are categorized into **primary** and **secondary groups** for segmentation. It also records their usual **payment type**.

#### `product_data`

The **`product_data`** table lists all products. Each product has a unique **ID**, its **name**, and up to **three categories** for classification. It also specifies **product variants**, **pieces per box**, and prices for both **individual pieces** and **full boxes**. The **status** indicates if the product is available.

### Entity Relationship Diagram

![ERD](Image/erd_image.png)

### **Acknowledgements**

Pratama Nusantara Dairy is a fictional company. This dataset inspired from real-world sales data and has undergone modification to remove obvious similarities.

## Detailed Insight

### Overall Performance

<p align="center">
  <img src="/Image/Table/WithoutTitle/table_overall_sales_performance_NO_TITLE.png" alt="Overall Performance" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

#### Total Sales, Returns, Transactions, and Customers over Month

<p align="center">
  <img src="/Image/Chart/chart_monthly_sales.png" alt="Sales Over Month" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

- Sales peaked in December 2024 at `Rp5.01 B` with increase of `5.5%` before dropping to `Rp3.57 B` with decrease of `26.9%` in February 2025. This significant drop likely reflects a "Post-Festive Slump," as sales often decline after the holiday season that spans from December to January.

<p align="center">
  <img src="/Image/Chart/chart_monthly_return.png" alt="Returns Over Month" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

- Return values show a concerning upward trend that requires further investigation. To understand the root cause, a deeper analysis into the types of returns is needed. An increase in returns suggests potential demand issues or stock quality issues that may have originated 1-6 months prior to the return date, if it is assumed that the type of return is "bad return" (The time frame for a "bad return" is 1-6 months after the transaction). 

<p align="center">
  <img src="/Image/Chart/chart_monthly_transactions.png" alt="Monthly Transactions" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

- The number of transactions has steadily decreased over the four-month period, even during the festive season. The most significant drop occurred in February 2025, with a `9.0%` decrease. This trend is in contrast to the sales trend, which saw an increase in December 2025. This indicates that the factor driving the rise in sales was not the number of transactions. Immediate action is required to increase transaction numbers in the coming months.

#### Average Sales per Transactions over Month

<p align="center">
  <img src="/Image/Chart/chart_monthly_avg_sales.png" alt="Average Sales per Transactions over Month" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

- The average sales value per transaction saw its largest increase in December 2024 at `12.8%`, followed by consecutive decreases in January and February, with the steepest decline of `19.7%` occurring in February. This December increase in average sales per transaction drove the rise in total sales, as the number of transactions consistently decreased over the entire four-month period. This indicates that customers were purchasing either higher quantities or more expensive products.

#### Average Unique Product per Transactions over Month

<p align="center">
  <img src="/Image/Chart/chart_avg_product.png" alt="Average Unique Products per Transactions over Month" style="width:80%; height:auto; display:block; margin:0 auto;">
</p>

- 

### Salesman Performance

#### Salesman Customer Segmentation

| salesman_id | customer_category_served                                                                                                           |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `SM03353`     | Minimarket, Supermarket                                                                                                           |
| `SM03376`     | Minimarket, Supermarket                                                                                                            |
| `SM03378`     | Second Dealer                                                                                                                      |
| `SM03385`     | Second Dealer                                                                                                                      |
| `SM03344`     | Bakery, Beverage Stall, Cafe, Canteen, Company, Food Supplier, Hotel & Leisure, Restaurant                                         |
| `SM03322`     | Healthcare Institution, Internal Selling, Market Retail, Minimarket, Residential Retail, Second Dealer                             |
| `SM03361`     | Minimarket, Residential Retail, Second Dealer                                                                                      |
| `SM03338`     | Market Retail, Minimarket, Residential Retail, Second Dealer                                                                       |
| `SM03332`     | Baby Store, Market Retail, Minimarket, Residential Retail, Second Dealer                                                           |
| `SM03367`     | Healthcare Institution, Market Retail, Minimarket, Residential Retail, Second Dealer                                               |
| `SM03317`     | Baby Store, Market Retail, Minimarket, Residential Retail, Second Dealer, Supermarket                                              |
| `SM03331`     | Baby Store, Beverage Stall, Healthcare Institution, Internal Selling, Market Retail, Minimarket, Residential Retail, Second Dealer |
| `SM03388`     | Internal Selling                                                                                                                   |

#### Overall Sales Performance by Salesman

![Monthly Transactions](/Image/Table/WithoutTitle/table_salesman_performance_overall_NO_TITLE.png)

- There are 6 salesmen who achieved sales above `Rp1.0 M` and 3 salesmen who achieved sales above `Rp2.0 M`.
- The highest sales were achieved by salesman SM03353 with a sales value of `Rp3,403,193,635` and the lowest sales were achieved by SM03388 with a sales value of `Rp7,668,108`. For non-Internal Selling only salesman, the lowest sales were achieved by SM03331 with a sales value of `Rp514,293,364`.
- A total of `267` transactions with a sales value of `Rp72,488,314` were not assigned to any salesman. If this is due to a system error, it must be resolved as soon as possible to get more accurate salesman performance.
- The highest average sales value was achieved by SM03353 at `Rp8,550,738`, followed by SM03376 with an average of `Rp8,155,428`. Both are Supermarket and Minimarket only salesman.
- Based on the high number of customer categories served and the low sales value from SM03331, it can be assumed that the area covered by SM03331 has low purchasing power.

#### Sales over Month by Salesman

![Sales over Month by Salesman](/Image/Table/WithoutTitle/table_salesman_performance_sales_NO_TITLE.png)

- There are two distinct sales trend patterns observed among the salesmen:
  - **December Peak**: Five salesmen experienced their highest sales in December 2024; 
  - **January Peak**: Seven salesmen experienced their highest sales in January 2025.
- These two patterns are also reflected in the [sales over month performance by product category](#sales-over-month-by-product-category).

#### Total Sales by Salesman & Product Category

![Total Sales by Salesman & Product Category](/Image/Table/WithoutTitle/table_sales_performance_by_salesman_n_product_category_NO_TITLE.png)

#### Total Sales by Salesman & Customer Category

![Total Sales by Salesman & Customer Category part 1](/Image/Table/WithoutTitle/table_sales_performance_by_salesman_n_customer_category_NO_TITLE_1.png)

![Total Sales by Salesman & Customer Category part 2](/Image/Table/WithoutTitle/table_sales_performance_by_salesman_n_customer_category_NO_TITLE_2.png)

![Total Sales by Salesman & Customer Category part 3](/Image/Table/WithoutTitle/table_sales_performance_by_salesman_n_customer_category_NO_TITLE_3.png)

![Total Sales by Salesman & Customer Category part 4](/Image/Table/WithoutTitle/table_sales_performance_by_salesman_n_customer_category_NO_TITLE_4.png)

### Customer Performance

#### Overall Sales Performance by Customer Category

![Customer Category Overall Performance](/Image/Table/WithoutTitle/table_customer_cat_performance_overall_NO_TITLE.png)

#### Sales over Month by Customer Category

![Sales over Month by Customer Category](/Image/Table/WithoutTitle/table_customer_cat_performance_sales_NO_TITLE.png)

#### Total Sales by Product Category & Customer Category

![Total Sales by Product Category & Customer Category](/Image/Table/WithoutTitle/table_product_n_customer_cat_performance_sales_NO_TITLE.png)

#### Top 3 Customer by Sales per Customer Category

![Top 3 Customer by Sales per Customer Category](/Image/Table/WithoutTitle/table_top_3_customer_NO_TITLE_1.png)

![Top 3 Customer by Sales per Customer Category](/Image/Table/WithoutTitle/table_top_3_customer_NO_TITLE_2.png)

#### 3 Customers with Highest Returns per Customer Category

### Product Performance

#### Overall Sales Performance by Product Category

![Product Category Overall Performance](/Image/Table/WithoutTitle/table_product_cat_performance_NO_TITLE.png)

#### Sales over Month by Product Category

![Product Category Overall Performance](/Image/Table/WithoutTitle/table_product_cat_performance_sales_NO_TITLE.png)

#### Top 10 Product by Sales

![Top 10 Product by Sales](/Image/Table/WithoutTitle/table_top_10_product_by_sales_NO_TITLE.png)

#### Bottom 10 Product by Sales

![Top 10 Product by Sales](/Image/Table/WithoutTitle/table_bottom_10_product_by_sales_NO_TITLE.png)

#### Top 10 Products with Highest Returns

![Top 10 Product by Returns](/Image/Table/WithoutTitle/table_top_10_product_by_returns_NO_TITLE.png)

#### Top 10 Products with Highest Return to Sales Ratio

## Recommendations


