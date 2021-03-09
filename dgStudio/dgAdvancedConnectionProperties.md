---
title: Advanced Connection Properties

Id: dgAdvancedConnectionProperties
TocParent: dgWorkingwithDatabaseNamesMain
TocOrder: 36

keywords: Database connections
keywords: Database connection properties
keywords: Advanced properties
keywords: Advanced connection properties
keywords: Database name properties, advanced

---

Other DataGate connection properties can be associated with a connection or database name by clicking the **Advanced** button on the New Database Name, Database Connection, and Edit Database Name dialogs. This button displays the Connection Properties dialog window. This dialog shows ALL properties associated with the database name, including those which can be set on the primary properties dialog.

The dialog is a Windows standard property grid, displaying the property name in the left column, and its value in the right column. Selecting a property name or value cell will display a description of the property in the bottom pane of the window. Buttons above the grid allow you to sort the properties in various ways. The property names and their values are as follows.

#### Database Name:
The string **identifier** for a database name is used to reference the database name in a program (See the <a href="dgWorkingwithDatabaseNamesMain.htm" target="Main">Working with Database Names</a> section for more information). This identifier is shown in the DataGate Explorer tree under Local Database Names. In the Advanced Connection Properties grid, the value of this property is read-only. To change the database name identifier, use the Rename command on the database name node after the database name dialog has been closed. If no database name is associated with the connection properties, this value will be an **empty string** .

#### File Types:
This property allows you to filter which objects are shown as library contents displayed by DataGate Explorer. You may filter these types:

- All – Show all types of objects not otherwise filtered (this is the default value).
- All Logical – Show only logical files (including simple logical, multiformat, join,
						and SQL logical), unless otherwise filtered.
- Join – Show only join logical files, unless otherwise filtered.
- Physical – Show only physical files, unless otherwise filtered.
- Print – Show only print files, unless otherwise filtered.
- Simple Logical – Show only simple logical files, unless otherwise filtered.
- Data Areas – Show only Data Areas (DataGate Studio 9.1 and later only), unless
						otherwise filtered.

Note that this property only affects the DataGate Explorer display, not general access to the database. Applications using the connection can access any object type that the user has authority to.

#### Initial Library List:
With this property, you may optionally specify a list of library names that should be used to set an initial library list on the server database, upon each successful connection. Some DataGate server platforms associate a library list with a user profile. Note that any library list specified here will override the user profile's library list. The default value of this property is an empty list.

#### Label:
The value of this property, the server database label, is identical to the value entered in the Label field of the primary connection dialog. Enter the label of the actual database in which the database name points to. The primary connection dialog features a Browse button which displays a dialog allowing you to Select a Database server and label. There is no default value for Label.

#### Objects From:
This property allows you to filter which libraries are displayed by DataGate Explorer. This is useful when a server database consisting of many hundreds of libraries is slow to respond to a request to enumerate all libraries. You may filter libraries using these settings:

- All Libraries – Display all libraries not otherwise filtered (this is the default value).
- Library List – Display only libraries from the library list associated with the server
						job, unless otherwise filtered.
- User Library List – Display only libraries from the user portion of the library list
						associated with the server job, ignoring the system portion of the library list,
						unless otherwise filtered.
- Specific Libraries – Display only those libraries listed in the Specific Libraries
						property of the Advanced Connection Properties (explained below), unlessotherwise filtered.

Note that this property only affects the DataGate Explorer display, not general access to the database. Applications using the connection can access any library that the user has authority to.

#### Password:
The value of this property, the server user's password, is identical to the value entered in the Password field of the primary connection dialog. The displayed value of the property is obfuscated for security. The password value entered is only used if the value of the User property is not "*DOMAIN" or "*PROMPT". The default value is an empty string.

#### Password Type:
This property supports legacy DataGate servers using passwords of LeftPad 31 characters or less. In particular, when accessing DataGate/400 servers where the iSeries host uses the pre-V5R1 10-character password authentication scheme, this property may need to be set to the "Legacy" value. The default value is " **SecurePassphrase** ".

- Legacy – The password sent to the server must be 31 characters or less in LeftPad.
						If the iSeries server requires pre-V5R1 password authentication, you may need to
						specify this value to access a DataGate/400 server.
- SecurePassphrase – The password sent to the server is not limited to 31
						characters. Use this value to take advantage of the improved password security
						available in V5R1 and later iSeries servers.

#### Platform Attribute:
This property is used internally by DataGate client to initialize the connection to the database. Normally, its value should not be changed. When the " **Is SQL Database** " checkbox is selected on the primary connection dialog, the value of this property will be set to the keyword "*SQLOLEDB". In all other cases, the value of this property is either "*DATALINK" or an empty string. The default value is "*DATALINK".

#### Pooling Timeout:
The value of this property, the database connection pooling timeout, is identical to the value entered in the Idle Timeout in Minutes field of the primary connection dialog. Setting the value of this property to zero ** *disables* ** the database connection pooling feature. Note that if the Pool Connections checkbox is cleared on the primary connection dialog, the value of this property is zero. The default value is zero.

#### Server Host:
The value of this property, the server database host, is identical to the value entered in the Server field of the primary connection dialog. You may enter the server name that hosts the database. The primary connection dialog features a Browse button which displays a dialog allowing you to Select a Database server and label. The value of this property may be any valid TCP/IP hostname or IP address that refers to the networked database server host. There is no default value.

#### Show System Objects:
This property allows you to filter objects displayed by DataGate Explorer. This is particularly useful on iSeries systems, where system-related objects may be interspersed with user or application objects. You may filter objects using these settings:

- True – Display all objects not otherwise filtered (this is the default value).
- False – Display only objects not otherwise filtered that do not have the "system" attribute.

#### Specific Libraries:
The value of this property defines the libraries displayed by DataGate Explorer, but ** *only* ** if the value of Objects From is 'Specfic Libraries'. You may enter all the libraries you wish to be shown, subject to other filters, here. The default value is an empty list. Note that this property only affects the DataGate Explorer display, not general access to the database. Applications using the connection can access any library that the user has authority to.

#### TCP Port:
This property defines the TCP communications port number to be used by DataGate in establishing a connection to the server. The default value of this property is 5042, the registered port number for DataGate servers. In certain cases, DataGate servers may be configured to listen for incoming connections on an alternate port. You may change the default to the configured port using this property.

#### Text:
This property may be used to enter any comments to be associated with the connection. The default value is an empty string.

#### User:
The value of this property, the server database user, is identical to the value entered in the User field of the primary connection dialog. There is no default value. You may enter the name of a server user authorized to access the database. Otherwise, the property value may be one of the following keywords.

- *DOMAIN – Use the current Windows Domain user credentials to authenticate
						access to the server. Note that this method only works for Windows-based
						database servers, and only when both the client and server machines are
						members of the Windows Domain.
- *PROMPT - Upon each connection attempt, the DataGate client will raise a
						user/password dialog for the user to enter credentials for access to the server.

Note that DataGate saves encrypted user and password information on the local machine when a non-keyword value is entered for the User property.

#### Section summary:

- <a href="dgWorkingwithDatabaseNamesMain.htm" target="Main">Working with Database Names</a>
- <a href="dgCreatingDatabaseNames.htm" target="Main">Creating Database Names</a>
- <a href="dgModifyingDatabaseNames.htm" target="Main">Modifying Database Names</a>
- <a href="dgPublicandPrivateDatabaseNames.htm" target="Main">Public and Private Database Names</a>
- <a href="dgChangingDatabaseNames.htm" target="Main">Renaming Database Name Indentifiers</a>
- <a href="dgDatabaseNameParameters.htm" target="Main">Database Name Parameters</a>
- <a href="dgAdvancedConnectionProperties.htm" target="Main">Advanced Connection Properties</a>

