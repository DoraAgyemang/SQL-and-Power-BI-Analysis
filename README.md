# SQL-and-Power-BI-Analysis

## Overview

This project seekes to analyse the product history and sales of products of a a compay as to how the products are doing om monthly basis. we will also get to the details of the products.

### Data Source

The primary Dataset used for this analysis is the AdventureWorks 2014. 
https://1drv.ms/u/s!AiZu-urEabOdgYIlFcCGIxckz7l6Mg?e=uwNFy0  
### Tools

- Microsoft SQL Server Management Studio
- Power BI

### Importaing Data

- AdventureWorks2014 was downloaded from the link above and imported into the SQL Database server.
  The tables Product TransactionHistory and Sales.CurrencyRate,  were imported into Power BI for visualization
  - In PowerBi Server, go to Home, Get data and select from SQL Server

    ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6e3b393a-119a-497a-b2d6-2f84511ca8c0)

  - A pop up menu appears which requires the user to input the SQL database server name.
    
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/c5472450-6ce9-40b1-8955-e459ea8c07ec)

- Go to SQL server and select **connect** from the **object explorer panel** and click **database engine**.
  ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/f567dc50-a040-43a8-8f36-3eb46d6aea34)

- Copy the server name 
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/4669698e-e9f3-42ca-a562-50ad7136c029)

- In Power Bi desktop, paste the server name in the option written server in the pop up menu and click okay

  ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/13afa2d6-784c-49ea-8963-7351a7a66d88)

- Select the tables ProductTransanctionHistory and Sale.CurrencyRate and click on Load.

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/f25d0297-66b6-4da7-9474-9ac4952dbf35)<p>
- The tables have now been imported into the Power Bi desktop and ready for our analysis.

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6a97f9d0-3c79-41c7-9117-893ee2f4bef0)<p>

### Exploratory Data Analysis

Exploratory data analaysis (EDA) entails delving into our tables and creating visuals to analyse the data to answer questuins such as:
a)
- Actual Cost for each Transaction Type on a month-to-month.
  ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/39b0da0b-75c1-4e07-b890-bd7f0cac7b9f)<p>
  From the above visual it can be seen that the month of March had the higest Actual Cost and June with the lowest Actual cost
-	A table showing Category of Average Quantity into 3 groups namely High Quantity, Mid Quantity, and Low Quantity.
  
-	A visual showing Total Actual Cost for each Transaction Type. 
-	Create a Dashboard for the above analysis

b)
- A visual showing the Sales Currency Average rate by Year.
  
- A visual showing Sales Currency Average rate by Quarterly.
- A visual showing Sales Currency Avarage rate by Month.
- Create a dasboard for the above Visuals

  ### Data Analysis

  In this Analysis we will create visuals  to answer the exploratory Data Anylysis question a).
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/67b1072e-fb2b-458d-80da-eb110d9df656)<p>
  In the above visuals, you could see the aAverage quantity by month was grouped into AverageQuantity group to show the trends in the monthly average. Anew measure was used to group 
  th Average into Average Quantity group Using the below querry
  ```
AverageQuantityGroup = IF([Average Quantity]<= 30, "Low Quantity",
IF([Average Quantity]<= 44, "Mid Quantity", "High Quantity"))
  ```
  



