---
title: Working with Export Files

Id: dgWorkingwithExportFilesMain
TocParent: Welcome
TocOrder: 50

keywords: exporting files, about
keywords: DataGate Studio, exporting files
keywords: databases, exporting files
keywords: exporting files, creating
keywords: creating export files

---

To create and use database snapshots for application deployment and light-duty backup tasks, DataGate Studio provides the **DataGate Import/Export tool** as well as the [Record Import/Export Tool](dgRecordImportExport.html). The former can export database libraries, files, members, and optionally, member data; while the latter allows Import and Export of member data from and to ASCII-friendly CSV and XML files. The DG Import/Export tool also supports data area exports. 

The Import/Export tool features a tree view similar to the Windows Backup tool, which allows you to select individual objects or entire libraries for export to a single file on the local computer. Likewise, with the import function, you are presented with the contents of the export file in a tree view, with which you may individually select and exclude the objects to be imported.

**Please note the following:** 

- DataGate Import/Export is not designed for use as a full-featured backup tool.
				Although it is capable of creating snapshots of an entire database, the DataGate
				client/server connection interface may not, in certain environments, produce
				acceptable performance for large scale backup tasks, especially in comparison to
				similar platform-based tools. To protect your data, you are advised to use the
				database server platform's tools for periodic backups.
- The former ASNA DataGate Database Manager application featured an archive
				utility for creating snapshot files of the DataGate for Windows database. These
				files are not compatible with the DataGate Import/Export tool. DataGate
				Import/Export is a superior tool, in that it can create snapshots of any DataGate
				database, not just DataGate for Windows. Users of the archive tool can usually
				transition easily to DataGate export files.
- The DataGate Import/Export tool is separate from the <a href="dgRecordImportExport">Record Import/Export</a> feature, 
			which allows developers to import/export to and from ASCII-friendly CSV and XML files. See the Record Import/Export tool page for more information.

The following topics explain DataGate's Import and Export features.

- <a href="dgCreatingExportFiles.htm" target="Main">Creating Export Files</a>
- <a href="dgImportingExportedData.htm" target="Main">Importing Exported Data</a>
- <a href="dgMigratingDBManagerArchiveFilesToDGStudioExportFiles./htm" target="Main">Migrating Database Manager 
                   		Archive Files to Datagate Studio Export Files</a>
- <a href="dgRecordImportExport.htm" target="Main">Record (CSV/XML) Import/Export</a>

