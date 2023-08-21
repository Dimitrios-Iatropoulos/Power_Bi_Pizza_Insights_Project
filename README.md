# Power_Bi_Pizza_Insights_Project
Analyzing pizza sales data from a fictional pizzeria using Power BI to uncover trends, customer preferences, and sales patterns. Gain valuable insights into pizza orders, sizes, so we can make business decisions with data-driven analysis.
# Data Source #
The dataset used for this project can be found [here](https://www.kaggle.com/datasets/shilongzhuang/pizza-sales) and contains 1 table with 12 relevant features
# Data Transformation #
The following data transformation steps were taken:
- Replaced values in "pizza_size column" (e.g., M to Medium).
- Removed "order_time" and "pizza_ingredients" columns as it didn't provide any value to my analysis.
- Renamed the column names from "pizza_name," "pizza_size," "quantity," and "category" to "Name," "Size," "Quantity," and "Category." 
-	A Calendar table was created from "order_date" column using the following DAX:
  
`calendar = calendar(min(pizza_sales[order_date]), max(pizza_sales[order_date]))`
-	Established the relationship between the two tables manually.

# DAX Measures #
The DAX measures formulated for this project are:

1.	Total Orders: `Total Orders = DISTINCTCOUNT(pizza_sales[order_id])`
2.	Total Sales: `Total Sales = sum(pizza_sales[total_price])`
3.	Total Pizzas Sold: `Total Pizzas Sold = sum(pizza_sales[Quantity])`
4.	Average Order Value: `AOV = [Total Sales]/[Total Orders]`

# Data Analysis and Visualization #
#### Top Metrics
In the analysis of the fictional pizzeria's top metrics, the total sales for the period reached $817.860, driven by a number of orders totaling 21,350. This resulted in the sale of 49,574 individual pizzas. Furthermore, the calculated average order value stood at $38,31 reflecting a consistent pattern of customer spending.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/1.png)
#### Sales By Month
The sales trends by month in the fictional pizzeria demonstrate a dynamic pattern over the year. July emerges as a standout month with approximately $73000 in sales. Likewise, May, March and November also present robust sales around $70,000. On the other hand, the months of September and October showcase lower sales at around $64,000 each. These variations suggest potential seasonal trends that can guide the pizzeria's business strategies and decision-making.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/2.png)

#### Sales By Name
The analysis of pizza names unveils captivating insights into the pizzeria's menu preferences. The "Thai Chicken Pizza" claims the top spot as the best-performing pizza, generating impressive sales of $43,434. Following closely is the "Barbecue Chicken Pizza" contributing significantly with sales totaling $42,768. Additionally, the "California Chicken Pizza" showcases strong popularity, raking in sales of $41,709.

On the flip side, the analysis reveals pizzas with relatively lower sales. The "Brie Carre Pizza" emerges as one of the least-performing pizzas, with sales amounting to $11,588. Similarly, the "Green Garden Pizza" reports sales of $13,955, and the " Spinach Supreme Pizza" also lands among the bottom performers with sales of $15,277.

An additional layer of sophistication is applied through conditional formatting, visually enhancing the sales distribution across these pizzas. The formatting seamlessly transitions from the minimum to the maximum sales, using a color gradient.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/4.png)

#### Sales By Category
In the examination of sales by category, it becomes apparent that the Classic category leads the way, accounting for approximately 26.9% of total sales with a revenue of around $220,000. Following closely is the Supreme category, contributing around 25.5% of the total sales, equivalent to approximately $208,000. The Chicken category stands as the third top contributor with roughly 24% of total sales, translating to approximately $196,000. The Veggie category, holds a slightly smaller share at 23.7%, resulting in approximately $194,000 in revenue. These proportions provide valuable insights into customer preferences and highlight the key categories driving the majority of the pizzeria's sales.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/5.png)

#### Sales By Size
In the exploration of sales by size, a compelling pattern emerges. The Large size category stands out as the most popular choice, contributing a significant 45.9% to the overall sales revenue. Following closely is the Medium size, representing around 30.5% of total sales. The Small size holds a notable portion with approximately 21.8% of sales. The X-Large and XX-Large sizes contributing  a smaller fraction 1.7% and 0.1% respectively. This distribution underscores the appeal of larger sizes and the significance of medium and small sizes in maintaining a well-rounded menu. It offers insights into customer preferences for different occasions and appetites.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/6.png)

#### Comprehensive Pizza Metrics
In the "Comprehensive Pizza Metrics" table, the analysis reveals that the category "Classic" illustrates a broad range of sizes, orders, pizzas sold, and sales figures. The category "Classic" demonstrates its popularity, with the highest number of orders for the "Small" size, reaching a remarkable 5,300 orders, while the least ordered falls under the "XX-Large" size, with a count of just 28 orders.

When examining the category's pizza sales, the "Small" size shines with distinction, having the highest pizzas sold, totaling 6,139. In contrast, the "XX-Large" size pizza in the "Classic" category has the lowest pizzas sold, reflecting a significantly modest count.

Furthermore, in terms of sales value, the "Veggie" category's "Large" size pizzas dominate, securing the highest sales among all combinations. On the contrary, the "Classic" category's "XX-Large" size pizzas exhibit the lowest sales value in this comprehensive analysis.

It's noteworthy to mention that the use of conditional formatting with icons in the "Orders," "Pizzas Sold," and "Sales" columns adds an additional layer of insight to this detailed examination, enabling easy identification of these metrics at a glance.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/7i.png)

#### Sales Forecasting
Ιn the Sales Forecasting section, a line chart has been developed to provide insights into the anticipated sales trends for the upcoming months. This graph offers a visualization of sales over time, with the x-axis representing days, months, and years, and the y-axis representing sales figures. A addition to the graph is the inclusion of a forecasted line, extending into the future, supported by a 95% confidence interval. This line enables a visual prediction of sales trends, with projected values for specific dates.

The graph's illustration extends further with the integration of an average line, positioned at the level of $2,300. This reference line provides a clear benchmark  by which to evaluate the sales trajectory. Additionally, you can cleary see both the minimum and maximum points for sales across all dates. This demonstrates the range within which sales have varied, revealing the diversity in customer activity.

Looking into the furure and taking the example of February 20, the forecast predicts a projected sales amount of $2,490. This forecast provides valuable insights for strategic business planning. Furthermore, the graph's visualization aids in identifying potential growth or decline periods, enabling stakeholders to make informed choices.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/3.png)

#### Slicers
In order to provide a interactive experience, I've added two slicers into the dashboard: the Category Slicer and the Size Slicer. These slicers offer a focused and dynamic way to explore the data. With the Category Slicer, you can delve into sales trends for different pizza categories. On the other hand, the Size Slicer allows you to examine how different pizza sizes impact overall sales performance. These slicers give you the power to tailor your analysis based on your specific interests and questions, making it easier to uncover insights and trends.

![Alt text](https://github.com/jimiatro/Power_Bi_Pizza_Project_Insights/blob/main/images/8.png)

# Suggestions #
- **Strategic Marketing**: Focusing marketing efforts on top-selling categories like "Classic," "Supreme," and "Chicken" can further boost sales. Special deals or promotions could target these categories to capitalize on customer preferences.

- **Size Emphasis**: Given the popularity of "Large" and "Medium" sizes, the pizzeria could optimize stock and resources for these sizes, ensuring customer satisfaction.

- **Efficiency Observations**: Utilizing the sales forecasting insights, the pizzeria can gain more informed insights into ingredient acquisition, staff scheduling, and production capacity.

# License #

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Feedback #
I would love to hear your thoughts on my project! If you have any suggestions or comments, please feel free to open an issue or send me an email at jimiatro@hotmail.com.





