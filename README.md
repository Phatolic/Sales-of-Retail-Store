# Sales-of-Retail-Store

## Tables of Contents
- [Project Overview](https://github.com/Phatolic/Sales-of-Retail-Store#project-overview)
- [Data Sources](https://github.com/Phatolic/Sales-of-Retail-Store#data-sources)
- [Data Transformation & Modeling](https://github.com/Phatolic/Sales-of-Retail-Store#data-transformation-and-modeling)
- [Data Analysis](https://github.com/Phatolic/Sales-of-Retail-Store#data-analysis)
- [Dashboard](https://github.com/Phatolic/Sales-of-Retail-Store#dashboarding)
- [Results](https://github.com/Phatolic/Sales-of-Retail-Store#results)

### Project Overview

This data analysis project aims to provide insights into the performance of the retail store in 2019 and 2020. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's sales and profits.  

---
### Data Sources

- Location table: Contains customers information (Index, Location No, State).
- Products table: Contains products information (Index, Product Code, Product Name, Unit Price, Cost Price).
- Agents table: Contains agents information (Index, Agent Code, Job Grade, Location, Title, Shift).
- Orders table: Contains orders information (Order No, Order Date, Agent Code, Location No, Product Code, Quantity, Warehouse Code, Returns, Shippers Code, Customer Satisfaction).
- Shippers table: Contains shippers information (Index, Shippers Code, Shippers, Delivery Cost).
- Warehouse table: Contains warehouses information (Index, Warehouse Code, Warehouse Location).

---
### Data Transformation and Modeling

#### Power Query

- Location table: Renamed as Dim_Customers.
- Products table: Renamed as Dim_Products.
- Agents table: Renamed as Dim_Agents.
- Orders table: Renamed as Fact_Table. Create the Cus_Satisfaction Status column from the Customer Satisfaction column with 3, 4, 5 are High, Medium, Low respectively.
- Shippers table: Renamed as Dim_Logistics.
- Warehouse table: Renamed as Dim_Warehouses.

> Click Close and Load to -> Create a connection -> Add to the data model. Apply this step to every table.
  
#### Power Pivot
#### Diagram View

  ![Star_schema](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/077b8f61-466a-47f9-8df4-1ce6ef0a4299)

> Star schema
#### Data View
- Fact_Table table:
  + Order Date: Format as Date type.
  + Order Date (#Month): Extract month number from the Order Date column.
  + Order Date (Month Name): Extract month name from the Order Date column.
  + Order Date (Year): Extract year from the Order Date column.
  + Order Date (Quarter): Extract month from the Order Date column and place into the 4 quarters.
    
- Dim_Products table:
  + Shoe Size column: Extract size of shoe from Product Name column. Ex: Adidas Shoe Size - 38 -> Size - 38.
    
- KPIs:
  + Sales: ```Sales:=SUMX(Fact_Table, Fact_Table[Quantity] * RELATED(Dim_Products[Unit Price]))```
  + COGS: ```COGS:=SUMX(Fact_Table,Fact_Table[Quantity]*RELATED(Dim_Products[Cost price]))```
  + Total QTY: ```Total QTY:=SUM(Fact_Table[Quantity])```
  + Total Delivery Cost: ```Total Delivery Cost:=SUMX(Fact_Table, Fact_Table[Quantity] * RELATED(Dim_Logistics[Delivery Cost]))```
  + Total Profit: ```Total Profit:=[Sales] - [COGS] - [Total Delivery Cost]```

---
### Data Analysis   
<b>- Pivot tables created in Analysis tab in the workbook.  </b>  

1. KPIs

    ![KPI](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/7f1a9d22-6353-416a-b2a4-fcfe5415d6f4)

2. Monthly sales in two years

    ![Sales](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/d6e48672-5951-4f19-8a7f-47092a093b58)

3. Profit by Agents

    ![ProfitAgent](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/24d1e068-1b24-4ceb-8846-5c5d56b961ce)

4. Profit by Agent Shifts

    ![ProfitAgentShift](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/29584857-3dab-4de8-a87b-ebde1d5a9616)

5. Warehouse Quantity Sold

    ![WarehouseQtySold](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/74a2d666-2d2d-4c58-9771-fa1de2839fd6)

6. Shipping Cost

    ![ShippingCost](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/817662e7-40e1-4f07-9bd8-865d70f724d4)

7. Customer Satisfaction
   
    ![CustomerSatisfaction](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/c5d26c87-5e82-4ec2-ac05-b2702d2338a4)

8. Top 4 products Profit
    
    ![Top4](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/90b9cb94-6d57-4a58-bd03-c5228bf291e1)

9. Profit by Shoe Size

    ![ProfitShoeSize](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/61ef2b73-5b79-4b84-9ce9-d460489ec163)

10. Profit by Year
    
    ![ProfitYear](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/fd39c7f9-8420-4da0-96a9-cbd449e2335a)

---
### Dashboarding

- Build charts for pivot tables.
- Format the charts and build the dashboard.  
- Add slicers.
  
    ![Dashboard](https://github.com/Phatolic/Sales-of-Retail-Store/assets/144981161/d4db3886-b0e3-44f3-80d1-1a922806255f)

---
### Results

<b>-> </b>The sales figure fluctuates throughout the years with the lowest sales is the February sales. Perhaps it is because it has less days.  

<b>-> </b>The customer satisfaction status not very positive with just 40% customers with high satisfaction.

<b>-> </b>Discover that the 2020 sales in nearly doubled the sales in 2019.

##### -> It seems that although the sales is growing with the incredible rate, the customer satisfaction about the company is quite bad so it may cause some problems for the company in the long-run.


