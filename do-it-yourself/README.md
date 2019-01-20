# Building a Tableau connector to Acumatica from Scratch
The following explains how one can import data from Acumatica Generic Inquires (GIs) into Tableau Desktop. As an example, the procedure will import AR-Invoice and Memos data into Tableau. <br/><br/>
System requirements: Acumatica v2018 R2 and Tableau Desktop 2018.3. However, these instructions are the same (or very similar) even with other Acumatica and Tableau versions. <br/><br/>
A) Setting up Acumatica to render data via OData to external applications like Tableau: 
1. Log in to your Acumatica portal and find Generic Inquiry. There are two main paths: 1) More Items > Configuration > Customization > Generic Inquiry. 2) System > Customization > Generic Inquiry. 
2. Click the search icon in the Inquiry Title box, find "AR-Invoices and Memos", and double-click on it.
3. Be sure "Expose via OData" checkbox is checked. If not, check it and click the Save icon. 
4. Do the same procedure above for other GIs that you want to import to Tableau.<br/><br/>
B) Setting up Tableau Desktop to import data from Acumatica. 
1. etc
