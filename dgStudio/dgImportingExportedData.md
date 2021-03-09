---
title: Importing Exported Data

Id: dgImportingExportedData
TocParent: dgWorkingwithExportFilesMain
TocOrder: 52

keywords: importing files, about
keywords: DataGate Studio, exporting files
keywords: databases, exporting files
keywords: exporting files, creating
keywords: creating exporting files

---

DataGate Studio export files can be restored to a database using the DataGate Import/Export tool. You can examine the export file's contents, select the objects to be restored, and choose the target database.

**Note -** The DataGate Import/Export tool is separate from the [Record Import/Export](dgRecordImportExport.html) feature, which allows developers to import/export to and from ASCII-friendly CSV and XML files.

### To Restore Objects from an Export File

1. Select **DataGate Import/Export**  from the DataGate menu. The DataGate
				Import/Export tool window will display.
2. Click the **Load for Import**  button on the window's toolbar. A file chooser dialog will be shown.		

![](../images/dgImpExpCommands.png)
3. Select the export file to be opened. By default, the chooser will display only files
				with the extension . **dgie** , the registered extension for DataGate export file.  
				The .dgie extension is registered with Windows when DataGate Studio is installed.

Click **OK** to open the file. The root library of the objects in the export file is shown in the main window tree view.
4. Expand the tree to display the objects in the export file. Click the empty square next
				to the object names in the tree for each object you wish to restore.				

Clicking the square will put a check in it, all files with checks next to them will be restored to the target library; unchecked files in the same library will be excluded.
5. Click the **Import Objects**  button on the toolbar. A drop down list of current DataGate
				Explorer connections will be shown.				

Database connections will only be available for selection if you have first created them in DataGate Explorer.
6. Select the **connection**  corresponding to the target database. The import process
				will begin.

The progress of the import process can be viewed in the DataGate Studio Status Bar and Output window. The time required to complete an import process is affected by the following factors.

- The number of database objects, and the size and count of database records to export.
- The performance of the database server.
- For remotely hosted database servers, the latency of the network.
- The performance of the local computer.

The import process runs in a worker thread, so you may continue to perform other tasks in DataGate Studio while it completes.

### Summary of this Section

- <a href="dgCreatingExportFiles.htm" target="Main">Creating Export Files</a>
- <a href="dgImportingExportedData.htm" target="Main">Importing Exported Data</a>
- <a href="dgMigratingDBManagerArchiveFilesToDGStudioExportFiles.htm" target="Main">Migrating Database Manager 
                   		Archive Files to Datagate Studio Export Files</a>
- <a href="dgRecordImportExport.htm" target="Main">Record (CSV/XML) Import/Export</a>

