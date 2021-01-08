Data Analysis Project using Power BI - Sales/ Revenue Insight for a company

This project shows the sales insight of a company named Atliq Hardware in Delhi which sells a large number of products each year across India.
I have generated a power BI based dashboard to track the sales and revenue of the company regionwise/ customerwise for last 3 years, so that management can take decision to boost the sales and revenue.

The report helps to see:

* Overall sales/Revenue
* Yearly Revenue/ Sale 
* Monthly Revenue/ Sale 
* Sale & Revenue by Customer 
* Sale & Revenue by Region 
* Top 5 Customers 
* Top 5 Sales Quantities by Region

Tools that we used:

-> Microsoft Power BI Desktop 
-> MYSQL Workbench

Skills required to create Dashboard & Report:

Data Cleansing 
SQL Query Language
DAX language 
Analytical Skills 

Below are some queries that I used to verify my report - 

--> To see all transactions in 2020 -

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

--> To see total revenue in year 2020 -

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

--> To see total revenue in year 2020, January Month -

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

--> To see total revenue in year 2020 in perticular region for example Mumbai region - 

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark002";
 
