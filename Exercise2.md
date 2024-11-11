### Exercise 2: DLT Pipelines-Unity Catalog for Data governance, Metastore experience Retrieval Augmented Generation and Machine Learning

### Task 2.1: Explore Delta Live Table pipeline (Data Transformation)

Delta Live Tables (DLT) allow you to build and manage reliable data pipelines that deliver high-quality data in Lakehouse. DLT helps data engineering teams simplify ETL development and management with declarative pipeline development, automatic data testing, and deep visibility for monitoring and recovery.

1. Go back to the azure portal, Resource Group that mentioned below.

```BASH
 <inject key= "resourcegroup" enableCopy="true"/>
```

2. Search for the Azure Databricks in the Resource group search field.

 ![azuredatabricks](media/databrickssearch.png)

3. Click on the **Launch Workspace**.

 ![azuredatabricks](media/launchdatabricks.png)

4. Click on the **Sign in with Microsoft Entra ID**.

![databrickssignin.png](media/labMedia/databrickssignin.png)

5. Scroll down in the left navigation pane and click on **Delta Live Table**.

![task-2.2.2new.png](media/labMedia/task-2.2.2new.png)

6. Click on the **Create pipeline** button.

![task-2.2.3.1new.png](media/labMedia/task-2.2.3.1new.png)

7. Enter the name of the pipeline as "DLT_Pipeline" , scroll down to the **Paths** and click on the **file icon** to browse the notebook.

```BASH
DLT_Pipeline
```
![task-2.2.3new.png](media/labMedia/task-2.2.3new.png)

8. Click on **Shared**, click on **Analytics with ADB**, click on the **01 DLT Notebook** and then click on the **Select** button.

![task-2.2.4new.png](media/labMedia/task-2.2.4new.png)

9. Click on the **Create** button.

![task-2.2.5new.png](media/labMedia/task-2.2.5new.png)

>**Note**: Do not click on the **Start** button. Due to time constraints, We will not be executing this pipeline.

10. If we were to execute it, we would see a result similar to the one in the following screenshot. Click on the screenshot for a better view.

![task-2.2.7.png](media/labMedia/task-2.2.7.png)

---

### Task 2.2: Explore the data in the Azure Databricks environment with Unity Catalog (unified governance solution for data and AI).

We saw how Contoso utilized DLT pipelines to create a medallion architecture on their data. Now let’s look at how data governance was managed on this curated data across the organization and made easy with Unity Catalog.
 
With the acquisition of Litware Inc., Contoso had a lot of data integration and interoperability challenges. They wanted to make sure that the transition was smooth, and their data engineers and data scientists could easily assimilate the data processed by Databricks. Thankfully, they were able to leverage Gen AI features right within Azure Databricks to understand and derive insights from this data.

>**Note**: Due to time constraints, the following steps will be completed via an online Click-by-Click exercise.
>Please follow the green beacons for this exercise.
- This exercise will be performed outside the VM browser.
- Please return back to the VM browser once you see the **End of Task 2.2** screen.
- Once you press the **Agree** button, press the **A** key on your keyboard if you do not see the annotations.

	
1. Click on the [**hyperlink**](https://regale.cloud/Microsoft/viewer/3066/task-22-explore-the-data-in-azure-databricks-environment-with-unity-catalog/index.html#/0/1)

2. Continue with next excercise.

### Task 2.3: Create mirrored Azure Databricks catalog in Fabric and analyze data using T-SQL

Mirroring Azure Databricks catalog structure to Fabric enables the access of the underlying catalog data through shortcuts. Hence any changes in data are reflected immediately in Fabric. There is no data movement or data replication.

1. Navigate back to the Microsoft Fabric tab on your browser 
```BASH
https://app.powerbi.com/
```

2. Click on the **ContosoSales...** and select **New item** from menu bar.

![Task-2.3_1.png](media/labMedia/Task-2.3_1.png)

3. In the **New item** window, scroll down and click on **Microsoft Azure Databricks catalog (preview)**.

![Task-2.3_2.png](media/labMedia/Task-2.3_2.png)

4. A **New source** window pops up. Select the **Create new connection** radio button.

![Task-2.3_3.png](media/labMedia/Task-2.3_3.png)

5. In the URL field of the connection string, copy paste the provided URL below.

```BASH
 <inject key= "databricksurl" enableCopy="true"/>
```

8. Now, select **Service principal** from 'Authentication kind' dropdown box, and enter the following details.

- Tenant ID: 

```BASH
<inject key= "TenantID" enableCopy="true"/>
```
- Service principal client ID: 

```BASH
<inject key= "ClientID" enableCopy="true"/>
```

- Service principal Key:

```BASH
<inject key= "Secret" enableCopy="true"/>
```

9. click on the **Connect** button.

![Task-2.3_7.png](media/labMedia/Task-2.3_7.png)

10. Click on **Next** button.

![Task-2.3_7.1.png](media/labMedia/Task-2.3_7.1.png)

11. In the **Choose data** screen, select the **Catalog name** from the dropdown box, and select the tables to be mirrored into Fabric, then select the checkbox **Automatically sync future catalog changes for the selected schema** to mirror future tables and click on **Next** button.

![Task-2.3_8.png](media/labMedia/Task-2.3_8.png)

12. Enter the **Artifact name** for your mirrored Databricks Catalog and click on **Create** button.

![Task-2.3_9.png](media/labMedia/Task-2.3_9.png)

13. Click on **Monitor catalog** button to track the mirroring status.

![Task-2.3_10.1.png](media/labMedia/Task-2.3_10.1.png)

14. Click on the **View SQL endpoint** button. You can also select the tables to preview data.

![Task-2.3_10.png](media/labMedia/Task-2.3_10.png)
