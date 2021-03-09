---
title: Installing DataGate&#174; for SQL Server

Id: dssInstallMain
TocParent: dssGettingStartedMain
TocOrder: 10

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Installing DataGate&#174; for SQL Server

###  Preparing to Install DataGate&#174; for SQL Server

---

**Meet System Requirements** 

To run **DataGate&#174; 16.0 for SQL Server** and **ASNA DataGate&#174; 16.0** you must have certain hardware and software installed on your computer. 

**The system requirements include:** 

- Windows Server 2008 R2, Windows Server 2012, Windows Server 2016, Windows 7, 
					Windows 8 Pro, Windows 10
- TCP/IP with TCP port 5042 enabled/allowed in firewall
- You must be signed on with Administrative privileges in 
					order to start the DataGate&#174; Service and to license both 
					products
- At least 500 MB free disk space

DataGate&#174; 16.0 for SQL Server also requires that either Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 (or both) be installed, configured and running. Note that Micorosoft SQL Server 2005 is no longer supported by this or future versions of DataGate&#174; for SQL Server. 

### <a name="Review_Installation_Options"></a>Review Installation Options

#### <u>Before</u> installing ASNA DataGate&#174; 16.0 for SQL Server, consider the following: 

- Verify that the respective **Microsoft SQL Server 
					Service**  for each Instance is started, and that the 
					Auto-start service when OS starts is selected.
- Review the
					[Licensing DataGate&#174; for SQL Server](http://devnet.asna.com/documentation/Help110/Readmes/DSS_110_Readme.htm#Install_DSS">
					Installation Instructions</a> for installing DataGate&#174; 16.0 for SQL Server and be prepared to make the appropriate 
					selections when running Setup.
- Read the
					<a href="http://devnet.asna.com/documentation/Help110/Readmes/DSS_110_Readme.htm#Release_Notes">
					Release Notes</a> section in this document, or on the
					<a href="http://devnet.asna.com/">ASNA Developer Network</a> 
					site or DataGate&#174; for SQL Server for the latest on product 
					issues, as well as known fixes, known bugs, etc.

---

### Installing DataGate&#174; 16.0 for SQL Server
DataGate&#174; for SQL Server (DSS) is also installed with the **AVR** and **Windows Deployment** installations. However, to install DSS on a system that does not have AVR, you can install from the Developer Network Downloads page. 

When installing DataGate&#174; for SQL Server, you should be signed on with **Administrative Privileges** to start the DataGate&#174; Service. If you are not signed on with Administrative Privileges, a Warning will display – stating that you need to have Administrative privileges to start the DataGate&#174; Service. Therefore, you may want to check with your Network Administrator prior to installing to ensure you have Administrative privileges. 

1. Go to <a href="http://devnet.asna.com/">
				http://devnet.asna.com</a>.
2. Click on
				<a href="http://devnet.asna.com/login.aspx?ReturnUrl=/_layouts/Authenticate.aspx?Source=%2Flogin%2Easpx%3FReturnUrl%3D%252fdownloads%252f%5Flayouts%252fAuthenticate%2Easpx%253fSource%253d%25252fdownloads%25252fPages%25252fAVR81%2">
				Sign In</a> link on the top right corner and sign in to your 
				DevNet account, or select
				<a href="http://devnet.asna.com/CreateAccount.aspx">Create an 
				Account</a> on the left to create a new account.
3. Once you are signed in, click on the
				<a href="http://devnet.asna.com/downloads/Pages/default.aspx">
				Downloads</a> link at the top.
4. Scroll down and select the product 
				and version you wish to download.
5. On the next screen, the list of products 
				in the product suite selected will display for you to select 
				from.
6. Select the product to install. The 
				Release Notes for that product will display. In the right hand 
				corner "Downloads" window, you will see the list of products 
				available based on your sign in. Select the icon of the product 
				to install. The installation exe will display for you to **Run**  
				now, or **Save**  to your system and install later.

### Enabling SQL Database(s) to be used as QTEMP Library 
The DataGate&#174; for SQL Server dialog ( **Stored Procedures** ) displays during the installation of DataGate&#174; for SQL Server and when selecting the Stored Procedures option. It allows you to select a SQL Server instance and connect to SQL Server. You can set security information, as well as specify a SQL database to be used as a QTEMP library. 

*Note that after DSS is installed, you can access this dialog at any time from **Start - Programs - ASNA .NET Product Suite - DataGate&#174; 16.0 for SQL Server - ASNA DataGate&#174; 16.0 for SQL Server Stored Procedures** .* 

#### To Enable SQL Server Instance(s) 

7. Enter or select the following to the SQL Server instance 
				dialog.

					<li> **SQL Server 
					Instance:** <ul>
						<li>This option displays the list of 
						currently running and available named SQL Server 
						instances specified on your system for DataGate&#174; setup.
8. Click on the arrow to the right 
						to change or select another SQL Server Instance (if 
						available).

</li>
9. **Use Trusted 
					Connection:**
10. This option allows you to use 
					integrated Login security to connect with SQL Server.
11. If checked (default), DataGate&#174; will 
					use integrated Login security to connect with SQL Server.
12. If unchecked, you will need to enter 
					a valid Login Name and Password to connect.
13. **Login Name:**
14. This box is disabled if **Use 
					Trusted Connection**  is checked.
15. If enabled, specify a Login Name 
					used to connect to SQL Server.
16. **Password:**
17. This box is disabled if **Use 
					Trusted Connection** is checked.
18. If enabled, specify the Password for 
					the Login Name used to connect to SQL Server.
19. **QTEMP 
					library support:**
20. This option allows you to enable, or 
					specify a SQL database name to be used as the special QTEMP 
					library. **By default, this option will be disabled.**
21. To enable this support, click on the
 **Enable**  button to enable the ability for a SQL 
					database name to be used as the special QTEMP library. When 
					the Enable button is selected, the "SQL Database to be used 
					as QTEMP library" option will be enabled, for you to specify 
					a SQL Database to be used as a QTEMP library.
22. To disable this support (if 
					previously enabled), click on the **Disable**  button. The 
					"SQL Database to be used as QTEMP library" option will be 
					disabled and appear 'dimmed'.
23. **SQL Database to be used as QTEMP 
					library:**
24. This option will only be available 
					if the Enable button has been clicked.
25. Specify the name of a SQL database 
					to be used as the special QTEMP library. The name of the 
					database does not have to be QTEMP, but it will be accessed 
					by DataGate&#174; in response to requests for QTEMP library 
					requests.
26. If the database does not exist, it 
					will be created with default attributes.
27. **Install 
					Button:**
28. Selecting **Install**  will save 
					the entries to the dialog and continue with the 
					installation.
29. *Please note that the Install 
					button will only be enabled when the **Enable**  button is 
					selected.*
30. **Done 
					Button:**
31. Selecting **Done**  indicates you 
					are finished with the dialog, and that you will not specify 
					a SQL Database to be used as a QTEMP library.  The DSS 
					installation will continue.
32. *However, please note that 
					selecting Done while accessing the Stored Procedures dialog 
					from **Start - Programs - ASNA Product Suite - DataGate&#174; 16.0 for SQL Server - ASNA DataGate&#174; 16.0 for SQL Server Stored 
					Procedures**  will display a dialog stating "DataGate&#174; For 
					SQL Server was cancelled or was unable to install properly 
					will display". Select the **OK**  button to 
					close the dialog box.*
33. **Help 
					Button:**
34. Select Help to display the help 
					topic for additional information.
</ul>
				</li>

###  Also in this section
- <a href="dssInstallLicense.html)
- [Configuring DataGate&#174; for SQL Server](dssInstallConfig.html)
- [Troubleshooting DataGate&#174; for SQL Server](dssInstallTroubleshoot.html)
- [Uninstalling DataGate&#174; for SQL Server](dssInstallUninstall.html)
- [Manually Installing DataGate&#174; for SQL Server in a Clustered Environment](dssInstallingCusters.html)

