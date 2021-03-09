---
title: AdgConnection.Close Method

Id: dcsAdgConnectionClassCloseMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 3

keywords: Close method
keywords: AdgConnection.Close method

keywords: how to, close database connection
keywords: how to, release database connection
keywords: release connection resources
keywords: database connections, release resources
keywords: close database connection

---

Sets the [ State](dcsAdgConnectionClassStateProperty.html) property to <span>Closed</span>, and releases connections to the database provider.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Close();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub Close()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Close Access(*Public)** 
      </pre>

Exceptions

None.
Remarks

This method sets the **State** property of the **AdgConnection** object to Closed. Additionally, if the current value of **State** is Open, the connection to the database provider is released, along with any unmanaged resources associated with that connection. 

Note that you must explicitly call either the <span> **Close** </span> or [Dispose](dcsAdgConnectionClassDisposeMethod.html) methods on <span> **AdgConnection** </span> objects in the **Open** state before the objects are finalized, to release unmanaged resources associated with their database connections. If unmanaged resources are not released prior to object finalization, unexpected results can occur, including program termination and loss of data.
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  //Disconnects from the dataBase by closing the connection.
  adg.Close();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  'Disonnects from the dataBase by closing the connection.
  adg.Close()</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  //Disconnects from the dataBase by closing the connection.
  adg.Close()</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      <span>
        [AdgConnection Class](dcsAdgConnectionClass.html)
        <br />
        [AdgConnection Class Members](dcsAdgConnectionMembers.html)
        <br />
        [State Property](dcsAdgConnectionClassStateProperty.html)
        <br />
        [Dispose Method](dcsAdgConnectionClassDisposeMethod.html)
        <br />
        [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
        <br />
      </span>

