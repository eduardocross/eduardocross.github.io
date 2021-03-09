---
title: Manually Installing DSS in a Clustered Server Environment

Id: dssInstallingClusters
TocParent: dssInstallation
TocOrder: 35

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; for SQL Server Reference Manual
				   </span><br />
				   </td>
			    </tr>
</table>

# Manually Installing DSS on a Clustered SQL Server

---

## Introduction 
A clustered SQL Server configuration involves two or more Nodes and a common storage facility as shown on the image below:

<img align="center" src="../images/ClusterImg01.png" />

DataGate&#174; for SQL Server (DSS) should be installed individually on each one of the Nodes of the cluster. Installing DSS involves two steps, first the installation of the DataGate&#174; Services on the Windows machine and second, the installation of some stored procedures and tables on the master SQL Server database.

The following steps walk through installing DSS on a cluster with two nodes; step 6 may be repeated as many times as is necessary to accommodate clusters with more than 2 nodes.
1. Install DSS on the first node

Logon to the first Node with administrator privileges then run the installation program **dss-setup-16.0.xx.y.exe** and follow the wizard's instructions (i.e. click Begin, Next, Install, or Finish as appropriate). 

<img align="center" src="../images/ClusterImg06.png" />

Click Finish to close the "Installation Completed Successfully" dialog (shown above). A new dialog, "DataGate&#174; for SQL Server Stored Procedures," (shown below) will be open; this will be used to install the stored procedures to the SQL cluster.

<img align="center" src="../images/ClusterImg07.png" />
2. Install the stored procedures

Fill out the dialogue to fit your situation.
3. Select your cluster's instance from the dropdown list.
4. This box should be checked if you are using Windows Authentication 
					on your SQL cluster, and the account you used to login to Windows is an Administrator 
					for the cluster; otherwise, uncheck this box.  If you checked this box, Skip to number 4.
5. This section should be used if you are not using Windows Authentication to install
					 the stored procedures.  Enter SQL credentials for a cluster Administrator.
6. If you would like to Enable <code>QTEMP</code>, select this checkbox and enter the name you would like to use for QTEMP.
7. Once the other fields are updated appropriately, click 'Install' to install the stored procedures.
 **Note:**  You may click 'Install All' to install the stored procedures to all instances listed in the 
						drop down list; to do this, the credentials entered must be applicable to all instances.

After the Wizard completes, a window will pop up to let you know if it completed successfully and report any errors.

<img align="center" src="../images/ClusterImg08.png" />

Click OK

Close the Stored Procedures Wizard.
8. License DSS on Node 1

Open the ASNA Registration Assistant and apply the DSS license to the server. Each node will have a unique Machine Code, so you will need a License Key for each Machine.

<img align="center" src="../images/ClusterImg09.png" />
9. Allow Port 5042 on the Firewall

<img align="center" src="../images/ClusterImg10.png" />

The DataGate&#174; client/server protocol normally uses port 5042. This port must allow TCP into the server.<br />
10. Repeat previous steps, except step 2, on other nodes

On the other nodes you must:
11. Install DataGate&#174; for SQL Server
12. License DSS
13. Allow Port 5042 on the Firewall

You will NOT need to install the stored procedures again, they only need to be installed once per cluster.
14. Test connection

After installing the DataGate&#174; client, create a DataGate&#174; Database Name pointing its Server parameter to the SQL Cluster Name (Note the individual Node name) and test the connection.

<img align="center" src="../images/ClusterImg13.png" />

<img align="center" src="../images/ClusterImg14.png" />

The following screen shows DataGate&#174; Studio using the newly created Database Name.

<img align="center" src="../images/ClusterImg15.png" />
<div>

