<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<hr />

# osTicket - Prerequisites and Installation

## Installation Steps

### 1. Create an Azure Virtual Machine Windows 10, 4 vCPUs

<p>Provisioning an Azure Virtual Machine with Windows 10 and 4 virtual CPUs provides the necessary compute resources to host the osTicket application and its dependencies in the cloud.</p>

<br />

<p>
  <img width="811" alt="image" src="https://github.com/user-attachments/assets/abab3da0-df14-4ed6-af2a-863a2c2ba102" />
</p>

<hr />

### 2. Log into the VM with Remote Desktop

<p>Remote Desktop Connection allows secure access to the newly created Azure Virtual Machine, enabling you to manage and configure the server environment.</p>
<br />
<p>Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”. We will use the files in this folder to install osTicket and some of the dependencies.</p>

<hr />

### 3. Install / Enable IIS in Windows WITH CGI

<p>
  Internet Information Services (IIS) is Microsoft's web server. Enabling it with the Common Gateway Interface (CGI) feature is necessary to allow the web server to execute dynamic content, such as PHP scripts, which osTicket relies on.
</p>
<br />

- IIS comes built in with the Windows Operating System (client side).
- Can be enabled from the Control Panel -> Programs -> Programs and Features -> Internet Information Services -> 
    World Wide Web Services -> Application Development Features -> [X] CGI
<p>
  <img width="829" alt="image" src="https://github.com/user-attachments/assets/fcf8fe46-a312-4765-bb60-31e226add0f3" />
</p>
<p>
  <img width="798" alt="image" src="https://github.com/user-attachments/assets/2c224f68-6c59-49da-9c24-6a2795b4e66e" />
</p>
<p>
  <img width="1154" alt="image" src="https://github.com/user-attachments/assets/cc901606-ea2b-42ed-9a85-eca13ce18ce4" />
</p>

<p>Enabling IIS transforms the Windows client operating system into a functional web server, capable of hosting web applications.</p>
<br />
<hr />

### 4. Install PHP Manager for IIS

<p>PHP Manager for IIS is an extension that provides a user-friendly interface within the IIS Manager to manage PHP installations, settings, and extensions. osTicket is written in PHP, so this manager simplifies its configuration within IIS.</p>
<br />
<p>
  From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<p>
  <img width="920" alt="image" src="https://github.com/user-attachments/assets/22eea359-f60d-4934-a6b5-2f93b74541f3" />
</p>
<p>
  <img width="849" alt="image" src="https://github.com/user-attachments/assets/6fdc31fc-5065-4a61-b363-5824ebbcf87e" />
</p>
<p>From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi). The URL Rewrite Module for IIS allows you to create custom URL rewriting rules to improve SEO and provide user-friendly URLs for your web applications.</p>
<br />
<hr />

### 5. Create the directory C:\PHP

<p>Creating a dedicated directory for PHP installation helps in organizing the server file system and makes it easier to manage PHP-related files.<br /></p>
<p>
  <img width="406" alt="image" src="https://github.com/user-attachments/assets/99f310bc-8ba8-4365-98ca-c08b1168ae2e" />
</p>
<hr />

### 6. From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

<p>Extracting the PHP 7.3.8 files into the C:\PHP directory makes the PHP interpreter and its associated libraries accessible to IIS, allowing it to process PHP code.</p>
<br />
<hr />

### 7. From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe

<p>The Visual C++ Redistributable package installs runtime components of Visual C++ libraries required for running applications developed with Visual C++. PHP for Windows often depends on these libraries.</p>
<br />
<hr />

### 8. From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

<p>Installing MySQL Server provides the database management system that osTicket will use to store its data, such as tickets, user information, and configurations</p>
<br />
- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
- Username: root
- Password: root
<p>Installing MySQL on the same VM means that the client is now running both a web server (IIS) and a database server (MySQL) simultaneously. This is common in smaller deployments or development environments.</p>
<br />
<hr />

### 9. Open IIS as an Admin

<p>Running IIS Manager as an administrator ensures that you have the necessary privileges to make configuration changes to the web server.</p>
<br />
<p>
  <img width="402" alt="image" src="https://github.com/user-attachments/assets/b3707c74-724c-43c6-b0a2-e597cfffd2c2" />
</p>
<p>IIS Manager provides a graphical interface for configuring and managing your IIS web server, similar in functionality to cPanel in Apache environments.</p>
<br />
<hr />

### 10. Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

<p>Registering the PHP executable (php-cgi.exe) with IIS through PHP Manager tells the web server how to process PHP files. This step links IIS with your PHP installation.<br /></p>
<p>
  <img width="1181" alt="image" src="https://github.com/user-attachments/assets/15ac6b87-e840-4618-9193-9ac6587d6990" />
</p>
<hr />

### 11. Reload IIS (Open IIS, Stop and Start the server)

<p>Restarting the IIS server after registering PHP ensures that the new configuration is loaded and active.</p>
<br />
<hr />

### 12. Install osTicket v1.15.8

<p>This step involves deploying the osTicket application files to the web server's document root, making them accessible through the web browser.</p>
<br />
<p>From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”. Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”.</p>
<p>Reload IIS (Open IIS, Stop and Start the server)</p>
<p>Go to sites -> Default -> osTicket<br />
On the right, click “Browse *:80”</p>
<p>
  <img width="612" alt="image" src="https://github.com/user-attachments/assets/ec4efb98-af9f-47ff-b545-0aa93e7a65ce" />
</p>
<hr />

### 13. Enable PHP extensions

<p>Enabling specific PHP extensions extends the functionality of PHP, allowing osTicket to utilize features like IMAP for email integration and Intl for internationalization.</p>
<br />
<p>Note that some extensions are not enabled.</p>
<p>Go back to IIS, sites -> Default -> osTicket<br />
Double-click PHP Manager<br />
Click “Enable or disable an extension”<br />
Enable: php_imap.dll<br />
Enable: php_intl.dll<br />
Enable: php_opcache.dll</p>
<p>
  <img width="1181" alt="image" src="https://github.com/user-attachments/assets/4aed4e4a-f61b-4491-95e5-3c2287d589b1" />
</p>
<p>Refresh the osTicket site in your browser to observe the changes after enabling the extensions.</p>
<br />
<hr />

### 14. Rename and Configure osTicket Configuration File

<p>Renaming the sample configuration file and setting appropriate permissions is a crucial step in the osTicket installation process, preparing it for the web-based setup.<br /></p>
<p>Rename: ost-config.php<br />
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php<br />
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<p>Assign Permissions: ost-config.php<br />
Disable inheritance -> Remove All<br />
New Permissions -> Everyone -> All<br />
  - While setting "Everyone" to "Full Control" simplifies the initial setup in a lab environment, it's generally **not recommended** for production systems due to security implications. In a real-world scenario, you would grant more restrictive permissions to the web server's user account.<br /></p>
<p>
  <img width="1080" alt="image" src="https://github.com/user-attachments/assets/8ac88567-2541-4619-bd3a-6e2768125549" />
</p>
<p>
  <img width="783" alt="image" src="https://github.com/user-attachments/assets/525f1c30-4caf-48aa-9a4c-5f34ac2f709b" />
</p>
<p>
  <img width="695" alt="image" src="https://github.com/user-attachments/assets/5b7dafe6-d379-4c00-8419-ae3ac35f34e9" />
</p>
<hr />

### 15. Continue Setting up osTicket in the browser

<p>The web-based setup wizard guides you through the final configuration of osTicket, including database connection details and administrator account creation.<br /></p>
<p>Continue Setting up osTicket in the browser (click Continue)<br />
Name Helpdesk<br />
Default email (receives email from customers)</p>
<hr />

### 16. Install HeidiSQL

<p>HeidiSQL is a free, lightweight MySQL database administration tool that provides a graphical user interface for managing MySQL databases. It simplifies tasks like creating databases and managing database objects.</p>
<br />
<p>From the “osTicket-Installation-Files” folder, install HeidiSQL.</p>
<p>Open Heidi SQL<br />
Create a new session, root/root<br />
Connect to the session<br />
Create a database called “osTicket”</p>
<p>
  <img width="931" alt="image" src="https://github.com/user-attachments/assets/3a61b61f-44e5-43ef-a085-c75592846b77" />
</p>

<p>
  <img width="890" alt="image" src="https://github.com/user-attachments/assets/1c03ea98-b3be-47b2-9579-7776cee58d7d" />
</p>
<hr />

### 17. Continue Setting up osTicket in the browser

<p>Provide the database connection details to the osTicket setup wizard, linking the application to the MySQL database you created.</p>
<br />
<p>Continue Setting up osTicket in the browser<br />
MySQL Database: osTicket<br />
MySQL Username: root<br />
MySQL Password: root<br />
Click “Install Now!”</p>

<hr />

### 18. Success, osTicket is now installed with no errors!

<p>This confirms that the installation process has completed successfully, and osTicket is ready to be used.</p>
<br />
<p>
  <img width="616" alt="image" src="https://github.com/user-attachments/assets/cafd70b6-6011-41d6-b50c-5cd9b6499966" />
</p>
<hr />

### 19. Final Steps and Cleanup

<p>These final steps involve securing your osTicket installation by removing the setup directory and setting appropriate permissions on the configuration file.<br /></p>
<p>Browse to your help desk login page: http://localhost/osTicket/scp/login.php<br /><br />
End Users osTicket URL:<br />
http://localhost/osTicket/<br /><br />
