# Vitamiinihaku

An app for searching for descriptions of vitamins on Fineli API with search criteria, 

and then have the descriptions received via inputted email.


<b> Technologies used: 

Python, HTML, JavaScript, AWS SES & Lambda & Cloudformation, serverless


<b> How it works:

The user gives their email address and a search criterium (one word) and submits the form. The user is then notified whether 
the action was successful by letting them know they'll be receiving the results via email, or whether an error occurred
in which case the user is prompted to try again.


<b>index.html</b> is the UI with the above mentioned form

<b>handler.py</b> is the python code for searching the API for relevant information and triggering the event to send email to the user,
with data collected from the form. If the search criteria doesn't match anything in the API, the user will be notified per email
in this case as well. Otherwise the description of wanted vitamin will be emailed to the user using AWS SES (Simple Email Service).

<b>serverless.yml</b> is the YML file which defines AWS resources needed for the action and to be deployed.
