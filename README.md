# Openprovider-WHMCS-SSL

https://support.openprovider.eu/hc/en-us/articles/26725066143378-WHMCS-SSL-plugin-Installation-configuration-and-management

WHMCS SSL plugin - Installation, configuration and management
Openprovider SSL module allows you to resell our SSL Certificates through your WHMCS website.

Requirements:
1. WHMCS versions - 7.x.x to latest
2. PHP 7.4 or above
3. Openprovider reseller account

How to upload the files?
1. Download the module file. Extract the zip file on your computer.
2. Connect to the server where WHMCS is installed via your web hosting control panel (cPanel/Plesk/Webmin, etc.) or via FTP.
3. Go to the extracted folder “modules/addons/openprovider_ssl” and upload this
folder “openprovider_ssl” into “<WHMCS_ROOT>/modules/
addons/”

4. Inside your WHMCS root directory, go to the folder "crons " and upload the file
"priceSync.php" from extracted zip.

5. Inside your WHMCS installed directory, go to this path "/modules/servers " and upload this
folder "openprovider_ssl" from extracted zip.

 

Configure the addon module
1. Log in to your WHMCS admin area. Go to System Settings >> Find Addon Modules and
click on it.



2. Find the Openprovider SSL Addon module and click the Activate button. And after that click Configure button. Then check Full Administrator permit access to the module and enter product margin and group name. Once done, click the Save Changes button.



3. Now, from WHMCS Admin dashboard, navigate to 'Addons' → 'Openprovider SSL'



4. Go to the API Setting page to enter the API credentials for API connection.

   1. Enter API URL: https://api.openprovider.eu/v1beta 
   2. Enter Username (Openprovider username)
   3. Enter Password (Openprovider password)
   4. Test connection and then Save Setting



5. After adding the API credentials, go to the ”Sync Product” page and click on ”Sync Product”
and then click on ”Create Product” to create all packages in WHMCS.



6. Under ”Logs” admin users can see the all performed actions/module operations. Admins can also delete the logs.



Configure the server module
1. From your WHMCS admin area, go to System Settings >> Servers



2. Click the Add New Server and click on the Go to Advanced Mode button



3. Add the server for API connectivity by entering following details.
  1. Enter a name, for example SSL Server
  2. Enter API URL under Hostname field “api.openprovider.eu”
  3. Select “Module” as Openprovider SSL Certificate module”
  4. Enter “Username” as your Openprovider username
  5. Enter “Password” as Openprovider password



 



6. Make “Test Connection”



7. If everything is fine, then click on “Save Changes” button to save the configuration.

8. After creating the server click on Create New Group, Enter Group name and
assign above created server to that group and save the changes.



Configure the Product with Server Module
1. Go to System Settings >> Products/Services



2. Edit the SSL Products one by one and go to the ”Module Settings“ tab. Select the ”Module Name” as
OpenProvider SSL.



3. Server Group as “SSL Server” group that you created above for API connectivity.

4. After that you will have a configuration section to configure the module. Configure
module by choosing and entering correct information as given below.

  1. Map specific SSL product
  2. Enable “Auto Renew’
  3. Enable “DNS Automation”
  4. Choose “Signature Hash Algorithm”
  5. Choose “Period”
  6. CSR (Optional)
  7. Make auto provision setting
  8. Save Changes



After configuring the module with the product. Go to “System Settings” >> “Configurable Options”
Module will create the configurable group for number of domains. Find that group
and click on edit button.
After that you will get a configurable option “No. Of domains”. Edit this option to
update the price for specific billing cycles and currencies.
Now your product is ready for order.

Manage purchased SSL Certificates
Client Area:

1. Login to your client area
2. Go to “Services >> My Services”
3. Click on purchased SSL certificate.



 



 

Admin Dashboard:

1. Login as your WHMCS admin >> Go to Orders >> List All Orders



2. Click on the SSL order you want to view/check.



 
