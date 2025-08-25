# SALES-DASHBOARD
An interactive dashboard built on POWERBI to visualize sales trends based on various filters and product details overview.


## ✨ FEATURES
- Interactive charts and graphs
- Filter by Year-Quarter, Region, Gender, Region, Category and Email
- Multiple DAX function added to provide dynamic KPIs and cards.



## ✨ TECH USED
- Build using POWERBI
- Dataset in csv format
- Transformed using POWER QUERY

## ✨ POWER QUERY TRANSFORMATION
- Validated data types of all the columns in every table.
- Merged Sales 2015,2016 and 2017 data into on final_Sales table.
- Verified column Quality and Column Distribution for every table
  <img width="1450" height="643" alt="image" src="https://github.com/user-attachments/assets/ef3e1fa5-970f-4837-b407-ccb1df8ec159" />

  ## ✨ DATA MODELING

  <img width="1391" height="789" alt="image" src="https://github.com/user-attachments/assets/2c02aa80-31a1-4511-a620-f244da1ee7b2" />
 

  ## ✨ DAX CALCULATIONS

  CARDS 
  - Total Sales - Sum of all the sales 
  - Count of Orders - DistinctCount of orders
  - Total Returns - DistinctCount of all returns quantities
  - Percentage of Return Quantities- %return = sum(Returns[ReturnQuantity])/DISTINCTCOUNT(Final_Sales[OrderNumber])
CHARTS
- STACKED BAR CHART - Sales by Sub Category and Status
- Status is a calculated column based on annual Income if income is more than 1Lakh then high, between 1Lakh and 70k, medium otherwise Low.
- MAP - Total Sales measure by Country
- TABLE - based on field parameters for measures and dimension.
- Measures- MeasureSelector = {
    ("TotalSales", NAMEOF('MeasureTable'[Totalsales]), 0),
    ("Returns", NAMEOF('MeasureTable'[totalReturns]), 1),
    ("Order Count", NAMEOF('MeasureTable'[CountOrder]), 2)
}
- Dimension - Dimension = {
    ("Customer Name", NAMEOF('Customers'[FullName]), 0),
    ("Product Name", NAMEOF('Products'[ProductName]), 1)
  }
- LINE CHART - Total Sales by Date
- Adjusted Sales based on range parameter - WHATIF analysis - Price adjustment as percentage = GENERATESERIES(-50, 50, 10)
KPI CARDS
- Total Sales for a year-month based on previous month Sales- previousmonthsales = CALCULATE(sum(Final_Sales[Sales]),DATEADD(Datetable[Date],-1,month))
- Total orders for a year-month based on previous month orders - previousmonthorder = CALCULATE(DISTINCTCOUNTNOBLANK(Final_Sales[OrderNumber]),DATEADD(Datetable[Date],-1,month))

  ## ✨ PRODUCT OVERVIEW
  - CARDS
  - product Price and Product Cost based on a selected product
  - TABLE - FULL NAME - concatenate version of first name and last name, Gender, EmailAddress, Total Sales and parent Status.
  - PARENT STATUS is a calculated column based on if condition,if total children >0, then parent otherwise not parent.
  - PIE CHARTS
  - Total Sales by Marital Status
  - Total Sales by Parent Status
    RIBBON CHART- Total Sales by year and country

  ## ✨ TOOLTIP
  <img width="430" height="303" alt="image" src="https://github.com/user-attachments/assets/f6c6afaa-b1c2-4d9a-8184-51b816aad3f2" />

