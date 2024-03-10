<h1>Home Folders</h1>

<h2>Description</h2>
In this lab we're going to create  user home directory on the server and assign home directory to users in the domain.
 
<br />


<h2>Environments Used </h2>

- <b>Windows 10</b> 

<br />
Create a folder named “Public” on your C: drive  <br/>
<img src="https://i.imgur.com/tn8tAJd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We will now share the folder and allow any member of the group “Domain Users” to use it.
Right-click the “Public” folder, select “Properties,” and click the “Sharing” tab. Then click the “Advanced Sharing…” button. <br/>
<img src="https://i.imgur.com/IkzS9Fs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Tick the “Share this folder” check box, verify that “Public” is the “Share name:” and click the “Permissions” button.
Select “Everyone” in the “Groups or user names:” text box, then click the “Remove” button. <br/>
<img src="https://i.imgur.com/Hw5SdEI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next, click the “Add…” button. Enter “Domain” into the “Enter the object names to select (examples):” text box, then click the “Check Names” button.
Select the “Domain Users” group from the “Matching names:” list and click “OK” <br/>
<img src="https://i.imgur.com/QZWJJB7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click the “OK” button on the “Select Users, Computers, Service Accounts, or Groups” dialog box. <br/>
<img src="https://i.imgur.com/kernPkJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the “Full Control” check box in the “Permissions for Domain Users” section of the “Permissions for Public” dialog box. Then click the “OK” button.
<img src="https://i.imgur.com/ERGNFyp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click the “OK” button on the “Advanced Sharing” dialog box.
<img src="https://i.imgur.com/m0RkRIH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
To complete this configuration, click the “Close” button on the “Public Properties” dialog box.
<img src="https://i.imgur.com/qi84nAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Mapping the shared “Public” folder to all the domain end-users 
<img src="https://i.imgur.com/qonM6lV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Use the “End Users” Query  to select the users that will get a roaming profile. Right-click and scroll down the menu. Click “Properties”.
<img src="https://i.imgur.com/dKWRQgC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open the “Profile” tab and check the “Profile Path” text box. Enter the path \\Server1\RoamingProfile\%username% and click “OK”
Note: %username% is a system variable. It will translate to the various user names when the user’s Roaming folder is created.
<img src="https://i.imgur.com/d7P2cMc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once the Desktop is displayed, open the “RoamingProfile” folder. If you can see a new folder with the user name followed by a ‘.V6’ the roaming profiles are working and the user will have access to their environment and Desktop regardless of what computer they use, as long as that computer is registered on the domain. 
<img src="https://i.imgur.com/58lapz0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Allow “Full Control” by checking the checkboxes and click “Apply”. Click “OK”.
<img src="https://i.imgur.com/GVEK8be.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Copy the “Network Path” (\\Server1\RoamingProfile) of this folder and click “Close”
<img src="https://i.imgur.com/ErYQK0k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open “Server manager dashboard” and click “Tools”. Scroll down the menu and click “Active Directory Users and Computers”.
<img src="https://i.imgur.com/sGywZzg.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Use the “End Users” Query  to select the users that will get a roaming profile. Right-click and scroll down the menu. Click “Properties”.
<img src="https://i.imgur.com/uXUXtaA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open the “Profile” tab and check the “Profile Path” text box. Enter the path \\Server1\RoamingProfile\%username% and click “OK”
Note: %username% is a system variable. It will translate to the various user names when the user’s Roaming folder is created.
<img src="https://i.imgur.com/inS6lUM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once the Desktop is displayed, open the “RoamingProfile” folder. If you can see a new folder with the user name followed by a ‘.V6’ the roaming profiles are working and the user will have access to their environment and Desktop regardless of what computer they use, as long as that computer is registered on the domain. 
<img src="https://i.imgur.com/ykQwTtA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />




