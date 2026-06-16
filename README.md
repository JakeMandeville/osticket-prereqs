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

<p>
  After getting set up in your virtual machine Enable IIS using CGI:
    <list><li>From Windows search open the "Turn Windows feautres on or off"</li>
    <li>Open the path Internet Information Servies > World Wide Web Services > Application Development Features > Enable CGI and begin the install.</li></list>
  <p align="center"><img src="https://github.com/JakeMandeville/course-pictures/blob/main/OSTicket/Enable%20IIS%20install%20CGI.png" alt="CGI install placeholder"></p>
</p>
  Once CGI is install begin installing PHP Manager from the <a href="https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10">Microsoft Website</a>
</p>
<br />
