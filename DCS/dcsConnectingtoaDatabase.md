---
title: Connecting to a Database Using a Database Name

Id: dcsConnectingtoaDatabase
TocParent: dcsConnectingtoaDatabaseMain
TocOrder: 0

keywords: connecting to a database, using a database name
keywords: database names
keywords: database label
keywords: databases, connecting to
keywords: database names, using to connect to a database

---

The DataGate notions of "database name" (a registered client-side reference to a set of database connection parameters) and "database label" (the server-side identifier for database servers) are provided to help you identify and connect to a database.

The way to connect to a database is through the [ AdgConnection](dcsAdgConnectionClass.html) object. The following code fragment creates an AdgConnection object and connects to a database referred to by the database name "ASNA Local DB".
<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection Cx;
  Cx = new AdgConnection("ASNA Local DB");
  Cx.Open();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim Cx As AdgConnection
  Cx = New AdgConnection("ASNA Local DB")
  Cx.Open()</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  Dclfld Name(Cx) Type(AdgConnection)
  Cx = *New AdgConnection("ASNA Local DB")
  Cx.Open()</pre>

The first line declares a variable reference to an **AdgConnection** object. The second line uses the New clause to create an instance of the DCS AdgConnection class, which is assigned to the *Cx variable.* The constructor of the class accepts a string parameter which refers to a registered database name. The third line creates a connection to the database named in the constructor. 
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <span>
        <br />
      </span>
      <span>
        [ Disconnecting 
							from a Database](dcsDisconnectingfromaDatabase.html)
        <br />
      </span>

