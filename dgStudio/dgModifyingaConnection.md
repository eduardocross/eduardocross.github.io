---
title: Modifying Database Connections

Id: dgModifyingaConnection
TocParent: dgWorkingwithConnectionsMain
TocOrder: 12

keywords: Database Connections
keywords: changing connections
keywords: Modifying connections

---

To update the connection properties of a connection you use the Modify Connection command on the connection node's context menu. To rename a non-database namebased connection node, use the Rename Object command on the DataGate menu. Database name-based connections cannot be renamed. 

Note that modifying an existing connection does not change an open connection's properties or status. To apply property changes to an open connection, you must close, and then reopen the connection.

#### To Modify an Existing Database Connection

1. Select **DataGate Explorer**  from the **DataGate**  menu. The DataGate Explorer tool
				window will display.
2. Select the connection node to modify under Connections. Right-click the node to
				display the context menu, and select Modify Connection. The Connection editing
				dialog will display.
3. Select one of the two primary radio buttons: " **Use registered Database Name** " or
				" **Enter Connection Details** ". The edit controls on the form associated with your
				choice are enabled, and the other controls are disabled.
4. Select the parameters for the connection, as explained [here](dgDatabaseConnectionParameters.html).
5. After clicking **OK** , the dialog will close and the connection will be modified. You may
				click **Cancel**  to discard your changes and close the dialog.

#### Section summary:

- [Creating a New Connection](dgCreatingNewConnection.html)
- [Opening and Closing Connections](dgOpeningandClosingConnections.html)
- [Removing a Database Connection](dgRemovingaConnection.html)
- [Database Connection Parameters](dgDatabaseConnectionParameters.html)
- [Database Connection Clipboard Functions](dgConnectionClipboard.html)

