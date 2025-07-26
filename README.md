# *Pratama Nusantara Dairy* - Sales Performance Analysis (Nov 2024 - Feb 2025)

## Project Background
### Company Info
**Pratama Nusantara Dairy (PND)** is an Indonesian dairy company with two main plants in Bekasi and Bandung. PND offers 90 SKUs and distributes through 70+ partners across Indonesia. This project focuses on analysis of sales data from November 2024 to February 2025 for one of the city in Sumatra. The objective is to gain **deeper**, **actionable insights** into the sales performance attributed to individual salesman, customer, and product. Recommendations will be provided to improve sales performance, mainly for Area Business Manager.
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
#### Total Sales over Month
#### Month over Month Sales Growth
#### Total Return over Month
#### Total Transactions over Month

### Salesman Performance
#### Total Sales over Month by Salesman
#### Total Transactions over Month by Salesman
#### Other Metrics

### Customer Performance
#### Performance by Customer Category

### Product Performance
#### Performance by Top-Level Product Category
#### Performance by Product Variant

### Discount Performance Analysis

## Recommendations


