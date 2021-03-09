---
title: DataGate&#174; for SQL Server Help

Id: Welcome
TocParent: -1

keywords: ASNA DataGate&#174; for SQL Server
keywords: DataGate&#174; for SQL Server
keywords: DSS
keywords: DSS Intro

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[ASNA 
				   DataGate&#174; 16.0 for SQL Server](Welcome.html)</span></td>
			    </tr>
</table>

# DataGate&#174; for SQL Server Help
This document contains information and advice on using DataGate&#174; for SQL Server. The terms *DataGate&#174; for SQL Server* and *DSS* are used interchangably thoughout this guide. 

### What's New in 16.0?
DataGate&#174; 16.0 for SQL Server includes built-in Secure Socket Layer (SSL) protection, a new layer of defense between your data and hostile internet prescences. For details on how DataGate&#174; handles SSL, see the [SSL for DataGate&#174; Guide](../SSL/DataGateSSLServer.html) and the [SSL Deployment Guide](../SSL/SSLDeployment.html). 

### What is DSS?
DataGate&#174; for SQL Server (DSS) is a client/server database middleware that connects Windows clients with MS SQL Server. The concepts surfaced by the DSS API are based on the IBM i database (DB2/400): ISAM style record level access. The client is built as a .NET assembly. The client and the server communicate via TCP/IP using its own protocol.

The server implementation for MS SQL Server runs as a multi-threaded Windows system service (dgServer.exe); this service executes on the same machine where the SQL Server instance is running. dgServer.exe is an unmanaged C++ program that uses <code>SqlOleDB</code> to access SQL Server data and schema.

Each DataGate&#174; Client connection results in two OLEDB session connections from the DataGate&#174; Server to SQL Server. These connections can stay open throughout the day doing select, update, delete and insert operations. The **OLEDB** connections close when the application closes the DataGate&#174; connection.

In order to satisfy the ISAM style requests, DSS makes heavy use of Scrollable Server Cursors. DSS associates a server cursor with each open file; it typically requests a single row at a time from the rowsets used in conjunction with the server cursor. Each application can maintain a large set of active server cursors. Record locks are maintained via row locks on the server cursor.

The mapping of OS/400 construct to SQL Server is as follows:
<table>
			<tr><th>OS/400 construct</th><th>SQL Server artifacts</th></tr>
			<tr><td>Physical File</td><td>Table with an index. The Index is named as the Table name.</td></tr>
			<tr><td>Logical File – Simple</td><td>View plus an index on the Table. The Index is named as the View name.</td></tr>
			<tr><td>Logical File – Join</td><td>View (outer or inner join) plus an index on the first Table. The Index is named as the View name</td></tr>
			<tr><td>Logical File - Multiformat </td><td>Not supported</td></tr>
			<tr><td>Member</td><td>If a physical of simple logical file allows for multiple members, in addition to the file's table (or view),
			each member also uses a table (or view)</td></tr>
			<tr><td>Print file</td><td>Table with a single row containing the print file description</td></tr>
			<tr><td>Data Area</td><td>Table with a single row</td></tr>
			<tr><td>Library</td><td>Database</td></tr>
			<tr><td>Library List</td><td>Collection of database names</td></tr>
			<tr><td>QTEMP</td><td>Temporary tables and view created on a designated database and associated with each OLEDB session</td></tr>
			<tr><td>Record Lock</td><td>Server Cursor Lock</td></tr>
			<tr><td>Object Lock</td><td>SQL Server 'application lock'</td></tr>
</table>

DSS 'decorates' the Tables and Views with the following custom properties
<table>
			<tr><th>Property</th><th>Object</th><th>Value Usage</th></tr>
			<tr><td>Access Path</td><td>File's table or view</td><td>Key description: Key fields, direction and uniqueness</td></tr>
			<tr><td>Text ???</td><td>File or member's table or view</td><td>Uses provided descriptions</td></tr>			
			<tr><td rowspan="2">FileOrMember</td><td>File's table or view</td><td>*BOTH: Single Member File
*FILE: Multimember File
</td></tr>
			<tr><td>Member's table or view</td><td>Member's parent file name</td></tr>
	<tr><td>Wait for Record</td><td>File's table or view</td><td>Seconds to wait for a record if it is locked by some other application</td></tr>
</table>

### In This Guide

- [DSS Installation Guide](DSSInstallation.html)
- [DSS Configuration](DSSConfiguration.html)
- [DSS Porting Considerations](DSSPorting.html)
- [DSS ASNA  Visual Programming Considerations](DSSAVRConsiderations.html)
- [DSS Support for "." Characters in Filenames](DSSFileCreation.ht">Creating "Files" in DSS</a>
- <a href="DSSDotFilenameSuppport.html)
- [Differences Between DataGate, DG/400, and DSS](DSSVS.html)

