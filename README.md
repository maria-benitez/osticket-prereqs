<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This exercise outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<p>
<img width="1094" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/ab159337-f52d-4cfa-9bbe-816709f32209">
</p>
<p>
Created a Virtual Machine running Windows 10 in Azure. I will use this virtual machine to install osTicket.
</p>
<br />

<p>
<img width="1123" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d5b996fb-a588-4ac6-ad4d-159b47751c49">
<img width="1123" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/b3bdd15b-7e4c-470b-955d-9fbc2cf2daf9">
</p>
<p>
In the Virtual Machine, I will enable IIS with CGI and Common HTTP Features and IIS Management Console.
</p>
<br />

<p>
<img width="1122" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/3e6b40f2-0d4e-48b8-98ef-9840ba92f736">
</p>
<p>
Downloading and installing PHP Manager for IIS and the Rewrite Module.
</p>
<br />

<p>
<img width="1122" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/b719365b-537b-4bee-a552-b91c92c515f3">
</p>
Creating the directory C:\PHP.
</p>
<br />

<p>
<img width="1124" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d83f2d78-2f59-4521-962b-cb1f1dd783b7">
</p>
Downloading PHP 7.3.8 and unzipping the contents onto the C:\PHP directory I created.
</p>
<br />

<p>
<img width="1125" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/4f949abd-3291-4a15-ba8d-a126050edd99">
</p>
Downloading and installing VC_redist.x86.exe.
</p>
<br />

<p>
<img width="1125" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/d5f42380-4d98-4127-89d6-519661cefcd6">
</p>
Downloading and installing MySQL 5.5.62.
<p/>
<br />

<p>
<img width="1064" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/48d6634e-2b8c-466e-9166-9d5b5c0d32b2">
</p>
I will now register PHP from within IIS as an Admin using the php-cgi application that was dumped into C:\PHP. Then I will reload IIS.
</p>
<br />

<p>
<img width="1200" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/f13abd57-3390-455e-b69c-6bb0694b5d1e">
</p>
Downloading and installing osTicket v1.15.8. I will then reload IIS once osTicket has been installed.
</p>
<br />

<p>
<img width="1086" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/67c37517-b7c1-4b41-bd6c-e1d1805b1ed3">
</p>
Accessing osTicket Installer through IIS, I noticed some extensions are not enabled. Through the PHP Manager, I will enable these extensions. 
</p>
<br />

<p>
<img width="1434" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/2961589c-901f-4ed6-b77a-976e1772c3b0">
</p>
After enabling these extensions through the PHP manager, I can refresh the browser and observe these changes. 
</p>
<br />

<p>
<img width="1408" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/84a69a4c-e69d-46b2-bf54-4da2a4985bde">
</p>
Renaming ost-sampleconfig.php to ost-config.php.
</p>
<br />

<p>
<img width="763" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/328d1b74-e709-48d4-82e2-c9512aa09558">
</p>
Assigning permissions to ost-config.php. I have disabled inheritance and added new permissions to Everyone allowing full control.
</p>
<br />

<p>
<img width="1231" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/ab58c791-2e84-48d0-96eb-7a38e6f40919">
</p>
I will continue installing osTicket.
</p>
<br />

<p>
<img width="596" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/6aeb6bc1-1789-4ea2-bd64-8e4d5eb141ac">
</p>
Downloading and installing HeidiSQL.
</p>
<br />

<p>
<img width="1429" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/3515bb88-3b63-43ad-b67d-4b7c6a1cf0fd">
</p>
In HeidiSQL I created a new database named 'osTicket' which I then used to finish setting up osTicket in the browser. 
</p>
<br />

<p>
<img width="1432" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/77ca1f08-0f4e-4d7a-b8f9-bb33cc70ccf6">
</p>
Once osTicket is successfully installed, I can open a new browser window and access it through the End User URL.
</p>
<br />

<p>
<img width="885" alt="image" src="https://github.com/maria-benitez/osticket-prereqs/assets/147643771/4a8a6c10-8a52-4df6-bc40-b0eeac43f530">
</p>
 To finish up, I will do some cleanup. This includes deleting C:\inetpub\wwwroot\osTicket\setup and adjusting permissions on C:\inetpub\wwwroot\osTicket\include\ost-config.php to 'Read' only.
 </p>
 <br />

I will then continue to post-installation setup in 'Post-Installation Configuration'.
