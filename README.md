# ATLIQ-Sales-Insight : Data-Analysis-using-SQL-and-Power BI

## OVERVIEW:
    PROJECT NAME
    PROBLEM STATEMENTS
    APPROACH - PROJECT PLANNING & AIMS GRID
    DATA ANALYST APPROACH
    DATA ANALYSIS USING SQL
    DATA ANALYSIS USING TABLEAU
    NOTE

**About Project:**

•	Performed Data Cleaning, Analysing and Visualization on India based hardware company sales insights.

•	Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design star schema data model on Power BI.

•	Developed a Power BI dashboard to perform analysis, producing quantitative visualizations in Power BI to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.


About ATLIQ: 

•	AtliQ Hardware is Computer Hardware and peripheral Manufacture company.


Technologies Used: 

•	Advance Excel

•	MySQL | SQL Server

•	Power BI

•	Power Query


## PROBLEM STATEMENTS:

Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.

Q1. Revenue breakdown by cities.

Q2. Revenue breakdown by years & months. 

Q3. Top 5 customers by revenue & sales quantity.

Q4. Top 5 Products by revenue.

Q5. Net Profit & Profit Margin by Market.


## APPROACH - PROJECT PLANNING & AIMS GRID

1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.

2. Stake Holders: Who will be involved?
    
•	Sales Director
•	I.T. Team
•	Customer Service Team
•	Data & Analytics Team

3. End Result: What do we want to achieve?

An automated dashboard providing quick & latest sales insights in order to support data driven decision making.

4. Success Criteria: What will be our success criteria?
    
•	Dashboards uncovering sales order insights with latest data available.
•	Sales team able to take better decision & prove 10% cost savings of total spend.
•	Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.


## DATA ANALYSIS USING SQL:

    • Show all customer records
               
               SELECT * FROM customers;
    
    • Show total number of customers
               
               SELECT count(*) FROM customers;
    
    • Show transactions for Chennai market (market code for chennai is Mark001)
               
               SELECT * FROM transactions where market_code='Mark001';
    
    • Show distrinct product codes that were sold in chennai.
               
               SELECT distinct product_code FROM transactions where market_code='Mark001';
    
    • Show transactions where currency is US dollars.
               
               SELECT * from transactions where currency="USD"
    
    • Show transactions in 2020 join by date table.
               
               SELECT transactions., date. FROM transactions INNER JOIN date ON 
               transactions.order_date=date.date where date.year=2020;
    
    • Show total revenue in year 2020.
               
               SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
               where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
    
    • Show total revenue in year 2020, January Month.
        
               SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date 
               where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");


## DATA ANALYSIS USING Power BI:

Power BI Public Dashboards: Revenue & Profit Analysis Power BI
Creating Star Schema in Power BI

![Image](https://github.com/user-attachments/assets/d9df999c-2d32-4429-8758-f002b848fa39)

### Power BI Dashboard: Key Analysis

![Image](https://github.com/user-attachments/assets/a7a1806b-c659-4e1d-a9f8-454289648e94)


### Power BI Dashboard: Profit Analysis


![Image](https://github.com/user-attachments/assets/22a6648a-5225-4a4a-89f5-1f1714261871)

### Power BI Dashboard: Performance Analysis

![Image](https://github.com/user-attachments/assets/abeeabf0-72c5-41ff-b7af-45d52e7178e8)

## RECOMMENDATION:

Based on the dashboards Insights:

  1) Should Maintain healthy relationship with the customers in Bhubaneshwar, Hyderabad, Chennai as they are highest profit % by market.
  2) Make some stategy for Lucknow market as its revenue are less and also profit % are in negative.
  3) Figure out what need to be done as sales quantity in Kanpur, Surat, Patna, Bhubaneshwar, Chennai are the lowest.
  4) North zone have highest revenue contribution but lowest profit % whereas South zone have lowest revenue contribution but highest profit %. Try to increase customers in South zone.
  5) Delhi is the highest revenue contibutor and second highest profit contributor whereas Mumbai is the second highest revenue contributor and highest profit contributor. So its need to be implement the same market strategy as in mumbai to increase the profit % in Delhi.

