# Pizza Sales Analysis

### Dashboard Link : [Pizza Sales Analysis Dashbord.zip](https://github.com/user-attachments/files/18310108/Pizza.Sales.Analysis.Dashbord.zip)

## Problem Statement

The dataset contains pizza sales information, and the objective is to analyze key metrics and trends to provide actionable insights through visualizations in Power BI. This analysis focuses on:

1. Sales Performance: Total revenue, average order value, and total pizzas sold.
2. Customer Trends: Daily and monthly order patterns.
3. Category Insights: Sales distribution by pizza category and size.
4. Product Performance: Identifying top and bottom-performing pizzas based on revenue, quantity sold, and total orders.

The Power BI dashboard will visualize these insights to help optimize business strategies and decision-making.


### Steps followed 

- Step 1 : Load data into SQL Server and Do analysis for the above KPIs
- Step 2 : Connect SQL Server to POwerBI 
- Step 3. Open power query editor & in view tab under Data preview section, Check data overall and check what was the error in the data
- Step 4 : It was observed that in none of the columns errors & empty values were present but Pizza size should be like Regular, Medium, Large etc insted of L,M,XL.
- Step 5 : Different Visual are used for the different indication based on requirement and their sutability. 
- Step 6 : Visual filters (Slicers) were added for type of Pizzas.
- Step 7 : add calender to select the Data ranges based on date outlines. 
- Step 8 : Two dashbord is created 1. for Different KPIs indicators and another one for the Best and Worst selling of the pizza based on category, Size.
- Step 9 : Different  Visual was used to represent different KPis,

  (a) Daily and Mponthly Trends in Pizza Sales 

  (b) Total pizza Sales by Category 
  
  (c) Sales % By category and Size.
  
  (d) Top and Worsed Sellers By Revenue
  
  (e) Top and Worsed seller by pizza sold
  
  (f) Top and Worsed by Order Served

  
All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 10 : In the report view, under the insert tab, two text boxes were added to the canvas, in one of them Home tab mentioned & in the Best and Worsed Pizza sales was written.
 
- Step 11 : Calculated column was created in which, Pzzas were grouped into various groups.

for creating new column following DAX expression was written;
       
      Order Month = Upper(Left(pizza_sales[Month Name],3))

      Order Day = UPPER(left(pizza_sales[Day Name],3))  
        
        
- Step 12 : New measure was created to find unseen Details.

Following DAX expression was written for the same,
        
       Avg Order Value = [Total Revenue]/[Total Orders]

      Avg pizzas per order = [Total Pizza Sold]/[Total Orders]

      Total Orders = DISTINCTCOUNT(pizza_sales[order_id])

      Total Pizza Sold = sum(pizza_sales[quantity])

      Total Revenue = Sum(pizza_sales[total_price])

        
 -
# KPIs Of the DashBoard
![KPIs](https://github.com/user-attachments/assets/1d78801d-91d2-405d-a1ae-309241eb14fe)

 # Total Sales By Category and Size

![SalesByCategory and Size](https://github.com/user-attachments/assets/9ea5372a-e832-4594-9962-926d648f16ba)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Revenue Generated = 817860K

   Average Order Value = 30.30Rs

   Total Pizzas Sold = 49574k

   Total Orders = 21350

   Average Pizzas Per Order = 2.3


        Thus average order value will be 2 Pizzas per customer.
           
### [2] Daily and Monthly Pizza Sold

  # Daily :
    Saturday	3158
    Wednesday	3024
    Monday	2794
    Sunday	2624
    Friday	3538
    Thursday	3239
    Tuesday	2973
  
  # Monthly Trend: 
    February 1685
    June	 1773
    August	 1841
    April	 1799
    May	     1853
    December 1680
    January	 1845
    September 1661
    October	 1646
    July	 1935
    November 1792
    March	 1840
  
  ### [3]  % of Sales By Pizza Category
 Pizza Category Total Revenue PCT
 Classic	 220053.10	      26.91
 Chicken	 195919.50	      23.96
 Veggie	     193690.45	      23.68
 Supreme	 208197.00	      25.46
  
  ### [4] % of Sales By Pizza Size
    Size   Total Revenue  PCT
    L	    375318.70	45.89
    M	    249382.25	30.49
    S	    178076.50	21.77
    XL	    14076.00	1.72
    XXL	    1006.60	    0.12

  ### [5] Total Pizza Sold By Category
    Category    Total Sold
    Classic	        1178
    Supreme	        964
    Veggie	        944
    Chicken	        875

  ### [6] Top 5 Pizzas By Revenue:
    Pizzas Name                     Revenue
    1.The Thai Chicken Pizza	    43434.25
    2.The Barbecue Chicken Pizza	42768
    3.The California Chicken Pizza	41409.5
    4.The Classic Deluxe Pizza	    38180.5
    5.The Spicy Italian Pizza	    34831.25
     
 ### [7] Bottom 5 Sellers By Revenue
    Pizzas Name                     Revenue
    1.The Brie Carre Pizza	    11588.4998130798
    2.The Green Garden Pizza	13955.75
    3.The Spinach Supreme Pizza	15277.75
    4.The Mediterranean Pizza	15360.5
    5.The Spinach Pesto Pizza	15596

 ### [8] Top 5 Pizzas By Quantity
    Pizzas Name                 Total Sold
    1.The Classic Deluxe Pizza	    2453
    2.The Barbecue Chicken Pizza	2432
    3.The Hawaiian Pizza	        2422
    4.The Pepperoni Pizza	        2418
    5.The Thai Chicken Pizza	    2371
 
 ### [9] Bottom 5 Pizzas By Quantity
    Pizzas Name                 Total Sold
    1.The Brie Carre Pizza	        490
    2.The Mediterranean Pizza	    934
    3.The Calabrese Pizza	        937
    4.The Spinach Supreme Pizza	    950
    5.The Soppressata Pizza	        961
    
 ### [10] Best Selling Pizza
    1. By REVENUE
    The Thai Chiken Pizza contributes to Maximum    revenue.

    2. By QUANTITY
    The Classic Delux Pizza contributes to Maximum total quantities.

    3. TOTAL ORDERS
    The classic pizza contributes to Maximum Total order

 ### Worst Selling Pizza
    1. BYREVENUE
    The Brie Pizza Contributes to Minimum revenue.

    2. QUANTITY
    The Brie Pizza contributes to Minimum Quantities.

    3. TOTAL ORDERS
    The Brie Carre pizza contributes to Minimu,m Total order


