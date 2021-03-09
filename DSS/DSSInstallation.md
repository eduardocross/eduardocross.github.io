---
title: DataGate&#174; for SQL Server Installation

Id: DSSInstallation
TocParent: Welcome
TocOrder: 20

keywords: ASNA DataGate
keywords: ASNA DataGate&#174; for SQL Server
keywords: DSS Installation
keywords: Installing DSS
keywords: DataGate&#174; Installation
keywords: How to install DSS

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# Installation

---

## Installation Notes

### Preparing to Install DataGate&#174; for SQL Server

#### Meet System Requirements
To run **DataGate&#174; 16.0 for SQL Server** you must have certain hardware and software installed on your computer. 

#### The system requirements include: 

- Windows Server 2012 R2, 2014, or 2014 R2; Windows 7, Windows 8 Pro, or Windows 10 Pro
- TCP/IP with TCP port 5042 enabled/allowed in firewall
- You must be signed on with Administrative privileges in order to start the DataGate&#174; Service and to license both products
- At least 500 MB free disk space

DataGate&#174; 16.0 for SQL Server also requires that either Microsoft SQL Server 2012 R2 or later be installed, configured and running. Note that Microsoft SQL Server 2005-2012 are no longer supported by this or future versions of DataGate&#174; for SQL Server. 

### Review installation options

#### <u>Before</u> installing ASNA DataGate&#174; 16.0 for SQL Server, consider the following: 

- Ensure that Microsoft for SQL Server has been installed, or install Microsoft for SQL Server. Refer to Microsoft SQL Server documentation for further information.
- Be sure the computer meets the **system requirements**  for DataGate&#174; 16.0 for SQL Server. For more information, see System Requirements.
- Verify that the respective **Microsoft SQL Server Service**  for each Instance is started, 
	and that the Auto-start service when OS starts is selected.
- Review the Installation Instructions for installing DataGate&#174; 16.0 for SQL Server and be prepared to make the appropriate selections when running Setup.
- Read the Release Notes section in this document, or on the 
	<a href="http://devnet.asna.com/">ASNA Developer Network</a> site or DataGate&#174; for SQL Server for the latest on product issues, as well as known fixes, known bugs, etc.

### Installing DataGate&#174; 16.0 for SQL Server
DataGate&#174; for SQL Server (DSS) is also installed with the **AVR 16.0** and **Windows Deployment** installations.&#160; However, to install DSS on a system that does not have AVR, you can install from the Developer Network Downloads page.&#160; 

When installing DataGate&#174; for SQL Server, you should be signed on with **Administrative Privileges** to start the DataGate&#174; Service. If you are not signed on with Administrative Privileges, a Warning will display – stating that you need to have Administrative privileges to start the DataGate&#174; Service. Therefore, you may want to check with your Network Administrator prior to installing to ensure you have Administrative privileges. 

#### To Install from ASNA Developer Network (DevNet) 

1. Go to <a href="http://devnet.asna.com" style="color: #524D52; text-decoration: underline;">http://devnet.asna.com</a>.
2. Click on 
        <a href="http://devnet.asna.com/login.aspx?ReturnUrl=/_layouts/Authenticate.aspx?Source=%2Flogin%2Easpx%3FReturnUrl%3D%252fdownloads%252f%5Flayouts%252fAuthenticate%2Easpx%253fSource%253d%25252fdownloads%25252fPages%25252fAVR81%2" style="color: #524D52; text-decoration: underline; text-underline: single">
            Sign In</a> link on the top right corner and sign in to your DevNet account, or select
	    <a href="http://devnet.asna.com/CreateAccount.aspx" style="color: #524D52; text-decoration: underline;">
	        Create an Account</a> on the left to create a new account.
3. Once you are signed in, click on the <a href="http://devnet.asna.com/downloads/Pages/default.aspx" style="color: #524D52; text-decoration: underline;">Downloads</a> link at the top.
4. Scroll down and select the 16.0 product and version you wish to download.
5. On the next screen, the list of products in the product suite selected will display for you to select from.
6. Select the product to install.&#160;The Release Notes for that product will display.&#160; 
        In the right hand corner &quot;Downloads&quot; window, you will see the list of products available based on your sign in.&#160; 
        Select the icon of the product to install.&#160; The installation exe will display for you to **Run**  now, 
        or **Save**  to your system and install later.

#### Silent Installation
To set up a silent installation, you must download the Mobile RPG package or otherwise have it available on your Windows machine or network.

Then, in a command prompt, enter the path to the folder where the AVR installation package is saved followed by Setup.exe, using the following syntax:
<pre>ASNA.Setup.exe [options] </pre>

The following options are required for silent installation:
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-s&#160;&#160;&#160;&#160;&#160;&#160; Run the installation with no user interface.</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-a&#160;&#160;&#160;&#160;&#160;&#160; Accept the ASNA Software License Agreement (required to run in silent 
		mode)</span> </span>
Other available installation options are:
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-?&#160;&#160;&#160;&#160;&#160;&#160; 
		Displays the command line usage dialog. -f&#160;&#160;&#160;&#160;&#160;&#160; Full: Install all components.</span> </span> <br />

 <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-c&#160;&#160;&#160;&#160;&#160;&#160; Core: Install required components.</span> </span> <br />

 <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-o&#160;&#160;&#160;&#160;&#160;&#160; 
		Optional: Install required and optional components.</span> </span> <br />

 <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-h&#160;&#160;&#160;&#160;&#160;&#160; 
		Help: Install required and help components.</span> </span> <br />
 <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-netfx45 
		.NET Fx 4.5: Install .NET Framework 4.5 Support if present on machine.</span> </span> <br />
 <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-np&#160;&#160;&#160;&#160;&#160; Do 
		not prompt the user to reboot if Reboot is required.</span> </span>
**Note:** Multiple installation options may be used.
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">Ex. 
		\&quot;ASNA.Setup.exe -s -a -o -netfx45\&quot; will install the required components, 
		optional components, and .NET 4.5 Support.</span> </span>
To repair an installation from the command line:
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-r&#160;&#160;&#160;&#160;&#160;&#160; 
		Repair the installation.</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">Will 
		repair all features that are installed and have not previously been 
		upgraded by another product.</span> </span>
To uninstall from the command line:
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">-u&#160;&#160;&#160;&#160;&#160;&#160; 
		Uninstall the product.</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt;">Will 
		remove all features that are part of the product package, are not 
		permanent (ASNA Services for example is permanent, so will not be 
		uninstalled), and are not shared with other ASNA products that are 
		currently installed on the machine.</span> </span>

###  Enabling SQL Database(s) to be used as <code>QTEMP</code> Library 
The DataGate&#174; for SQL Server dialogs ( **Stored Procedures** ) display during the installation of DataGate&#174; for SQL Server and when selecting the Stored Procedures option.&#160; It allows you to select a SQL Server instance and connect to SQL Server.&#160; You can set security information, as well as specify a SQL database to be used as a QTEMP library. <br /> Additionally, these dialogs allow users to update, repair, or remove the ASNA Stored procedures through the same dialog tree. 

*Note that after DSS is installed, you can access this dialog at any time from **Start - Programs - ASNA .NET Product Suite - DataGate&#174; 16.0 for SQL Server - ASNA DataGate&#174; 16.0 for SQL Server Stored Procedures** .* 

####  To Install SQL Server Instance(s) 

7. Select the Install Option on the Action Selection dialog

            <li class="LongList" > **Instance Selection:** <ul class="NoBullets">
                    <li class="LongList">The left (Available Instances) column displays the list of currently running, 
					available, named SQL Server instances on your system. The right (Selected Instances) column 
					contains those instances ASNA's Stored Procedures will be installed on.
8. Select instances then click on the arrow to the right to move them into the
					Selected Instances column. Alternately, clicking the double-right chevron (&gt;&gt;) 
					 will shift all instances into the Selected Column.
9. Click **Next**  when done to move on to the next page

</li>
10. **Settings**
11. <code> **QTEMP** </code>

12. This section lets users enable the QTEMP database, and specify a name for
					it (you will be warned if a database with the chosen name already exists).

13. **SQL Credentials**

14. This section lets users choose whether to access the instance(s) with a
					trusted connection, and if not, to enter credentials to use.

</ul>
    </li>

