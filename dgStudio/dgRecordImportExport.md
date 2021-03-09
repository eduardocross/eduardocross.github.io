---
title: Record Import/Export

Id: dgRecordImportExport
TocParent: dgWorkingwithExportFilesMain
TocOrder: 55

keywords: exporting files, about
keywords: DataGate Studio, exporting files
keywords: databases, exporting files
keywords: exporting files, creating
keywords: creating exporting files
keywords: exporting files
keywords: new export files
keywords: making export files

---

As of version 12.0, DataGate Studio facilitates conversion of member data to or from tradition CSV (comma separated values) or XML data in UTF-8 encoded files with a new feature called **Record Import/Export** . This new feature works parallel to the pre-existing DG Import/Export facility, the table below explains the difference between them.
<table>
			<tr><th>DG Import/Export</th><th>Record Import/Export</th></tr>
			<tr><td>Focused on application deployment and light-duty database backup 
			within the DataGate/IBM i domain</td><td>Targets data interoperability with other databases and 
			common formats (e.g., to get the data into a spreadsheet, or a partner's EDI gateway).</td></tr>
			<tr><td>Produces/consumes a defined XML schema-based format, in compressed or uncompressed .dgie files</td>
			<td>Produces/consumes  CSV or XML data (with embedded schema) in UTF8 "ASCII-compatible" encoded files.</td></tr>
			<tr><td>Operates on all object types in the database.</td><td>Operates only on the data records of member objects.</td></tr>
			<tr><td>Can operate on a single object or entire libraries of objects in the database.</td><td>Effects only a single member at a time</td></tr>
			<tr><td>Operates on the metadata AND the data.</td><td>Only operates on record data.</td></tr>
</table>

### Accessing Record Import/Export
To **Import** data from a CSV or XML file

1. Right click on a member to Import into in the DataGate Explorer treeview. The following context menu will pop up: <br />
			![](images/RecordImport1.png)
2. Select **Import CSV Records**  or **Import XML Records**  to open the Record Import/Export dialog.
3. A dialog box similar to the one shown below will appear.  <br />
			![](images/RecordImport3.png)
4. Enter or browse to the name of a file to import, then click **OK** .

To **Export** data to a CSV or XML file

5. Right click on a member to Import into in the DataGate Explorer treeview. Then hover over any of the **Data by ...**  options and this sub-menu will appear: <br />
			![](images/RecordImport2.png)
6. Select **Import CSV Records**  or **Import XML Records**  to open the Record Import/Export dialog.
7. A dialog box similar to the one shown below will appear.  <br />
			![](images/RecordImport4.png)
8. Enter or browse to the output file, and configure any desired CSV/XML options (text/field delimiters, whether to include 
			the XML schema) and click **OK**

### Summary of this Section

- <a href="dgCreatingExportFiles.htm" target="Main">Creating Export Files</a>
- <a href="dgImportingExportedData.htm" target="Main">Importing Exported Data</a>
- <a href="dgMigratingDBManagerArchiveFilesToDGStudioExportFiles.htm" target="Main">Migrating Database Manager 
                   		Archive Files to Datagate Studio Export Files</a>

