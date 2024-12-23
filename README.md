# n8n-htx-onboarding

I have used n8n to create the new employee record in Airtable, where tasks were created in the Todoist app thereafter. The n8n is hosted in the Cloud via Render.

Production URL for users to input new employee details to create new employee account and tasks: https://n8n-ojkl.onrender.com/form/newEmployeeOnboard
<br>
<br>
![image](https://github.com/user-attachments/assets/0ee29827-77df-4a0b-844b-b79816de3f54)
<br>
<br>
![image](https://github.com/user-attachments/assets/89f674ff-a31a-4cf5-9380-4cd4e43d3953)

Record should be created in database which is integrated to Airtable:
<br><br>
![image](https://github.com/user-attachments/assets/cec0275e-75c1-4ae8-8eb0-e56b76d1926f)

As I have chosen the employee onboarding tasks of 'New employee issues (laptop, staff pass, welcome goody bag)', 3 tasks should be created in the Todoist app which was being integrated with: <br><br>
![image](https://github.com/user-attachments/assets/5e077f22-3c37-4cb8-9cc6-d1c4219ba3d0)

Design of the system:<br><br>
![image](https://github.com/user-attachments/assets/fc44ca44-e7c6-4cb2-8cd1-6cd4312f29fc)

<br>
Referring to the image above, the workflow is triggered when a form where the new employee details were keyed in was submitted. I made some edits in the 'Edit Fields' section to take only relevant values from the fields from the form, as well as created a new field called 'Full Name' which is the concatenation of 'First Name' + ' ' + 'Last Name'. After that, I create the record in the Airtable database. After the record is successfully created, I integrate to the 'Todoist' app where 3 tasks were created in the app to notify the users of the 'New employee issues (laptop, staff pass, welcome goody bag)' tasks.

I have created an error workflow which will email to the specified email address of any failures in the workflow mentioned above.
<br><br>
![image](https://github.com/user-attachments/assets/d76174c5-82db-469c-b968-998f657cdb8b)

This is an example of an email that will be received if the workflow fails:<br><br>
![image](https://github.com/user-attachments/assets/02356493-7c58-4ad7-ba7c-e054e9740902)
<br><br>
The email provides details as to at which node the workflow has failed (ie did the workflow fail at creating records in Airtable or at integration to Todoist app) and also the timestamp where the failure occured. With the timestamp, the error log can be easily retrieved.


