# Integrating Tableau and Acumatica
The following explains how one can import data from Acumatica Generic Inquires (GIs) into the example Tableau workbooks provided. As an example, the procedure will import Acumatica "AR-Invoices and Memos" data into Tableau. 

System requirements: Acumatica v2018 R2 and Tableau Desktop 2018.3 running on Windows or Mac. However, these instructions are the same (or very similar) to other Acumatica and Tableau versions. 


### 1. Setting up Acumatica to render data to external applications like Tableau:
- Log in to your Acumatica portal and find the Generic Inquiry with the same name as the sample workbook. There are two main paths: 1) More Items > Configuration > Customization > Generic Inquiry. 2) System > Customization > Generic Inquiry.
- Click the search icon in the Inquiry Title box, find and double-click on "AR-Invoices and Memos".
- Be sure the "Expose via OData" checkbox is checked. If not, check it and click the Save icon.
- Repeat the steps above for whichever workbooks you downloaded and want to connect.
- Important: Find out from your system administrator the OData Feed URL to your Acumatica site. For instance, for an Acumatica portal https://abcorp.acumatica.com, the OData Feed URL might be something like https://abcorp.acumatica.com/odata/abcorp.

### 2. Setting up Tableau Desktop to import data from Acumatica:
- Installing Tableau Desktop: Go to https://www.tableau.com/support/releases and select a Tableau Desktop version to download (we recommend downloading the latest version). Download and run the Tableau installer, follow the prompts to complete the installation. You'll need admin rights to the computer where you're installing Tableau.
- Open one of the Tableau workbooks that you downloaded from the Example Tableau Workbooks folder.
- Click the Data Source button in the bottom left corner, which will open the OData connection wizard.
- Replace "localhost/acumaticatest1/odata" with the URL that you collected in step 1, keeping the name of the GI on the end of the new URL you are creating.
- Update the Authentication method to match what you set up when installing your Tableau Desktop.
- Enter your Username and Password if using that Authentication method and Save.  
- This will run a query to gather your data and you should now be seeing your companies data in the example Tableau workbook.



### 3. Possibilities and limitations:
- To combine data from two of more GIs into Tableau, you might use GI object linking or Tableau table linking and unions. Please search online documentation for instructions.
- You might also want to publish your Tableau workbooks to Tableau Online (https://www.tableau.com/products/online/request-trial). This will allow you to expose your Tableau reports to other users via web browsers and mobile device apps. This will also allow you to insert your Tableau reports and dashboards directly inside Acumatica dashboards.
- The approach described here establishes a direct connection between Tableau and Acumatica. This connection retrieves data and stores it in a Tableau extract to get new data from your Acumatica instance, you will need to refresh the extract.
- Retrieving data via OData protocol can be very slow (average of a few thousand records every 10 seconds).
- There are vendors like DataSelf Corp that have optimized the Tableau and Acumatica integration to overcome the OData protocol limitations. See below for details.

### 4. Further support and assistance:
- Tableau support: https://www.tableau.com/support
- Acumatica support: https://www.acumatica.com/acumatica-service-offerings/
- DataSelf Corp: https://dataself.com/acumatica-bi-analytics/. DataSelf Corp is a Tableau and Acumatica certified partner which can assist you in maximizing and expediting your return-on-investment in Tableau and Acumatica. DataSelf provides dozens of connectors, and 5,000+ reports and dashboards for areas such as sales, inventory, services and financials, so your team can focus on data analysis on day one, instead of building everything from scratch.
