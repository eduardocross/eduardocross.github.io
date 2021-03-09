---
title: Creating Export Files

Id: dgCreatingExportFiles
TocParent: dgWorkingwithExportFilesMain
TocOrder: 51

keywords: exporting files, about
keywords: DataGate Studio, exporting files
keywords: databases, exporting files
keywords: exporting files, creating
keywords: creating exporting files
keywords: exporting files
keywords: new export files
keywords: making export files

---

With the DataGate Import/Export tool, you can create a database snapshot of particular objects and their data, and place that snapshot in a file on your local computer. This export file can be imported into another database, or transported to a different computer for import, as in an application deployment scenario.

**Note -** The DataGate Import/Export tool is separate from the <a href="dgRecordImportExport">Record Import/Export</a> feature, which allows developers to import/export to and from ASCII-friendly CSV and XML files.

### To Create an Export File

1. Select **DataGate Import/Export**  from the DataGate menu. The DataGate
				Import/Export tool window will display.
2. Click the **New Export**  button on the window™s toolbar. A drop down list of current
				DataGate Explorer connections is shown.		
				![](../images/dgImpExpCommands.png)
3. Select the connection to use to export objects and data from. The root library of
				the database is shown in the main window tree view.

Database connections will only be available for selection if you have first created them in DataGate Explorer.
4. Expand the **tree**  to display the objects you wish to export. Click the empty square
				next to the object names in the tree you wish to export. 

Clicking the square will put a check in it, all files with checks next to them will be exported; unchecked files in the same library will be excluded.
5. Click the **Save Export**  button. A Save As file chooser dialog is displayed.
				Navigate to the folder to contain the export file, and then type the file name. Click
				the **Save**  button to save the export file, or **Cancel**  to close the dialog without saving.
				The export process begins when you press **Save** .

The default extension for DataGate export files is . **dgie** . You may use any extension, but this extension is registered with Windows so that the file opens in DataGate Studio with the Windows **Open** command.

The progress of the export process can be viewed in the DataGate Studio Status Bar and Output window. The time required to complete an export process is affected by the following factors.

- The number of database objects, and the size and count of database records to export.
- The performance of the database server.
- For remotely hosted database servers, the latency of the network.
- The performance of the local computer.

The export process runs in a worker thread, so you may continue to perform other tasks in DataGate Studio while it completes.

### Summary of this Section

- <a href="dgCreatingExportFiles.htm" target="Main">Creating Export Files</a>
- <a href="dgImportingExportedData.htm" target="Main">Importing Exported Data</a>
- <a href="dgMigratingDBManagerArchiveFilesToDGStudioExportFiles.htm" target="Main">Migrating Database Manager 
                   		Archive Files to Datagate Studio Export Files</a>
- <a href="dgRecordImportExport.htm" target="Main">Record (CSV/XML) Import/Export</a>

