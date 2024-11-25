# CoffeeSales
A quick Excel project designed by Mo Chen on YouTube (https://www.youtube.com/@mo-chen). It uses some made-up data on a coffee companies sales. The aim was to create some useful columns and visualisations, which we then format as a nice dashboard:
![image](https://github.com/user-attachments/assets/02760061-82c7-48e7-a03b-e5d0f1f8b7c1)
We can use the slicers and the timeline to change all of the graphs simultaneously:
![image](https://github.com/user-attachments/assets/5f88672b-3df6-4cb9-abbc-dffe7137de88)
In this repository, I go over the process used to create this final dashboard.

## The Data
The spreadsheet has the following subsheets, which have the following columns:
- "customers", which contains information on the customers placing orders:
   - Customer ID
   - Customer Name
   - Email
   - Phone Number
   - Address Line 1
   - City
   - Country
   - Postcode
   - Loyalty Card
- "products", which contains information on the coffee products on offer:
   - Product ID
   - Coffee Type
   - Roast Type
   - Size
   - Unit Price
   - Price per 100g
   - Profit
- "orders", which contains information on the orders that customers have placed:
   - Order ID
   - Order Date
   - Customer ID
   - Product ID
   - Quantity

## The Process
- Filling in the orders sheet:
  - Use XLOOKUP to fill in Customer Name, Email and Country columns
  - Use IF to change any unusual values to more consistent values
  - Use INDEX MATCH power lookups to fill in Coffee Type, Roast Type, Size and Unit Price
  - Multiply Quantity and Unit Price to obtain new column Sales
  - Use 4 nested IF functions to change abbreviations in Coffee Type column to their full names (e.g. "ARA" to "Arabica")
  - Similar to change abbreviations in Roast Type column to their full names (e.g. "D" to "Dark")
  - Use XLOOKUP to add Loyalty Card column
  - Convert the whole sheet to a table
 
- Creating pivot tables:
  - Create a pivot table which shows the sales in each month, for each coffee type
  - Create and format an accompanying line graph
  - Add a timeline feature
  - Add a slicer for Roast Type and Size
 
- Creating further visuals:
  - Duplicate the pivot table created above, so that the slicers and timeline can control all graphs simultaneously on the dashboard
  - Edit the pivot table to show sales by country, and to show the 10 customers who have spent the most
  - Create the accompanying bar charts
 
- Create the dashboard:
  - Paste the 3 created graphs, slicers and timeline into a new subsheet titled "dashboard"
  - Report connections from the slicers and timeline to all 3 graphs, so they control them all simultaneously
  - 
