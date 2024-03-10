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
Right-click the folder you created and scroll down its menu. Click “Properties”. <br/>
<img src="https://i.imgur.com/IkzS9Fs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open the sharing tab and click “Advanced Sharing”. <br/>
<img src="https://i.imgur.com/Hw5SdEI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Check the “Share this Folder” check box and click on “Permissions”  <br/>
<img src="https://i.imgur.com/kOOoQkr.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Choose “Everyone” from “Group or user names:” and click “Remove”. Click “Add”  <br/>
<img src="https://i.imgur.com/exLhsvx.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Search “Authenticated users” using the “Check Names” button and select when found. Then click “OK”
<img src="https://i.imgur.com/yvHU5S7.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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




