---
title: Managing Database Connections

Id: dcsManagingDatabaseConnections
TocParent: dcsConnectingtoaDatabaseMain
TocOrder: 0

keywords: databases, managing connections

---

[AdgConnection](dcsAdgConnectionClass.html) objects exist in one of two modes, as reflected by the [State](dcsAdgConnectionClassStateProperty.html) property. Initially, <span> **AdgConnection** </span> objects are in the <span>Closed</span> state. After successful execution of the [ Open](dcsAdgConnectionClassOpenMethod.html) method, the **AdgConnection** object is in the <span>Open</span> state. When open, <span> **AdgConnection** </span> objects represent a live connection to the database and can be used with other DCS objects and methods to perform access operations.

Prior to calling <span> **Open** </span>, you can use the [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) property to modify connection parameters. Changes to <span> **SourceProfile** </span> affect subsequent <span> **Open** </span> method calls. The characteristics of the database connection cannot be changed when in the Open state. See the next topic [ Database Name Handling](dcsDatabaseNameHandling.html) for a further introduction to <span> **SourceProfile** </span>.
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [SourceProfile Property](dcsAdgConnectionClassSourceProfileProperty.html)
      <br />
      [AdgConnection.State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [Database Name Handling](dcsDatabaseNameHandling.html)
      <br />
      [Connecting to a Database](dcsConnectingtoaDatabaseMain.html)

