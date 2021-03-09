---
title: Database Connection Parameters

Id: dgDatabaseConnectionParameters
TocParent: dgWorkingwithConnectionsMain
TocOrder: 14

keywords: Connection Parameters
keywords: Database connections
keywords: Database connection parameters
keywords: Database parameters
keywords: Connections, database

---

![](Images/DatabaseConnection.png) 

#### Use Registered Database Name
This button allows you to select one of the database names registered on the local computer to use for the new connection. Database names are stored connection parameters associated with a string identifier. You can manage database names in DataGate Explorer in the Local Database Names list. To select a database name, use the following parameters on the dialog.

#### Database Name:
Select one of the database names listed in this drop down box (click the down arrow on the right, or the keyboard down arrow, to reveal your choices). The database names listed here can be filtered by checking or clearing the "*Public Names Only" checkbox.

#### *Public Names Only:
Setting or clearing this checkbox updates the list of database names in the Database Name drop down box. When clear, the list displays all database names on the local computer, including the private and public database names. The public database names are prefixed with the "*Public/" string. When set, the list displays only the public database names, and without the "*Public/" prefix.

#### Enter Connection Details:
To enter connection details manually, rather than using a database name, select this radio button. This can be useful for quickly accessing a new database for an administrative task, rather than creating a database name for software development tasks. The parameters required for the connection are given below.

#### Server:
Enter the server that contains the actual database which the database name entered above points to. Select the **Browse** button to the right to take you to a dialog box allowing you to **Select a Database** server and database label. Otherwise, enter any valid TCP/IP hostname or IP address that refers to the networked database server host.

#### Label:
Enter the label of the actual database which the database name points to. Select the **Browse** button to the right to take you to a dialog box allowing you to Select a Database server and database label.

#### Is SQL Database:
To access a DataGate for SQL Server database server, set this checkbox. For non- SQL servers, clear the checkbox.

#### Authentication:
Select one of the three radio buttons to choose the authentication method for connecting to the DataGate server.

- **Use Windows Domain Authentication -** Use the current Windows Domain user
								credentials to authenticate access to the server. Note that this method only works
								for Windows-based database servers, and only when both the client and server
								machines are members of the Windows Domain.
- **Prompt for Authentication Information -** Upon each connection attempt, the
								DataGate client will raise a user/password dialog for the user to enter credentials for
								access to the server.
- **Use Server-based Authentication -** In the provided text boxes, enter the user and
								password which should be used for every connection attempt to authenticate access
								to the server. Note in this case that DataGate saves encrypted user and password
								information on the local machine.

#### User:
Enter the name of a server user authorized to access the database. User name is enabled for editing only if Use Server-based Authentication is selected. Note that DataGate saves encrypted user and password information on the local machine when Use Server-based Authentication is selected.

#### Password:
Enter the password for the user name given above. Password is enabled for editing only if Use Server-based Authentication is selected. Note that DataGate saves encrypted user and password information on the local machine when Use Serverbased Authentication is selected.

#### Pool Connections:
Select this option to enable database connection pooling. When database connection pooling is enabled, the communication to the server and to the server resources are kept in a special ' **pool** '. The next time the application requires database services, one of the available connections in the 'pool is assigned to it. Thus, enabling Pool Connections results in faster database connections.

If connection pooling is not enabled, when a database and all its associated files are closed, the connection and server resources are ended (i.e., in the case of DataGate, the DataGate Job ends). When the same application needs the database services again, a new connection and corresponding job has to be established. This overhead wastes resources and slows down the application.

#### Idle Timeout in Minutes:
This field will become enabled when the **Pool Connections** option is selected. You must specify an amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool. The default value is 1 minute. Enter a time from 1 – 255 minutes.

You want to select a value that is long enough that permits the application to quickly open again, but not so long that many jobs are remaining idle.

#### Advanced:
Press this button to display the **Connection Properties** dialog window (described [here](dgAdvancedConnectionProperties.html)). This dialog allows you direct access to all connection properties.

#### Test Connection:
Press this to create a test connection to the database server after you have entered all connection details or selected the database name. At the end of the test, a message box will display the results.

#### OK:
Select **OK** to confirm your selections (add the new connection, or modify the existing one).

#### Cancel:
Select **Cancel** to close the dialog without making any changes (nothing will be added or modified)..

#### Section summary:

- [Creating a New Connection](dgCreatingNewConnection.html)
- [Opening and Closing Connections](dgOpeningandClosingConnections.html)
- [Modifying Database Connections](dgModifyingaConnection.html)
- [Removing  a Database Connection](dgRemovingaConnection.html)
- [Database Connection Clipboard Functions](dgConnectionClipboard.html)

