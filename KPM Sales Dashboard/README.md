# KPM Sales Dashboard

## Business problem
To analyze and find the regions and product categories for improvement in business, also locate the best performing products and our top customers on the way. To find our Delivery performance and department level analysis on sales and profits.

## In page 1 the visuals are as follows. 

- Filter slider - Order date
- Line and stacked column chart - has 3 column, “Order date” by “order item total” and “order profit per order”.
- Clustered column chart - has 2 measures, “Order date” by “Total discount ratio” and “Total profit ratio” (Total discount ratio is to be 
  calculated just as Total Profit ratio measure was calculated but with the use of [Order Item Discount] and Orders[Sales].
- Pie Chart 1 - Order item total by Market.
- Pie Chart 2 - Order item total by Delivery status.
- Tree map - Order item total by Category Name.
- Map - Order item total by Location (Use CONCATENATE DAX- to link city, state and country, and then distribute the data colours with 
  respect Profit and Loss using function).
- Donut Charts - Order item total by Department Name.

## In Page 2 the visuals are as follows

- Filter slider - Order date (From Page 1).
- Line and stacked column chart - has 3 column, “order date” by “order item total” and “order profit per order”(From Page 1).
- Pie Chart 1 - Order item total by Market (From Page 1).
- Pie Chart 2 - Order item total by Delivery status (From Page 1).
- Donut Charts - Order item total by Department Name (From Page 1).
- Card - Custom sentence made using DAX (From previous assignment questions).
- Card - Total Revenue (From previous assignment questions).
- Card - Total Profit (From previous assignment questions).
- Card - Total Profit Ratio (From previous assignment questions).
- Card - Order Item Quantity (From previous assignment questions).
- Table - Department name, Category name, product name, #units sold, Total Profit, Total Profit Ratio, Total Revenue.
