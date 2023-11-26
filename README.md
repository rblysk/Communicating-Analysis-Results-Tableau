# COMMUNICATING-ANALYSIS-RESULTS-TABLEAU

**VISUALISING DATA USING TABLEAU**

**HANDS-ON PRACTICE**

-----

**YOUR ROLE**

You are an analyst in the AdventureWorks company in the Data Ops department, which is responsible for fulfilling internal data needs, from adding and integrating new data sources, writing ETLs and also developing dashboards which would be utilized by other teams.

Since you are well known across the company as the go-to guy for making amazing interactive dashboards, your colleague from the Sales team pays you a visit. 

Recently he has provided the Sales Director with your sales data analysis you did in the previous module (Spreadsheets sprint), though they have realized that this data would be something they would like to track overtime and they need it to be updated automatically. 

For this reason he is looking for a person to use this data and create Tableau Dashboard.

For this sprint we will be using Tableau Public. 

-----

**DATA**

As in one of the previous sprints you will be using AdventureWorks company data which is readily available on BigQuery. 

You have already analyzed part of this data while doing Spreadsheets Sprint, though got more familiar with databases once you moved to SQL sprint, so the data is already familiar to you. 

In case you need this data you can always refer to the schema of this database.


As you may have already guessed from the Hands On task intro, we will be using similar charts and graphs which you have already practiced in the Spreadsheets sprint. Since our aim is to make sure that you have skills to create dashboards, the main purpose of this Hand On task is not to get more practice writing SQL queries, but to get more practice developing interactive dashboards, which would be easy to understand and draw insights from. 

We will be using Sales Order Data, which you will copy to your own google account and then connect it as a data source in Tableau Public.


While creating this dashboard imagine that data in your spreadsheet is being updated daily. 

General advice when constructing a dashboard is to always think about the user and how you would look into the dashboard yourself if you were Director of Sales. 

How would you want to interact with the dashboard and what fields would you like to filter?

-----

**MONDAY**

On Monday you start with adding some main KPIs to the top of your dashboard: 

Orders Count, 

Total Sales ($), 

Average Order Value (AOV) and Avg. 

Days to Ship. 

For the last 2 KPIs you will need to implement custom calculations.

You then create 2 additional charts showing monthly sales:

**Monthly sales by year month**
**Monthly sales by month year over year**

To do this you start by connecting your personal copy of Sales Order Data to Tableau Public.

Next you create your KPI graphs as big numbers on top of the dashboard, followed by line charts for monthly sales. 

Of course you include a date range filter at the top of the dashboard, so your users could filter all these graphs by their selected dates.

-----

**TUESDAY**

On Tuesday you decide to add a new graph depicting sales by type: **Offline vs Online.**

You talk with your colleague from the sales department and find out that all the sales in salesorderheader table with no sales person ID actually indicate online sales, while sales with sales person ID provided depict Offline sales, done by sales people in your company.

To do this you add a new field called “Sales Type”. This field should be created using calculated field functionality.

-----

**WEDNESDAY**

On Wednesday your colleague from the Sales department says that the Sales Department is also very interested in dynamics of sales reasons and their performance over time. 

You decide to utilize the Tableau possibility of joining multiple tables. 

You know that sales reasons reside in a separate table called salesreason, so you connect your new table to Sales Order Header data to extract human readable sales reasons, instead of Sales Reason ID.

Looking at the data you realize it is not perfect. 

In the absolute majority of cases, the sales reason is not assigned, also you notice that in roughly 20% of orders, more than 1 reason is assigned to sale.

Since several reasons may be assigned you decide to create a stacked area chart which would indicate the most popular reasons captured for certain months over the year and express it as 100% of total sales.

-----

**THURSDAY**

On Thursday you decide to include some information about Sales person performance, so Sales Manager could see who out of his employees do best. 

For this you construct a bar chart showing the total number of sales per Salesperson ID. 

To provide a bit more information you add cumulative sales expressed as % of total sales.


You understand that for this chart to be created you do not want to have complex calculations of running total and total in your query. You decide that you will use a simplified approach to achieve the same result with the help of Tableau since it provides the ability to have advanced calculations as table calculations and utilize running total calculation.

Thus for your data you decide not to add additional data sources to DataStudio and simply reuse the dataset added on Monday which has the ability to show revenue by different sales persons.

-----

**FRIDAY**

On Friday you decide to finish your dashboard with some geographical analysis. 

You decide to join another table, which has Teritory ID and regions mapping. You will use Tableau functionality for reporting maps and will create one based on Total Sales.


To create such a graph you will need to join the SalesTeritories table with SalesOrderHeader table. 

Then use Map chart type and select country regions to be used as geographical indicators, your reporting metric should be total Sales.

-----

**THE PROJECT**

**MONDAY+TUESDAY:** https://public.tableau.com/app/profile/radvilas.blyskys/viz/Hands-onPracticeMonday-RadvilasBlyskys_/Dashboard1

**WEDNESDAY:** https://public.tableau.com/app/profile/radvilas.blyskys/viz/Hands-onPracticeWednesday-RadvilasBlyskys/Dashboard2

**THURSDAY:** https://public.tableau.com/app/profile/radvilas.blyskys/viz/Hands-onPracticeThursday-RadvilasBlyskys/Dashboard3

**FRIDAY:** https://public.tableau.com/app/profile/radvilas.blyskys/viz/Hands-onPracticeFriday-RadvilasBlyskys/Dashboard1
