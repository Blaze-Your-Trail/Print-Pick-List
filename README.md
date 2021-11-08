# Print-Pick-List
Allows user to send an email with case records to use as a pick list 
Open Controller - Replace the name of the folder that the Classic email templates are saved in line 34
In line 92 - add a Contact ID that you wish to email the print lists to
Check that the Contact ID in production is the same (best to create that before creating the Sandbox)
Line 34 and 41 in the test - please update the Email Template ID
Alternately you can create Custom Labels for the Contact and refer to this in the Controller System.Label.ContactID (given that ContactID was the name we gave the label), the Email Template and the Email Template Folder

