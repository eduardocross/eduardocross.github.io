---
title: Creating a New Database

Id: dgCreateaNewDatabase
TocParent: dgWorkingwithDatabasesMain
TocOrder: 41

keywords: database, create new
keywords: databases, make new
keywords: databases, creating
keywords: database, add new
keywords: database, new

---

Creating a new database creates the internal catalog object, which maintains the set of attributes and relationships for all of the database files within a particular database. Databases from earlier versions of ASNA Visual RPG and Acceler8DB must be "Labeled" in order that they may be used with the latest release. This process upgrades the internal structure of the database and stores information that allows clients to register a name for it.

After creating a database, you will be prompted to register, or add a database name in order to open or access the database in applications.

You can also easily create a new DataGate for Windows database by selecting **Database Wizard** from the Database menu.

#### To Create a New Database

1. Select **Work with <u>D</u>atabases**  from the DataGate menu. The Work with Databases dialog
					box will display.
2. In the left-hand tree view, select My Computer, or expand the Network list and select a
					remote computer.
3. In the previous step, if you selected a remote computer, you must make sure that you have
					specified a valid username and password to authenticate access to that computer.

The default value for Username, "*DOMAIN", is a keyword that causes DataGate Studio to use your current Windows Domain logon credentials to authenticate your access to the remote computer. In that case, you may leave the Password field blank. Otherwise, you must enter a user and password that has sufficient access on the remote computer to create the database.

If you have insufficient authority to create a new database, the command will fail.
4. Select the **<u>N</u>ew**  button to create a new database. The Label Database dialog
					box will display.

*Note that this is the same command and dialog used to label an existing database. In this case however, we will invoke a DataGate command to create the files and folder comprising a new database. The Label Database dialog box is shown below.* 
![](Images/AddNewDatabase.png)		

**Note** - Label Database Dialog can also be accessed by right-clicking a server in the DataGate Explorer treeview and selecting **New Database** .
5. Enter a name for the database in the **Label**  field. The label is the database's name with
					respect to the server, and is distinct from the client application-oriented "database name" you
					will add later.
6. Enter the complete **path**  of the directory in which the new database will be created, or where
					a database from an earlier version is located. If you are not sure of the folder in which the
					database will be placed, select the **...**  button to the right to Browse for a database folder.					

After selecting a desired folder, you may wish to create a new sub-directory in which to place the database. (The subdirectory does not need to exist, it will be created for you). Note that the path and folder of the database must be empty).
7. Enter a text **description**  of the database contents, if desired, entering up to 50 alphanumeric
					characters.
8. Under New or Existing Database, select **Create a New Database** .
9. Select the **OK**  button. The database will be created, the Label Database dialog will close, and
					the new label will be selected in the tree view of the Work with Databases dialog.

The newly-created database will appear in the Work with Databases tool. The database is created with a default set of properties which you can now modify if desired.

To use this database in an application, you will next need to create a database name to identify the database to the client. See [Working with Database Names](dgWorkingwithDatabasenamesMain.html) for more information.

#### Section summary:

- <a href="dgWorkingwithDatabasesMain.htm" target="Main">Working with Databases</a>
- <a href="dgLabelingaDatabase.htm" target="Main">Labeling an Existing Database</a>
- <a href="dgChangingaDatabase.htm" target="Main">Changing an Existing Database</a>
- <a href="dgRemovingaDatabase.htm" target="Main">Removing an Existing Database</a>
- <a href="dgBrowsingDatabases.htm" target="Main">Browse for a Database Folder</a>

