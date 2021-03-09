---
title: Troubleshooting DataGate&#174; for SQL Server

Id: dssInstallTroubleshoot
TocParent: dssInstallMain
TocOrder: 20

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Troubleshooting DataGate&#174; for SQL Server

---

### Troubleshooting IBM i TCP/IP Connectivity
If you are unable to connect to the IBM i database from ASNA's DataGate&#174; Database Manager, the following information may help identify possible incorrect setups on the IBM i.<br /><br />It is assumed that TCP/IP configuration has been completed correctly in Windows. If you are unsure whether TCP/IP is installed or correctly configured in Windows, contact your network administrator for assistance.<br /><br />TCP/IP names are a combination of host names (machine names) and domain names. A machine name for TCP/IP does not have to match the IBM i machine name; however, it will be a unique name - and it can be the same as the IBM i machine name.<br /><br />Throughout this example, the machine name used is 'machine', and the IBM i name is actually 'S1037242'. The domain name used throughout this example is 'domain.com'. Together the machine name and the domain name make a 'complete' TCP/IP name - 'machine.domain.com'. At your site, you should use your own domain name and own machine name.<br /><br />

1. First check to see if you are able to
 **ping**  the IBM i by name from Windows. For 
				  example, if the TCP/IP name of the IBM i is ' **machine.domain.com** ', 
				  then the following command should be issued from your machine 
				  from a Command Prompt:<br /><br /> **ping machine.domain.com** <br />

					  <li>If you do not get a 'reply' from the machine that was 
					  pinged, then TCP/IP may not be configured correctly, 
					  either on your machine or on the IBM i. If you receive a " **Bad 
					  command or filename** " error message when typing 
					  the **ping**  command, your machine may not 
					  have TCP/IP installed. Please check with your network 
					  administrator to make sure your machine has TCP/IP 
					  capability.
2. If you do get a response from the IBM i when the
 **ping**  command is issued, then it is still 
					  possible some settings on the IBM i may be incorrect. From 
					  a command line on the IBM i, issue the following command:
 **cfgtcp**

<br /></li>
3. From the **Configure TCP/IP**  
				  menu screen that appears, select the **Work with TCP/IP 
				  Interfaces**  (option 1).
4. The following menu screen will appear.<br />
				  <br />You should see something similar to this screen. If you do 
				  not, then TCP/IP is probably not configured on the IBM i 
				  properly, or it may not be completely installed. Check with 
				  your IBM i administrator to make sure the IBM i has TCP/IP 
				  installed.<br />
5. If there is an internet address other 
				  than 127.0.0.1 listed, select that address and enter an
 **option 5**  command to display the setting for 
				  that IP address.<br /><br />

					  <li>The **Interface**  status should indicate
 **Active** . If it does not, then the TCP/IP 
					  services, although installed, may not be started, or may 
					  have terminated. The TCP/IP services should be started.
6. Try re-connecting to the IBM i database after 
					  restarting the TCP/IP services. (To start the TCP/IP 
					  services you must have sufficient authority rights and 
					  issue the following command from a menu prompt: **STRTCP** ). After you have done this, then issue 
					  another **ping**  command to see if you get a 
					  reply.

<br /></li>
7. If you reach this point and are still 
				  having problems accessing the IBM i via TCP/IP, then **F12**  back to the main configuration screen for TCP/IP 
				  ( **Configure TCP/IP** ) and enter option 21 ( **Configure 
				  Related Tables** ) from the main TCP/IP configuration 
				  menu.<br /><br />

					  <li>On the **Configure Related 
					  Tables**  menu screen that appears next, select 
					  option 1, **Work with Service Table Entries** . 
					  You will then see the **Work with Service Table 
					  Entries**  menu screen. Scroll through the list of 
					  services to find the **DataGateServer**  
					  entry.
8. If there is no entry here, that is 
					  the problem. Make sure you perform the installation 
					  section for the IBM i as stated earlier in this chapter.
9. If the **DataGateServer**  
					  entry is found, then the default port will be 5042 (unless 
					  it was installed with a different port). It is strongly 
					  suggested to use Port 5042.

<br /><span class="MsoNormalSmall"> ***Note:** The 
				  protocol listed in the service table entry for the 
				  'DataGateServer' service should be ' **tcp** '. It 
				  is case sensitive, so if the letters are uppercase, you will 
				  need to remove the service and re-add the service with lower 
				  case letters.* </span></li>

<div>

### <a name="Troubleshooting_DataGate_Service">Troubleshooting DataGate&#174; Service</a> 
**If you are unable to start the DataGate&#174; Service, the following steps will assist in trouble shooting the possible causes.** <br /><br />When the DataGate&#174; service job is submitted for execution, the job is submitted under the user profile of DG8SVCPRF. This user profile is created during the installation and the system value for the Printer option will be assigned to this user profile. If the DataGate&#174; service job has trouble starting, a one page report outlining the possible cause of the problem will be generated for the user DG8SVCPRF and printed to the assigned printer. This report will not print unless the Output Queue associated with this printer automatically prints the generated reports. Otherwise, to view the list of reports that have not printed for this user, enter the following command:<br /> <br />WRKSPLF SELECT(DG8SVCPRF)<br /><br />At this point you will need to contact ASNA for further assistance.<br /><br />

*The most probable cause for the DataGate&#174; service job not starting is that the current DataGate&#174; service job is terminated with an ENDJOB command, so subsequent attempts to start the service will not be successful.* 

10. If the DataGate&#174; service job is not 
				  currently running and it won't start by issuing the **STRDG8SVR**  command, enter the following command:<br />
				  <pre> NETSTAT </pre>
11. Select **Option 3** . Work 
				  with TCP/IP Connection Status.
12. Select **F14**  to Display 
				  Port Numbers In the Local Port column, locate the Port Number 
				  you assigned as the Port for the DataGate&#174; Service (The default 
				  Port Number is 5042).
13. You will need to end this connection 
				  by selecting **Option 4** .
14. When this connection is ended 
				  successfully, you may now execute the **STRDG8SVR**  
				  command.

<div>

###  <a name="Troubleshooting_a_DataGate_Job_that_is_Not_Terminating"> Troubleshooting a DataGate&#174; Job that is Not Terminating</a> 
If you notice that a DataGate&#174; Job is still running after a client connection is lost, this is due to a TCP/IP feature called "Keep-Alive". Refer to the following to change the system's default Keep-Alive value.<br /><br />Keep-Alive packets are used to probe a connection that has been inactive for a long time. The server initiates a disconnect when the probes do not get through. This means that if the client connection is lost for a prescribed length of time, the server sends a disconnect message to its server job (usually the result of a system crash or power-down).<br /><br />The default Keep-Alive setting for Windows and IBM i is two hours, meaning that a DataGate&#174; thread or DataGate&#174; job would remain active for 2 hours after connection was lost with the client. The 2-hour default may be an unsatisfactory period of time for you, as files would continue to remain open, etc. on an abnormal disconnection until the Keep-Alive time had elapsed. <br /> <br />Refer to the following to modify the server machines' respective Keep-Alive period.<br /><br />

#### IBM i

15. Request the Configure TCP/IP menu by 
				  executing the command: **cfgtcp**
16. Select menu **item 3 - Change 
				  TCP/IP Attributes** .
17. Set TCP/IP Keep-Alive to the **number of minutes**  desired. (Note: 2 to 5 minutes 
				  should work well in most cases).

#### Windows
***WARNING** : Using Registry Editor incorrectly can cause serious, system-wide problems that may require you to reinstall Windows to correct them. Microsoft cannot guarantee that any problems resulting from the use of Registry Editor can be solved. Use this tool at your own risk. The following was derived from Article ID Q120642.* 

#### To Change these parameters, use the following procedure:

18. Run Registry Editor (REGEDT32.EXE or 
				  REGEDIT.EXE).
19. From the HKEY_LOCAL_MACHINE subtree, 
				  go to the following key: <br /> **\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters** 
				  <br /><br />
20. The Value is " **KeepAliveTime** ". 
				  If present (usually not), double click on it to edit in 
				  milliseconds. Otherwise, continue with Step 4.<br />
21. Select " **Edit -&gt; Add Value** ".
22. For Value name, enter **KeepAliveTime** .
23. From the Data Type drop down list, 
				  select **REG_DWORD**
24. Press **OK**
25. In the DWORD Editor dialog, enter the 
				  number of milliseconds. Select the **Radix Decimal**  
				  option.
26. Select **OK** .
27. Enter the Keep-Alive value in 
				  milliseconds; e.g. 5 minutes = 300000 msec.<br /><br />Valid 
				  Range: 1 - 0xFFFFFFFF<br />Default: 7,200,000 (two hours)<br />
				  <br /><span class="MsoNormalSmall"> *The parameter controls how 
				  often TCP attempts to verify that an idle connection is still 
				  intact by sending a Keep-Alive packet. If the remote system is 
				  still reachable and functioning, it will acknowledge the 
				  Keep-Alive transmission. Keep-Alive packets are not sent by 
				  default. This feature may be enabled on a connection by an 
				  application. <br />* </span>
28. After typing in the value, use the 
				  "Data Type" checkbox to set the value type.
29. Select **OK** .
30. Exit the Registry Editor.
31. Reboot the system to make the change 
				  take effect.

<div>

### <a name="Setting_up_a_Subsystem">Setting up a Subsystem</a> 
Basically, to set up a subsystem, you need to have a **routing entry** with a compare value of " **QCMDB** " that runs the program QCMD in **QSYS** .<br /><br />The subsystem that is used for the job queries must be set up with a proper routing entry in order for DataGate&#174; service to start. This routing entry **must run the program QCMD** in Library QSYS and have the compare value of 'QCMDB' or '*ANY'. If the subsystem has one of these routing entries, it may be used for DataGate. 
<div>

### <a name="Troubleshooting_Manually_Ending_Users_Jobs"> Troubleshooting Manually Ending Users Jobs</a> 
If DataGate&#174; is shut down and there are users connected, their jobs will still be out there and you have to manually end them. However, after manually ending the users' jobs, DataGate&#174; may not start for about 5 minutes. It will start the first DG8SVC job and then end it until the 5 minutes (or so) is up.<br /><br />It is likely that OS/400 is not reclaiming the DataGate&#174; TCP/IP port (5042) in a timely manner when the service and connection jobs are ended. When you "manually end" connections to DataGate, it may not have a chance to properly shut down TCP/IP resources. The system typically does not realize that those resources are no longer in use for some quantum. <br /><br />The best way to avoid this is to let the connections and service end normally, though in abnormal situations this isn't always possible. <br /><br />When you must use **ENDJOB** , etc., to end the connections and/or the service, you can sometimes use the **WRKTCPSTS** command to view the outstanding socket connections and end them. In such a case, if you find a socket in the "listening" state using the DataGate&#174; port, you can end this connection (but only if you are absolutely sure the service isn't running) using WRKTCPSTS. Likewise, if you find sockets connected to the DataGate&#174; port from external ports, you can end those (if you are sure that there are no jobs using the connection). The system will then reclaim the port, and a new instance of the DataGate&#174; service can use it immediately.
<div>

### <a name="Finding_an_iSeries_IP_address">Finding a IBM i IP address</a> 
If the user does not know the IP address of the IBM i to which they are trying to Name a database, do the following. Note however, that most users should never have to do this, and you may want to "call your Network Manager" instead of performing the steps below. 

32. In Windows, open a Command Prompt 
				  window and enter:<br /> **arp -a** <br />Note the IP 
				  addresses that appear. You will compare this list with the 
				  list generated in step 4. (Normally, there will be only one 
				  difference, and it will be the addition of the IBM i's IP 
				  address).<br />
33. For **Windows** : At a 
				  Command Prompt, enter:<br /><br />
				  <span style="font-family: Courier New;">IPCONFIG</span><br />
				  <br />The IP address of Windows will display. Note this IP 
				  address, since you will use it in step 3.<br /><br />
34. On the IBM i on a command line enter:<br />
				  <br />PING 'xxx.xxx.xxx.xxx'<br /><br />where xxx.xxx.xxx.xxx is the 
				  IP address of Windows noted in step 2.<br /><br />In the 
				  Configuration dialog, there's a drop down list box of 
				  adapters. Note that in most cases you will only have one 
				  Ethernet adapter, so the only challenge is to distinguish the 
				  Ethernet adapter from a dial-up adapter. This is usually easy, 
				  because dial-up adapters usually have a name like " **NdisWan4** ".
				  <br /><br /><br /><span class="NormalNote"> *It is also wise to NOT 
				  attempt to ping a Windows computer that is also running 5250 
				  emulation, etc., to the object IBM i. That's because that IBM 
				  i will **already**  be in the **arp**  
				  sorted "list", so one would not be able to tell which is the 
				  target IBM i because the list would be the same in steps 1 and 
				  4.*  </span><br /><br />
35. On Windows in the Command Prompt 
				  window, enter:<br /><br /> **arp -a** <br /><br />The IP 
				  addresses are sorted. Compare the list with the list in step 1 
				  and note the new IP address, this is the IBM i's IP address.

