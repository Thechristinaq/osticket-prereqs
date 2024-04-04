<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Heidi SQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Step 1: Create A Virtual Machine in Azure
- Step 2: Install/Enable IIS in Windows 
- Step 3: Install Files
- Step 4: Configure Extensions
- Step 5: Setup osTicket in the browser
- Step 6: Install HeidiSQL

<h2>Installation Steps</h2>

Step 1: 
<br> - Create a Virtual Machine in Azure with Windows 10 (22H2)
<br> - Using the Start menu, type "Remote Desktop Connection" and connect into the VM using the public IP address

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/feb464ce-7a0b-4513-acfd-a5c1606df949)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/f5fb7401-30de-4d32-8299-437f8e863206)


Step 2: Install/Enable IIS in Windows
<br> - Inside the VM, go to the start menu, control panel, programs, and in the programs and features, click turn windows features on or off
<br> - Inside the popup, you will check and double click Internet Information Services, check and double click Web Managment Tools, check IIS Management Console, check and double click World Wide Web Services, check and double click Application Development Features and check CGI, you will also Check and double click Common HTTP Features and check all six folders, press ok 
<br> - To check If you had did everything correctly, head over to your web broswer and in the search bar, type 127.0.0.1 and a IIS web portal will appear 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/44e9d665-7120-4622-9a19-ce2c3cc2fbf2)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/50c63b46-b022-44d6-a11a-1a45853bccd8)


Step 3: Install Files
<br> We will now install some files to set up our osTicking system, you can find these files by using google and downloading the files 
<br> 
