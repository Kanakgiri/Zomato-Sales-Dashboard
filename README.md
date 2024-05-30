# Zomato Sales Dashboard

## Purposes Of The Project

The goal is to provide insights to improve business operations, enhance customer satisfaction, and drive growth for the food delivery service. By analyzing the data, actionable recommendations are provided, such as which menu items to promote, which restaurants to partner with, or how to tailor marketing campaigns to different customer segments.


![Index](https://github.com/Kanakgiri/Zomato-Sales-Dashboard/assets/171118310/78263c65-8bf4-43d4-ab2a-62781c43af5e)
![Overview](https://github.com/Kanakgiri/Zomato-Sales-Dashboard/assets/171118310/25ba56cb-72c7-4c5d-83c1-6a9997226662)
![User Performance](https://github.com/Kanakgiri/Zomato-Sales-Dashboard/assets/171118310/b0b40346-ec34-4b2a-9558-e59cc5784704)
![City Performance](https://github.com/Kanakgiri/Zomato-Sales-Dashboard/assets/171118310/06d74fa4-6914-45cb-8937-27baeac53f85)

## About Data

The dataset has four files
- Menu  : This contains information like Menu-Id, Food-Id, Restaurant-Id, Price.
- Restaurant  : This contains information like Restaurant-Id, City, Adress, Ratings.
- Orders  : This contains information like Restaurant-Id, Order-Id, Order_Date, Quantity, Sales_Amount, User-Id.
- Users  : This contains information like User-Id, Name, Age, Gender, Marital_Status, Occupation.

## Tools Used

- Microsoft Excel
- Power BI

## Approach Used

- Feature Engineering: This will help us generate some new columns from existing ones using Power Query.

Restaurant table is Merged with Orders table using the common column `R-Id` and null values in `city` column is replaced by others. Users table is Merged with Orders table using the common column `User-Id`.

A new column `Year` is cretaed in Orders Table using column `order_date`.

``` Year = VALUE(format(orders[order_date],"yyyy")) ```

Seperate Measure_Table is created in Power BI which contains measures like Total users, Active users, Number of cities, Order count, Rating count, Sale value.

- Exploratory Data Analysis (EDA): Exploratory data analysis is done to answer the listed questions and aims of this project.

## Conclusion:

Zomato provided services in 822 cities and connected with 77,929 users who got 1,50,281 orders delivered.

## Business Questions Answered

1. What is the total sales and total number of quantities sold?
- The total is ₹ 987 million and total number of quantities sold is 2 million.

2. What are the total ratings and total number of orders?
- The total ratings are 148 thousand and the total number of orders is 150 thousand.

3. How many Veg and Non-Veg Dishes are there?
- There are 101 thousand Non-Veg Dishes and 271 thousand Veg dishes.

4. What is the total number of Active Users?
- The total number of Active Users is 78 thousand.

5. What is the user distribution by Age?
- Most of the users are of Age 23 (18,820) and Age 22(14,690) followed by Age 25,23 and 26.

6. Which City has the most sales?
- Tirupati (43 million) has the most sales followed by Electronic City.

7. What is the total number of restaurants?
- The total number of restaurants is 149 thousand.

8. What is the average order per User?
- The Average order per User is 1.93.

9. What type of Users by Occupation drive the most of the sale?
- Students drive the most of the sales (₹529 million) followed by employed (₹301 million) and self-employed (₹139 million).
