<h1>Home Folders</h1>

<h2>Description</h2>
In this lab we're going to create roaming Profiles in Windows Active Directory. Roaming profile allows users to logon to any computer in their organization and have all their personal files and setting apply to that computer. 
<br />


<h2>Environments Used </h2>

- <b>Active Directory</b> 

- <b>File Explorer</b>
  
- <b>Server Manager</b> 

<h2>Walk-through:</h2>
<br />
Create a folder named “RoamingProfile” on your C: drive  <br/>
<img src="https://i.imgur.com/YcQQTAe.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Right-click the folder you created and scroll down its menu. Click “Properties”. <br/>
<img src="https://i.imgur.com/0EH7Kai.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open the sharing tab and click “Advanced Sharing”. <br/>
<img src="https://i.imgur.com/nmyPt0k.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
