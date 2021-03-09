---
title: Migrating DB Manager Archive File to DG Studio Export Files

Id: dgMigratingDBManagerArchiveFilestoDGStudioExportFiles
TocParent: dgWorkingwithExportFilesMain
TocOrder: 53

keywords: Database Manager vs Datagate Studio
keywords: Archive Files vs Export Files
keywords: Migrating from Database Manager
keywords: Database Manager Archive Files
keywords: Datagate Studio Export Files

---

**Users of the ASNA Database Manager Archive utility must continue to use Database Manager to work with the archive files it produces, since the archive file format is incompatible with the DataGate Import/Export tool. Likewise, the export file format is incompatible with the Archive utility. However, DataGate Import/Export effectively replaces Archive utility functionality, and produces export files that can be saved and restored to any DataGate database, not just DataGate for Windows.** 

If you currently have archive files, but want to transition to export files, you can simply restore your archive file, using Database Manager, to a DataGate for Windows database, then use DataGate Import/Export to export the same objects contained in the archive.

### Summary of this Section

- <a href="dgCreatingExportFiles.htm" target="Main">Creating Export Files</a>
- <a href="dgImportingExportedData.htm" target="Main">Importing Exported Data</a>
- <a href="dgRecordImportExport.htm" target="Main">Record (CSV/XML) Import/Export</a>

