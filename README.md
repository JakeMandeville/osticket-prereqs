<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b>

<h2>List of Prerequisites</h2>
<list>
  <li>Windows Operating System</li>
  <li>Web Server - Internet Information Services</li>
  <li>PHP + PHP Manager</li>
  <li>MySQL</li>
  <li>C++ Redistributable</li>
  <li>Rewrite Module for IIS</li>
  <li>HeidiSQL (optional for database Management)</li>
</list>

<h2>Installation Steps</h2>

<p>Start off by depoloying a Virtual Machine of your choice, for this example <a href="https://azure.microsoft.com/en-us/get-started/azure-portal">Microsoft Azure</a> was used</p>
<h3>Prerequisites</h3>
<p>For a more detailed breakdown of the requirements you can navigate to the <a href="https://docs.osticket.com/en/latest/Getting%20Started/Installation.html#prerequisites">OSTicket documentation</a></p>
<p>
  After getting set up in your virtual machine Enable IIS using CGI:
    <list><li>From Windows search open the "Turn Windows feautres on or off"</li>
    <li>Open the path Internet Information Servies > World Wide Web Services > Application Development Features > Enable CGI and begin the install.</li></list>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/Enable%20IIS%20install%20CGI.png" alt="CGI install placeholder"></p>
<p><list>
  <li>Once this is set up you can verify this worked by navigating to the IIS site by entering "127.0.0.1" into an internet browser</li>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/IIS.png"></p>
  <li>If you wish you can also edit the code for this site by opening a notepad as an administrator and open C:\inetpub\wwwroot (view all file) and open the iisstart file, any changes made on this file will edit the ISS homepage.</li></list>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/IIS%20editing.png"></p>
</p>

</p><list>
  <li>Once CGI is installed begin installing PHP Manager and the Rewrite Module from the <a href="https://www.iis.net/downloads">Microsoft Website</a> or directly from the OSTicket documentation noted above.</li>
  
  <li>Create a directory in your C drive for PHP "C:\PHP" and begin installing <a href="https://www.php.net/downloads.php">PHP</a> and unzip the file into the PHP directory.</li>

  <li>Download a version of the <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170&utm_source=chatgpt.com">Microsoft Visual C++ Redistributable</a></li>

  <li>You will also need to download <a href="https://dev.mysql.com/downloads/installer/">MySQL</a></li>

  <list><li>Open Internet Information Services (IIS) Manager as an Admin</li>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/IIS%20admin.png"></p>
  <li>Open "PHP Manager" and Register a new PHP version and open the "C:\PHP\php-cgi.exe" file.</li>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/set%20up%20PHP.png"></p>
  <li>from the IIS Manager homepage restart your OSTicket server to make sure the PHP manager is properly running.</li>
  
  <li>Finally, you can install the latest version of OSTocket from the <a href="https://docs.osticket.com/en/latest/Getting%20Started/Installation.html">documentation</a></li>
  <li></li>Once OSTicket is installed Unzip the file and copy the "upload" folder into "c:\inetpub\wwwroot" and rename it "osTicket" and restart the IIS server again.</li></list>
<br />
<p>
  Back in IIS navigate to Sites > Default > osTicket and select "Browse *:80 (http) on the right hand side.
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/Set%20up%20osTicket.png"></p>
  To get into osTicket you will need to activate some extensions, back in IIS go to Sites > Default > osTicket and double-click PHP Manager and select "Enable or disable an extension" and enable the following extensions:
  <list><li>Enable: php_imap.dll</li>
  <li>Enable: php_intl.dll</li>
  <li>Enable: php_opcache.dll</li></list>
  Rename the "ost-sampleconfig.php" found in "C:\inetpub\wwwroots\osTicket\include\" to "ost-config.php"
  <br />
  Right click the "ost-config.php" file and open the properties, go to the security tab and select advanced, disable inheritance - then remove all and set new permissions.
</p>

<h2>Setup</h2>
<p>At this point if you go back into OSTicket you should be able to refresh the page anjd start setting up your helpdesk website, creating the name of your helpdesk, getting a URL, and setting up the email and Admin account. 
<br/>
  Next, you will have to get OSTicket set up with your database. <a href="https://www.heidisql.com/download.php">HeidiSQL</a> was used in this instance.
  <br/>
  Upon getting HeidiSQL installed, Create a New session, you will have to sign in using the User and Password set up on the MySQL server and set up a new database named osTicket.
  <img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/HeidiSQL%20osTicket%20DB.png">
  
</p>
