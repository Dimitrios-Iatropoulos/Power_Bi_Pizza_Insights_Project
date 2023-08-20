# Power_Bi_Pizza_Project_Insights
Analyzing pizza sales data from a fictional pizzeria using Power BI to uncover trends, customer preferences, and sales patterns. Gain valuable insights into pizza orders, sizes, so we can make business decisions with data-driven analysis.
## Data Source
The dataset used for this project can be found [here](https://www.kaggle.com/datasets/shilongzhuang/pizza-sales) and contains 1 table with 12 relevant features
## Data Transformation
The following data transformation steps were taken:
- Replaced values in "pizza_size column" (e.g., M to Medium).
- Removed "order_time" and "pizza_ingredients" columns as it didn't provide any value to my analysis.
- Renamed the column names from "pizza_name," "pizza_size," "quantity," and "category" to "Name," "Size," "Quantity," and "Category." 
-	A Calendar table was created from "order_date" column using the following DAX:
  
` calendar = calendar(min(pizza_sales[order_date]), max(pizza_sales[order_date]))`
-	Established the relationship between the two tables manually.





