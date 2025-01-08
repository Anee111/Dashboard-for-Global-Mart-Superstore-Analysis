# Dashboard for Global Mart Superstore Analysis PowerBI


Problem statement: To Create an analytical project to explore and optimize the e-commerce ecosystem. The project aims to analyze product performance by tracking sales, categories, sub-categories,  Customer insights will be derived by segmenting data based on regions, zip codes, and purchasing behavior. Orders will be analyzed to monitor delivery timelines, shipping modes, and statuses, helping to identify inefficiencies in the supply chain. Transactions will be assessed for revenue, discount patterns, and profit margins to improve financial decision-making. Return reasons and customer reviews will provide actionable insights to enhance product quality and service. The goal is to deliver a comprehensive dashboard that enables data-driven decisions to improve customer satisfaction, streamline operations,
and drive profitability.

Steps followed to create Dashboard:

1. Load
2. Transform
3. Presentation


   # 1. LOAD
    Global mart data is loaded to powerbi. The data is of csv format with below fields. There are three tables orders, people and returns.
![image](https://github.com/user-attachments/assets/289644e8-186c-40f8-9fcb-778eb28c6b7b)

Data model is created by having relationship as orders to returns ...> many to one relationship (both direction)
                                                orders to people ... > many to one relationship (single direction)


# 2. Transform

A. Data Cleaning
Date Formatting:
Converted Order Date and Ship Date columns to a proper Date data type.
checked whether all the fields are in appropriate data type.

Removing Duplicates:
Checked for and removing any duplicate rows in the dataset.

Handling Missing Values:
There are no missing values in the dataset.

Trimming and Cleaning Text:
Remove unnecessary whitespace in columns like Customer Name, City, or Product Name.


B. Data Transformation

Merging:
Merged peoples column people with orders and returns table returned column with orders .. For all the orders it is marked whether the order is returned yes or no.

Calculated Columns:
Create new calculated columns for additional insights:
cost price  =  sales - profit
day
month
year
quarter
profit margin
order age

Measures:
To easily identify created measures all the measures have been included in the separate measures table.


Hierarchy Creation:
Create hierarchies ( Category > Sub-Category > Product Name) for drilling down in visualizations.
                   ( Country > Region >  state >  city)
                   (Year >  Quarter > month > Weekno)
                   

# 3. Presentation

Created dashboard with kep KPI's Total sales, total profit, return rate, total customers.




