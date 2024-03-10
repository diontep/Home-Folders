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
<img src="https://i.imgur.com/T5DG5Xg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
To complete this configuration, click the “Close” button on the “Public Properties” dialog box.
<img src="https://i.imgur.com/m0RkRIH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Mapping the shared “Public” folder to all the domain end-users</h2>

Open “server manager” 🡪 “Dashboard,” and click the “Tools” menu. Scroll down the menu and click “Active Directory Users and Computers.”
<img src="https://i.imgur.com/qi84nAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the “Active Directory Users and Computers” applet, right-click “Saved Queries” and select “New”🡪 ”Query”
<img src="https://i.imgur.com/qonM6lV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Name the New Query “End Users”. You can add a description if you like. Note that the “Query root:” is set to “..\labscholas” which will result in the search being conducted for everything on the domain. You can set this to more specific locations if you are creating a query for something you know resides under a specific OU or location. 
Click the “Define Query..” button to continue. 
<img src="https://i.imgur.com/dKWRQgC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select “Users, Contacts, and Groups” from the “Find” dropdown menu of the “Find Users, Contacts, and Groups” dialog box. Select the “Advanced” tab and click the “Field” button.
<img src="https://i.imgur.com/d7P2cMc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select “User”🡪 ”Logon Name” from the menu.
<img src="https://i.imgur.com/58lapz0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />From the “Condition:” dropdown menu, select “Is (exactly)”. In the “Value:” field, enter “*.*” (star dot star). This is a wildcard. The ‘*’ stands for any string of characters, so we are searching for a logon name that is ‘anything dot anything’; the format we use for our users. Next, click the “Add” button.
<img src="https://i.imgur.com/mXMcEuN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Our search condition was added to the “Condition List:” of the “Find Users, Contacts, and Groups” dialog box. Now click the “OK” button.
<img src="https://i.imgur.com/31ZSD2N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click the “OK” button on the “New Query” dialog box to complete creating the query.
<img src="https://i.imgur.com/Sae8kzs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Our “End Users” query will be displayed under “Saved Queries” and its results, i.e., the list of users, will be displayed in the right pane. As this is saved, we can use this query again at any time.
<img src="https://i.imgur.com/freQlVV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select all the users, right-click, and select “Properties” from the menu.
<img src="https://i.imgur.com/P5HJbSq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the “Profile” tab on the “Properties for Multiple Items” dialog box. Tick the “Home folder” check box, select the “Connect” radio button, select “Q:” for a drive letter, and map it to \\Server1\Public – the UNC of the folder we created and shared earlier on this lab. Then click “OK”
<img src="https://i.imgur.com/BkaJbWO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The following message may be displayed, if so, Click the “OK” button.
<img src="https://i.imgur.com/magWein.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Test the automatic mapping of the folder “Public” to a domain user’s client Win 10 computer.</h2>
Reboot the Win 10 Lab VM, and log in using a domain user created in lab 2.1, such as e.smith – if this is the first time you log in with this user, you will need to set the password, and Windows will take a few minutes to set up.
Launch the “File Explorer” navigate to “This PC”. The “Public (\\Server1) (Q:)” share should be displayed.
<img src="https://i.imgur.com/zIWZGsU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click the “Public (\\Server1) (Q:)” share and create a folder for your user in it.
<img src="https://i.imgur.com/IKugITI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
