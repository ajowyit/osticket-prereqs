<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>⚠️ Prerequisites</h2>

- [Creating Virtual Machines in the Cloud](https://github.com/ajowyit/creating-virtual-machines)
- [osTicket Installation Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)(For reference purposes. Link to download zip file is below.)
- [osTicket Installation Files](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0)(For reference purposes. Link to download zip file is below.)

<h2>💻 Environments and Technologies</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Windows App (macOS)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL
- osTicket

<h2>👨‍💻 Operating Systems Used </h2>

- macOS Sequoia
- Windows 10</b> (21H2)

<h2>🧰 Installation Steps</h2>

<p>
 <img width="1710" alt="Screenshot 2025-06-09 at 10 54 10 PM" src="https://github.com/user-attachments/assets/840edc0f-da70-4a43-90db-b91669801e53" />
 <img width="1710" alt="Screenshot 2025-06-09 at 10 54 25 PM" src="https://github.com/user-attachments/assets/0bd034a9-8647-446a-bec9-77874c595c6c" />
<img width="1710" alt="Screenshot 2025-06-09 at 10 54 45 PM" src="https://github.com/user-attachments/assets/193b6137-5d54-4fce-b303-5e1c3eb7b4a3" />
</p>
<p>
 - In Azure, create a virtual machine named osTicket-vm. Refer back to this previous project if needed:[Creating Virtual Machines in the Cloud](https://github.com/ajowyit/creating-virtual-machines). Use the same configurations.
</p>
<p>
 - Log into it.
</p>
<p>
 - Open a browser like Microsoft Edge and paste this link to download the .zip file for the osTicket installation files into the browser and press Enter: [osTicket Installation Files](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0) 
</p>
<p>
 Click "Download anyway" 
</p>

 <br/>
<p>
<img width="1380" alt="Screenshot 2025-06-09 at 10 57 22 PM" src="https://github.com/user-attachments/assets/ec55f6ad-ad1d-4503-ac84-084d2b4b3ecb" />
</p>
<p>
 - From Downloads, drag the zip file on to the deskstop.
</p>
<br/>

<table>
  <tr>
    <td>
    <img width="322" alt="Screenshot 2025-06-09 at 10 57 38 PM" src="https://github.com/user-attachments/assets/c3085ec7-5ccb-4ce7-a491-bdfc618213d0" />
    </td>
    <td>
    <img width="616" alt="Screenshot 2025-06-09 at 10 57 46 PM" src="https://github.com/user-attachments/assets/128938d5-1368-489a-bf93-2ea39e58613f" />
    </td>
  </tr>
</table>
<p>
 - Right-click the folder. Click "Extract All..."
</p>
<p>
 - Confirm the correct destination (C:\Users\{username}\Desktop\osTicket-Installation-Files). Click Extract. Make sure the folder is called "osTicket-Installation-Files"</p>
<p>
 - After the folder is finished extracting all the files, you may have to minimize your windows to see it, but there should be an icon for the folder of the actual osTicket installation files on the browser.
</p>
<p>
 - We will use the files in this folder to install osTicket. You can delete the .zip file now it is no longer needed.
</p>
<br/>

<p>
 <img width="786" alt="Screenshot 2025-06-10 at 7 56 50 PM" src="https://github.com/user-attachments/assets/16d3aea6-f079-4ba7-a5b2-547c02f9471c" />
<img width="1125" alt="Screenshot 2025-06-10 at 7 57 16 PM" src="https://github.com/user-attachments/assets/d2af43ba-dcc4-4ac9-bbc2-c1efe24ababd" />
<img width="1127" alt="Screenshot 2025-06-10 at 7 58 49 PM" src="https://github.com/user-attachments/assets/d7afa8f6-4891-45c2-9498-f61423fcca18" />
<img width="906" alt="Screenshot 2025-06-10 at 8 00 17 PM" src="https://github.com/user-attachments/assets/09d78f35-3fea-4002-b3e7-816e4a51ee88" />
</p>
<p>
 - Next we will enable IIS (Internet Information Services) within Windows WITH CGI as well.
</p>
<p>
 - From the Start Menu, open up Control Panel. Under Programs, click "Uninstall a program". This should get you to the "Uninstall or change a program" window. 
</p>
<p>
 - On the left side, click "Turn Windows features on or off". A window will open where we can turn Windows features on or off. It is recommended to expand the window so you can see more.
</p>
<br/>

<p>
<img width="904" alt="Screenshot 2025-06-10 at 8 03 36 PM" src="https://github.com/user-attachments/assets/2c07675a-b8d4-4ac0-ae19-215327b94c76" />
<img width="907" alt="Screenshot 2025-06-10 at 8 05 02 PM" src="https://github.com/user-attachments/assets/e6e90e24-db1b-42f0-87f8-3191d4d75026" />
<img width="1125" alt="Screenshot 2025-06-10 at 8 18 36 PM" src="https://github.com/user-attachments/assets/450f790b-64ea-47f5-acc7-6bac92de686c" />
<img width="1036" alt="Screenshot 2025-06-10 at 8 37 44 PM" src="https://github.com/user-attachments/assets/4d63ee43-ca20-4d34-81ab-d225d9386402" />
</p>


<p>
 - In the Windows Features window, enable Internet Information Services by clicking the box. Then expand it. Then expand World Wide Web Services. Then expand Application Development Features.
</p>
<p>
 - Check the box next to CGI and click OK. Let the install do it's thing and click Finish once it completes. A window may pop up saying that Windows needs to reboot your PC to finish installing the requested changes. Click "Restart Now" to finish installation.
</p>
<p>
 - After restarting, go to the Browser and enter 127.0.0.1(the loopback address).
</p>
<p>
 - The default page will be show that we installed ISS. Without IIS enbled, if we went to 127.0.0.1, the "Hmmm... can't reach this page" message would appear instead. Make sure we are on the Internet Innformation Services Page.
</p>
<br/>

<p>
<img width="1126" alt="Screenshot 2025-06-10 at 8 54 19 PM" src="https://github.com/user-attachments/assets/1c4e58a3-1a65-49ea-8f00-c7fb79ab6990" />

<img width="498" alt="Screenshot 2025-06-10 at 8 55 03 PM" src="https://github.com/user-attachments/assets/c2623165-db08-42d6-93a8-a2c9016e1d9c" />

<img width="497" alt="Screenshot 2025-06-10 at 8 55 10 PM" src="https://github.com/user-attachments/assets/d6f36fe3-2f51-45d8-b86f-b7c6b5d13d77" />


 <img width="500" alt="Screenshot 2025-06-10 at 8 55 17 PM" src="https://github.com/user-attachments/assets/132cb3a5-9550-440e-8dbc-6d2937161c8d" />


</p>
<p>
 - Now, its time to start installing evrything we need for osTicket. We'll start with PHP Manager for IIS. PHP is a backend web server language. OsTicket basically runs on PHP. 
</p>
<p>
 - Open up osTicket installation files folder from the desktop and install PHP Manager for IIS. Double click PHPManagerForIIS_V1.5.0. 
</p>
<p>
 - When the installer window pops up, click "Next", select "I Agree", click "Next", and click "Close" when finished
</p>
<br/>

<p>
<img width="1131" alt="Screenshot 2025-06-10 at 9 03 05 PM" src="https://github.com/user-attachments/assets/b43ad3ee-82b7-48ec-87a2-171814535f45" />

<img width="500" alt="Screenshot 2025-06-10 at 9 03 25 PM" src="https://github.com/user-attachments/assets/d35e8e47-1c64-43e0-949c-913463b27651" />

<img width="497" alt="Screenshot 2025-06-10 at 9 03 55 PM" src="https://github.com/user-attachments/assets/87fbec7d-2684-4618-a64d-21090cf402b0" />

</p>

<p>
 - Next we want to install the Rewrite Module. Double click rewrite_amd64_en-US.msi. Accept the terms in the License Agreement and click "Install" installer window pops up. Then click "Finish" once it's done.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="686" alt="Screenshot 2025-06-11 at 1 03 14 AM" src="https://github.com/user-attachments/assets/c99b1ea6-04e5-4a18-a9a9-9f81c4f8b5dc" />
    </td>
    <td>
      <img width="1126" alt="Screenshot 2025-06-11 at 1 03 50 AM" src="https://github.com/user-attachments/assets/fffbf7f9-7032-42a4-8bbe-2cbc20efcffa" />
    </td>
  </tr>
</table>
<table>
  <tr>
    <td>
      <img width="1126" alt="Screenshot 2025-06-11 at 1 04 38 AM" src="https://github.com/user-attachments/assets/7a9cb069-cc02-44b0-8277-1082588b1847" />
    </td>
    <td>
      <img width="1123" alt="Screenshot 2025-06-11 at 1 04 47 AM" src="https://github.com/user-attachments/assets/810e45e3-3a20-436a-8133-c944344d057e" />
    </td>
  </tr>
</table>
<p>
 - Next we want to create a directory on the C drive called PHP. 
</p>
<p>
 - Open up File Explorer, then vavigate to Windows(C:) and create a new folder named "PHP". 
</p>
<br/>

<p>
 - Next we want to extract the PHP files from the osTicket-Installation-Files into the newly created PHP folder in the C drive.
</p>

<p>
 <img width="1704" alt="Screenshot 2025-06-11 at 1 10 31 AM" src="https://github.com/user-attachments/assets/2569bd9d-a1e5-4da3-a7a0-ff531a1eb271" />
</p>
<p>
 - Open up the osTicket-Installation-Files
</p>

<table>
  <tr>
    <td>
      <img width="789" alt="Screenshot 2025-06-11 at 1 10 55 AM" src="https://github.com/user-attachments/assets/cc6c25f6-8c2a-4d02-b32c-f32f687f441b" />
    </td>
    <td>
     <img width="616" alt="Screenshot 2025-06-11 at 1 11 15 AM" src="https://github.com/user-attachments/assets/94fd768e-ebca-488f-bc41-cd02522e96e3" />
    </td>
  </tr>
</table>
<table>
  <tr>
    <td>
      <img width="842" alt="Screenshot 2025-06-11 at 1 11 40 AM" src="https://github.com/user-attachments/assets/7395c0d2-e5ea-4756-ba17-5730c8cd782e" />
    </td>
    <td>
    <img width="617" alt="Screenshot 2025-06-11 at 1 12 21 AM" src="https://github.com/user-attachments/assets/9185848b-83e4-435b-b894-5186c58ec14b" />
    </td>
  </tr>
</table>
<p>
 - Right click the php zip file(php-7.3.8-nts-Win32-VC15-x86) then click "Extract All..."
</p>
<p>
 - A window will pop up for you to select a destination to extract the files. Click "Browse...". Then click  Windows (C:) on the left and then click the newly created PHP folder. Click "Select Folder". 
</p>
<p>
 - You'll be taken back to the "Select a Destination and Extract Files" window but you will see C:\PHP under "Files will be extracted to this folder". Click "Extract".
</p>
<p>
 <img width="856" alt="Screenshot 2025-06-11 at 1 12 59 AM" src="https://github.com/user-attachments/assets/14134fd2-6667-4416-a5d8-1467cd873af0" />
</p>
<p>
 - Now all of the files we just installed for osTicket should be in your PHP folder inside the Windows (C:) Drive.
</p>
<br/>

<p>
 <img width="791" alt="Screenshot 2025-06-11 at 1 37 47 AM" src="https://github.com/user-attachments/assets/4d4ac426-1a02-4d01-a68d-652ee436a281" />
</p>
<table>
  <tr>
    <td>
     <img width="482" alt="Screenshot 2025-06-11 at 1 38 18 AM" src="https://github.com/user-attachments/assets/4b880dd0-4f1a-4f1b-bcec-69c8bb9c29de" />
    </td>
    <td>
     <img width="482" alt="Screenshot 2025-06-11 at 1 38 58 AM" src="https://github.com/user-attachments/assets/326d79ba-310a-4fc1-bb34-1dc35c277ed1" />
    </td>
  </tr>
</table>
<p>
 - Now, from osTicket-Installation-Files, we want to install the VC Redistributable file (VC_redist.86). Double click it.
</p>
<p>
 - Next, check the box to agree to the license terms and condidions and click "Install". Once done installing close the window.
</p>
<br/>
<table>
  <tr>
    <td>
     <img width="794" alt="Screenshot 2025-06-11 at 1 44 21 AM" src="https://github.com/user-attachments/assets/566cbeec-724c-4e57-b26e-77b8f4b53fa5" />
    </td>
    <td>
     <img width="498" alt="Screenshot 2025-06-11 at 1 44 43 AM" src="https://github.com/user-attachments/assets/9593e2be-e35b-4460-8cf0-816ebb737298" />
    </td>
  </tr>
</table>
<p>
 - Next, we're going to install MySQL 5.5.62. MySQL is a database that osTicket is going to use to store all of our data. The data will be all the user accounts, ticketing information, and everything we do in osTicket. This will all be stored in the database. 
</p>
<p>
 - From osTicket-Installation-Files, Double click mysql-5.5.62-win32. The My SQL Server 5.5 Setup Wizard window should pop up. Click "Next".</p>
<table>
  <tr>
    <td>
     <img width="497" alt="Screenshot 2025-06-11 at 1 44 49 AM" src="https://github.com/user-attachments/assets/70904ca7-f12e-42b6-86d9-b5cef3352e6d" />
    </td>
    <td>
     <img width="500" alt="Screenshot 2025-06-11 at 1 47 45 AM" src="https://github.com/user-attachments/assets/b4a013f4-ec28-4b72-9ef9-4dd516f6b1d1" />
    </td>
  </tr>
</table>
<p>
 - Continue with the installation process. Check the box next to "I accept the terms in the License Agreement." and click "Next"
</p>
<p>
 - When it says "Choose Setup Type", click "Typical" and then click "Next".
</p>
<table>
  <tr>
    <td>
     <img width="498" alt="Screenshot 2025-06-11 at 1 48 00 AM" src="https://github.com/user-attachments/assets/dc337959-42d7-4474-9e81-eea5895600fa" />
    </td>
    <td>
     <img width="497" alt="Screenshot 2025-06-11 at 1 48 37 AM" src="https://github.com/user-attachments/assets/48d86881-de3c-4374-b9a9-ec1529112795" />
    </td>
  </tr>
</table>
<p>
 - When it says Ready to Install, click "Install".
</p>
<p>
 - Make sure there is a check next to "Launch the MySQL Instance Configuration Wizard". We are going to start the configuration wizard now. Click "Finish". The Configuration Wizard window will pop up.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="499" alt="Screenshot 2025-06-11 at 1 49 17 AM" src="https://github.com/user-attachments/assets/9f290ad7-7521-40c7-8dd6-df6cf1efcc25" />
    </td>
    <td>
      <img width="500" alt="Screenshot 2025-06-11 at 1 49 39 AM" src="https://github.com/user-attachments/assets/50992c2f-1613-4682-adee-97bdcd308ee8" />
    </td>
  </tr>
</table>

</p>
- Click "Next" when configuration wizard window pops up.
</p>
<p>
 - Select Standard Configuration and then click "Next >".
</p>
<table>
  <tr>
    <td>
      <img width="500" alt="Screenshot 2025-06-11 at 1 50 13 AM" src="https://github.com/user-attachments/assets/c25c10da-33cf-45ae-8c84-af0037bd374b" />
    </td>
    <td>
     <img width="502" alt="Screenshot 2025-06-11 at 1 52 04 AM" src="https://github.com/user-attachments/assets/218df7b1-d016-4940-a54c-60fee7ff46b8" />
    </td>
  </tr>
</table>
<p>
 - Click "Next".
</p>
<p>
 - For the root password. Use the word "root". This is bad to do in real life but we are making it simple to ensure we don't mess up, as this is very important. Then click "Next >".n
</p>
<table>
  <tr>
    <td>
      <img width="503" alt="Screenshot 2025-06-11 at 1 53 21 AM" src="https://github.com/user-attachments/assets/d3806cfe-b9e0-4894-beca-812830751f88" />
    </td>
    <td>
     <img width="502" alt="Screenshot 2025-06-11 at 1 54 06 AM" src="https://github.com/user-attachments/assets/ecda9d50-14f5-4d62-970d-6611ff7db28b" />
    </td>
  </tr>
</table>
<p>
 - Click "Execute". Next, click "Finish". This concludes the installation of the SQL database.
</p>



<br/>
<table>
  <tr>
    <td>
      <img width="783" alt="Screenshot 2025-06-11 at 2 16 20 AM" src="https://github.com/user-attachments/assets/c29dac65-6539-427a-96ae-c8e0eb1a5aaa" />
    </td>
    <td>
     <img width="1269" alt="Screenshot 2025-06-11 at 2 17 18 AM" src="https://github.com/user-attachments/assets/a5977cef-22f4-48aa-a3fb-60321ad142d5" />
    </td>
  </tr>
</table>

<p>
 - Next, we want to IIS (Internet Information Services as an admin.
</p>

<br/>
<table>
  <tr>
    <td>
      <img width="1269" alt="Screenshot 2025-06-11 at 2 19 38 AM" src="https://github.com/user-attachments/assets/8a4a6de2-c947-44db-ae7f-c55d09ad2f73" />
    </td>
    <td>
     <img width="1269" alt="Screenshot 2025-06-11 at 2 19 52 AM" src="https://github.com/user-attachments/assets/469ec360-905e-4062-9ab0-2e7250e7e3eb" />
    </td>
  </tr>
</table>

<p>
 - Next, we will register PHP from within IIS. This means that we are basically making the webserver aware of PHP's existance on the computer. We are telling it where it is. 
</p>
<p>
 - Click PHP Manager. Once on the PHP Manager page, click "Register new PHP version".
</p>

<table>
  <tr>
    <td>
     <img width="510" alt="Screenshot 2025-06-11 at 2 20 50 AM" src="https://github.com/user-attachments/assets/5e82199b-ea84-4710-a187-5fec62e024a3" />
    </td>
    <td>
      <img width="843" alt="Screenshot 2025-06-11 at 2 22 20 AM" src="https://github.com/user-attachments/assets/937ebd5f-1ad5-4e41-901c-94698526bda3" />
    </td>
  </tr>
</table>
<p>
 - A window to register new PHP version will pop up. Click the button with 3 dots "...".
</p>
<p>
 - Click Windows(C:) on the left, then click the PHP folder then select php-cgi. Click "Open".
</p>
<table>
  <tr>
    <td>
     <img width="508" alt="Screenshot 2025-06-11 at 2 23 43 AM" src="https://github.com/user-attachments/assets/a98d58d5-7fae-4ff8-a61a-3dc91af95c18" />
    </td>
    <td>
    <img width="1269" alt="Screenshot 2025-06-11 at 2 24 12 AM" src="https://github.com/user-attachments/assets/63cbcfb4-3e65-4237-bbe1-1a180f38bb84" />
    </td>
  </tr>
</table>
<p>
 - Click "OK".
</p>
<p>
 - Now Yyu should see the file under PHP Executable.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1270" alt="Screenshot 2025-06-11 at 2 25 10 AM" src="https://github.com/user-attachments/assets/35df33b6-a396-47d8-ba8e-89d3496a81b0" />
    </td>
    <td>
      <img width="1270" alt="Screenshot 2025-06-11 at 2 25 49 AM" src="https://github.com/user-attachments/assets/942dfc56-519e-45cf-aa94-e99934f7e97f" />
    </td>
  </tr>
</table>
<p>
 - Now we need to reload IIS for the PHP registration to take effect by stopping and restarting the web server.</p>
<p>
 - Right-click osTicket-vm in the top-left of IIS and select "Stop". You should see a green animation slide across the top bar. 
</p>
<p>
 - Give it a few seconds. Then, right-click osTicket-vm again and select "Start". (You can also use the Action buttons on the right side of IIS ).
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="856" alt="Screenshot 2025-06-11 at 5 53 39 PM" src="https://github.com/user-attachments/assets/967ecb46-50da-4bdf-a3b5-b12473399b17" />
    </td>
    <td>
      <img width="615" alt="Screenshot 2025-06-11 at 5 54 24 PM" src="https://github.com/user-attachments/assets/3506a303-55da-44ae-925f-5eb93920618e" />
    </td>
  </tr>
</table>

<p>
 - Go back to the osTicket Installation Files folder on the Desktop. We will unzip (osTicket-v1.15.8.zip).
</p>
<p>
 - Right-click osTicket-v1.15.8.zip. Select "Extract All..."
</p>
<p>
 - Extract the files into the osTicket-Installation-Files folder. 
</p>
<br/>

<p>
 <img width="1627" alt="Screenshot 2025-06-11 at 5 58 11 PM" src="https://github.com/user-attachments/assets/339f85ff-f688-4e71-ab67-dba47ff11817" />
</p>

<p>
 - Once the files are done extracting, open new osTicket-v1.15.8 folder.
</p>
<p>
 - There should be two folders inside: Scripts and Upload. 
</p>
<p>
 -  We'll come back to this folder in a bit.
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="857" alt="Screenshot 2025-06-11 at 6 01 04 PM" src="https://github.com/user-attachments/assets/6dbd4b76-64a4-4c40-b9d1-a805baa77c8c" />
    </td>
    <td>
     <img width="855" alt="Screenshot 2025-06-11 at 6 01 28 PM" src="https://github.com/user-attachments/assets/1b008310-3916-41d6-bd96-2461cf27995c" />
    </td>
  </tr>
</table>

<p>
 <img width="858" alt="Screenshot 2025-06-11 at 6 01 49 PM" src="https://github.com/user-attachments/assets/d7d4092e-2669-4865-b612-0636b8e89e45" />
</p>
<p>
 - In File Explorer, navigate to the C drive. (Windows(C:).
</p>
<p>
 - Open inetpub. In inetpub, open wwwroot. 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1625" alt="Screenshot 2025-06-11 at 6 03 27 PM" src="https://github.com/user-attachments/assets/db0d6ffd-5eed-4b98-aec3-632663b51e86" />
    </td>
    <td>
     <img width="1626" alt="Screenshot 2025-06-11 at 6 04 04 PM" src="https://github.com/user-attachments/assets/4ca2e95a-b3f1-488d-ae58-60a36cf9fd19" />
    </td>
  </tr>
</table>

<p>
 - Drag the "upload" folder from the "osTicket-v1.15.8" folder and drop it into the "wwwroot" folder. 
</p>
<p>
 - DO NOT copy and paste.  
</p>
<p>
 - Confirm that the "upload" folder  moved from "osTicket-v1.15.8" and into "wwwroot". 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="858" alt="Screenshot 2025-06-11 at 6 05 06 PM" src="https://github.com/user-attachments/assets/95e0dab2-e15e-4143-ab36-d72c516da2a9" />
    </td>
    <td>
    <img width="858" alt="Screenshot 2025-06-11 at 6 05 30 PM" src="https://github.com/user-attachments/assets/fae11c3d-f0ca-451a-a390-02cce63c2007" />
    </td>
  </tr>
</table>
<p>
 - In "wwwroot", rename "upload" to "osTicket".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1269" alt="Screenshot 2025-06-11 at 6 11 12 PM" src="https://github.com/user-attachments/assets/045312ee-d18d-4f3c-80bf-f00be0a7d45e" />
    </td>
    <td>
    <img width="1268" alt="Screenshot 2025-06-11 at 6 11 44 PM" src="https://github.com/user-attachments/assets/9fa33f43-e99a-46e2-bfc8-bf81a8728499" />
    </td>
  </tr>
</table>
<p>
 - Next, we'll need to reload IIS again. From the Start Menu, run IIS as an Admin. Right-click osTicket-vm and click "Stop". Wait a bit. Right-click osTicket-vm and click "Start". 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1269" alt="Screenshot 2025-06-11 at 6 37 08 PM" src="https://github.com/user-attachments/assets/dc3e63da-138e-44dd-978d-603f1fbe651a" />
    </td>
    <td>
      <img width="1034" alt="Screenshot 2025-06-11 at 6 40 30 PM" src="https://github.com/user-attachments/assets/79ea4522-3e65-4ea2-b98d-77cc8bc5202e" />
    </td>
  </tr>
</table>
<p>
 - Lets check our work and try to load the osTicket site.
</p>
<p>
 - In IIS on the left under Connections: expand osTicket-vm -> expand Sites -> expand Default Web Site -> click osticket.
</p> 
<p>
 - Then under Manage Folder and Browse Folder, click "Browse *:80 (http)".
</p>
<p>
 - If the osTicket site loads up (it should look like anInstaller page that says "Thank You for Choosing osTicket!") in the web browser then that means we have done everything right so far up to now! </p>
<p>
 - We still need to grab some missing extensions.
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="1271" alt="Screenshot 2025-06-12 at 6 48 22 PM" src="https://github.com/user-attachments/assets/7bdd0927-cb7e-4e2f-9b0e-613a3f0e9e7a" />
    </td>
    <td>
      <img width="1267" alt="Screenshot 2025-06-12 at 6 48 57 PM" src="https://github.com/user-attachments/assets/fdc561dd-1111-47de-80e1-ddf1039dcef9" />
    </td>
  </tr>
</table>
<p>
 - In IIS on the left: expand osTicket-vm -> expand Sites -> expand Default Web Site -> select osTicket. Double-click PHP Manager. 
</p>
<p>
 - In PHP Manager, under PHP Extensions, click "Enable or disable an extension". This will let us to enable the extensions we're missing.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1269" alt="Screenshot 2025-06-12 at 6 49 45 PM" src="https://github.com/user-attachments/assets/dc5a9948-927a-4a33-abc7-0dbbe307d613" />
    </td>
    <td>
      <img width="1269" alt="Screenshot 2025-06-12 at 6 50 10 PM" src="https://github.com/user-attachments/assets/b490e594-2e6b-4daa-b19b-ae2c3465fc01" />
    </td>
  </tr>
</table>
<p>
 - Locate "php_imap.dll". Select and Enable. 
</p>
<p>
 - Locate "php_intl.dll". Select and Enable.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1269" alt="Screenshot 2025-06-12 at 6 51 00 PM" src="https://github.com/user-attachments/assets/a93b8682-37ac-4490-a2d2-52b2a15c84d4" />
    </td>
    <td>
      <img width="1038" alt="Screenshot 2025-06-12 at 6 55 35 PM" src="https://github.com/user-attachments/assets/26c00229-29fc-4a41-8050-a63f7ff77f24" />
    </td>
  </tr>
</table>
<p>
 - Locate "php_opcache.dll". Select and Enable.
</p>
<p>
 - Refresh the browser and we can see that we have added the new extensions.
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="887" alt="Screenshot 2025-06-12 at 7 42 36 PM" src="https://github.com/user-attachments/assets/f2d0a9be-9e89-4858-93ea-4071827bf17d" />
    </td>
    <td>
      <img width="890" alt="Screenshot 2025-06-12 at 7 43 37 PM" src="https://github.com/user-attachments/assets/64baac15-b51f-448a-a7fa-61855b95fa69" />
    </td>
  </tr>
</table>
<p>
 - Next we need to rename a config file and assign permissions.
</p>
<p>
 - In File Explore: Windows(C:) -> inepub -> wwwroot -> osTicket -> include. Locate the "ost-sampleconfig.php" file.
</p>
<p>
 - Right click the file and click Rename.
</p>
<br/>

<table>
  <tr>
    <td>
    <img width="885" alt="Screenshot 2025-06-12 at 7 44 13 PM" src="https://github.com/user-attachments/assets/94857d3b-2fa5-4726-bff2-1f525ec149e1" />
    </td>
    <td>
      <img width="885" alt="Screenshot 2025-06-12 at 7 44 25 PM" src="https://github.com/user-attachments/assets/375b7aa5-f0b9-4174-9983-4dfc1296edf4" />
    </td>
  </tr>
</table>
<p>
 - Rename "ost-sampleconfig.php" to "ost-config.php". 
</p>
<p>
 - Once it is renamed correctly, right-click "ost-config.php" and click "Properties".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="364" alt="Screenshot 2025-06-12 at 7 45 00 PM" src="https://github.com/user-attachments/assets/5657f09f-51c3-4e84-a07f-734e1eb0b6e4" />
    </td>
    <td>
      <img width="769" alt="Screenshot 2025-06-12 at 7 45 34 PM" src="https://github.com/user-attachments/assets/c4fecb94-44e3-43fc-9ee5-bc3b8dc14e47" />
    </td>
  </tr>
</table>
<p>
 - We need to assign permissions for osTicket to make changes to this file on the backend.
</p>
<p>
 - In Properties, select the Security tab and click "Advanced". 
</p>
<p>
 - Click "Disable inheritance".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="523" alt="Screenshot 2025-06-12 at 7 46 03 PM" src="https://github.com/user-attachments/assets/f7fe7b16-056d-4caf-ba10-c3ba97ab438b" />
    </td>
    <td>
      <img width="770" alt="Screenshot 2025-06-12 at 7 46 17 PM" src="https://github.com/user-attachments/assets/38ad404b-bc8d-4905-bac6-17108acb3e44" />
    </td>
  </tr>
</table>
<p>
 - A window will pop up asking what you would like to do with the current inherited permisisons. Select "Remove all inherited permissons from this object.". 
</p>
<p>
 - All the permissions are gone now. Click "Add".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="920" alt="Screenshot 2025-06-12 at 7 46 55 PM" src="https://github.com/user-attachments/assets/b2fd7542-1aa7-4682-9a52-c7dc16724aba" />
    </td>
    <td>
      <img width="919" alt="Screenshot 2025-06-12 at 7 47 33 PM" src="https://github.com/user-attachments/assets/1421bba2-3f9d-41b0-b123-a4539708b55d" />
    </td>
  </tr>
</table>
<p>
 - Click "Select a principal". In the box, type "everyone". Click "Check Names". Everyone should now be capitalized and then click "OK". This is not a good idea in the real world but okay forthe purpose of this project. 
</p>
<br/>

<p>
 <img width="918" alt="Screenshot 2025-06-12 at 7 48 19 PM" src="https://github.com/user-attachments/assets/0a76aafc-a331-4955-9fb3-f0239f924a73" />
</p>
<p>
 - Next, check "Full control". Click "OK".
</p>
<br/>

<table>
  <tr>
    <td>
     <img width="770" alt="Screenshot 2025-06-12 at 7 49 07 PM" src="https://github.com/user-attachments/assets/5b879ae7-bcde-441d-92f8-d47d972bd410" />
    </td>
    <td>
      <img width="366" alt="Screenshot 2025-06-12 at 7 50 18 PM" src="https://github.com/user-attachments/assets/84e326be-24d5-423f-b4cf-16c3f6aace6b" />
    </td>
  </tr>
</table>
<p>
 - Review the permission changes we made. Hit "Apply", and click "OK".
</p>
<p>
 - In ost-config.php Properties we can also see our changes. Click "OK".
</p>
<br/>

<p>
 <img width="858" alt="Screenshot 2025-06-12 at 8 28 47 PM" src="https://github.com/user-attachments/assets/bf62765f-adcc-4cbc-97b4-d1a6ecca0795" />
</p>
<p>
 - Go back to the osTicket webpage in the browser. Click Continue at the bottom of the page. We will finish setting up osTicket here.
</p>
<p>
 - You will be taken to a page titled "osTicket Basic Installation". Fill out the System Settings and the Admin User parts of the page. Name your Help Desk how you see fit.</p>
<p>
 - The Default email doesn't need to be a real email. Once it's filled out, scroll down and continue to the Admin User part.
</p>
<p>
 - Put yourself as the Admin User. This email doesn'matter either but it has to be different from the one above.
</p>
<p>
 - Make the username and passwordthe following: Username: "adminuser" Password: "Password1". Let's keep it simple and make a note this information for later. 
</p>
<p>
 - Before we fill out the Database Settings, we need to install one last thing. 
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT60" src="https://github.com/user-attachments/assets/6dc3d06e-30e3-4fa3-956a-dc332b6cac2d" />
    </td>
    <td>
      <img width="1000" alt="OT61" src="https://github.com/user-attachments/assets/6bebe1fa-9e59-4314-a9f4-6ccf7b8c4eed" />
    </td>
  </tr>
</table>
<p>
 - Go back to the "osTicket-Installation-Files" folder on our Desktop. Install HeidiSQL. Double click "HeidiSQL_12.3.0.6589_Setup".</p>
<p>
 - HeidiSQL is an application that lets us to make a connection to our database, and configure it.
</p>
<p>
 - Find the "osTicket-Installation-Files" folder.
</p>
<p>
 - Select and download "HeidiSQL_12.3.0.6589_Setup". Agree, click "Next", and "Install". Make sure "Launch HeidiSQL" is checked, click "Finish and Skip".
</p>
<p>
 - Create a new Session Manager. Click +New. Under Settings, User is root and password is root like we had set up earlier. Click "Open".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT62" src="https://github.com/user-attachments/assets/21120f81-f277-4db9-b013-80712b35c638" />
    </td>
    <td>
      <img width="1000" alt="OT63" src="https://github.com/user-attachments/assets/f57d4bfa-5ae8-4bda-9e1b-01e0e44c75c2" />
    </td>
  </tr>
</table>
<p>
 - Right-click the dolphin Unamed, select "Create new", and click "Database".
</p>
<p>
 - Name the database "osTicket". Click "OK".
</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT64" src="https://github.com/user-attachments/assets/d43b69fc-9119-4b54-a4a3-e8cc672c671b" />
    </td>
    <td>
      <img width="1000" alt="OT65" src="https://github.com/user-attachments/assets/81757509-c7c7-438a-bc28-90ae592bb7ae" />
    </td>
  </tr>
</table>
<p>
 - Go back to the browser.
</p>
<p>
 - MySQL Database: osTicket - MySQL Username: root - MySQL Password: root
</p>
<p>
 - Click "Install Now".
</p>
<p>
 - osTicket has been successfully installed. 
</p>
<p>
 - Take note of the URLs. We'll break these down in the next project. Let's click on the link under "Your Staff Control Panel:" and check out the Staff Control Panel. 
</p>
<br/>

<img width="859" alt="Screenshot 2025-06-12 at 8 41 15 PM" src="https://github.com/user-attachments/assets/895fcf7d-686a-41d0-a66a-0305fd8139b2" />


<h2>✅ Conclusion</h2>

<p>This concludes our project. We successfully installed osTicket on our Windows virtual machine! Most companies use some form of a ticketing system in their every day operations. This project gave me the opportunity to experince a sample of what all is required to simply load a web page you might use at work. We'll dive into osTicket and do some post-install configurations in the next project. Don't forget to Stop (turn off) the VMs in Azure. As always, Thank You for your time and viewing this Project. We'll see you on the next one! 😎      
</p>
<br/>

