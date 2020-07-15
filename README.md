# ESX + SXAdmin
Here you can find the ESX package with the addition of my admin tool. Below you will find the 
guide to add all these new features automatically.

#  Guide Step by Step

## 1 - Import SQL
The first step to make this work is to import the SQL file you downloaded. Go to phpmyadmin with xamp and import the file, 
or you can select SQL and copy and paste the content of the file.

## 2 - Adding Resources
Put the contents of the file resources.rar in your resources folder.

## 2 - Call Resources in your server.cfg
Now you just need to open the server.cfg and add these lines below. Your file must look like the server.cfg I left you

```
# Set connection MYSQL-async
set mysql_connection_string "server=localhost;database=essentialmode;userid=root;"
 
# Disable Couchdb from essentialmode
set es_enableCustomData 1
 
# Mysql/Base
start mysql-async
 
#Fix Errors
restart sessionmanager
 
#Base
start es_extended
start esplugin_mysql
start essentialmode
start mysql-async
start es_admin2
start cron


#[ESX]
start esx_menu_default
start esx_menu_dialog
start esx_menu_list
start esx_voice
start esx_sit
start esx_rpchat
start esx_animations
start skinchanger
start esx_skin
start esx_identity
start esx_joblisting
start esx_status
start esx_optionalneeds
start esx_basicneeds
start esx_jail
start esx_customui
start esx_clothestore
start esx_addonaccount
start esx_jobs
start esx_shops
start esx_billing
start esx_society
start esx_datastore
start esx_addoninventory
start esx_policejob
start esx_ambulancejob
start esx_mecanojob

# [SX]
start sx_loadingscreen
start sx_adminmenu
# start sx_accountmanager # For this follow the SXAccountManager tutorial
start sx_admintool

```
