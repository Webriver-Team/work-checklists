# Setup local for existing project

## First step - Making a Local site

Firstly you will need a Local site onto which you will replicate the live site by placing files and things of live site.[ Click here for that checklist](../01_a_setting_up_local_host_new_project/README.md)

## Second Step - Replicating live site to Local

- First goto your live site wp-admin page and click on Plugins=>Add new![Add new plugin](2020-02-25-18-28-14.png)
- Then search for "wp file manager" and install the one by author "mndpsingh287" ![WP file manager](2020-02-25-18-30-53.png)
- Now click on "Wp file manager" to open it's page. ![Open Wp file manager](2020-02-25-18-32-15.png)
- Navigate to wp-content folder ![](2020-02-25-18-33-24.png)
- Download these three folder by right click and download option.![](2020-02-25-20-31-26.png)
  - Plugins
  - Uploads
  - Themes/Project-Theme
- Open your Local and goto the site's respective folder for files and empty these folder. ![](2020-02-25-18-37-33.png)
  - Plugins
  - Uploads
  - Themes/Project-Theme
- Go to current theme directory and extract the downloaded ZIP files into respective folders.
  - Plugins
  - Uploads
  - Theme
- Now go to your Local site's wp-admin
- Go to Add new plugin page.
- Search for "WP Migrate DB" by author "Delicious Brains" and install it. ![](2020-02-25-18-43-06.png)
- Open you Local site=> Tools => Migrate DB and copy these two values. ![](2020-02-25-18-46-04.png)
  - URL
  - File Path
- Go to live websites=>Tools=>Migrate DB ![](2020-02-25-18-44-30.png)
- Now paste the values you earlier copied, to these input fields respectively.
  - Url => Url
  - File Path => File Path
- Now uncheck these two checkboxes. ![](2020-02-25-18-55-35.png)
  - Export File -> Compress file with gzip
  - Advanced Options ->  Replace GUIDs
- <span id="sqldump-download"></span> Click on Export button at bottom and wait for the SQL file to be downloaded. ![](2020-02-25-18-58-03.png)
- Go to Local and click on Database tab on your site. Then click on "Open Adminer" to open your SQL database table.![](2020-02-25-19-48-01.png)
- If the page opens up normally then go ahead. If there is an error please [goto this link](#local-adminer-error) for further steps. Else follow the steps below.

<span id="local-adminer-fine"></span>

## If the Local Adminer works fine Go Ahead with these setps

- Open the Local Adminer for that specific site by clicking on the site. Then starting the site. Then Database tab for that site and finally clicking on Open Adminer.![](2020-02-25-21-12-04.png)
- The database for that site opens up. Click the checkbox that selects all tables. Now select "Drop Table" at bottom to drop the tables.![](2020-02-25-21-15-16.png)
- Now click on import in left top sidebar.
- Click to upload the SQL file downloaded  [here](#sqldump-download) and click execute to import that SQL file into this database.![](2020-02-25-21-17-04.png)
- Upon getting the confirmation message you are good to go [open the site](#local-open-site).


<span id="local-adminer-error"></span>

## Incase Local Adminer doesn't opens up correclty

- Use this process if you get an error like this.![](2020-02-25-21-08-47.png)
- If yes then continue else [go here](#local-adminer-fine).
- Install software named TablePlus ![](2020-02-25-20-02-53.png)
- Open the software
- Click on "Create a new connection" and select "MySQL". ![](2020-02-25-20-04-20.png)
- Now fillup the opened window of TablePlus from respective values of Local Adminer values. Then test the connection. ![](2020-02-25-20-10-47.png)
- By clicking on Connect and a new window will open up that will display all tables of the Local site.![](2020-02-25-20-12-59.png)
- Now select all tables. Then right click on them and select "Delete". Press OK to confirm. Now press "Ctrl + S" to save the changes to database. ![](2020-02-25-20-14-27.png)
- Now right click in sidebar. Then select Import->From SQL Dump. Now select the file download early from live site [see above](#sqldump-download). Click on import to complete the process.![](2020-02-25-20-16-03.png)

<span id="local-open-site"></span>

## The live site had been copied to Local site

- Just open up your Local and select the site. By clicking View site you will be able to see the site that is now replica of live site.![](2020-02-25-20-55-09.png)
