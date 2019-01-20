# Building a Tableau connector to Acumatica from Scratch
The following explains how one can import data from Acumatica Generic Inquires (GIs) into Tableau Desktop. As an example, the procedure will import AR-Invoice and Memos data into Tableau. <br/><br/>
System requirements: Acumatica v2018 R2 and Tableau Desktop 2018.3 running on Windows or Mac. However, these instructions are the same (or very similar) to other Acumatica and Tableau versions. <br/><br/>
1. Setting up Acumatica to render data via OData to external applications like Tableau: 
  - Log in to your Acumatica portal and find Generic Inquiry. There are two main paths: 1) More Items > Configuration > Customization > Generic Inquiry. 2) System > Customization > Generic Inquiry. 
  - Click the search icon in the Inquiry Title box, find and double-click on "AR-Invoices and Memos".
  - Be sure the "Expose via OData" checkbox is checked. If not, check it and click the Save icon. 
  - Repeat the steps above for other GIs that you might want to import to Tableau.
  - Important: Find out with your system administrator the OData Feed URL to your Acumatica site. For instance, for an Acumatica portal https://abcorp.acumatica.com, the OData Feed URL might be something like https://abcorp.acumatica.com/odata/abcorp.<br/><br/>
2. Setting up Tableau Desktop to import data from Acumatica. 
- Installing Tableau Desktop: Go to https://www.tableau.com/support/releases and select a Tableau Desktop version to download (we recommend downloading the latest version). Download and run the Tableau installer, follow the prompts to complete the installation. You'll need admin rights to the computer where you're installing Tableau. 
- Run Tableau Desktop, on the left panel, click To a Server > More... > OData.
- On the OData prompt, fill out the Server (Acumatica OData Feed URL - see the last step in section 1 above), select Authentication = Username and Password, and enter your credentials. 
- Note: as of 01/20/2019, Tableau Desktop will fail to connect to Acumatica. a Tableau support case has been opened. 
