### Exercise 5: Explorer Data Science experience in Microsoft Fabric (Optional)
 
Microsoft Fabric offers Data Science experiences to empower users to complete end-to-end data science workflows for data enrichment and business insights.

You can complete a wide range of activities across the entire data science process, all the way from data exploration, preparation and cleansing to experimentation, modeling, model scoring and serving predictive insights to BI reports.

### Task 5.1: Build ML models and experiments using Copilot in Fabric

![task-3.1.1.png](media/labMedia/exercise5_1.1.png)

To understand the cause behind Contoso’s declining revenue, the team needed to dive deeper into their customers’ spending pattern. 

Copilot responds to queries in natural language or generates customized code snippets for tasks like creating charts, filtering data, applying transformations, and building machine learning models.

Let’s see how copilot for notebook helped you to quickly create data science notebooks.

1. Switch to the **Data Science** experience using the experience switcher icon in the left corner.

   ![task-3.1.1.png](media/labMedia/exercise5_1.2.png)

2. Click on Import notebook.

   ![task-3.1.2.png](media/labMedia/exercise5_1.3.png)

3. Click on the **Upload** button.

   ![task-3.1.2.png](media/labMedia/exercise5_1.3.1.png)

4. Browse to the fabricnotebooks folder in your VM and select **Build ML models and experiments using Copilot for Data Science in Fabric** notebook.

5. Click on the **Open** button.

![task-3.1.2.png](media/labMedia/exercise5_1.3.2.png)

6. Wait for the notebook to **upload**.

![task-3.1.2.png](media/labMedia/exercise5_1.3.3.png)

7. Click on the **ContosoSales...** workspace from the left navigation pane.

![task-3.1.2.png](media/labMedia/exercise5_1.3.4.png)

8. Click on **Filter**, expand **Type** and select **Notebook**.

![task-3.1.2.png](media/labMedia/exercise5_1.3.5.png)

9. Click on the **Build ML models and experiments using Copilot for Data Science in Fabric** notebook.

![task-3.1.2.png](media/labMedia/exercise5_1.3.6.png)

10. Click on **Lakehouses** in the Explorer pane.

![task-3.1.2.png](media/labMedia/exercise5_1.3.7.png)

11. Click on **Missing Lakehouses** and then click on **Remove all Lakehouse**.

![task-3.1.2.png](media/labMedia/exercise5_1.3.8.png)

12. Click on the **Continue** button.

![task-3.1.2.png](media/labMedia/exercise5_1.3.9.png)  

13. Click on the **+ Lakehouse** button.

![task-3.1.2.png](media/labMedia/exercise5_1.3.10.png) 

14. Make sure that **Existing Lakehouse** radio button is selected and then click on the **Add** button.

![task-3.1.2.png](media/labMedia/exercise5_1.3.11.png)

15. Select the **lakehouse** checkbox.

![task-3.1.2.png](media/labMedia/exercise5_1.3.12.png)

16. Click on the **Add** button.

![task-3.1.2.png](media/labMedia/exercise5_1.3.13.png)

17. Click on the **Copilot** button and then click on the **Get Started** button.

![task-3.1.2.png](media/labMedia/exercise5_1.6.png)

18. Run the **first cell** of the notebook to install the copilot packages.

>**Note:** This may take a while to execute, please wait till this load completely.

![task-3.1.2.png](media/labMedia/exercise5_1.7.png)

19. Copy and paste the **below prompt** in the textbox.

```
Load the "customerchurndata" table from the lakehouse into a Spark DataFrame. Then convert that into pandas dataframe as df
```

20. Click on the **send** button.

![task-3.1.2.png](media/labMedia/exercise5_1.8.png)

21. Click on the **Copy code** icon.

>**Note:** The new cell will be created right above the cell.

![task-3.1.2.png](media/labMedia/exercise5_1.8.2.png)

22. Click on a **+ Code** above the first cell of the notebook.

![task-3.1.2.png](media/labMedia/exercise5_1.8.1.png)

23. Paste the **copied query** and run the new **cell**.

![task-3.1.2.png](media/labMedia/exercise5_1.9.png)

24. Paste the following at the **end of your browser URL** and press the **Enter** key. 

```
&debug.enableCopilot=1&debug.enableChatWidget=1&debug.enableQuickAssist=1
```

![task-3.1.2.png](media/labMedia/exercise5_1.10.png)

25. Click on a **+ Code** above the cell, place your **cursor** in the cell and then click on the **Copilot** button.

![task-3.1.2.png](media/labMedia/exercise5_1.10.1.png)

26. Enter the below prompt in the Copilot textbox: 

```
Create a pivot table of average with min and max total amount by store contract and churn. Then show output of the pivot table.
```

27. Click on the **Send** icon.

![task-3.1.2.png](media/labMedia/exercise5_1.11.png)

28. Click on the **Accept** button.

![task-3.1.2.png](media/labMedia/exercise5_1.12.png)

29. Run the cell and observe the output.

![task-3.1.2.png](media/labMedia/exercise5_1.12.1.png)

30. Add a **new code cell** to the notebook, paste following **query** to the cell and then run the **cell**.

```
%%chat 
Create a seaborn scatterplot with Tenure Total Amount and Churn
```

![task-3.1.2.png](media/labMedia/exercise5_1.13.png)

31. Introduce an error in a previous cell by **removing a character** in the code.

32. Run the **code cell** with the error.

33. Click on **Fix with copilot**.

![task-3.1.2.png](media/labMedia/exercise5_1.14.png)

With prepared data and with the help of copilot as we just saw, you may explore the data to understand the patterns it contained.

The rest of the notebook has similar PySpark queries to explore customer churn prediction.


### Task 5.2: Leverage AI skills for Q&A

1. From the left navigation pane select **Data Science** experience.

![task-5.2](media/labMedia/AIskill1.png)

2. Click on **>** Forward Arrow and select **AI Skill**.

![task-5.2](media/labMedia/AIskill2.png)

3. Enter Name as **Contoso-Assistance** 

![task-5.2](media/labMedia/AIskill3.png)

4. Click on **lakehouse** and then click on the **Confirm** button.

![task-5.2](media/labMedia/AIskill4.png)

5. Click on **refresh** and Expand **Tables** then select the following tables.

- dimcustomer
- dimdate
- dimproduct
- dimreseller
- factinternetsales
- factresellersales

![task-5.2](media/labMedia/AIskill5.png)

6. Click on **Get Started**.

![task-5.2](media/labMedia/AIskill6.png)

8. Type **What is the most sold product?** in the chatbox and click on the **Send** button.

![task-5.2](media/labMedia/AIskill7.png)

9. AI Skill answered the question fairly well based on the selected tables.

However, the SQL query needs some improvement, it orders the products by order quantity, when total sales revenue associated with the product is the most important consideration, as shown in the above screenshot.

To improve the query generation, let's provide some instructions, as shown in these examples:

```
Whenever I ask about "the most sold" products or items, the metric of interest is total sales revenue and not order quantity.

The primary table to use is FactInternetSales. Only use FactResellerSales if explicitly asked about resales or when asked about total sales.
```

10. Copy the above notes and paste it in **Notes for model** box. Type **What is the most sold product ?** in the chatbox and then click on the **Send** button.  

Asking the question again returns a different answer, **Mountain-200 Black, 46**, as shown in the below screenshot:

![task-5.2](media/labMedia/AIskill8.png)

In addition to instructions, examples serve as another effective way to guide the AI. If you have questions that your AI skill often receives, or questions that require complex joins.

11. In the example SQL queries click on **edit** icon.

![task-5.2](media/labMedia/AIskill9.png)

12. Click on **+ Add example** and enter the following question and their respective SQL queries.

|Question| SQL query|
|--------|----------|
|who are the top 5 customers by total sales amount?|SELECT TOP 5 CONCAT(dc.FirstName, ' ', dc.LastName) AS CustomerName, SUM(fis.SalesAmount) AS TotalSpent FROM factinternetsales fis JOIN dimcustomer dc ON fis.CustomerKey = dc.CustomerKey GROUP BY CONCAT(dc.FirstName, ' ', dc.LastName) ORDER BY TotalSpent DESC;|
|what is the total sales amount by year?|SELECT dd.CalendarYear, SUM(fis.SalesAmount) AS TotalSales FROM factinternetsales fis JOIN dimdate dd ON fis.OrderDateKey = dd.DateKey GROUP BY dd.CalendarYear ORDER BY dd.CalendarYear;|

![task-5.2](media/labMedia/AIskill10.png)

13. Click on **close(X)** button.

![task-5.2](media/labMedia/AIskill11.png)

14. Type **who are the top 5 customers by total sales amount?** in the chatbox and click on **Send** button.

![task-5.2](media/labMedia/AIskill12.png)

15. Click on **Publish**.

![task-5.2](media/labMedia/AIskill13.png)

16. In the pop-up screen click on **Publish**.

![task-5.2](media/labMedia/AIskill14.png)

17. Notice that AI skill is published successfully.

![task-5.2](media/labMedia/AIskill15.png)