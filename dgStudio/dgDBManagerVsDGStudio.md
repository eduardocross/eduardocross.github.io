---
title: Comparison of DB Manager and DG Studio

Id: dgDBManagerVsDGStudio
TocParent: Welcome
TocOrder: 3

keywords: Database manager
keywords: Manager vs Studio comparison

---

The venerable predecessor of DataGate Studio, ASNA Database Manager, uses the DataGate COM client library for database access. **Database Manager has been retired from the ASNA product lineup following the release of DataGate Studio 9.1.** 

Former users of Database Manager will find new featuress and enhancement to many of the replacement functions implemented by DataGate Studio. Some of these and other comparisons are listed below.

**Active Directory Access** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager allows you to browse the database in its Active Dictionary
					pane, which is the primary axis for most management tasks.</td>
				<td>Similarly, DataGate Studio offers the DataGate Explorer tool, which presents
					database servers, connections, and database names in a tree view control.
					You browse the database by expanding a connection node, which represents a live
					view of the database.</td>
			</tr>
</table>

**File Definition Access** 
<table border="1">			
			<tr>
				<th>Database Manager</th>
				<th>DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager provides the Definition Work Area pane for viewing
					and designing database file definitions. **Database Manager does not provide a
					way to save file definitions outside of the database.** </td>
				<td>DataGate Studio offers an XML-based, graphical designer view of file definitions,
					in a standard document window. DataGate Studio file definitions can be saved as
					source code files and arranged in a DataGate project as well.</td>
			</tr>
</table>

**Data Area Access** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager does **not**  provide access to data area objects.</td>
				<td>DataGate Studio fully supports data areas in DataGate/400 and DataGate for SQL
					Server databases.</td>
			</tr>
</table>

**File Editing** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager invokes the **Acceler8DB File Editor** , a grid-based
					viewer to display and update database files.</td>
				<td>DataGate Studio allows you to display and update files using two different integrated
					viewers, which are displayed as document windows.
- **Single-row editor -**  useful for
						files with duplicate keys. It displays
						one record at a time for editing, and
						provides controls for navigating
						through the file.
- **Multi-row editor -** grid-based,
						with scrollbars for navigating the
						records and fields.

</td>
			</tr>
</table>			

**Archiving** 
<table border="1">			
			<tr>
				<th>Database Manager</th>
				<th>DataGate Studio</th>
			</tr>
			<tr>
				<td>The Database Manager Archive utility provided a way to import and export files
					and data to and from DataGate for Windows databases.
 **Note that Database Manager archive files cannot be used in DataGate Studio.** </td>
				<td>DataGate Studio™s Import/Export tool is a client/server-based archiving scheme,
					which allows you to import to, and export from, any DataGate database; including
					DataGate/400 and DataGate for SQL Server.
					Export file catalog browsing is much improved in comparison to Database Manager archiving.</td>
			</tr>
</table>				

**Print File Designer** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager can only manipulate OLE print files by invoking the
 **Acceler8DB Print File Editor.** </td>
				<td>DataGate Studio integrates the **.NET Print File Designer**  (originally delivered with
					ASNA Visual RPG for .NET), and enhances it to provide a code view of the underlying
					XML document. ***Note that .NET print files can only be used with DataGate for .NET, and OLE
					print files cannot be used with DataGate for .NET*** .  However, DataGate Studio includes a
 **conversion utility**  to help upgrade your existing OLE print files to .NET print files.</td>
			</tr>
</table>			

**Database Name Registration** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager saves database name Connection information 
				in the **Windows registry.** </td>
				<td>DataGate Studio still honors database name information in the registry, 
				but newly-created database names are now saved to a **.NET configuration file** . This
				scheme prevents unnecessary use of the Windows registry, which is less broadly 
				accessible in current Windows operating systems. **Note that .NET configuration file based
				database names are only available to the DataGate .NET data provider (not Database Manager or
				DataGate COM)** .</td>
			</tr>
</table>

**Connection Information Management** 
<table border="1">			
			<tr>
				<th style="height: 25px">Database Manager</th>
				<th style="height: 25px">DataGate Studio</th>
			</tr>
			<tr>
				<td>Database Manager can only access databases for which a database name has been registered.</td>
				<td>DataGate Studio allows connections todatabases without the use of a database name.
				The process of entering database connection information has been streamlined, and includes a **test** 
				function, which allows you to confirm the validity of connection parameters as they are entered.
				Database connections are managed independently of database names in DataGate Studio. However, connections
				may also be based on database names.</td>
			</tr>
</table>		  

