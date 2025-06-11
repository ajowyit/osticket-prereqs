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
<p>- Back to the osTicket Installation Files, right-click the (php-7.3.8-nts-Win32-VC15-x86) file and select Extract All...</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT14" src="https://github.com/user-attachments/assets/0efbd85d-8f29-4e54-8ae5-f433053f926a" />
    </td>
    <td>
      <img width="1000" alt="OT15" src="https://github.com/user-attachments/assets/1f354857-d088-408d-a75b-b67e995db66b" />
    </td>
  </tr>
</table>
<p>- Instead of just extracting right away, click Browse, navigate to Windows(C:), and select the new PHP folder we just created.</p>
<p>- Confirm the Destination and click Extract. After its finished, you can open the PHP folder and see all the PHP files we just installed for osTicket.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT16" src="https://github.com/user-attachments/assets/9231bade-a226-4d7d-b1cf-fe8c3b3eaea9" />
    </td>
    <td>
      <img width="1000" alt="OT17" src="https://github.com/user-attachments/assets/47a41d2f-ec6e-4d42-a806-0075137c61e0" />
    </td>
  </tr>
</table>
<p>- Now, back to the osTicket Installation Files and install a couple more files.</p>
<p>- From osTicket-Installation-Files, install the VC Redistributable file (VC_redist.86). Click Yes and let it do it's thing.</p>
<p>- Next, we'll install MySQL 5.5.62. MySQL is a database that osTicket is going to use to store all of our data. The data will be all the user accounts, ticketing information, and everything we do in osTicket. This will all be stored in the database on the backend. </p>
<p>- Download (mysql-5.5.62-win32)</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT18" src="https://github.com/user-attachments/assets/b0e4f2ed-328b-4db6-9ee2-ad2c1f02b72b" />
    </td>
    <td>
      <img width="1000" alt="OT19" src="https://github.com/user-attachments/assets/8cd4289a-ab6e-4e84-893b-0acb823f726e" />
    </td>
  </tr>
</table>
<p>- Run the installer for MySQL. Choose "Typical" for Setup Type and click Next. See Figure 17 </p>
<p>- Once Install is complete, check the box next to "Launch the MySQL Instance Configuration Wizard", and click Finish.</p>
</p>- Click Next to start the configuration wizard.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT20" src="https://github.com/user-attachments/assets/67164ce9-a990-4cf0-8c9e-4fbf926dcce6" />
    </td>
    <td>
      <img width="1000" alt="OT21" src="https://github.com/user-attachments/assets/55f3d36b-e17c-41dc-8fbc-e2d9f41d9f23" />
    </td>
  </tr>
</table>
<p>- Select "Standard Configuration", and click Next. See Figure 19</p>
<p>- We'll leave the next options alone and hit Next as shown in Figure 20.</p>
<br/>

<img width="600" alt="OT22" src="https://github.com/user-attachments/assets/ee7d67a1-c2d8-4be9-af92-45a13a4f972c" />

<p>- Okay, we've done a lot of jumping from folder to folder and changing windows to this point. Stand up, stretch, get something to drink, and maybe a snack so we can get locked in. This next step is beyond SUPER IMPORTANT! Absolutely DO NOT MESS THIS UP! (No Pressure) 😏</p>
<p>- ⚠️ Just type the word ROOT in both boxes. Yes, ROOT in all caps. ⚠️ </p>
<p>- Later on, the username will be root but the password is ROOT. This would be really bad in the real world but we're keeping simple for this project. A ton of people struggled with this part in the lab. The huge issue is we won't know its wrong until the end when osTicket fails to launch. </p>
<p>- Click Next, Execute on the next screen, and then Finish.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT23" src="https://github.com/user-attachments/assets/9713df38-bb52-4b7a-b5ec-1bf21f3302ec" />
    </td>
    <td>
      <img width="1000" alt="OT24" src="https://github.com/user-attachments/assets/8cfd5c58-0513-4465-862b-ca9078059580" />
    </td>
  </tr>
</table>
<p>- Now that the scary part is over, we are going to Register PHP from within IIS. Open IIS as an Admin from the Start Menu.</p>
<p>- In IIS, open PHP Manager by double-clicking the icon.</p>
<p>- Click "Register new PHP version", then click the three dots, and browse to the C drive. Windows(C:). </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT25" src="https://github.com/user-attachments/assets/918df4c8-2c52-4f02-a6c3-9cfa40046631" />
    </td>
    <td>
      <img width="1000" alt="OT26" src="https://github.com/user-attachments/assets/8777aa50-74e6-4c60-b5f7-f9adca31fb95" />
    </td>
  </tr>
</table>
<p>- Select PHP and click Open.</p>
<p>- In PHP, select php-cgi, click Open, and then OK.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT27" src="https://github.com/user-attachments/assets/048674f6-3ed7-42cc-b11b-2610149f683f" />
    </td>
    <td>
      <img width="1000" alt="OT37" src="https://github.com/user-attachments/assets/8a0ef05c-1589-4359-8ac2-a62ab43ad511" />
    </td>
  </tr>
</table>
<p>- We need to reload IIS for the PHP registration to take effect.</p>
<p>- Right-click osTicket-vm in the top-left of IIS and select Stop. You should see a green animation slide across the top bar. </p>
<p>- Give it a couple seconds. Then, right-click osTicket-vm again and select Start. (You can use the Action buttons on the right side of IIS as well).</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT28" src="https://github.com/user-attachments/assets/fb5dfacd-98f9-4cce-bbe9-106cc942c442" />
    </td>
    <td>
      <img width="1000" alt="OT29" src="https://github.com/user-attachments/assets/c377e374-99c6-4d8c-99a0-ba212b3d8fba" />
    </td>
  </tr>
</table>
<p>- Now run back to the osTicket Installation Files folder on the Desktop.🏃‍♂️‍➡️ We need to unzip (osTicket-v1.15.8.zip).</p>
<p>- Right-click osTicket-v1.15.8.zip and select Extract... </p>
<p>- Go ahead and extract the files into the osTicket-Installation-Files folder. You'll notice the new folder at the top. See Figure 28</p>
<br/>

<img width="600" alt="OT30" src="https://github.com/user-attachments/assets/dbd3243f-71e4-4150-b6f0-fa3eeb10bdbf" />

<p>- When it finishes extracting the files, double-click the new osTicket-v1.15.8 folder.</p>
<p>- There will be two folders inside. Scripts and Upload. </p>
<p>- Pause on this folder and move the window to the side for now. We'll be back for this in a couple seconds.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT31" src="https://github.com/user-attachments/assets/d1811c77-75f4-4f00-b2d8-b54b95a42732" />
    </td>
    <td>
      <img width="1000" alt="OT32" src="https://github.com/user-attachments/assets/6c8bb4ae-a65f-45ba-b711-5e0fd7e886b8" />
    </td>
  </tr>
</table>
<p>- Use File Explorer and navigate to the C drive. (Windows(C:).</p>
<p>- Open inetpub. Within inetpub, open wwwroot. </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT33" src="https://github.com/user-attachments/assets/d4928144-2b92-4380-883a-68ca3e5edcc7" />
    </td>
    <td>
      <img width="1000" alt="OT34" src="https://github.com/user-attachments/assets/6d2ea203-60ba-4fb5-9082-1734c954934e" />
    </td>
  </tr>
</table>
<p>- ⚠️ Now, drag the "upload" folder from "osTicket-v1.15.8" folder and drop into the "wwwroot" folder. ⚠️</p>
<p>- DO NOT just copy and paste. I made this mistake during my first run through of the lab and osTicket failed to launch at the end.🤦‍♂️😩  </p>
<p>- Confirm the "upload" folder actually moved from "osTicket-v1.15.8" and into "wwwroot". See Figure 33</p>
<br/>

<img width="600" alt="OT35" src="https://github.com/user-attachments/assets/e44f2551-3c10-47ce-88de-7efc70d636ee" />

<p>- ⚠️ Within "wwwroot", rename "upload" to "osTicket" exactly like in Figure 34. ⚠️ </p>
<p>- This is another area where people stuggled during the lab. So double check before moving on. </p>
<p>- Next, we'll need to reload IIS again. (Stop, Start the web server) From the Start Menu, run IIS as an Admin. Right-click osTicket-vm and click Stop. Wait a couple seconds, then right-click osTicket-vm and click Start. Refer back to Figure 26 and Figure 27 if needed.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" height="350" alt="OT38" src="https://github.com/user-attachments/assets/27d503c2-ef04-4100-b1bf-abf209c1c014" />
    </td>
    <td>
      <img width="1000" alt="OT39" src="https://github.com/user-attachments/assets/e6f78834-d85d-4958-b823-2adfcc5065db" />
    </td>
  </tr>
</table>
<p>- Since we're already in IIS. Lets check our work and attempt to load the osTicket site..</p>
<p>- In IIS on the left side of the screen, under Connections, go in this order:</p> 
 <p> osTicket-vm -> Sites -> Default Web Site -> osticket. (See Figure 35) /p>
<p>- Then on the left side, under Browse Folder, click Browse *:80 (http).</p>
<p>- Well looky there! We did it! Trust me when I say this is a GREAT sign. This means that we've done evrything correct up to this point.🎉 </p>
<p>- Alright, settle down because there's still work to be done. We need to grab some missing extensions before we can party. See Figure 36</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT40" src="https://github.com/user-attachments/assets/a304e8c4-1876-4289-ae04-041c6dd65b68" />
    </td>
    <td>
      <img width="1000" alt="OT41" src="https://github.com/user-attachments/assets/ab2161b6-9cc7-47bc-80da-303396c58671" />
    </td>
  </tr>
</table>
<p>- In IIS, go Sites -> Default Web Site -> osTicket. Double-click PHP. </p>
<p>- Under PHP Extensions, click "Enable or disable an extension". This opens PHP Extensions and will allow us to enable the ones we're missing.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT42" src="https://github.com/user-attachments/assets/577fd5f4-171d-4e7b-8a3b-a2fb330f171b" />
    </td>
    <td>
      <img width="1000" alt="OT43" src="https://github.com/user-attachments/assets/8419caa7-9ee7-410f-a61b-d6bf51f24ccf" />
    </td>
  </tr>
</table>
<p>- Scroll through and locate "php_imap.dll". Select and Enable. </p>
<p>- Scroll some more and locate "php_intl.dll". Select and Enable.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT44" src="https://github.com/user-attachments/assets/abe343fb-2dd3-41c3-8bc0-462075b4b331" />
    </td>
    <td>
      <img width="1000" alt="OT45" src="https://github.com/user-attachments/assets/9ec4be3e-bafc-4381-8618-64774db13552" />
    </td>
  </tr>
</table>
<p>- Last but not least, scroll through and locate "php_opcache.dll". Select and Enable. </p>
<p>- Now, you can simply refresh the browser and observe the new draft picks to the extension team. Fly Eagles Fly! 🦅 🏆 </p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT46" src="https://github.com/user-attachments/assets/ae88f162-18eb-4de5-af66-ad7101d4135c" />
    </td>
    <td>
      <img width="1000" alt="OT47" src="https://github.com/user-attachments/assets/a6049c4b-24dc-43a3-bc37-84fcfaea8459" />
    </td>
  </tr>
</table>
<p>- Next, we need to rename a config file and assign some permissions. </p>
<p>- Use File Explore and navigate this path: Windows(C:) -> inepub -> wwwroot -> osTicket. Open "include".</p>
<p>- Within "include", locate the "ost-sampleconfig.php" file. This is the file we need to rename.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT48" src="https://github.com/user-attachments/assets/3d07decb-060a-448b-b3a4-716ba195266d" />
    </td>
    <td>
      <img width="1000" alt="OT49" src="https://github.com/user-attachments/assets/e64a4ec1-5a1c-44aa-bf11-2d00a0f87578" />
    </td>
  </tr>
</table>
<p>- ⚠️ Rename "ost-sampleconfig.php" to "ost-config.php". ⚠️ Name it exactly like you see in Figure 45. This is another IMPORTANT step in our success later and everybody wants the Pizza Party! Andolini's Pizzeria is straight 🔥 if you're ever in Oklahoma! 😁  </p>
<p>- Now that we got the config file renamed correctly, right-click "ost-config.php" and click Properties.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="396" alt="OT50" src="https://github.com/user-attachments/assets/aec1c679-5b53-42bf-947f-b0794471cc66" />
    </td>
    <td>
      <img width="1000" alt="OT51" src="https://github.com/user-attachments/assets/0dcccb1c-0c7c-4c5e-b285-52036c9386db" />
    </td>
  </tr>
</table>
<p>- We need to assign permissions for osTicket to make changes to this file on the backend.</p>
<p>- In Properties, select the Security tab and click Advanced. </p>
<p>- Click Disable inheritance.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT52" src="https://github.com/user-attachments/assets/cd2bb0a3-b748-4c38-b8ab-248647364007" />
    </td>
    <td>
      <img width="1000" alt="OT53" src="https://github.com/user-attachments/assets/c4b5c83b-22f1-4495-a123-2e0bcd849f89" />
    </td>
  </tr>
</table>
<p>- Select "Remove all inherited permissons from this object". </p>
<p>- Since all the permissions are gone now, click Add.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT54" src="https://github.com/user-attachments/assets/fb69374c-e4a8-4034-b94b-2dcd99b26c92" />
    </td>
    <td>
      <img width="1000" alt="OT55" src="https://github.com/user-attachments/assets/0ce68638-e626-4b4d-81e8-4ecaeb5a2460" />
    </td>
  </tr>
</table>
<p>- Click "Select a principal" and then in the box, type "everyone". This would not a good idea in the real world but its okay for this project. </p>
<p>- Hit "Check Names" and click OK.</p>
<p>- Next, check "Full control" and click OK.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT56" src="https://github.com/user-attachments/assets/e7b45e2e-cc2e-486d-99fa-2cf439909769" />
    </td>
    <td>
      <img width="500" height="450" alt="OT57" src="https://github.com/user-attachments/assets/d48c7a76-2e32-4853-9c73-bcb2285438fa" />
    </td>
  </tr>
</table>
<p>- Review the permission changes we made, confirm your screen looks like Figure 53, hit Apply, and click OK.</p>
<p>- We can see our changes here as well. Click OK.</p>
<br/>

<table>
  <tr>
    <td>
      <img width="1000" alt="OT58" src="https://github.com/user-attachments/assets/cd36a756-1ca5-4e09-b40f-4053312ec347" />
    </td>
    <td>
      <img width="1000" alt="OT59" src="https://github.com/user-attachments/assets/a45d41a6-c605-45a5-8941-ad0afe07ff53" />
    </td>
  </tr>
</table>
<p>- Go back to the osTicket webpage in the browser and click Continue at the bottom of the page. We will finish setting up osTicket here.</p>
<p>- This is your Help Desk to name how you see fit. So do you boo.</p>
<p>- The Default email doesn't have to be a real email. Once you got this filled out, scroll down.</p>
<p>- Put yourself as the Admin User. This email doesn'matter either but it does need to be different from the one above.</p>
<p>- Username: "adminuser" Password: "Password1". Keep it simple and note this information for later. </p>
<p>- Before we fill out the Database Settings, we will need to install one last thing to get this information. </p>
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
<p>- We'll make one final visit to the "osTicket-Installation-Files" on our Desktop and install HeidiSQL.</p>
<p>- HeidiSQL is an application that allows us to make a connection to our database, configure it, and use our Help Desk super powers for the greater good.</p>
<p>- Find the "osTicket-Installation-Files" folder that's buried under the hundreds on windows we've opened so far. 🤣</p>
<p>- Select and download "HeidiSQL_12.3.0.6589_Setup". Agree, click Next, and Install. Make sure "Launch HeidiSQL" is checked, click Finish and Skip.</p>
<p>- Create a new Session Manager. Click +New. Under Settings, User is root and password is ROOT (VERY IMPORTANT). Click Open.</p>
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
<p>- Right-click the dolphin Unamed, select Create new, and click Database.</p>
<p>- ⚠️ Name the database "osTicket".⚠️ This is another IMPORTANT step towards our success. Click OK. See Figure 60</p>
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
<p>- Now back to the browser to complete the Database Settings</p>
<p>- MySQL Database: osTicket - MySQL Username: root - MySQL Password: ROOT</p>
<p>- Click Install Now.</p>
<p>- CONGRATULATIONS! We did it! osTicket has been successfully installed. </p>
<p>- Take note of the URLs on Figure 62. We'll break these down in the next project, but check out the Staff Control Panel. </p>
<br/>

<img width="600" alt="OT66" src="https://github.com/user-attachments/assets/8ab1af80-d866-45ee-9c74-979b0c408f0d" />


<p>- There's just something about riding off into the sunset. Lets take a moment to reflect upon the journey we just embarked.</p>
<br/>

<h2>✅ Conclusion</h2>

<p>This concludes our project. We successfully installed osTicket on our Windows virtual machine! Most companies use some form of a ticketing system in their every day operations. This project gave me the opportunity to experince a sample of what all is required to simply load a web page you might use at work. We'll dive into osTicket and do some post-install configurations in the next project. Don't forget to Stop (turn off) the VMs in Azure. As always, Thank You for your time and viewing this Project. We'll see you on the next one! 😎      
</p>
<br/>

