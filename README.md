# GeolocationForm-v2
# This repository is an update to my previous [Geolocation Form](https://github.com/geo2004/GeolocationForm).

HTML Form in this code is further improved by adding **capability to upload files in certain Google Drive Folder and some specific functionalities**.  

[Example.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example.html)  is the main form which you can modify at ease.  

[Example2.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example2.html)  is the main form with additional progress bar and complete message once form submission is finished.  

[Example3.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example3.html)  is the main form with additional progress bar and complete message once form submission is finished, and capabilities to upload multiple files and the rest of the form data are duplicated in every row of uploaded file.  

[Example4.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example4.html)  is the main form with additional progress bar and complete message once form submission is finished, and capabilities to upload single image file in any format (JPEG, TIF, PNG, BMP you name it) and inject the captured Geolocation to the EXIF Metadata using [PIEXIFJS](https://piexifjs.readthedocs.io/en/latest/about.html), before uploading the file to Google Drive. 

[ExampleMap.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/ExampleMap.html) is an implementation of real-time (5 minutes reloading time) geospatial visualization of the captured data from the form. I am using Leaflet JS for this implementation, accompanied by Papaparse JS for in-place conversion between CSV to JSON (Google already dropped JSON in the GSheets publishing options). Read the code comment for further explanation about how to implement this code. 

[Example5.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example5.html) is a form like [Example3.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example3.html), only I add a map viewer (using Leaflet JS) for the geolocation information, along with accuracy value obtained from the device's GNSS, so you can confirm if the geolocation is accurate enough before form data submission.

[GAppScript](https://github.com/geo2004/GeolocationForm-v2/blob/main/GAppScript) file is the Google App Script code which has function to send the files to dedicated Google Drive folder, and at the same time send the other form data to Google Sheet document.  

Looks the tutorial in [Geolocation Form](https://github.com/geo2004/GeolocationForm) about how to use the script on your HTML form and GSheet. 


#### Additional notes  
1. This new Google App Script didn't use trigger anymore, so you don't have to set one if you want. However, adding trigger will be useful on debugging the code. 
2. Pay attention to the code screenshot below. **Uploads** is the name of the folder in your Google Drive, modify it if you want to set a different name. 
3. **Sheet1** is the Google Sheet's Sheet Name, change it if the sheet name in your Google Sheet document is different. 
4. The example **[[obj.date, obj.email, obj.identity, obj.description, obj.latitude, obj.longitude, obj.name, link]]** array should exactly match (case sensitive) with the Google Sheet's columns name/headers and "name" HTML element in the HTML form (except the latitude and longitude are using ID element). If you set a different "name" element in the HTML form and GSheets Headers/Columns Name (bottom picture below), modify this array, or else, the code will not works. 
5. [Example.html](https://github.com/geo2004/GeolocationForm-v2/blob/main/Example4.html) in this repo is using eight columns, if you want to add more columns in your form, change the 8 value on this line **sheet.getRange(lr+1, 1, 1, 8)** according to the form columns number.  

![image](https://user-images.githubusercontent.com/46329778/228274474-e7ad08a7-926a-401c-a61f-392ccde50878.png)

![image](https://user-images.githubusercontent.com/46329778/228312477-8ae1ff81-a1bc-40f2-9603-669d34e7021f.png)

