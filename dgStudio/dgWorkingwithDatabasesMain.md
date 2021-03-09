---
title: Working with Databases

Id: dgWorkingwithDatabasesMain
TocParent: Welcome
TocOrder: 40

keywords: databases, working with
keywords: DataGate databases
keywords: databases, intro to
keywords: overview of databases

---

DataGate Studio is the primary database management tool set for all DataGate servers, but it is the only database management program for DataGate for Windows servers. When using DataGate for Windows servers, one of the first tasks is to create and label a database. This can be accomplished with the Work with Databases tool or through dialogs accessed via the DataGate Explorer treeview.

![](images/WorkwithDatabases.png)

The Work with Databases tool provides these functions:

- <a href="dgCreateaNewDatabase.htm" target="Main">Create a New Database</a>
- <a href="dgLabelingaDatabase.htm" target="Main">Labeling an Existing Database</a>
- <a href="dgChangingaDatabase.htm" target="Main">Changing an Existing Database</a>
- <a href="dgRemovingaDatabase.htm" target="Main">Removing an Existing Database</a>
- <a href="dgBrowsingDatabases.htm" target="Main">Browse for a Database Folder</a>
- <a href="dgDatabaseWizard.htm" target="Main">The Database Wizard</a>

Creating a new database creates the internal catalog object, which maintains the set of attributes and relationships for all of the database files within a particular database. After creating a database, you must **Add** a database name that references the database to access.

Databases from earlier versions of ASNA Visual RPG and DataGate must be in order that they may be used with the latest release. This process upgrades the internal structure of the database and stores information that allows clients to register a name for it
