PROJECT 2

LITA Capstone Report: Customer Data Performance 

CONTENT
 Customers Data
 Customers Subscription Type
 Customers Subscription Duration
 Region-wise Customers Performance

OVERVIEW
This repository contains data and insights on our company's customer performance, providing a comprehensive view of our customers metrics and trends and also to know the fast moving subscription

DATA ANALYSIS TOOLS
Microsoft Excel
SQL
Power Business Intelligent(POWER BI)

MICROSOFT EXCEL

DATA CLEANING 
Customers Data was clean by removing duplicate. how did i achieved this, i highlighted the sheet by pressing ctr+shift+down arrow on the keyboard, go to data and click on remove duplicate

ADD COULUMN
I added a column to the data to get my subscription duration

Use of Excel Pivot Table and graghic to get the following
Revenue by Region
Revenue by Subsription Type
Top 10 Customers by Revenue

![REVENUE BYYEAR](https://github.com/user-attachments/assets/7dc16666-43a1-4689-a8f3-4bd0b1e7dc07)

![SUBSCRIPTION TYPE BY REVENUE](https://github.com/user-attachments/assets/804e7980-a8a0-4a4b-8875-732c4e14b2dd)

![Top 10 Customers](https://github.com/user-attachments/assets/f4337d66-a9a0-4e41-a3b3-23fe6399fba5)

![Revenue by Region](https://github.com/user-attachments/assets/309b8251-bbee-45f4-91c6-e6f9be33441a)

![Revenue by Canceled png1](https://github.com/user-attachments/assets/af9eddfd-d5d5-4363-a6b5-83c8979ef93e)

![Customer's Data (Revenueby Canceled)](https://github.com/user-attachments/assets/c523706a-dd7f-4d1f-8fc3-9517151b9b8e)

SQL
CREATE DATABASE LITA_CAPSTONEPROJECT_DB

Right on the Data base 
Click on task
Click on import Data

select * from [dbo].[CustomerData$]

------retrieve the total number of customers from each region-------

SELECT region, COUNT(CustomerID) AS total_customers
FROM [dbo].[CustomerData$]
GROUP BY region;

-----find the most popular subscription type by the number of customers-----

SELECT SubscriptionType, COUNT(CustomerID) AS total_customers
FROM [dbo].[CustomerData$]
GROUP BY SubscriptionType
ORDER BY total_customers DESC

SELECT CustomerID, SubscriptionStart, SubscriptionEnd
FROM [dbo].[CustomerData$]
WHERE DATEDIFF(month, SubscriptionStart, SubscriptionEnd) < 6
 AND Canceled = 0

 Power Bi
 From Canvas click on Get Data and import your data
Select data and click on Transform data.
Remove duplicate data by selecting your entire column and click 'delect duplicate rows.
Select Table view add Column for Subscription duration, Rename the new column as Subscriptionn Duration, use the formular Datediff(SubscriptionEnd,SubscriptionEnd,Month).
Click on Close and apply.
Click on Home and go to your Report view.
Build your interactive dashboard .

![CUSTOMER PERFORMANCE ANALYSIS](https://github.com/user-attachments/assets/4925ed2d-ae2a-4a7e-90f2-741f150eba2b)


