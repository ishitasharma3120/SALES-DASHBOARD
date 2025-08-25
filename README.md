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
  - Total Sales - Sum of all the sales 
  - Count of Orders - DistinctCount of orders
  - Total Returns - DistinctCount of all returns quantities
  - Percentage of Return Quantities- %return = sum(Returns[ReturnQuantity])/DISTINCTCOUNT(Final_Sales[OrderNumber])
  - 
