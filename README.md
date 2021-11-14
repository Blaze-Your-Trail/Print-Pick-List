# Print-Pick-List - Allows user to send an email with case records to use as a pick list 
Create 3 custom labels in sandbox for ContactID (18 digit), EmailTemplateID (15 digit so drop the 2F), EmailTemplateFolderID (Folder Name)
Create an OUtbound Change Set with the Controller, Test, Visual Force Page and the three custom labels and the List View Button
You need to create one Contact to email all the pick lists to in order to print them - something like orders@. this needs to be created in both sandbox and production (for testing)
