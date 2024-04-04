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
- Step 3: Install Files (has a 7 step process)
- Step 4: Configure Extensions
- Step 5: Renaming and Assigning Permissions
- Step 6: Setup osTicket in the browser and install HeidiSQL


<h2>Installation Steps</h2>

Step 1: 
- Create a Virtual Machine in Azure with Windows 10 (22H2)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/feb464ce-7a0b-4513-acfd-a5c1606df949)

- Using the Start menu, type "Remote Desktop Connection" and connect into the VM using the public IP address

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/f5fb7401-30de-4d32-8299-437f8e863206)


Step 2: Install/Enable IIS in Windows
- Inside the VM, go to the start menu, control panel, programs, and in the programs and features, click turn windows features on or off
- Inside the popup, you will check and double click Internet Information Services, check and double click Web Managment Tools, check IIS Management Console, check and double click World Wide Web Services, check and double click Application Development Features and check CGI, you will also Check and double click Common HTTP Features and check all six folders, press ok 
 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/44e9d665-7120-4622-9a19-ce2c3cc2fbf2)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/50c63b46-b022-44d6-a11a-1a45853bccd8)

- To check If you had did everything correctly, head over to your web broswer and in the search bar, type 127.0.0.1 and a IIS web portal will appear
  
![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/b699f4a9-4fb7-4637-b97c-325d219c19bf)


Step 3: Install Files (has a 7 step process) 
- We will now install some files to set up our osTicking system, you can find these files by using google and downloading the files (there will be 8 steps in this portion)
- 1st, download and install PHP Manager for IIS (PHPManagerForIIA_V1.5.0.msi) (I have already installed the PHP Manager, follow the prompt for installation)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/02f7fc6a-4cca-4e83-8c21-2f7a9ddc862b)

- 2nd, download and install Rewrite Module (reweire_amd64_en-US.msi) (I have already installed the Rewrite Module, follow the prompt for installation)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/4d34600e-f4c3-4338-bcb8-f6549c032cfb)

- 3rd, create a folder called PHP in the C drive and download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86) and unzip the contents into the PHP folder that we created

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/270cc768-0075-4b88-9e40-4eb30ce939ab)
 
- 4th, download and install VC redist.x86.exe

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/19eb71c9-5390-4e47-99d7-9e587f0580e8)
 
- 5th, download and install MySQL 5.5.62 (mysql-5.5.62-win32.ms1), click typical setup and install, launch the configuration wizard, click standard configuration, enter a password that you will remember for the root password, click next and execute

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/8aa7a18b-2252-48f8-a24b-026398022f9e)

- 6th, in the start menu, type and open IIS as an admin by right clicking the application and selecting run as administrator, once inside click the PHP manager, register new PHP version, browse for the PHP file in the C drive that we had created in the 3rd step, then click php-cgi. return to the home page after and restart the server (it is a good idea to restart the server when you make changes in the IIS manager)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/5602dc37-527b-4c55-95df-45538b69fa4b)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/fe6ca64e-37a6-471b-be62-90b292cff8f0)

- 7th, download the osTicket v1.15.8 file, once downloaded, right click on the folder and click extract all into the wwwroot folder, after the files have been extracted, return to the wwwroot folder and change the upload file name to "osTicket" 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/b5e72eb5-17f0-4584-83dd-cbec3f1e4e54)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/c98d7f0a-60e0-4055-8fa6-8c2a7830be00)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/9e93655d-e9b5-413c-ac8e-d51a39301d8e)

Step 4: Configure Extensions
- In the IIS manager, restart the server, click Sites, Default Web Site, osTicket, double click PHP manager and then click Enable or disable an extention under PHP Extensions
- Within PHP extentions, scroll down and enable "php_imap.dll, php_intl.dll, and php_opcache.dll and then restart the server in the home page after this changes
- Click on Sites, Default Web Site, osTicket, and click on Browse *:80 (http), you will see the osTicket Installer page If everything has been installed and configured ok so far 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/41df97e0-59dc-4ec8-b33e-909763a2bdc0)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/09039dec-7f15-441a-842f-e39cee387092)


Step 5: Renaming and Assigning Permissions
- In the C folder, click inetpub, wwwroot, osTicket, include, scroll down to ost-sampleconfig.php, change it to ost-config.php (delete the word sample)

 ![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/5d27b5df-337d-4f0f-bf1a-0391130b4711)

- Once you have changed the name, right click into ost-config.php, click properties, advanced, disable inheritence, remove all inherited permissions from this object

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/63849632-b7c9-4c9f-bcfc-af07876bca68)

- In the same window, click add, select a principle, type everyone, click check names and ok, check all the boxes and click ok, apply, then ok 

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/bcaf516e-2318-4b75-8c48-20a93a460ed4)


Step 6: Setup osTicket in the browser and install HeidiSQL
- Return to the osTicket Installer webpage and click ok, fill in the information until you get to the Database Settings section
![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/d6315935-049f-4f88-8612-9b37108c4d01)
- Download and install HeidiSQL (HeidiSQL_12.3.0.6589_Setup), open HeidiSQL, click new, session in root folder, type the username and password and click ok
![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/34a8d757-dd37-411d-9f9d-0edafc40b4de)
- Right click on the left side portion, click create new. database, name it osTicket and use the information to set up the Database Settings section on the osTicket installer webpage, once finished, click install now

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/afee915c-d6be-47cb-9b2a-0abe6bcc7e6d)

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/8eaef088-0361-451b-a23d-6de7d5995bf7)

- In the web browser search bar, type http://localhost/osTicket/scp/login.php and log in with your credentials

![image](https://github.com/thechristinaq/osTicket---Prerequisites-and-Installation/assets/165831241/1097c021-9d19-45c5-8f12-bfbffeceea63)

- Congratulations, hopefully it was installed with no errors!!
