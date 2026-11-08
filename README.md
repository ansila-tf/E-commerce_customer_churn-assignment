E-Commerce Customer Churn Analysis (MySQL)

Project Overview

This project focuses on analyzing e-commerce customer churn using MySQL. It includes data cleaning, data transformation, exploratory data analysis, and customer returns analysis.

Tools Used

* MySQL
* MySQL Workbench

Database Details

Database Name: ecomm

Tables:

* customer_churn
* customer_returns

1. Data Cleaning

Performed the following data cleaning operations:

* Imputed missing values using Mean for:
    * WarehouseToHome
    * HourSpendOnApp
    * OrderAmountHikeFromlastYear
    * DaySinceLastOrder
* Imputed missing values using Mode for:
    * Tenure
    * CouponUsed
    * OrderCount
* Removed records where WarehouseToHome was greater than 100.
* Replaced Phone with Mobile Phone in PreferredLoginDevice.
* Replaced Mobile with Mobile Phone in PreferedOrderCat.
* Replaced COD with Cash on Delivery.
* Replaced CC with Credit Card.

After cleaning, the dataset contained 5,628 customer records.

2. Data Transformation

* Renamed PreferedOrderCat to PreferredOrderCat.
* Renamed HourSpendOnApp to HoursSpentOnApp.
* Created ComplaintReceived column:
    * Yes if Complain = 1
    * No otherwise
* Created ChurnStatus column:
    * Churned if Churn = 1
    * Active otherwise
* Dropped the original Churn and Complain columns.

3. Exploratory Data Analysis

Performed 17 SQL analysis tasks:

1. Counted churned and active customers.
2. Calculated average tenure and total cashback of churned customers.
3. Calculated the percentage of churned customers who complained.
4. Identified the city tier with the highest churned customers preferring Laptop & Accessory.
5. Identified the most preferred payment mode among active customers.
6. Calculated total order amount hike for single customers preferring Mobile Phone.
7. Calculated the average number of registered devices among UPI users.
8. Identified the city tier with the highest number of customers.
9. Identified the gender that used the highest number of coupons.
10. Calculated customer count and maximum app hours for each preferred order category.
11. Calculated total order count for Credit Card users with the maximum satisfaction score.
12. Calculated average satisfaction score of customers who complained.
13. Identified preferred order categories among customers who used more than five coupons.
14. Identified the top three categories with the highest average cashback.
15. Analyzed preferred payment modes for customers with 10 months of tenure and more than 500 orders.
16. Categorized warehouse-to-home distance and analyzed churn status.
17. Retrieved details of married customers in City Tier 1 whose order count was above the overall average.

4. Customer Returns Analysis

Created a customer_returns table with the following columns:

* ReturnID
* CustomerID
* ReturnDate
* ReturnAmount

Inserted 8 sample return records.

5. Final JOIN Analysis

Used an INNER JOIN between customer_returns and customer_churn to retrieve return details and customer information for customers who had churned and submitted complaints.

Conclusion

This project demonstrates the use of MySQL for data cleaning, data transformation, customer behavior analysis, churn analysis, aggregation, subqueries, and table joins.

Through this assignment, I gained practical experience in handling real-world datasets and extracting meaningful insights using SQL.
