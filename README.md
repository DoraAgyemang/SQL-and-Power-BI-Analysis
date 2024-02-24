# SQL-and-Power-BI-Analysis

## Overview

This project seeks to analyse the product history and sales of products of a compay as to how the products are doing on monthly basis based on the Transaction type. We will also get to the details of the products.

### Data Source

The primary Dataset used for this analysis is the AdventureWorks 2014. 
https://1drv.ms/u/s!AiZu-urEabOdgYIlFcCGIxckz7l6Mg?e=uwNFy0  
### Tools

- Microsoft SQL Server Management Studio
- Power BI Desktop

### Importaing Data

- AdventureWorks2014 was downloaded from the link above and imported into the SQL Database server.
  The tables Product TransactionHistory and Sales.CurrencyRate,  were imported into Power BI for visualization
  - In PowerBi desktop, go to Home, click on **Get data** and select **From SQL Server**

    ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6e3b393a-119a-497a-b2d6-2f84511ca8c0)<p>

  - A pop up menu appears which requires the user to input the SQL database server name.
    
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/c5472450-6ce9-40b1-8955-e459ea8c07ec)<p>

- Go to SQL server and select **connect** from the **object explorer panel** and click **database engine**.
  ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/f567dc50-a040-43a8-8f36-3eb46d6aea34)<p>

- Copy the server name

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/4669698e-e9f3-42ca-a562-50ad7136c029)<p>

- In Power Bi desktop, paste the server name in the option written **server** in the pop up menu and click okay

  ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/13afa2d6-784c-49ea-8963-7351a7a66d88)<p>

- Select the tables ProductTransanctionHistory and Sale.CurrencyRate and click on Load.

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/f25d0297-66b6-4da7-9474-9ac4952dbf35)<p>
- The tables have now been imported into the Power Bi desktop and ready for our analysis and visualozation.

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6a97f9d0-3c79-41c7-9117-893ee2f4bef0)<p>

### Exploratory Data Analysis

Exploratory data analaysis (EDA) entails delving into our tables and creating visuals to analyse the data to answer questions such as what is the:<p>

a)
- Actual Cost for each Transaction Type on a month-to-month?<p>
 ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/8cc0c842-a63d-4fa2-bb2d-474ee3bf4194)<p>
From the above visual it can be seen that the month of March had the higest Actual Cost and June with the lowest Actual cost.<p>
 In the AdventureWorks2014 database, the transaction types P, S, and W are related to the SalesOrderHeader table and represent the following:

- **P**: Purchase Order
- **S**: Sales Order
- **W**: Work Order

- Average Quantity for every month? Group into 3 groups namely High Quantity, Mid Quantity, and Low Quantity.
 ![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6d92a76e-30d2-45d8-8f37-8c97950f9f4c)<p>
In the above visuals, you could see the Average quantity by month was grouped into AverageQuantity group to show the trends in the monthly average. A new measure was used to group  the Average into Average Quantity group Using the below querry.
 ```
AverageQuantityGroup = IF([Average Quantity]<= 30, "Low Quantity", IF([Average Quantity]<= 44, "Mid Quantity", "High Quantity"))
```
- Total Actual Cost for each Transaction Type.<p>
  

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/99f6306f-dac6-4502-b65f-a0ed907209c6)<p>

 A Dashboard was created for the above analysis<p>
 

![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/67b1072e-fb2b-458d-80da-eb110d9df656)<p>

b)
- Sales Currency Average rate by Year.<p>
  
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/1872d9db-4f41-49b1-866f-47547079d6ea)<p>

From the Analysis, It is observed the year 2013 recorded the highest Sales Rate with £360,000 whereas 2011 had the lowest with £170,000

- Sales Currency Average rate by Quarterly.<p>
 
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/6dab2570-68c5-4496-9c78-1097596fe65f)<p>

The 1st Quarter is observed to have had the highest currency rate with £290,000. The lowest sales currency rate, £244,000, was recorded in the 3rd Quarter. Furthermore, the currency rate for the last two quarters were below the average, £279,363.
 
- Sales Currency Avarage rate by Month.<p>
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/4b34c751-efac-480b-aa36-70363dab7edd)
<p>

Most of the monthly currency rates ere below the average, £100,723. from mid-year. However, the rates in the first 5 months were higher than the average. With £102,950, May recorded the highest rate whilst June was observed to have had the lowest, £75,691.

- A dasboard for the above Visuals<p>
  
![image](https://github.com/MYZDEE/SQL-and-Power-BI-Analysis/assets/128803445/d4d38122-931b-46ef-b5ae-8b2f45d58a8f)<p>

### Conclusion
In conclusion the Visuals created are analysis to find out the products with the highest sales within the month, the total prices of the products, Average cost of the products ect. These are the necessary analysis from the data. However, these are not the only analysis that can be derived from the data available. 



  

 
  



