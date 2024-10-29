# Step-by-Step Instructions to Deploy an ARM Template Using PowerShell

## Prerequisite:
### Github Token extraction

1. Log into Github and click on the **Profile** Icon.

![Simulator.](ARMSetupImages/Image4.png)

2. Scroll down the page and click on **Developer settings**.

![Simulator.](ARMSetupImages/Image5.png)

3. Click on **Personal access tokens** dropdown and select **Tokens (Classic)**.

![Simulator.](ARMSetupImages/Image6.png)

4. In the **Confirm Access** window, provide the password and click on the **Confirm** button.

![Simulator.](ARMSetupImages/Image7.png)

5. Add a note in the **Note** textbox, select the expiration days from the **Expiration** dropdown, and select **repo** checkbox.

![Simulator.](ARMSetupImages/Image08.png)

6. Click on the **Generate token** button.

![Simulator.](ARMSetupImages/Image9.png)

7. Click on copy token from "clipboard" and save it for future reference.

![Simulator.](ARMSetupImages/Image10.png)


## Deploying ARM Template using Cloud Shell

1. Log into Microsoft Azure portal and click on **Cloud Shell** icon from the menu bar.

![Simulator.](ARMSetupImages/Image1.png)

2. Select **Powershell**.

![Simulator.](ARMSetupImages/Image2.png)

3. Click on **No storage account required** button, then select the required subscription from the **Subscription** dropdown and click on **Apply**.

![Simulator.](ARMSetupImages/Image3.png)

4. In the Cloudshell, enter the below command and press "enter".

```
git clone -b main --depth 1 --single-branch https://github.com/dreamdemos-ms/MS-Ignite.git ignite24
```

![Simulator.](ARMSetupImages/Image12.png)

5. Enter your Github **username** and press the **Enter** key.

6. Paste the **token** generated in the Github Token extraction steps and press the **Enter** key.

![Simulator.](ARMSetupImages/Image13.png)

**Note**: Wait till the clone completes as seen in the following screenshot.

![Simulator.](ARMSetupImages/Image14.png)

7. Paste the following command in Powershell.

```
cd ignite24/02_Lab
```

![Simulator.](ARMSetupImages/Image15.png)

8. Check for the setup file using "ls" command and run the script with following command.

```
./labSetup.ps1
```

![Simulator.](ARMSetupImages/Image16.png)

9. Browse the **URL** in another tab of your browser and copy the **code**.

    ![Simulator.](ARMSetupImages/Image17.png)

10. Paste the **code** and click on the **Next** button.

    ![Simulator.](ARMSetupImages/Image18.png)

11. Select the **Azure account** to sign in.

     ![Simulator.](ARMSetupImages/Image18.1.png)

12. Click on the **Continue** button.

    ![Simulator.](ARMSetupImages/Image18.2.png)

13. When you see the below **screenshot**, close the tab of your browser and go back to the **Cloudshell tab**.

    ![Simulator.](ARMSetupImages/Image18.3.png)

14. Select the desired subscription and then press the Enter key.

    ![Simulator.](ARMSetupImages/Image18.4.png)

15. Browse the **URL** in another tab of your browser and copy the **code**.

    ![Simulator.](ARMSetupImages/Image18.5.png)

16. Paste the **code** and click on the **Next** button.

    ![Simulator.](ARMSetupImages/Image18.png)

17. Select the **Azure account** to sign in.

     ![Simulator.](ARMSetupImages/Image18.6.png)

18. Click on the **Continue** button.

    ![Simulator.](ARMSetupImages/Image18.7.png)

19. When you see the below **screenshot**, close the tab of your browser and go back to the **Cloudshell tab**.

    ![Simulator.](ARMSetupImages/Image18.8.png)

20. Select the region as per your preference.

    ![Simulator.](ARMSetupImages/Image18.9.png)

>**Note:** It takes approximately 20 minutes for the deployment

21. Once the deployment is successful, verify if the following resources are deployed.

| S.No | Resource Name |  Resources |
|------|----------|----------|
| 1    | evh-thermostat-... | EventHub Namespace  |
| 2    | kv-ignite-... | Azure Key Vault  |
| 3    | stignite...  | Storage Account   |
| 4    | mssql...    | SQL Server     |
| 5    | SalesDb | SQL Database    |
| 6    | app-realtime-simulator-...  | WebApp - Thermostat |
| 7    | asp-realtime-simulator-... | App Service Plan  |
| 8    | adb-ignite-... | Azure Databricks Workspace | 

22. Goto the resource group in Azure Portal **rg-ignite24-...** and click on the **app-realtime-simulator-..**

    ![Simulator.](ARMSetupImages/Image18.10.png)

23. Click on the browse button.

    ![Simulator.](ARMSetupImages/Image18.11.png)

24. Wait for the simulator app to browse until you see a screen as shown in the below screenshot.

    ![Simulator.](ARMSetupImages/Image18.11.png)

