# GeolocationForm-v2
# This repository is an update to my previous [Geolocation Form](https://github.com/geo2004/GeolocationForm).

HTML Form in this code is further improved by adding **capability to upload files in certain Google Drive Folder**.  

[Example.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example.html)  is the main form which you can modify at ease.  

[Example2.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example2.html)  is the main form with additional progress bar and complete message once form submission is finished.  

[Example3.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example3.html)  is the main form with additional progress bar and complete message once form submission is finished, and capabilities to upload multiple files and the rest of the form data are duplicated in every row of uploaded file.  

[GAppScript](https://github.com/geo2004/GeolocationForm-v2/GAppScript) file is the Google App Script code which has function to send the files to dedicated Google Drive folder, and at the same time send the other form data to Google Sheet document.  

Looks the tutorial in [Geolocation Form](https://github.com/geo2004/GeolocationForm) about how to use the script on your HTML form and GSheet. 


#### Additional notes  
1. This new Google App Script didn't use trigger anymore, so you don't have to set one if you want. However, adding trigger will be useful on debugging the code. 
2. Pay attention to the code screenshot below. **Uploads** is the name of the folder in your Google Drive, modify it if you want to set a different name. 
3. **Sheet1** is the Google Sheet's Sheet Name, change it if the sheet name in your Google Sheet document is different. 
4. The example **[[obj.date, obj.email, obj.identity, obj.description, obj.latitude, obj.longitude, obj.name, link]]** array should exactly match (case sensitive) with the Google Sheet's columns name/headers and "name" HTML element in the HTML form (except the latitude and longitude are using ID element). If you set a different "name" element in the HTML form and GSheets Headers/Columns Name (bottom picture below), modify this array, or else, the code will not works. 

![image](https://user-images.githubusercontent.com/46329778/228274474-e7ad08a7-926a-401c-a61f-392ccde50878.png)

![image](https://user-images.githubusercontent.com/46329778/228312477-8ae1ff81-a1bc-40f2-9603-669d34e7021f.png)

