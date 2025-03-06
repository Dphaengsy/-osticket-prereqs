# -osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

Azure Virtual Machine

Osticket Installation files

Heidi SQL


<h2>Installation Steps</h2>


![image](https://github.com/user-attachments/assets/92e6adac-3350-4da7-bbf4-70cdc9ff74f4)












Create a VM named osticket-vm, put it in a resource group called Osticket. Use Window 10 Pro image for the VM, with 2vCPUs






![image](https://github.com/user-attachments/assets/e601dcd6-3d13-4ccb-b80d-26bde64f0dc2)





















Access Remote Desktop protocol. Copy the Public IP address in the azure portal for the VM and use it to establish the RDP connection.




![image](https://github.com/user-attachments/assets/72c96f26-e137-4327-9699-fdae54203dcc)











Once connected to the VM, enable IIS by opening the Control Panel and navigating to Turn Windows Features On or Off. Scroll down to locate Internet Information Services (IIS) and select the checkbox to activate it. Then Select World Wide Web Services > Application Development Features > enable CGI



![image](https://github.com/user-attachments/assets/773922bd-2db1-4dce-8eff-4ceb1c7c4783)







From the osTicket Installation folder, locate and install PHP Manager to proceed with the setup and Within the same folder, install the Rewrite Module to continue configuring the environment.



![image](https://github.com/user-attachments/assets/1205b38a-f563-4f90-9ecf-56e51fa02b31)







Open File Explorer and create a new folder at C:\PHP. Then Download PHP 7.3.8 and unzip the files into the C:\PHP directory.



![image](https://github.com/user-attachments/assets/5cb0e2a0-2fe5-43e1-ad2f-092e9aea5e2f)






Install VC_redist.x86.exe from the osTicket Installation folder to ensure the necessary Visual C++ Redistributable components are in place.





![image](https://github.com/user-attachments/assets/0bbd1878-7beb-4dff-bcde-fdab61f77ccb)






Install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the osTicket Installation folder to set up the MySQL database server. During installation, select Typical Setup.





![image](https://github.com/user-attachments/assets/abde5830-3387-4b88-b638-99e686c10a9b)





Open IIS mananger as an Admin. Register PHP within IIS by configuring the necessary settings. Afterward, restart the server by selecting Stop and Start.







![image](https://github.com/user-attachments/assets/b8d38684-cb42-468c-9d9e-4265c9478635)








Inside the osTicket folder, unzip the osTicket and copy the upload folder to C:\inetpub\wwwroot. Then, within C:\inetpub\wwwroot, rename the upload folder to osTicket.




![image](https://github.com/user-attachments/assets/b1d85dd9-d3bc-4ef4-b409-49f8afa79076)





Reload IIS after that go into IIS manager  to sites -> Default -> osTicket. On the right click Browse :80
Enable the necessary PHP extensions by navigating to Sites -> Default -> osTicket, then double-click PHP Manager. Select "Disable or enable an extension" and enable php_intl.dll, php_opcache.dll, and php_imap.dll





![image](https://github.com/user-attachments/assets/e406e98d-65bc-4230-bb34-aa409dc4f250)






Download and install HeidiSQL from the osTicket installation files, after that creat a new session on HeidiSQL and connect to the session and create a database named osTicket.


In the osTicket browser setup page, input the database information from HeidiSQL, and fill out all required fields





![image](https://github.com/user-attachments/assets/aa072e1b-fae1-4747-867e-7fff4fb84bf8)



