# Connecting Tableau to Acumatica - Ready-to-go Templates
The following explains how one can import data from Acumatica Generic Inquires (GIs) into the predefined Tableau workbooks (*.twb) included above. These workbooks contain preconfigured settings to connect to Acumatica and sample reports and dashboards.

To learn how to create new connectors to Acumatica, visit https://github.com/dataself/Tableau-Acumatica-Connectors/tree/master/do-it-yourself.

System requirements: Acumatica v2018 R2 and Tableau Desktop 2018.3 running on Windows or Mac. However, these instructions are the same (or very similar) to other Acumatica and Tableau versions. Go to https://www.tableau.com/support/releases to download Tableau Desktop.

### 1. Setting up Acumatica to render data to external applications like Tableau:
- As an example, this procedure will use the included "AR-Invoices and Memos.twb" Tableau workbook to import data from your Acumatica "AR-Invoices and Memos" GI. 
- Log in to your Acumatica portal and find the Generic Inquiry with the same name as the predefined Tableau workbook (ex.: "AR-Invoices and Memos"). There are two main paths: 1) More Items > Configuration > Customization > Generic Inquiry. 2) System > Customization > Generic Inquiry.
- Click the search icon in the Inquiry Title box, find and double-click on "AR-Invoices and Memos".
- Be sure the "Expose via OData" checkbox is checked. If not, check it and click the Save icon.
- Important: Find out from your system administrator the OData Feed URL to your Acumatica site. For instance, for an Acumatica portal https://abcorp.acumatica.com, the OData Feed URL might be something like https://abcorp.acumatica.com/odata/abcorp.

### 2. Using ready-to-go Tableau templates to import data from Acumatica:
- Download a Tableau workbook (ex.: AR-Invoices and Memos.twb) from the list at the top of this page and double-click the downloaded file. This will launch Tableau Desktop. 
- Click Cancel since Tableau will try to connect to an Acumatica sample site used to build the templates. 
- Click Edit Connection, and in the OData Server: box, replace "http://localhost/acumaticatest1/odata/" with the OData Feed URL that you collected in step 1, keeping the name of the GI on the end of the new URL you are creating (ex.: https://abcorp.acumatica.com/odata/abcorp/AR-Invoices%20and%20Memos).
- Enter your Acumatica Username and Password and Save. This will validate that your credentials have access to your Acumatica data. 
- Click the other tabs at the bottom to view sample reports and dashboards. The first tab you visit will trigger the data import process from Acumatica which might take a while depending on the size of GI's dataset. Click the other tabs to view the sample reports and dashboards.
- To refresh the data from Acumatica again, click F5. 

### 3. Possibilities and limitations:
- The approach described here establishes a direct connection between Tableau and Acumatica. This connection retrieves data and stores it in a Tableau extract.  Every time you need to get new data from your Acumatica instance, you will need to refresh the extract.
- Retrieving data via OData protocol can be very slow (average of a few thousand records every 10 seconds).
- Not matter what BI tool you use, retrieving large amounts of data from Acumatica might cause performance issues in your Acumatica site. So, if this is a concern, you should consider refreshing the extracts outside of normal business hours and also avoid refresh extracts in parallel.
- You might also want to explore publishing your Tableau workbooks to Tableau Server such as Tableau Online (https://www.tableau.com/products/online/request-trial). This will allow you to:
  - Expose your Tableau reports to other users via web browsers and mobile device apps
  - Insert your Tableau reports and dashboards directly inside Acumatica dashboards.
- To publish to an existing Tableau Server, click on "Server" in the top bar and select Publish Workbook.  When prompted for your Tableau Server information, provide it, then select which project you would like it saved in, enter a name and click Publish. 
- There are vendors like DataSelf Corp that have optimized the Tableau and Acumatica integration to overcome many of the OData protocol and Tableau limitations. See below for details.

### 4. Further support and assistance:
- Tableau support: https://www.tableau.com/support
- Acumatica support: https://www.acumatica.com/acumatica-service-offerings/
- DataSelf Corp: https://dataself.com/acumatica-bi-analytics/. DataSelf Corp is a Tableau and Acumatica certified partner which can assist you in maximizing and expediting your return-on-investment in Tableau and Acumatica. Out-of-the-box, DataSelf provides dozens of connectors and 5,000+ reports and dashboards for areas such as sales, inventory, services, and financials. This allows your team to focus on data analysis on day one, instead of building everything from scratch.
