---
title: Configuring DataGate&#174; for SQL Server

Id: dssInstallConfig
TocParent: dssInstallMain
TocOrder: 15

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Configuring DataGate&#174; for SQL Server

### Configuring TCP/IP on Supported Windows Platforms
*This process assumes that your machine is on a TCP/IP Network. If you are unsure of the type of Network, or do not understand any of the steps, please contact your Network Administrator.* 

You should use automated IP settings (DHCP) whenever possible, for the following reasons: 

- If your location changes, you do not have 
				  to modify your IP settings.
- DHCP is enabled by default.
- Automated IP settings are used for all 
				  connections, and they eliminate the need to configure settings 
				  such as DNS, WINS, and so on.

#### To Configure TCP/IP on Windows Platforms

1. Open Control 
				  Panel (in Windows XP, by selecting **Start – Control 
				  Panel** ).
2. Double-click 
				  the **Network Connections**  Icon to open the 
				  Network settings.
3. Click the 
				  connection you want to configure, and then, under **Network Tasks** , click **Change settings of this 
				  connection** .
4. Do one of the 
				  following:

					  <li>If the connection is a local area connection, on the
 **General**  tab, under **This 
					  connection uses the following items** , click
 **Internet Protocol (TCP/IP)** , and then 
					  click **Properties** .
5. If this is a dial-up, VPN, or incoming connection, 
					  click the **Networking**  tab. In **This 
					  connection uses the following items** , click
 **Internet Protocol (TCP/IP)** , and then 
					  click **Properties** .

</li>
6. Do one of the 
				  following:

- If you want IP settings to be assigned automatically, 
					  click Obtain an IP address automatically, and then click 
					  OK.
7. If you want to specify an IP address or a DNS server 
					  address, do the following:
					  <ol type="a">
						  <li>Click **Use the following IP address** , 
						  and in **IP address** , type the IP 
						  address.
8. Click **Use the following DNS server 
						  addresses** , and in **Preferred DNS 
						  server**  and **Alternate DNS server** , 
						  type the addresses of the primary and secondary DNS 
						  servers.

</li>
				  <li class="LongList" style="MARGIN-LEFT: 0.2in">To configure 
				  DNS, WINS, and IP Settings, click **Advanced** .<br />
				  If these differ from your configuration or you are not sure of 
				  the network configuration, please contact your Network 
				  administrator! </li>
				  <li class="LongList" style="MARGIN-LEFT: 0.2in">Follow the 
				  procedure to **verify that TCP/IP is installed correctly** .
				  </li>
			  </ol>

##  Verifying that TCP/IP is Installed Correctly
To verify that TCP/IP is installed correctly and can communicate with the IBM i, you will need to know the IBM i's TCP/IP address and **Full** domain name. If you do not know, please contact your Network Administrator! 

#### To Verify that TCP/IP is Installed Correctly

9. Open a Command Prompt (in Windows 7  or 8 
				  by typing **CMD**  into the Start Menu search 
				  bar).
10. Type the command **ping**  
				  followed by the TCP/IP address of the IBM i.
11. If TCP/IP is functioning correctly, you 
				  should receive four replies.

## Configuring Support for Terminal Emulation
DataGate&#174; 10.2 introduced support for the execution of interactive programs via a DataGate&#174; connection, the actual handling of the 5250 data stream is part of Monarch and Wings in the form of a browser based terminal emulator. In order for this support to be enabled, the following configuration parameters must be established on the IBM i, these parameters do not affect non Monarch/Wings installations where terminal emulation is not needed. 

- The IBM i Telnet server must be started.
- If the system has a firewall enabled, ensure that 
				  connections on port 23 are accepted from the Loopback address 
				  127.0.0.1.
- The System Value QRMTSIGN should be set to *VERIFY.

## Naming a IBM i Database 

### To Name a IBM i Database For TCP/IP Connectivity

12. Select **DataGate&#174; Explorer**  from the **DataGate**  
				  menu. The DataGate&#174; Explorer tool window will display.
13. Click the **Add New Database Name**  button on the right 
				  side of the toolbar at the top of DataGate&#174; Explorer window (or 
				  alternately, right-click the **Local Database Names**  node 
				  and select **Add New New Database name**  on the context 
				  menu). The New Database Name dialog is displayed, as shown 
				  below.
14. Select primary parameters for the database name, as 
				  explained in the
				  [
				  DataGate&#174; Studio Help](http://devnet.asna.com/documentation/Products/dgStudio/dgHelpHome.html), Database Name Parameters topic.
15. After clicking **OK** , the dialog will close 
				  and the identifier of the new database name will be selected 
				  in edit-mode, under Local Database Names in DataGate&#174; Explorer. 
				  Change the default, "New Database Name", to the identifier you 
				  wish to refer to the database name with.

Enter a "Name" to call the database on your computer. This is the **identifier** you will use to refer to the database in your applications.

Alternatively, selecting the **Database Wizard** from the the **DataGate** menu will begin a series of prompts that will guide you through creating a database name.

##  Configuring Multiple Versions of DataGate&#174; for SQL Server Using TCP/IP 

#### To Configure an Additional DataGate&#174; for SQL Server on the same IBM i using TCP/IP

16. Create a new installation library.
17. Install DataGate&#174; into the newly created 
				  library by following the steps found in the Installation Notes 
				  in the sections entitled **Installing DataGate&#174; for SQL Server 
				  using FTP**  or **Installing DataGate&#174; for SQL Server 
				  using a IBM i CD-ROM drive** .<br /><br />
				  <span class="MsoNormalSmall"> *Note: Make sure to specify an 
				  unused port, a new TCP Service Table Name, and the new Library 
				  specified in Step 1.*  </span>

