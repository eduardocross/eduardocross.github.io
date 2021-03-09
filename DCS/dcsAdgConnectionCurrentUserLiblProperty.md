---
title: AdgConnection.CurrentUserLibl Property

Id: dcsAdgConnectionCurrentUserLiblProperty
TocParent: dcsAdgConnectionPropertiesMain
TocOrder: 0

keywords: CurrentUserLibl property
keywords: AdgConnection.CurrentUserLibl property

keywords: how to, change library list for open database connection
keywords: library list changed for open database connection
keywords: database connections, library list changed
keywords: connections, database library list changed

---

Set-only property used to change the current library list of an open database connection.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string[] CurrentUserLibl { set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public WriteOnly Property CurrentUserLibl As String ()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp CurrentUserLibl Access(*Public) Type(*String) Rank(1)
   BegSet** 
      </pre>

				Property Value

String array. Set-only.
Remarks

This property may be used to change the user library list for the current database connection.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

