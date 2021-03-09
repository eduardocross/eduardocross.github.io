---
title: Changing a Database

Id: dgChangingaDatabase
TocParent: dgWorkingwithDatabasesMain
TocOrder: 43

keywords: database names, working with
keywords: databases, changing
keywords: changing a database
keywords: modify a database
keywords: alter a database

---

Once a DataGate for Windows database has been created, you can change its description, library lists, and other options. Use the **Work with Databases** menu option from the **DataGate** menu to make changes to a database, or right click on it in the treeview and select **Edit** .

You can also easily make changes to existing Databases by selecting **Database Wizard** from the Database menu.

### To Change an Existing Database

1. Select **Work with <u>D</u>atabases**  from the DataGate menu. The Work with Databases dialog
					box will display.
2. The servers available will display on the left. Double-click on another server to change. If you
					need to view a TCP/IP server that is not shown, enter the name of the TCP/IP server and press
					the **<u>A</u>dd**  button to the right. The server will then be visible in the display box above. The
					server, label, path, description and other properties of the selected database will automatically
					display.

Note: If you wish to access a remote server, be sure and enter a valid username and password for validating access to the server, under "Administrator Account for Remote Server". The default value for Username, "*DOMAIN", is a keyword that causes DataGate Studio to use your current Windows Domain logon credentials to authenticate your access to the remote computer. In that case, you may leave the Password field blank. Otherwise, you must enter a user and password that has sufficient access on the remote computer to create the database.
![](..\images\DatabaseLabel.png)

**Note** - The Label Database Dialog can also be accessed by right-clicking a database in the DataGate Explorer treeview and selecting **Edit** .
3. Change the database's description, if desired.
4. Change the database's default library lists, if desired.

You may change the System library list or the User library list. Each field is a multi-line text box, in which you can enter as many library names (one per line) as the database server supports for each list.

The System library list is the library list that is imposed on all users of the database. The user you specify under "Administrator Account for Remote Server" must have sufficient authority to change the System library list.

The User library list is the library list associated with the current user (the user you specify under "Administrator Account for Remote Server").
5. Enable or disable any of the following options, if desired.	

#### Default Private QTemp
Most DataGate servers, by default, provide each database job with a private QTemp library. If instead, you want a single QTemp library to be shared by all jobs, clear this checkbox. Note that DataGate/400 does not support the shared QTemp option.

#### Check DB at Startup
This option tells the DataGate for Windows server to open the database when it is starting (before accepting connections) to trigger automatic index recovery. Without this option, automatic index recovery is not initiated until a connection attempts to open the database. This option is only relevant for DataGate for Windows servers.

#### Level 20 Security
By default, DataGate for Windows connections are validated against the current domain or by username/password local to the machine where DataGate server is running. A valid connection provides automatic access to any database label available on the server.

Designating level 20 security validates the connector's credentials against the specific label's root folder security setting, thus allowing the database to be independently secured from other databases on the server. Note that this option is only relevant for DataGate for Windows servers.
6. Select the **Appl<u>y</u>**  button to make the desired changes to the selected database.

Note: the Apply button will only be enabled if you have entered changes to the database's properties.

#### Section summary:

- <a href="dgWorkingwithDatabasesMain.htm" target="Main">Working with Databases</a>
- <a href="dgCreateaNewDatabase.htm" target="Main">Creating a New Database</a>
- <a href="dgLabelingaDatabase.htm" target="Main">Labeling an Existing Database</a>
- <a href="dgRemovingaDatabase.htm" target="Main">Removing an Existing Database</a>
- <a href="dgBrowsingDatabases.htm" target="Main">Browse for a Database Folder</a>

