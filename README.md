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
<p>
  Once this is set up you can verify this worked by navigating to the IIS site by entering "127.0.0.1" into an internet browser
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/IIS.png"></p>
  If you wish you can also edit the code for this site by opening a notepad as an administrator and open C:\inetpub\wwwroot (view all file) and open the iisstart file, any changes made on this file will edit the ISS homepage.
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/IIS%20editing.png"></p>
</p>

</p>
  Once CGI is installed begin installing PHP Manager and the Rewrite Module from the <a href="https://www.iis.net/downloads">Microsoft Website</a> or directly from the OSTicket documentation noted above.
  <br />
  Create a directory in your C drive for PHP "C:\PHP" and begin installing <a href="https://www.php.net/downloads.php">PHP</a> and unzip the file into the PHP directory.
  <br />
  Download a version of the <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170&utm_source=chatgpt.com">Microsoft Visual C++ Redistributable</a>
  <br />
  Finally you will need to download <a href="https://dev.mysql.com/downloads/installer/">MySQL</a>
</p>

<br />
