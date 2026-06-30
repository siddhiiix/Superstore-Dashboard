# Superstore-Dashboard
**OVERVIEW**
<img width="1510" height="876" alt="Overview1" src="https://github.com/user-attachments/assets/b5a51146-8130-468a-bee1-b46ae139f343" />

**SEGMENT**
<img width="1515" height="885" alt="Segment2" src="https://github.com/user-attachments/assets/251ec940-3a6c-43e3-843d-f5d3092fe6f0" />

**PRODUCT**
<img width="1501" height="883" alt="Product3" src="https://github.com/user-attachments/assets/a8ed3e8a-ac85-4665-9594-d07b657241d8" />

**ABOUT THE PROJECT**

The project aims to empower SuperStore by providing valuable sales performance insights and actionable improvements. Through Power BI's visually appealing reports and interactive dashboards, decision-makers can effortlessly explore data, gaining valuable insights to drive informed actions.

It will enhance decision-making and optimize business operations with an interactive dashboard that visualizes sales, profit, top customers and states by sales, subcategory analysis, returned orders, and many more insights and offers slicer-based filtering for improved insights and performance optimization.

**DATASET**
This dataset is the Superstore dataset. This contains 2 excel files:

1. SuperStore Orders
This excel file contains the data about orders made by customers for any product. This table also contains information about customers like name, address and information about orders like product name, order-id, product category. There are total 19 columns and 5899 rows in this excel file.

2. SuperStore Returns
This excel file contains information about the returned order id.

**DAX Formulas used in Measures**

1. Total Sales
   
Total Sales = SUM(Orders[Sales])

2. Total Profit
   
Total Profit = SUM(Orders[Profit])

3. Extract Year from Date
   
Year = Year(Orders[Order Date])

4. Extract Month from Date
   
MonthNo = Month(Orders[Order Date])

5. Year over Year Growth%
    
YoY Sales Growth% =  VAR PYSales =  CALCULATE([Total Sales], DATEADD(Orders[Order Date], -1, YEAR))  RETURN  DIVIDE(([Total Sales]-PYSales), PYSales)*100

6. Gross Margin%
    
Gross Margin% = DIVIDE([Total Profit], [Total Sales])*100
