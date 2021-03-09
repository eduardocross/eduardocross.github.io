---
title: Labeling a Database

Id: dgLabelingaDatabase
TocParent: dgWorkingwithDatabasesMain
TocOrder: 42

keywords: database, labeling
keywords: databases, label
keywords: adding a label to a database
keywords: label a database

---

DataGate for Windows databases from earlier versions of ASNA Visual RPG and Acceler8DB must be " **Labeled** " so that they can be used with the latest release. This process upgrades the internal structure of the database and stores information that allows clients to register a name for it.

You can also easily Label existing Databases by selecting **Database Wizard** from the Database menu.

#### To Label an Existing Database

1. Select **Work with <u>D</u>atabases**  from the DataGate menu. The Work with Databases dialog
					box will display.
2. In the left-hand tree view, select My Computer, or expand the Network list and select a
					remote computer.
3. In the previous step, if you selected a remote computer, you must make sure that you have
					specified a valid username and password to authenticate access to that computer.

The default value for Username, "*DOMAIN", is a keyword that causes DataGate Studio to use your current Windows Domain logon credentials to authenticate your access to the remote computer. In that case, you may leave the Password field blank. Otherwise, you must enter a user and password that has sufficient access on the remote computer to create the database.

If you have insufficient authority to label the database, the command will fail.
4. Select the **<u>N</u>ew**  button to label a database. The Label Database dialog box will display.

*Note that this is the same command and dialog used to create a database. In this case however,we have the files comprising a DataGate for Windows database in a particular folder already. The Label Database dialog box is shown below.* 
![](../images/AddNewDatabase.png)
**Note** - Label Database Dialog can also be accessed by right-clicking a server in the DataGate Explorer treeview and selecting **New Database** .
5. Enter a name for the database in the **Label**  field. The label is the database's name with
					respect to the server, and is distinct from the client application-oriented "database name" you
					will add later.
6. Enter the complete **path**  of the directory in which the database is located.
7. Enter a text **description**  of the database contents, if desired, entering up to 50 alphanumeric
					characters.
8. Under New or Existing Database, select **Label and <u>E</u>xisting Database** .
9. Select the **OK**  button. The database will be label, the Label Database dialog will close, and
					the new label will be selected in the tree view of the Work with Databases dialog.

The newly-created database will appear in the Work with Databases tool. You can now modify the database's properties if desired.

To use this database in an application, you will next need to create a database name to identify the database to the client. See [Working with Database Names](dgWorkingwithDatabasenamesMain.html) for more information.

#### Section summary:

- <a href="dgWorkingwithDatabasesMain.htm" target="Main">Working with Databases</a>
- <a href="dgCreateaNewDatabase.htm" target="Main">Creating a New Database</a>
- <a href="dgChangingaDatabase.htm" target="Main">Changing an Existing Database</a>
- <a href="dgRemovingaDatabase.htm" target="Main">Removing an Existing Database</a>
- <a href="dgBrowsingDatabases.htm" target="Main">Browse for a Database Folder</a>

