# Print-Pick-List - Allows user to send an email with case records to use as a pick list 
ENSURE YOU ARE WORKING IN SANDBOX

**Before you begin:**
Ensure you have a verified email address that can act as the ‘from’ address using the Custom Label.

**Step 1**
Create 1 Contact Record named Order Email DO NOT CHANGE.

**Step 2**
Create 1 Classic Email Template named Print Pick Lists using the formula fields as required. You may like to create a folder that holds only this Email Template.

**Step 3**
Create 4 Custom Labels:
ContactID - Value is the 18 Digit ID of the Contact Record you created above, you get this ID from the URL
EmailTemplateID - Value is the ID of the Email Template you created above,  use the 15 digits after the %2F in the URL
EmailTemplateFolderID - Value is the name of the folder where the email template you created is saved (name, not API)
OrgWideEmailID - Value is any of the verified Organisation-Wide Email addresses setup in your org, written as the email itself, i.e. example@example.com

**Step 4**
Repeat Step 1 above in Production (you will need this in production for the change set to validate successfully on deployment)

**Step 5**
Push the components created in Step 2 and Step 3 to Production

**Step 6**
In the developer console, create a Visualforce Page and name it PrintPickListsFromCase - populate it using the Markup provided in this repository

**Step 7**
In the developer console, create an Apex Class and name it PrintPickListsController - populate it using the Markup provided in this repository

**Step 8**
In the developer console, create an Apex Class and name it PrintPickListsController_Test - populate it using the Markup provided in this repository

**Step 9**
Run all Tests to ensure it passes and that Code Coverage is acceptable (make corrections if required, there may be unique information in your org that means this code needs to be edited to suit)

**Step 10**
Create a List Button on the Case Object and name it Print Pick Lists.  It should Display in existing window with sidebar and the Content Source should be the Visualforce Page that was created in the developer console. The description should be: “Sends the selected cases to request@ as an email for easy printing”.

**Step 11**
Once testing is successful, create an Outbound Change Set and include:
2 x Apex Classes
1 x Visualforce Page
1 x Button
Upload to Production.

**Step 12**
In Production, navigate to Inbound Change Sets to find the change set that was just uploaded and Validate, ensuring you select the option ‘Run Specified Tests’ and input PrintPickListsController_Test into the box.

**Step 13**
Once successfully validated, select Deploy and repeat the option ‘Run Specified Tests’, inputting PrintPickListsController_Test into the box.

**Step 14**
Navigate to the Case Object to add the Print Pick Lists button to the List View Layout.

**Test, test, test.**
