---
title: Database Name Parameters

Id: dgDatabaseNameParameters
TocParent: dgWorkingwithDatabaseNamesMain
TocOrder: 35

keywords: database name parameters
keywords: parameters
keywords: database name options

---

![](Images/EditDBNameProperties.png) 

#### Server:
Enter the server that contains the actual database which the database name entered above points to. Select the **Browse** button to the right to take you to a dialog box allowing you to **Select a Database** server and database label. Otherwise, enter any valid TCP/IP hostname or IP address that refers to the networked database server host.

#### Label:
Enter the label of the actual database which the database name points to. Select the **Browse** button to the right to take you to a dialog box allowing you to Select a Database server and database label.

#### Is SQL Database:
To access a DataGate for SQL Server database server, set this checkbox. For non- SQL servers, clear the checkbox.

#### Authentication:
Select one of the three radio buttons to choose the authentication method for connecting to the DataGate server.

- **Use Windows Domain Authentication &#8211;** Use the current Windows Domain user
								credentials to authenticate access to the server. Note that this method only works
								for Windows-based database servers, and only when both the client and server
								machines are members of the Windows Domain.
- **Prompt for Authentication Information &#8211;** Upon each connection attempt, the
								DataGate client will raise a user/password dialog for the user to enter credentials for
								access to the server.
- **Use Server-based Authentication &#8211;** In the provided text boxes, enter the user and
								password which should be used for every connection attempt to authenticate access
								to the server. Note in this case that DataGate saves encrypted user and password
								information on the local machine.

#### User:
Enter the name of a server user authorized to access the database. User name is enabled for editing only if Use Server-based Authentication is selected. Note that DataGate saves encrypted user and password information on the local machine when Use Server-based Authentication is selected.

#### Password:
Enter the password for the user name given above. Password is enabled for editing only if Use Server-based Authentication is selected. Note that DataGate saves encrypted user and password information on the local machine when Use Server-based Authentication is selected.

#### Pool Connections:
Select this option to enable database connection pooling. When database connection pooling is enabled, the communication to the server and to the server resources are kept in a special " **pool** ". The next time the application requires database services, one of the available connections in the pool is assigned to it. Thus, enabling Pool Connections results in faster database connections.

If connection pooling is not enabled, when a database and all its associated files are closed, the connection and server resources are ended (i.e., in the case of DataGate, the DataGate Job ends). When the same application needs the database services again, a new connection and corresponding job has to be established. This overhead wastes resources and slows down the application.

#### Idle Timeout in Minutes:
This field will become enabled when the **Pool Connections** option is selected. You must specify an amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool. The default value is 1 minute. Enter a time from 1 – 255 minutes.

You want to select a value that is long enough to permit the application to quickly open again, but not so long that many jobs are remaining idle.

#### Advanced:
Press this button to display the <a href="dgAdvancedConnectionProperties.htm" target="Main"> Connection Properties</a> dialog window. This dialog allows you direct access to all connection properties.

#### Test Connection:
Press this to create a test connection to the database server after you have entered all connection details or selected the database name. At the end of the test, a message box will display the results.

#### OK:
Select **OK** to confirm your selections (add a new Database Name, or modify the existing one).

#### Cancel:
Select **Cancel** to close the dialog without making any changes (nothing will be added or modified).

#### Section summary:

- <a href="dgWorkingwithDatabaseNamesMain.htm" target="Main">Working with Database Names</a>
- <a href="dgCreatingDatabaseNames.htm" target="Main">Creating Database Names</a>
- <a href="dgModifyingDatabaseNames.htm" target="Main">Modifying Database Names</a>
- <a href="dgPublicandPrivateDatabaseNames.htm" target="Main">Public and Private Database Names</a>
- <a href="dgChangingDatabaseNames.htm" target="Main">Renaming Database Name Indentifiers</a>
- <a href="dgDatabaseNameParameters.htm" target="Main">Database Name Parameters</a>
- <a href="dgAdvancedConnectionProperties.htm" target="Main">Advanced Connection Properties</a>

