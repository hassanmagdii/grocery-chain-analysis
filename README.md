# grocery-chain-analysis
Power BI project analyzing retail sales performance across multiple cities and countries. Includes dashboards explaining uneven category sales, discount effectiveness, and salesperson performance, with actionable insights for next-quarter planning.

# Note
You will find the project files here, in addition to the Power PI file.
https://drive.google.com/drive/folders/1krK7eBqPJpIG7rn_-D5tqZwjp6Gmfd58?usp=sharing 

# Dashboard 
![grocery-chain-analysis](https://github.com/user-attachments/assets/98f2e2f7-20ae-4155-a90f-c57f6eb3abbc)
- **Total Net Sales** : 4.33B $
- **Total Quantity**: 88M $
- **AOV**: 641
- **AVG Discount%**: 3%
- **YOY**: 8.60%
- **Net Sales by Month**: Distribution of sales by months
- **Net Sales by Category**: Distribution of sales by categories
- **T. Sales by Customers**: Analysis of Sales for customers
- **T. Sales by Sales Persons**: Analysis of sales for sales person
- **Net Sales by Gender**: Distribution of sales by gender
- **T. Sales and QTY. by City**: Distribution of sales and quantity by city

# Technical Steps 
1. **connect to power bi**
- Open Power BI Desktop.
- Import each CSV as its own query. Ensure types: IDs as text, dates as Date/DateTime, numeric as Decimal/Whole.
- sales.csv: keep SalesID, SalesPersonID, CustomerID, ProductID, Quantity, Discount, TotalPrice, SalesDate, TransactionNumber. Add GrossAmount = Quantity * RELATED Price later via measure (do NOT merge in PQ to keep star).
- products.csv: keep ProductID, ProductName, Price, CategoryID, Class, ModifyDate, Resistant, IsAllergic, VitalityDays. Trim/Clean text; remove duplicates on ProductID.
- categories.csv: keep CategoryID, CategoryName; Trim/Clean; remove duplicates.
- customers.csv: keep CustomerID, FirstName, LastName, CityID, Address; create CustomerName = FirstName & ' ' & LastName; remove duplicates on CustomerID.
- employees.csv: keep EmployeeID, FirstName, LastName, CityID, Gender, HireDate; create EmployeeName = FirstName & ' ' & LastName; remove duplicates.
- cities.csv: keep CityID, CityName, CountryID (Zipcode may be repurposed if needed). Remove duplicates.
- countries.csv: keep CountryID, CountryName, CountryCode; remove duplicates.
- Create a Date table in DAX after loading (CALENDAR) and mark as date table.

2.  **Make a Dashboard**
- **Total Net Sales** : Use a card visual to display Total Net Sales
- **Total Quantity**: Use a card visual to display Total Quantity
- **AOV**: Use a card visual to display AOV
- **AVG Discount%**: Use a card visual to display AVG Discount
- **YOY**: Use a card visual to display YOY
- **Net Sales by Month**: Use line chart to display Net Sales by Month
- **Net Sales by Category**: Use stacked bar chart to display Net Sales by Category
- **T. Sales by Customers**: Use stacked bar chart to display Total Sales by Customers
- **T. Sales by Sales Persons**: Use stacked column chart to display Total Sales by Sales Persons
- **Net Sales by Gender**: Use Donut chart to display Net Sales by Gender
- **T. Sales and QTY. by City**: Use Azure map to display Total Sales and Quantity by City

# Contact
Created by [Hassan Elshaer]  
Email [alshaerhassan72@gmail.com] 
[LinkedIn]( www.linkedin.com/in/hassan-elshaer-20849a23a )
[GitHub](https://github.com/hassanmagdii)
