# KoboJSON
This reporsitory is created to pull kobo form data using their api to google spreadsheet. It uses json data format while pulling te data while using kobo api.

It will be easy to handle the data collected at koboform. As we know spreadsheet has wide range of flexibility on caring and sharing options between multiple users to share data and analyse with each other.

Anyways!

First step, it is to get the api url from your project which you deployed at kobo server to collect data.
[https://support.kobotoolbox.org/api.html]

As mentioned in the above link, how to get token API token from your account.
OR
Select ACCOUNT SETTINGS (from where you normally log out), then there you see an optio for api token and press the eye like button beside those asterisk to view your Token. 

Second step,
Login into kobo account from where you will like to pull data,
[https://kc.humanitarianresponse.info/api/v1/data]
Go to above link, there are two buttons, one is OPTIONS, and another one is GET, both are in blue color.

When you will click on GET button, you will get list of file formats (json, jsonp, api, xml, csv, xls, xlsx, csv, xml). 

Thats where you will get something back in your hand, wait !!!

Choose json format, and where you will reach at the below link (with some data in JSON format):
[https://kc.humanitarianresponse.info/api/v1/data?format=json]

Ex:
{"id":123456,"id_string":"ldfaskndflnakndkfk","title":"ABCXYZ","description":"As you wish here","url":"https://kc.humanitarianresponse.info/api/v1/data/123456?format=json"}

you will see each project details (id, id_string, title, description, url) within this {}, where url is we need to copy.

CHANGE the url copied from above into this,
[https://kc.humanitarianresponse.info/api/v1/data/123456.json"]

When you click on above link, you will get download option for the selected format.

NOW, we can pull this data into spreadsheet.

Third step,
open any blank spreadsheet, go to TOOLS then select SCRIPT EDITORS.

Add there new script named koboJSON, paste the contents from koboJSON.gs file here.

Three things you will need to edit there, 
1. Add api token [Line 4]
2. Add username of your kobo account [Line 5]
3. Add password of you kobo account [Line 6]

Then select koboFORM() function and click on run.

Go to any cell of any blank sheet, write down,
=koboJSON("https://kc.humanitarianresponse.info/api/v1/data/123456.json")

VOILA!! YOU MADE WONDERS USING KOBO AND SPREADSHEET ! STAY HAPPY, SPREAD HAPPINESS 

~This repository welcomes coders, users, anyone to make it more useful.

***********************************ANURAG ******************************
