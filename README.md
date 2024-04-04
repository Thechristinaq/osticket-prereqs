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
<br> 1st, download and install PHP Manager for IIS (PHPManagerForIIA_V1.5.0.msi) (I have already installed the PHP Manager, follow the prompt for installation)
<br> 2nd, download and install Rewrite Module (reweire_amd64_en-US.msi) (I have already installed the Rewrite Module, follow the prompt for installation)
<br> 3rd, create a folder called PHP in the C drive 
<br> 4th, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86) and unzip the contents into the PHP folder that we created 
<br> 5th, download and install VC redist.x86.exe 
<br> 6th, download and install MySQL 5.5.62 (mysql-5.5.62-win32.ms1), click typical setup and install, launch the configuration wizard, click standard configuration, enter a password that you will remember for the root password, click next and execute 
<br> 7th, in the start menu, type and open IIS as an admin by right clicking the application and selecting run as administrator 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/02f7fc6a-4cca-4e83-8c21-2f7a9ddc862b)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/4d34600e-f4c3-4338-bcb8-f6549c032cfb)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/270cc768-0075-4b88-9e40-4eb30ce939ab)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/19eb71c9-5390-4e47-99d7-9e587f0580e8)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/a070d939-1735-4915-ae30-a8810f20373e)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/97892a9d-4ad8-47bd-8625-29a9d09f372d)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/5602dc37-527b-4c55-95df-45538b69fa4b)




