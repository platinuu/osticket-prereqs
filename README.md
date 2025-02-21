![image](https://github.com/user-attachments/assets/ece77627-39e6-4375-b672-377e869a8c48)![image](https://github.com/user-attachments/assets/091b75d7-b6b9-4833-b061-a4a5192d77e2)![image](https://github.com/user-attachments/assets/66bdd450-e02b-4165-a8d8-917a069b054f)# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket on the cloud using Azure.<br/>


<h2> Files Used</h2>

- ### [Download](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2>Software & Technologies Used</h2>

- Windows 10
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)

<h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable

<h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br/>
<p>
<h3 align="center">First, start by creating a Resource Group inside Azure.</h3>
<br/>
</p>
<p>
  <img src="https://github.com/user-attachments/assets/34e8e520-b443-49f2-a403-92f81343bf37">
</p>
<p>
<h3 align="center">Then create a Windows 10 Virtual Machine, with 2 to 4 Virtual CPUs. For the username and password, it can be anything as we'll be using this information to remote in with our main computer. When creating the Virtual Machine, allow Azure to create a new Virtual Network (Vnet):</h3>
<br/>
</p>
<p>
	<img src="https://github.com/user-attachments/assets/98ca87c1-6d85-4433-bebc-c543d1e3b304"/>
</p>
<br/>
<br/>
<h3 align="center">Open RDP on your computer and connect to your Virtual Machine that was created in Azure. </h3>
<h3 align="center">If you're on MacOS or Linux, you need to download the RDP app from the AppStore on MacOS or XRDP for Linux. </h3>
<br/>
<p>
	<img src="https://github.com/user-attachments/assets/27248782-52c9-46d9-acff-6aa4d8992d4c"/>
</p>
<br/>
<br/>
<h3 align="center">Now we need to install and enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br/>
<p>
	<img src="https://github.com/user-attachments/assets/22ca3134-8c13-45f8-8f4f-03a302e26e6e"/>
</p>
<br/>
<br/>
<h3 align="center">Find the "Internet Information Services," expand it and then expand the "World Wide Web" tab. Then, expand the Application Developer tab. Finally check the "CGI" button and press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br/>
<p>
  <img src="https://github.com/user-attachments/assets/603304be-9e6a-41f2-afb1-d33569c49eb6"/>
</p>
<br/>
<h3 align="center">Install PHP Manager</h3>
<br/>
<p>
<h3 align="center">Download the PHP manager file, and agree with all the terms.</h3>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br/>
<p>
<h3 align="center">Download the Rewrite Module file, then agree with all the terms and it should be installed.</h3>
<p>
  <img src="https://github.com/user-attachments/assets/ed786db8-97c5-4eda-b16a-ad07210b0fe2"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY IN C:\ CALLED PHP</h3>
<br/>
<p>
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> here</a>, then extract it by going to where you download the file, right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>
  <img src="https://github.com/user-attachments/assets/4a83ca84-9d04-4032-8bef-229c782af0b3"/>
</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, and agree with any terms and agreements and finish installing.
</h3>
<p>
  <img src="https://github.com/user-attachments/assets/2e6f51a1-28a4-4e40-9270-3b753c2cf85d"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, and aree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  <img src="https://github.com/user-attachments/assets/ed94a277-ce9d-40ae-aeb7-52e643e204f2"/>
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder into c:\inetpub\wwwroot:
</p>
	<img src="https://github.com/user-attachments/assets/08615007-c8fb-4b06-82e6-693015801a32" />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/d228ffa0-7129-4837-aabe-38828f3bf860" />
</p>
<br/>
<br/>
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br/>
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/0e9c4c78-6e6a-4a10-8d0a-ec6af73328c5"/>
</p>
<br/>
<br/>
<h3 align="center">Enable Extensions in IIS (Some extensions are not enabled)</h3>
<br/>
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/ed9b7b1b-5c24-4730-9c88-9fab948b9e64" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser</h3>
<br />
<p>
	<img src="https://github.com/user-attachments/assets/ac709f22-1393-48a7-84a2-ecf9c410ad98" />
</p>
<br/>
<br/>
<h3 align="center">Rename</h3>
<br/>
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/778d5cce-ccfb-4cf8-853c-b1817c50dd10" />
</p>
<br/>
<br/>
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br/>
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/cdba27eb-2611-434e-980b-9e02e12bb307" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/2b47a54d-9bd7-4dae-9cf2-a2576d30d9fb" />
</p>
<p>
	<img src="https://github.com/user-attachments/assets/1a868daf-1a3d-4108-9b3a-2fe524ad0dda" />
</p>
<br/>
<p><i>Note that this shouldn't be done in a professional environment, this is only for testing purposes.</i></p>
<br/>
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://github.com/user-attachments/assets/971c0258-412d-483a-bc79-84bd982af78d" />
</p>
<br/>
<br/>
<h3 align="center">Download and Install HeidiSQL</h3>
<br/>
<p>
	<img src="https://github.com/user-attachments/assets/5fd50502-f41e-471b-bb1b-0cdacd072e23" />
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/43afe95d-8da4-4451-8c79-a26ddfa919d6"/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/f5156010-c96e-42a2-a61f-a8c5e269bbcf" />
</p>
<br/>
<br/>
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br/>
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/e7decd01-819e-4446-a58f-acac51c6d664" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, if everything is correct, then you just successfully installed osTicket with no errors!</hp>
<p>
	<img src="https://github.com/user-attachments/assets/4634d4d7-2e53-4dd3-9653-0408a7a6e043" />
</p>
<br/>
<br/>
<h3 align="center">Clean up</h3>
<br/>
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/c641f643-8934-440a-b160-2e561fff1473" />
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://github.com/user-attachments/assets/bc1fac79-9f3b-4266-bce5-8cf18833cfed" />
</p>
<br/>
<br/>
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<br />
<h3 align="center"> Congrats, you've finished installing osTicket!</h3>
