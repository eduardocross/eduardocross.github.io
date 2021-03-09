---
title: DSS Operation QTemp

Id: DSSQTemp
TocParent: DSSOperation
TocOrder: 10

keywords: ASNA DataGate
keywords: SQL Server QTemp
keywords: QTemp
keywords: Operating QTemp
keywords: DSS QTemp
keywords: QTemp in DSS

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# DSS Operation: QTemp

---

To implement the IBM i concept of <code>QTEMP</code> (a private library for each Job), DataGate&#174; for SQL Server (DSS) uses the following technique:
- Designate an installation-defined SQL Server database (e.g. <code>QTempDB</code>) as the repository of objects
 stored in the <code>QTEMP</code> libraries for ALL the <code>'Jobs'</code> or connections.
- Assign a unique ID to each DataGate&#174; client (connection).
- Whenever a DataGate&#174; client refers to an object in the <code>'QTEMP'</code> library, DSS appends the unique ID 
to the name and attempts to locate it on the <code>QTempDB</code> database.
- When the connection gets closed (the DG Client goes away), DSS delete all objects in <code>QTempDB</code> with the client's ID.
- Users accessing <code>QTEMP</code> programmatically must have read write access to the SQL Server designated database (e.g. <code>QTempDB</code>).

The SQL Server database designated as <code>QTEMP</code> can be set in the ASNA Stored Procedures Wizard during the initial installation, on the dialog shown below:

![](images/QTemp1.png)

The designated database can also be changed directly by modifying the contents specified in the file

![](images/QTemp2.png)
