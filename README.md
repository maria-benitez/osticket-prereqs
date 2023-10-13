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

- Windows 10</b> (21H2)

SCREENSHOTS:
1. <img width="1094" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/ab159337-f52d-4cfa-9bbe-816709f32209">
2. <img width="1123" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d5b996fb-a588-4ac6-ad4d-159b47751c49">
3. <img width="1123" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/b3bdd15b-7e4c-470b-955d-9fbc2cf2daf9">
4. <img width="1122" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/3e6b40f2-0d4e-48b8-98ef-9840ba92f736">
5. <img width="1122" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/b719365b-537b-4bee-a552-b91c92c515f3">
6. <img width="1124" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d83f2d78-2f59-4521-962b-cb1f1dd783b7">
7. <img width="1125" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/4f949abd-3291-4a15-ba8d-a126050edd99">
8. <img width="1125" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d5f42380-4d98-4127-89d6-519661cefcd6">
9. <img width="1064" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/48d6634e-2b8c-466e-9166-9d5b5c0d32b2">
10. <img width="1200" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/f13abd57-3390-455e-b69c-6bb0694b5d1e">
11. <img width="1086" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/67c37517-b7c1-4b41-bd6c-e1d1805b1ed3">
12. <img width="1434" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/2961589c-901f-4ed6-b77a-976e1772c3b0">
13. <img width="1408" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/84a69a4c-e69d-46b2-bf54-4da2a4985bde">
14. <img width="763" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/328d1b74-e709-48d4-82e2-c9512aa09558">
15. <img width="1231" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/ab58c791-2e84-48d0-96eb-7a38e6f40919">
16. <img width="596" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/6aeb6bc1-1789-4ea2-bd64-8e4d5eb141ac">
17. <img width="1429" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/3515bb88-3b63-43ad-b67d-4b7c6a1cf0fd">
18. <img width="1432" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/77ca1f08-0f4e-4d7a-b8f9-bb33cc70ccf6">
19. <img width="885" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/4a8a6c10-8a52-4df6-bc40-b0eeac43f530">

STEPS:
1. Created a Virtual Machine running Windows 10 in Azure. I will use this virtual machine to install osTicket. 
2-3. In the Virtual Machine, I will enable IIS with CGI & Common HTTP Features & IIS Management Console.
4. Downloading & installing PHP Manager for IIS & the Rewrite Module.
5. Creating the directory C:\PHP.
6. Downloading PHP 7.3.8 & unzipping the contents onto the C:\PHP directory I created.
7. Downloading & installing VC_redist.x86.exe.
8. Downloading & installing MySQL 5.5.62.
9. I will now register PHP from within IIS as an Admin using the php-cgi application that was dumped into C:\PHP. Then I will reload IIS.
10. Downloading & installing osTicket v1.15.8. I will then reload IIS once osTicket has been installed.
11. Accessing osTicket Installer through IIS, I noticed some extensions are not enabled. Through the PHP Manager, I will enable these extensions. 
12. After enabling these extensions through the PHP manager, I can refresh the browser & observe these changes. 
13. Renaming ost-sampleconfig.php to 
ost-config.php.
14. Assigning permissions to ost-config.php. I have disabled inheritance & added new permissions to Everyone allowing full control.
15. I will continue installing osTicket.
16. Downloading & installing HeidiSQL.
17. In HeidiSQL I created a new database named 'osTicket' which I then used to finish setting up osTicket in the browser. 
18. Once osTicket is successfully installed, I can open a new browser window & access it through the End User URL.
19. To finish up, I will do some cleanup. This includes deleting 
C:\inetpub\wwwroot\osTicket\setup & adjusting permissions on 
C:\inetpub\wwwroot\osTicket\include\ost-config.php to 'Read' only.

I will then continue to post-installation setup in 'Post-Installation Configuration'.
















<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
