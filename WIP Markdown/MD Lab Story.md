# Replacement Tokens & Values

* Storage Account Key: `@lab.Variable(storageaccountkey)`
* SQL Endpoint: `@lab.Variable(sqlEndpoint)`
* Destination URI: `@lab.Variable(destinationUri)`
* Workspace URL: `@lab.Variable(workspaceurl)`
* Event Hub key: `@lab.Variable(EventHubKey)`

# Modern Analytics with Microsoft Fabric, Copilot and Azure Databricks DREAM Lab (Lab332)
**The estimated time to complete this lab is 45-60 minutes.**

**DISCLAIMER**

This presentation, demonstration, and demonstration model are for informational purposes only and (1) are not subject to SOC 1 and SOC 2 compliance audits, and (2) are not designed, intended or made available as a medical device(s) or as a substitute for professional medical advice, diagnosis, treatment or judgment. Microsoft makes no warranties, express or implied, in this presentation, demonstration, and demonstration model. Nothing in this presentation, demonstration, or demonstration model modifies any of the terms and conditions of Microsoft’s written and signed agreements. This is not an offer and applicable terms and the information provided are subject to revision and may be changed at any time by Microsoft.

This presentation, demonstration, and demonstration model do not give you or your organization any license to any patents, trademarks, copyrights, or other intellectual property covering the subject matter in this presentation, demonstration, and demonstration model.

The information contained in this presentation, demonstration and demonstration model represents the current view of Microsoft on the issues discussed as of the date of presentation and/or demonstration, for the duration of your access to the demonstration model. Because Microsoft must respond to changing market conditions, it should not be interpreted to be a commitment on the part of Microsoft, and Microsoft cannot guarantee the accuracy of any information presented after the date of presentation and/or demonstration and for the duration of your access to the demonstration model.

No Microsoft technology, nor any of its component technologies, including the demonstration model, is intended or made available as a substitute for the professional advice, opinion, or judgment of (1) a certified financial services professional, or (2) a certified medical professional. Partners or customers are responsible for ensuring the regulatory compliance of any solution they build using Microsoft technologies.

**Copyright**

© 2023 Microsoft Corporation. All rights reserved. 

By using this demo/lab, you agree to the following terms:

The technology/functionality described in this demo/lab is provided by Microsoft Corporation for purposes of obtaining your feedback and to provide you with a learning experience. You may only use the demo/lab to evaluate such technology features and functionality and provide feedback to Microsoft. You may not use it for any other purpose. You may not modify, copy, distribute, transmit, display, perform, reproduce, publish, license, create derivative works from, transfer, or sell this demo/lab or any portion thereof.

COPYING OR REPRODUCTION OF THE DEMO/LAB (OR ANY PORTION OF IT) TO ANY OTHER SERVER OR LOCATION FOR FURTHER REPRODUCTION OR REDISTRIBUTION IS EXPRESSLY PROHIBITED.

THIS DEMO/LAB PROVIDES CERTAIN SOFTWARE TECHNOLOGY/PRODUCT FEATURES AND FUNCTIONALITY, INCLUDING POTENTIAL NEW FEATURES AND CONCEPTS, IN A SIMULATED ENVIRONMENT WITHOUT COMPLEX SET-UP OR INSTALLATION FOR THE PURPOSE DESCRIBED ABOVE. THE TECHNOLOGY/CONCEPTS REPRESENTED IN THIS DEMO/LAB MAY NOT REPRESENT FULL FEATURE FUNCTIONALITY AND MAY NOT WORK THE WAY A FINAL VERSION MAY WORK. WE ALSO MAY NOT RELEASE A FINAL VERSION OF SUCH FEATURES OR CONCEPTS. YOUR EXPERIENCE WITH USING SUCH FEATURES AND FUNCITONALITY IN A PHYSICAL ENVIRONMENT MAY ALSO BE DIFFERENT.

## Table of Contents
 
## Exercise 1: Data Engineering experience, Data ingestion from a spectrum of analytical data sources into OneLake
 
 - Task 1.1: Use the Data Pipelines/Data Flow ‘No Code-Low Code experience’

 - Task 1.2: Use the ‘New Shortcut’ option from external data sources

 - Task 1.3: Transform data using Dataflow Gen2 ‘No Code-Low Code experience’ Copilot
 


## Exercise 2: DLT Pipelines, Unity Catalog (Data governance), Metastore experience, Retrieval Augmented Generation (RAG) and Machine Learning (ML)
 
 - Task 2.1: Explore Delta Live Table pipeline (Data Transformation)
 
 - Task 2.2: Explore the data in the Azure Databricks environment with Unity Catalog (unified governance solution for data and AI)
	
 - Task 2.3 Deploy LLM Chatbots with the Data Intelligence Platform (optional)


## Exercise 3: Building an AI-Powered Enterprise Chatbot with Microsoft Fabric and Azure AI Studio
- Task 3.1 :  Leveraging Microsoft OneLake to store knowledgebase

	1 . Once all resources are created by Powershell Script using ARM Template, dive in to the resources, Select **Azure AI hub**
	
	2 . Launch Azure AI hub resource  
        <img src="media/img-1.png" width="800"/>

	3 . Show Azure AI hub Home page    
        <img src="media/1.png" width="800"/>

	4 . Click on Connections in the AI studio home page and add connection to Azure AI Search
	   	
	<img src="media/3.png" width="800"/>

	5 . Select Azure AI Search  
        <img src="media/4.png" width="800"/>

	6 . Here it is Azure AI Search Connection  
	<img src="media/5.png" width="800"/>
	
	7 . Click on Projects and Select Pre-created Project
  
	<img src="media/2.png" width="800"/>
	
	8 . Select **Data** from Left menu and click on **New data** source Connection
  
	<img src="media/6.png" width="800"/>

	9 . Click on **New Connection**
  
	<img src="media/7.png" width="800"/>

	10 . Select **Service** as **Microsoft OneLake**
  
	<img src="media/8.png" width="800"/>

	11 . Open WorkSpace YOu created at starting of the lab, Select Lakehouse from it.
    
	<img src="media/9.png" width="800"/>

	12 . Open the Lakehouse and Upload **input** folder into the files.
  
	<img src="media/10.png" width="800"/>

	13 . The **input** folder you get from the path **MS-Ignite\Pre-Day\artifacts\aistudio**, Select it
  
	<img src="media/11.png" width="800"/>

	14 . Click on Newly created input folder and click on three dots and select properties 

	<img src="media/12.png" width="800"/> 
	<img src="media/13.png" width="800"/>
 
        15 . Copy the Onelake URL from it

	<img src="media/14.png" width="800"/>

	16 . Go back to the AZure AI hub tab , paste the OneLake artifact URL, remove the **/input** from the url and paste it

	<img src="media/15.png" width="800"/>
	<img src="media/16.png" width="800"/>

	17 . Select Authentication method as **Microsoft Entra ID based** , Pass the Connection name as **OneLake**, Click on **Create connection**
  
	<img src="media/17.png" width="800"/>

	18 . Select created data connection **onelake** from the drop down,select **input** folder and Click on **next**
	
	
	<img src="media/18.png" width="800"/>
	<img src="media/19.png" width="800"/>

	19 . Provide Data name and Click on **create**

	<img src="media/20.png" width="800"/>
	<img src="media/21.png" width="800"/>

- Task 3.2 : Indexing OneLake data in Azure AI Studio, enabling efficient search and retrieval based on user queries.
		
	1 . Click on **Indexes** from the left menu , create **New index**

	<img src="media/22.png" width="800"/>
	
	2 . Select **Azure AI search** from the drop down of **Data source** and click on **Next**
	
	<img src="media/23.png" width="800"/>
	<img src="media/24.png" width="800"/>

	3 . Select existing Azure AI Search , Azure AI search Index. CLick on **Next**

	<img src="media/25.png" width="800"/>

	4 . Click on Next

	<img src="media/26.png" width="800"/>
	<img src="media/27.png" width="800"/>

	5 . It will show like something wrong, don't confuse, wait for some time and refresh the page
	
	<img src="media/28.png" width="800"/>
	<img src="media/29.png" width="800"/>

- Task 3.3 : Integrating Azure OpenAI to refine search results and deliver more precise, context-aware answers to users.
- Task 3.4 : Deploying and testing a Prompt flow to automate query handling, ensuring quick and optimized responses.
	
	1 . Click on **Prompt flow** from the left menu, Click on **create**

	<img src="media/30.png" width="800"/>

 	2 . Scroll down and Select the **upload**  option
  
	<img src="media/31.png" width="800"/>
	
  	3 . The Zip file path **MS-Ignite\Pre-Day\artifacts\aistudio**

  	<img src="media/32.png" width="800"/>

	4 . Select flow type as **Chat flow** and Click on **Upload**

	<img src="media/34.png" width="800"/>

	5 . Click on **Start compute session**
	
	<img src="media/35.png" width="800"/>

	**Note:** It will take 5 around  mins, wait for some time	

	6 . Click on **Chat** and try using the chat

	<img src="media/36.png" width="800"/>

	7 . Paste this Question in Chat **"What can we learn and deduce around retaining Millennials** and click on send icon.
	
	<img src="media/37.png" width="800"/>


  	8 . we can see the response

	<img src="media/38.png" width="800"/>

	9 . Ask one more question, Paste this question **"Identify the key drivers of Conto's nagative market perception,especially amoong Millennials"**
	
	<img src="media/39.png" width="800"/>

	10 . CLick on Deploy
  
	<img src="media/40.png" width="800"/>

 

## Exercise 4: Power BI Experience
 
- Task 4.1: Create a Semantic model and generate insights using Copilot for Power BI


## Exercise 5: Real-time Analytics experience - Explore Streaming data using Copilot for KQL DB (Optional)
 
- Task 5.1: Ingest real-time/historical data into KQL DB using Eventstream
 
- Task 5.2: Analyze/discover patterns, identify anomalies and outliers using Copilot

##Optional
## Exercise 6: Data Science experience - Explore Machine Learning and Business Intelligence scenarios in ADB (read only)
 
- Task 6.1: Build ML models, experiments, and log ML models in the built-in model registry using MLflow and batch scoring

## Overview
!IMAGE[buildarch.png](instructions262125/buildarch.png)

This lab showcases Modern Analytics with Microsoft Fabric and Azure Databricks, featuring a cost-effective, performance-optimized, and cloud-native Analytics solution pattern. This architecture unifies our customers' data estate to accelerate data value creation. The visual illustrates the real-world example of a fictitious company called Contoso, a retailer with thousands of brick-and-mortar stores across the world and an online store. Contoso is acquiring Litware Inc., a company that has curated marketing and sales data processed by Azure Databricks. Their data is stored in the gold layer in ADLS Gen 2. In the following exercises, you will see how the Contoso team leveraged the power of Microsoft Fabric to ingest data from a spectrum sources, combine it with their existing data from ADLS Gen2, and derive meaningful insights. You will witness how the team used a shortcut to reference the existing Litware Inc. data from ADLS Gen2. Finally, you will see the advantages of Unity Catalog and deploying LLM Chatbots with the Data Intelligence Platform.

The lab scenario starts on January 30th. The company's new CEO, April, recently noticed negative trends in their KPIs, including:

- High customer churn

- Declining sales revenue

- High bounce rate on their website

- High operating expense

- Poor customer experience

April asks Rupesh, the Chief Data Officer how they could create a data driven organization and reverse these adverse KPI trends. Rupesh talks to his technical team, including Eva, the data engineer, Miguel, the data scientist and Wendy, the business analyst. Rupesh tasks them with designing and implementing a solution pattern to realize this dream of a data driven organization. Our story centers around Rupesh and his team. They recognize that the existence of data silos within Contoso's various departments presents a significant integration challenge.

During this lab you will execute some of these steps as a part of this team to reverse these adverse KPI trends.

### Exercise 1: Data Engineering experience - Data ingestion from a spectrum of analytical data sources into OneLake

*Before we start executing the steps, we will trigger the simulator app to start streaming data to eventhub.*

1. Open a **Microsoft Edge browser** from VM desktop.

2. Click on browser url field and click +++https://app-realtime-simulator-@lab.LabInstance.Id.azurewebsites.net+++ to browse app service and press **Enter**.

>**Note**: **Do not click anywhere else on the screen until all of the text has been auto filled.**

3. You will see a page like the one shown below.You can proceed with next steps while it loads.

	!IMAGE[task-1.3.png](instructions262125/task-1.3.png)

### Task 1.1: Use the Data Pipelines/Data Flow ‘No Code-Low Code experience’
In this exercise, you will act as the Data Engineer and transfer Contoso's data from Azure SQL Database into the Lakehouse. 
1. Open a new tab and click on +++**https://app.powerbi.com/**+++ to populate the **Power BI** URL and press **Enter**.

2. Enter following email by clicking on username +++**@lab.CloudPortalCredential(User1).Username**+++ and click on **Submit**.

!IMAGE[submit.png](instructions262125/submit.png)

3. Enter the password by clicking on +++**@lab.CloudPortalCredential(User1).Password**+++ and click on **Sign in**.

!IMAGE[unamepass.png](instructions262125/unamepass.png)

4. If prompted to stay signed in, select **Yes**.

!IMAGE[staysignin.png](instructions262125/staysignin.png)

5. Click on the **Continue** button.

!IMAGE[signup1.png](instructions262125/signup1.png)

6. Click on **Business phone number box** and type a 10-digit number in the box by clicking on +++1230000849+++. 

!IMAGE[signup2.png](instructions262125/signup2.png)

7. Again, click on the **Get Started** button.

	!IMAGE[signup3.png](instructions262125/signup3.png)

	**Wait for the PowerBI Workspace to load**

	

	*Close* the top bar for a better view.


8. Click the **+ New workspace** button.

	!IMAGE[task-1.1.2.png](instructions262125/task-1.1.2.png)

9. Type the name +++**ContosoSales@lab.LabInstance.Id**+++ **validate** the available name and click **Apply**.

>**Note**:  If you see the pop message **Upgrade to Power BI Pro License** do the following steps. Else skip to next exercise .

10. *Click on the **Try free** button.*
   !IMAGE[task-1.1-new2.png](instructions262125/task-1.1-new2.png)

11. *Click on the **Got it** button to continue.*
   !IMAGE[task-1.1-new3.png](instructions262125/task-1.1-new3.png)

12. Click on **Workspaces** to verify if the workspace with the given name was created, if not perform the steps above again.

>**NOTE:** If the workspace you created is not visible, perform **step 8** again.

!IMAGE[task-1.1-new4.png](instructions262125/task-1.1-new4.png)

>If the name contosoSales.. is already taken, refresh the page and check again. The workspace might already be created.
   


### Create/Build a Lakehouse
Now, let's see how each department in Contoso could easily create a Lakehouse in their workspace without any provisioning by simply providing the name, given the proper access rights of course!

1. Click on the **left bottom icon** and click on **Data Engineering**.

!IMAGE[task-wb1.png](instructions262125/task-wb1.png)

2. In the new window, under Data Engineering, click **Lakehouse**.

!IMAGE[task-wb2.png](instructions262125/task-wb2.png)

3. Enter the name by clicking on +++**lakehouse**+++.

4. Click the **Create** button.

   !IMAGE[task-1.2.3.png](instructions262125/task-1.2.3.png)

5. Click on **Workspaces** in the left navigation pane and select +++ContosoSales@lab.LabInstance.Id+++

!IMAGE[task-1.3.02.png](instructions262125/task-1.3.02.png)

12. Click the **Data Engineering** icon in the bottom left corner of the screen to select **Data Factory**.

!IMAGE[task-wb3.png](instructions262125/task-wb3.png)

13. Click on **Data pipeline**.

!IMAGE[task-1.3.2.png](instructions262125/task-1.3.2.png)

14. In the pop-up, type the pipeline name +++Azure SQL DB Pipeline+++ and click on the **Create** button.

!IMAGE[task-1.3.3.png](instructions262125/task-1.3.3.png)

15. In the Data pipeline window, click on **Copy data assistant**.

!IMAGE[task-1.3.4.png](instructions262125/task-1.3.4.png)

16. In the pop-up, scroll down through the resources, click on **Azure SQL Database** and then click on the **Next** button.

>**Note** You may not see the **Azure SQL Database** in the same location as shown in the screenshot.

!IMAGE[task-1.3.5.png](instructions262125/task-1.3.5.png)

17. Select the **Create new connection** radio button.


*Steps from here are optional. You may move to Task 1.2*

!IMAGE[task-1.3.6.png](instructions262125/task-1.3.6.png)


18. In the **Server** field, Type SQL Server Endpoint +++@lab.Variable(sqlEndpoint)+++ and Enter +++SalesDb+++ in the **Database** field.

!IMAGE[task-1.3.15.png](instructions262125/task-1.3.15.png)

19. Scroll down and select **Basic** for Authentication kind, enter +++labsqladmin+++ as the Username, +++Smoothie@2024+++ as the Password and click on the **Next** button.

!IMAGE[task-1.3.16.png](instructions262125/task-1.3.16.png)

>**Note:** Close any pop-up that you see throughout the lab.
   
!IMAGE[task-1.3.16.1.png](instructions262125/task-1.3.16.1.png)

>**Note:** Wait for the connection to be created.

20. Click on the **checkbox** for **Select all** and then click on the **Next** button.

!IMAGE[task-1.3.17.png](instructions262125/task-1.3.17.png)

21. Scroll down and click on **Lakehouse**, then click on the **Next** button.

!IMAGE[task-1.3.18.S.png](instructions262125/task-1.3.18.S.png)

22. Click on the **Existing Lakehouse** radio button, click on the **dropdown**, select **lakehouse...** and then click on the **Next** button.

!IMAGE[task-1.3.19.png](instructions262125/task-1.3.19.png)

23. Select the **Load to new table** radio button, click on the **checkbox** beside **Source** and then click on **Next**.

!IMAGE[task-1.3.20.png](instructions262125/task-1.3.20.png)

24. Click on **Save + Run**.

!IMAGE[task-1.3.21.png](instructions262125/task-1.3.21.png)

25. Click on the **OK** button in the Pipeline run window.

!IMAGE[task-1.3.21.0.png](instructions262125/task-1.3.21.0.png)

>**Note:** Wait for the pipeline to execute.

26. Click on the bell icon at the top right of the screen to verify the **Running status** of the pipeline.

!IMAGE[task-1.3.22.png](instructions262125/task-1.3.22.png)

27. Congratulations! You have successfully transferred the Sales data from Azure SQL Database to Lakehouse for Contoso.

28. Similarly, you can get data into the Lakehouses using pipelines from a variety of other sources like Snowflake, Dataverse, etc. Now, your next task is to ingest data from the acquired company, Litware Inc., into the lakehouse from ADLS Gen 2. Data such as customer churn, sales, campaigns and also website bounce rate. Per the architecture diagram, once all the data is in OneLake, Contoso can derive deep insights from it. So, let’s start by creating a shortcut for this external data.

---

### Task 1.2: Use ‘New Shortcut’ option from external data sources

Now this is something exciting! This section shows how easy it is to create shortcuts without actually moving data. That is the power of OneLake! In this exercise, you will ingest the curated marketing, sales, customer churn and product reviews data for Litware from ADLS Gen2. 

1. In the contosoSales... workspace, click on **Filter** and select **Lakehouse**.

!IMAGE[task-1.3-ext-shortcut1.png](instructions262125/task-1.3-ext-shortcut1.png)

2. Click on the **lakehouse...**.

>**Note:** There are 3 options for lakehouse..., namely Lakehouse, Dataset (default) and SQL endpoint. Make sure you select the **Lakehouse** option.

!IMAGE[task-wb4.png](instructions262125/task-wb4.png)

3. Click on the **three dots (Elipse)** on the right side of Files.

4. Click on **New shortcut**.

!IMAGE[task-wb5.png](instructions262125/task-wb5.png)

5. In the pop-up window, under **External sources**, select the **Azure Data Lake Storage Gen2** source.

!IMAGE[task-1.3-ext-shortcut4.png](instructions262125/task-1.3-ext-shortcut4.png)

>**Note:** Wait for the screen to load.

6. In the screen below, we need to enter the connection details for the ADLS Gen2 shortcut.

!IMAGE[task-1.3-ext-shortcut11.png](instructions262125/task-1.3-ext-shortcut11.png)

8. Type the endpoint +++https://stfabricadb@lab.LabInstance.Id.dfs.core.windows.net/+++ under the **URL** field.

9. In the **Authentiation kind** dropdown, select **Account Key**.

10. Type the **account key** +++@lab.Variable(storageaccountkey)+++

11. Click on **Next**.

!IMAGE[task-1.3-ext-shortcut9.png](instructions262125/task-1.3-ext-shortcut9.png)

12. Select the **data** checkbox and click on the **Next** button.

!IMAGE[task-wb6.png](instructions262125/task-wb6.png)

13. Click on the **Create** button.

!IMAGE[task-1.3-ext-shortcut10.png](instructions262125/task-1.3-ext-shortcut10.png)

14. And there you go! Your shortcut is now ready! Simply click on the newly created shortcut named **data**.

!IMAGE[task-wb7.png](instructions262125/task-wb7.png)

15. Scroll down in the **middle of the screen**, click on the **three dots (Elipse)** on the right side of **website_bounce_rate.csv**.

16. Click on **Load to Tables** and select **New table**.

!IMAGE[task-wb8.png](instructions262125/task-wb8.png)

17. In the pop-up verify the **New table name** and then click on the **Load** button. And just like that you now have a table in OneLake with all the website bounce rate information for Contoso to leverage. How cool is that? Next, we proceed with data transformation using Dataflow Gen2 to transform the Sales data ingested from Litware. 

!IMAGE[task-new3.png](instructions262125/task-new3.png)

---

### Task 1.3: Transform data using Dataflow Gen2 ‘No Code-Low Code experience’ Copilot

In this exercise, you will experience how easy it is to use Copilot to transform Litware's sales data into the silver layer. 

1. Click on the **Data Factory** icon on the bottom left corner of the screen and select **Data Factory**.

!IMAGE[task-1.3.1.png](instructions262125/task-1.3.1.png)

2. Click on **Dataflow Gen2**.

!IMAGE[task-1.2.02.png](instructions262125/task-1.2.02.png)

3. Click on the **Get data** button.

!IMAGE[task-1.2.03.png](instructions262125/task-1.2.03.png)

4. In the pop-up window, From **OneLake data hub** and click on **lakehouse**.

!IMAGE[task-1.2.04.S.png](instructions262125/task-1.2.04.S.png)

5. Click on the **Next** button.

!IMAGE[task-1.2.05.1.png](instructions262125/task-1.2.05.1.png)

6. Expand **Lakehouse**, **Files**, **data** and check the **sales_data.csv** checkbox, then **click** on the **Create** button.

!IMAGE[task-wb9.S.png](instructions262125/task-wb9.S.png)

8. Click on the **Copilot** button, paste the **prompt** provided below in the text box and click on the **send** icon.

+++Use first row as header in sales_data table+++


!IMAGE[task-wb10.png](instructions262125/task-wb10.png)

9. Similarly, you can paste the following prompts in Copilot for data transformation.

+++Remove empty rows from GrossRevenue and NetRevenue column from sales_data table+++

>**Note:** Due to time constraints, we will not publish and run the Dataflow from the Pipeline.

10. Click on the **close** icon at top right of the **Dataflow** window.

!IMAGE[task-1.2.08.png](instructions262125/task-1.2.08.png)

>If necessary, scroll up to show the close icon.

11. Click on **Yes**. Congrats for completing this data transformation! Now, as you know, Litware was primarily using Azure Databricks with their data stored in ADLS Gen2 before the acquisition. Post merger, as one unified company – Contoso, they decided to leverage Azure Databricks to build and manage reliable data pipelines via Delta Live Tables (DLT). After that, you will see the amazing power of Unity Catalog that Contoso’s data architects used to quickly learn all about Litware's data without having to go through tons of documents. And all by simply leveraging AI and data intelligence. Let us see how.

!IMAGE[task-1.2.09.png](instructions262125/task-1.2.09.png)

---

### Exercise 2: DLT pipelines, Unity Catalog (data governance), Metastore experience, RAG and ML

### Task 2.1: Delta Live Table pipeline (Interactive)

Delta Live Tables (DLT) allow you to build and manage reliable data pipelines that deliver high-quality data in Lakehouse. DLT helps data engineering teams simplify ETL development and management with declarative pipeline development, automatic data testing, and deep visibility for monitoring and recovery.

1. Open new tab in your browser and sign in to the Azure Databricks Workspace, by clicking on
+++https://@lab.Variable(workspaceurl)+++ and press **ENTER**.

2. Click on the **Sign in with Microsoft Entra ID**.

!IMAGE[task-2.2.1new.S.png](instructions262125/task-2.2.1new.S.png)

3.	In the left navigation pane click on **Delta Live Table**.

!IMAGE[task-2.2.2new.png](instructions262125/task-2.2.2new.png)

4. Click on the **Create pipeline** button.

!IMAGE[task-2.2.3.1new.png](instructions262125/task-2.2.3.1new.png)

5. Enter the name of the pipeline as +++DLT_Pipeline+++ and click on the file icon to browse the notebook.

!IMAGE[task-2.2.3new.png](instructions262125/task-2.2.3new.png)

6. Click on **Shared**.

7. Click on **Analytics with ADB**.

8. Click on the **01 DLT Notebook**.

9. Click on the **Select** button.

!IMAGE[task-2.2.4new.png](instructions262125/task-2.2.4new.png)

10. Click on the **Create** button.

!IMAGE[task-2.2.5new.png](instructions262125/task-2.2.5new.png)

>**Note**: Due to time constraints we have pre-loaded the output tables in your Databricks. We will not be executing this pipeline.

14. The result would look similar to the following screen.

!IMAGE[task-2.2.7.png](instructions262125/task-2.2.7.png)

---

### Task 2.2: Explore the data in Azure Databricks environment with Unity Catalog (unified governance solution for data and AI).

We saw how Contoso was able to utilize DLT pipelines to create a medallion architecture on their data. Now let’s look at how data governance was managed on this curated data across the organization and how it was made easy with Unity Catalog.
 
With the acquisition of Litware Inc., Contoso had a lot of data integration and interoperability challenges. Contoso wanted to make sure that the transition was smooth and their data engineers and data scientists could easily assimilate the data processed by Databricks. Thankfully, they had the help from a wide selection of Gen AI features right within Azure Databricks to understand and derive insights from this data. Let's see how!

>**Note**: Due to time constraints, the following steps
will be completed via an online Click-by-Click. Please follow the green beacons for this exercise.

	
1.	Open the following link in a new tab [here](https://regale.cloud/Microsoft/viewer/3066/task-22-explore-the-data-in-azure-databricks-environment-with-unity-catalog/index.html#/0/0)

2.	Follow the green beacons and expand **litware_unity_catalog db**.

3.	Expand the **rag** schema and click on **tables**.

4.	Click on **silver_customer_churn** table.

!IMAGE[task-2.1new.png](instructions262125/task-2.1new.png)

5.	Click on **Accept** in 'AI Suggested Comment' box and Click on **AI Generate**.

!IMAGE[task-2.1.1new.png](instructions262125/task-2.1.1new.png)
	
We can see that AI in Azure Databricks has autogenerated the description for the table and its columns. Users can choose to accept the descriptions or edit them further. This improves the ease of governance on this new data for Contoso. There’s no need for Contoso’s data engineers to read through tons of documents to learn about Litware's data. How cool is that? Next, let's see how easy it is to query this data.

!IMAGE[task-2.2new.png](instructions262125/task-2.2new.png)
	
6.	Select the dropdown on **Create**.

7.	Click on **Query**.

!IMAGE[task-2.3new.png](instructions262125/task-2.3new.png)
	
8.	Select the **Assistant** tab.

9.	Click on the query area and click on send button.
	
!IMAGE[task-2.4new.png](instructions262125/task-2.4new.png)
	
By simply using a natural language query and leveraging the AI generated table and field descriptions mentioned earlier, Azure Databricks generates an equivalent SQL query. There’s no need to be skilled in SQL queries and so business friendly, right?
	
10. Click on the **Arrow** to replace the current code.

!IMAGE[task-2.4.1new.png](instructions262125/task-2.4.1new.png)

11.	Click on **Run**.

12.	Check the output.


!IMAGE[task-2.5new.png](instructions262125/task-2.5new.png)

Users also have the capability to fix errors in queries with the AI assistant. Let's intentionally introduce an error by misspelling a table name and see the AI's response.
	
13.	In the query, click on **churnstatus** to misspell it.

14.	Click on **Run** to see the error.

15.	Click on **Diagnose error** to fix the query issue. See how easily the error is fixed! It is like having a virtual assistant available 24 hours!

!IMAGE[task-2.6new.png](instructions262125/task-2.6new.png)

16. Click on the **Arrow** to replace the current code.

!IMAGE[task-2.4.1new.png](instructions262125/task-2.4.1new.png)
	
Data discovery is also made simple within Azure Databricks. Users can simply search for table names or the information they are looking for in the global search and all the relevant items are returned, again leveraging the table and field descriptions created by AI and data intelligence mentioned earlier.
	
17.	Click on **Search*.

18.	Click on **Open search in a full page**.

!IMAGE[task-2.7new.png](instructions262125/task-2.7new.png)

19. Click to search for **campaigns** and click on show all results. Now, the next big challenge for Contoso was to get visibility of their Market Sentiment KPI. Remember, the Market Sentiment before the acquisition was at an all-time low. News articles and analyst reviews were being continuously published. All this unstructured data had to be efficiently assimilated so that the Market Sentiment could be tracked. That brings us to the next task. Let us see!

!IMAGE[task-2.7new.png](instructions262125/task-2.7new.png)

---
### Task 2.3 (OPTIONAL)Deploy LLM Chatbots With the Data Intelligence Platform 

Contoso also wanted to improve how efficiently they analyzed hundreds of documents and news articles about their big merger and their company policies. Why? To track and improve their Market Sentiment KPI. Azure Databricks provides just the solution with its Delta Lake architecture supporting unstructured data, like PDF documents, with Lang chain models leveraging the Databricks Foundation Model for creating custom chatbots. Let's see how this was done.

>**Note**: This section is optional. Due to time constraints, the following steps will be completed via an online Click-by-Click for setting up the Unity Catalog. Please follow the green beacons and the instructions on the screen for this exercise.


1. Open the following link in a new tab.
[here](https://regale.cloud/Microsoft/viewer/3067/task-23-deploy-llm-chatbots-with-the-data-intelligence-platform/index.html#/0/0).

---

### Exercise 3: Power BI Experience
 
### Task 3.1: Create Semantic model and generate insights using Copilot for Power BI

Great work so far. Go Contoso! With all the disparate sources data as well as Litware's data in OneLake, it is now time to get some awesome insights and visualizations from this data. So, let's dive deep into the experience of the Business Analyst, Wendy, for just that. Based on all the gathered data, Wendy is expected to create Power BI reports for other data citizens and stakeholders. Let's step into her shoes to experience the power of Copilot for Power BI in conjunction with Direct Lake Mode.

1. Click on **Workspaces** and select **contosoSales...** 

!IMAGE[task-1.3.02.png](instructions262125/task-1.3.02.png)

2. Click on **Filter** and select **Lakehouse**.

!IMAGE[task-1.3-ext-shortcut1.png](instructions262125/task-1.3-ext-shortcut1.png)

3. Click on the **lakehouse**.

>**Note:** There are 3 options for lakehouse..., namely Lakehouse, Dataset (default) and SQL endpoint. Make sure you select the **Lakehouse** option.

!IMAGE[task-wb11.png](instructions262125/task-wb11.png)

4. Click on the **New semantic model**. 

!IMAGE[task-new4.png](instructions262125/task-new4.png)

5. Enter +++website_bounce_rate_model+++ in the Name field. 

6. Select workspace as **contosoSales...** and scroll down.

!IMAGE[task-new5.png](instructions262125/task-new5.png)

7. Select **website_bounce_rate** table and click on the **Confirm** button. 

!IMAGE[task-new6.png](instructions262125/task-new6.png)

>Wait for the semantic model creation.

8. To create a new report using this semantic model, click on the **New Report** at the top bar.
 
!IMAGE[task-new7.png](instructions262125/task-new7.png)

9. Click on the **Copilot** icon, collapse all the other panes and then click on the **Get started** button. You will now see how easy it is for the data analyst to create compelling Power BI reports and get deep insights with literally no hands-on coding!

!IMAGE[task-new8.png](instructions262125/task-new8.png)
	
10. Click on the **Prompt Guide** button.  

11. Select the option **What's in my dataset?**
   
!IMAGE[task-new9.png](instructions262125/task-new9.png)

The first option, “What’s in my dataset?’ provides an overview of the contents of the dataset. It identifies and describes what the datasets and attributes are all about and provides a concise summary of the content. So, there’s no need to wait for someone to explain the dataset. This improves the efficiency and volume of report creation for Contoso.

12. Click on the **Prompt Guide** button. 

13. Select the option **Suggest content for this page**. 

!IMAGE[task-new10.png](instructions262125/task-new10.png)
	
The copilot can not only describe the dataset, but it can also recommend the kind of reports that could be created using this data.

14. Click on the **Customer** related suggested insight as shown in step 1 of the screenshot **Customer Behavior Insights**.

>The Customer insight for you might differ from the screenshot.

15. Click on the **Edit** button as shown in step 2 of the screenshot.  

!IMAGE[task-new11.png](instructions262125/task-new11.png)

16. Replace the prompt with following: +++Create a report Bounce Rate analysis, to show the correlation between customer sentiment, particularly among millennials and Gen Z, unsuccessful product searches across different devices, and the website's bounce rate by customer generations.+++  

17. Click on the **Send** button and wait for the results to load. 

!IMAGE[task-new12.png](instructions262125/task-new12.png)
	
>**Note:** If you see the error message saying, 'Something went wrong.', try refreshing the page and restart the task. Being in a shared environment, the service may be busy at times.

Based on this report, we notice that the website bounce rate for Contoso is especially high amongst the Millennial customer segment. Let’s ask Copilot if it has any recommendations for improving this bounce rate.

We’ll ask Copilot for suggestions based on the results and data in the report. 

18. Enter the following prompt in Copilot, +++Based on the data in the page, what can be done to improve the bounce rate of millennials?+++ and press the **Send** button.
	
!IMAGE[task-new13.png](instructions262125/task-new13.png)
	
19. Observe the suggestions provided by Copilot. So, you see copilot creates the desired Power BI report and even goes a step further to give powerful insights. How cool is that? Wendy realizes that in order for the website bounce rate to improve, Contoso needs to transform their mobile website experience for millennials. And this helps them reduce their millennial related customer churn too! Now, what if Contoso’s leadership team needed a quick summary of this entire report? All good, let’s see the SmartNarratives feature in action! 
	
!IMAGE[task-new14.png](instructions262125/task-new14.png)
	
20. Expand the **Visualizations** pane and select the **Narratives** visual. 

21. Click on **Copilot (preview)** within the visual.

!IMAGE[task-new15.png](instructions262125/task-new15.png)
	
22. Select **Give an executive summary**. 

23. Click on **Update** and observe the generated summary. See how easy it was to get an executive summary? And all this with absolutely no IT resource dependency!
 
!IMAGE[task-new16.png](instructions262125/task-new16.png)
	
The summary could also be generated in another language if specified. Additionally, the summary updates if you filter the report on any visual. How cool is that!

---

### Exercise 4: Real-time Analytics experience, explore Streaming data using Copilot for KQL DB

Imagine it is 6 am on the day of Contoso's big Thanksgiving sale. Customers are flocking to their stores in large numbers. We are about to witness the very culmination of Contoso's phenomenal transformation with Microsoft Fabric and ADB. Specifically, we will see how near real-time data is used to make decisions for the next moment in Contoso's stores to ensure optimal temperatures are maintained for their customers while they shop at the big sale! Let's see how! 

### Task 4.1: Ingest real-time/historical data into KQL DB using Eventstream

1. While you are in the Fabric workspace homepage, click **experience** button on the **bottom left** of the screen and then select **Real-Time Analytics**.

!IMAGE[task-wb12.png](instructions262125/task-wb12.png)

2. In Real-Time Analytics experience screen click on **KQL Database**.

!IMAGE[task-wb13.png](instructions262125/task-wb13.png)

3. Enter the name +++Contoso-KQL-DB+++.

4. Click on the **Create** button and wait for the database to be created.

!IMAGE[task-5.1.4.png](instructions262125/task-5.1.4.png)

5. Click on the **Real-Time Analytics** at the bottom left corner of the screen and select **Real-Time Analytics**.

!IMAGE[task-wb14.png](instructions262125/task-wb14.png)

6. Select **Eventstream**.

!IMAGE[task-wb15.png](instructions262125/task-wb15.png)

7. Enter the name as +++RealtimeDataTo-KQL-DB+++ and click on **Create** button.

!IMAGE[task-5.2.1new1.0.2.png](instructions262125/task-5.2.1new1.0.2.png)

8. Click on the **Add external source** button.

!IMAGE[task-5.2.1new1.0.3.png](instructions262125/task-5.2.1new1.0.3.png)

9. Click on the **Azure Event Hub** button.

!IMAGE[task-5.2.1new1.0.4.png](instructions262125/task-5.2.1new1.0.4.png)

10. Enter the value for **Event Hub namespace** +++evh-thermostat-@lab.LabInstance.Id+++ and enter the **Event Hub** value as +++thermostat+++.

!IMAGE[task-5.2.5-2.png](instructions262125/task-5.2.5-2.png)

11. Scroll down and select **Shared Access Key** for Authentication kind, enter +++thermostat+++ as the Shared Access Key Name and then Enter the value +++@lab.Variable(EventHubKey)+++ in the **Shared Access Key**.

12. Select Data format as **JSON** and then click on the **Connect** button.

!IMAGE[task-5.2.5-3.png](instructions262125/task-5.2.5-3.png)

>**Note:** Wait for the connection to be established.

13. Click on the **Next** button.

!IMAGE[task-5.2.1new7.png](instructions262125/task-5.2.1new7.png)

14. Click on the **Add** button.

!IMAGE[task-5.2.1new8.png](instructions262125/task-5.2.1new8.png)

15. In the Eventstream canvas, click on the **Add destination** dropdown and select **KQL Database**.

!IMAGE[task-5.2.1new9.png](instructions262125/task-5.2.1new9.png)

16. Select the **Event processing before ingestion** radio button, enter +++RealTimeData+++ as the Destination name.

17. Select **contosoSales...** and **Contoso-KQL-DB** from the respective 'Workspace' and 'KQL Database' dropdowns.

18. Finally click on the **Create new** button.

!IMAGE[task-5.2.12.png](instructions262125/task-5.2.12.png)

19. Enter the table name as +++thermostat+++ and then click on the **Done** button.

!IMAGE[task-5.2.13.png](instructions262125/task-5.2.13.png)

20. Enter the Input data format as **Json**.

!IMAGE[task-5.2.14.png](instructions262125/task-5.2.14.png)

21. Click on the **Publish** button.

!IMAGE[task-5.2.15.png](instructions262125/task-5.2.15.png)

Real-time data from the event hub has been ingested successfully into the KQL Database. Next, as customers walk in aisles and the temperatures fluctuate, let us see how KQL queries proactively identify anomalies and help maintain an optimal shopping experience!

---

### Task 4.2: Analyze/discover patterns, identify anomalies and outliers using Copilot

Kusto Query Language is a powerful tool. In this scenario KQL is used to explore Contoso’s data, discover patterns, identify anomalies and outliers, create statistical modeling, and more.

We use KQL to query the thermostat data that’s streaming in near real-time from the devices installed in Contoso’s stores.

1. Click on the **Workspaces** and select **contosoSales...** workspace from left navigation pane.

!IMAGE[task-5.3.1.png](instructions262125/task-5.3.1.png)

5. Click on the **Real-Time Analytics** at the bottom left corner of the screen and select **Real-Time Analytics**.

!IMAGE[task-wb14.png](instructions262125/task-wb14.png)

3. Select **KQL Queryset**.

!IMAGE[task-wb16.png](instructions262125/task-wb16.png)

4. Enter +++Query Thermostat Data in Near Real-time using KQL Script+++ as the name and click on the **Create** button.

!IMAGE[task-5.3.3.png](instructions262125/task-5.3.3.png)

5. **Wait** for the query set creation and a new screen will display. In this screen, click on **Contoso-KQL-DB**, verify the workspace name and then click on the **Connect** button.

!IMAGE[task-5.3.4.png](instructions262125/task-5.3.4.png)

6. Place your cursor inside the **query** field, select all using **Ctrl + A** and **delete** the pre-written query.

!IMAGE[task-5.3.5.png](instructions262125/task-5.3.5.png)

7. Click on the **Copilot** button.

!IMAGE[task-5.3.6.png](instructions262125/task-5.3.6.png)

8. **Paste** the query provided below in the query section.

+++What is the average temperature every 1 min?+++

9. Click on the **send** icon.

10. Click on the **Insert** button.

!IMAGE[task-5.3.7.png](instructions262125/task-5.3.7.png)

11. Select the **script**, click on the **Run** button and you get the desired result.

!IMAGE[task-5.3.8.png](instructions262125/task-5.3.8.png)

*Similarly you can use the below prompt*

+++Are there any anomalies for this device?+++

So, imagine if one of the aisles had a sudden rise in temperature. Customers start leaving that aisle and the wait time in checkout lines start to increase. But thanks to the KQL Queries, those anomalies would be tracked and immediate notifications would be generated to bring the aisle temperature back to optimal levels! Now, after all these amazing data transformations in OneLake in a healthy ecosystem with Azure Databricks, can we actually predict customer churn for the future? Absolutely! In fact, in the next exercise, let’s see the power of Microsoft Fabric and Azure Databricks to do just that!

---

### Exercise 5: Data Science experience, explore Machine Learning and Business Intelligence scenarios in ADB (read only)
 
We saw how Contoso combined historical gold layer data from ADLS Gen2 with all the OneLake data via shortcuts. Additionally, we saw how all that data could be easily accessed in Azure Databricks (thanks to the standard delta parquet format). Delta live tables were created in Azure Databricks for further curation of data. Contoso can now leverage the power of machine learning models in ADB on that data to gain meaningful insights and predict customer churn. Let's explore the Data Science Experience in Azure Databricks as Data Scientists!

### Task 5.1: Build ML models, experiments, and log ML model in the built-in model registry using MLflow and batch scoring

The architecture diagram shown here illustrates the end-to-end MLOps pipeline using the Azure Databricks managed MLflow.

After multiple iterations with various hyperparameters, the best performing model is registered in the Databricks MLflow model registry. Then it is set up as the model serving in the Azure Databricks Workspace for low latency requests.
	
!IMAGE[task-3.1.1.png](instructions262125/task-3.1.1.png)

1. Navigate back to the **Databricks workspace** we started for the previous exercise.

2. In the left navigation pane, select **Workspace** and click **Workspace** again. Select **Shared**, click on **Analytics with ADB** and finally click on the **03 ML Solutions in a Box.ipynb** notebook.

!IMAGE[task-3.1.2.png](instructions262125/task-3.1.2.png)

Now that we've ingested and processed our customer data, we want to understand what makes one customer more likely to churn than another. Let’s if we can produce a machine learning model that can accurately predict if a particular customer will churn.

Ultimately, we would like to understand our customers' sentiment so we can create targeted campaigns to improve our sales.

3. Navigate to **cmd 10**.

With the data prepared, we can begin exploring the patterns it contains. 

Let's start by examining the customer churn outcome based on factors like a customer's tenure in months and their total amount spent at Contoso. As a result, we can see a high churn rate is seen if the customer's tenure is low, and they have a lower spend amount.

!IMAGE[task-3.1.4.png](instructions262125/task-3.1.4.png)

4. Navigate to **cmd 20**.

5. Navigate to **cmd 21**. 

!IMAGE[task-3.1.5.png](instructions262125/task-3.1.5.png)

By registering this model in Model Registry, we can easily reference the model from anywhere within Databricks.    

6. Review the **cmd 29** cell.

Let’s look at the comparison of multiple runs in the UI.

You can visualize the different runs using a parallel coordinates plot, which shows the impact of different parameter values on a metric.

The best ML model for Customer Churn is selected and registered with Databricks model registry.

!IMAGE[task-3.1.6.png](instructions262125/task-3.1.6.png)

7. Navigate to **cmd 38**.

For low-latency use cases, you can use MLflow to deploy the model for online serving. The serving system loads the Production model version from the Model Registry. 

!IMAGE[task-3.1.7.png](instructions262125/task-3.1.7.png)

8. Navigate to **cmd 40**.

It is then used to predict the probability of Customer Churn using the deployed model and this model endpoint is ready for production.

!IMAGE[task-3.1.8.png](instructions262125/task-3.1.8.png)

9. Navigate to **cmd 41**. 

Once we have the predicted data, it is stored back in delta tables in the gold layer back in OneLake.

!IMAGE[task-3.1.9.png](instructions262125/task-3.1.9.png)

---

Congratulations! You as Data Engineers have helped Contoso gain actionable insights from its disparate data sources, thereby contributing to future growth, customer satisfaction, and a competitive advantage.

In this lab we experienced the creation of a simple integrated, open and governed Data Lakehouse foundation using Modern Analytics with Microsoft Fabric and Azure Databricks.

In this lab we covered the following:

First, we explored the Data Engineering experience and learned how to create a Microsoft Fabric enabled workspace, build a Lakehouse, and ingest data into OneLake along with other data engineering operations with dataflow copilot.

Second, we explored an analytics pipeline using open Delta format and Azure Databricks Delta Live Tables to build a simple Lakehouse and integrate with OneLake with shortcuts.

Third, we explored data governance and generative AI features in Azure Databricks with Unity Catalog. We also explored ML and BI scenarios on the Lakehouse. Here we reviewed MLOps pipeline using the Azure Databricks managed MLflow with Azure ML.

Fourth, we saw the Power BI experience in Fabric with copilot and direct lake mode.

Fifth, we explored Streaming data using KQL DB for a Real-time Analytics experience. Here, we created a KQL Database, ingested real-time and historical data into KQL DB, analyzed patterns to uncover anomalies and outliers with the help of copilot.

Finally, we leveraged Power BI to derive actionable insights from data in the Lakehouse using Direct Lake mode.
