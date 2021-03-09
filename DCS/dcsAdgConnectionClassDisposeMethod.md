---
title: AdgConnection.Dispose Method

Id: dcsAdgConnectionClassDisposeMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 4

keywords: Dispose method
keywords: AdgConnection.Dispose method
keywords: how to, release database connection
keywords: how to, close database connection
keywords: release connection resources
keywords: database connections, release resources
keywords: dispose database connection

---

Sets the [ State](dcsAdgConnectionClassStateProperty.html) property to <span>Closed</span>, and releases connections to the database provider.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public virtual new void Dispose();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOverridable Sub Dispose()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Dispose Access( *Public ) Modifier( *NotOverridable )** 
      </pre>

Exceptions

None.
Remarks

This method sets the [ State](dcsAdgConnectionClassStateProperty.html) property of the <span> **AdgConnection** </span> object to <span>Closed</span>. Additionally, if the current value of State is <span>Open</span>, the connection to the database provider is released, along with any unmanaged resources associated with that connection. 

Note that you must explicitly call either the [ Close](dcsAdgConnectionClassCloseMethod.html) or <span> **Dispose** </span> methods on <span> **AdgConnection** </span> objects in the Open state before the objects are finalized. This releases unmanaged resources associated with their database connections. If unmanaged resources are not released prior to object finalization, unexpected results can occur, including program termination and loss of data.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [Close Method](dcsAdgConnectionClassCloseMethod.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />

