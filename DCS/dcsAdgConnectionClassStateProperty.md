---
title: AdgConnection.State Property

Id: dcsAdgConnectionClassStateProperty
TocParent: dcsAdgConnectionPropertiesMain
TocOrder: 2

keywords: State property
keywords: AdgConnection.State property

keywords: open state of database connection
keywords: state of database connection
keywords: database connections, state of
keywords: connections, state of

---

Gets the current state of the connection. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ConnectionState State { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property State As ConnectionState** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp State Access(*Public) Type(ConnectionState)
   BegGet** 
      </pre>

Property Value

**System.Data.ConnectionState** . (set-only)
Remarks

This property provides the ability to query the current state of **AdgConnection** objects.

Currently, **AdgConnection** supports two values of the **System.Data.ConnectionState** enumeration, Open and Closed. Open implies that a database connection currently exists under the control of the object. Closed signifies the absence of such a connection. **AdgConnection** objects are constructed in the Closed state.

The value of **State** will be set to Open by a successful call to the [Open](dcsAdgConnectionClassOpenMethod.html) method. Likewise, the value will be set to Closed by [ Close Method](dcsAdgConnectionClassCloseMethod.html) or [Dispose Method](dcsAdgConnectionClassDisposeMethod.html) calls. 
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here we need to use an AdgConnection "dataBase" to open
     a file.  We first check to make sure that the AdgConnection has 
     been initialized and that the connection has been made to
     avoid throwing an exception. */
  FileAdapter dbFile =  null;
  AdgDataSet dataSet = null;
  if (dataBase != null &amp;&amp; dataBase.State == ConnectionState.Open)
  {
     dbFile = new FileAdapter(dataBase);
     dbFile.OpenNewAdgDataSet(out dataSet);
  }
  else
  { 
     //If the AdgConnection was not ready, you cannot immediately
     //open the file, so take alternative action here.
  }</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
  </span>' Here we need to use an AdgConnection "dataBase" to open
  ' a file.  We first check to make sure that the AdgConnection has 
  ' been initialized and that the connection has been made to
  ' avoid throwing an exception.
  Dim dbFile As FileAdapter
  Dim dataSet As AdgDataSet
  If Not dataBase Is Nothing And dataBase.State = ConnectionState.Open Then
     dbFile = New FileAdapter(dataBase)
     dbFile.OpenNewAdgDataSet(dataSet)
  Else 
     'If the AdgConnection was not ready, you cannot immediately
     'open the file, so take alternative action here.
  End If</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here we need to use an AdgConnection "dataBase" to open
     a file.  We first check to make sure that the AdgConnection has 
     been initialized and that the connection has been made to
     avoid throwing an exception. */
  DclFld dbFile Type(FileAdapter)
  DclFld dataSet Type(AdgDataSet)
  If dataBase &lt;&gt; *Nothing *And dataBase.State = ConnectionState.Open
     dbFile = *New FileAdapter(dataBase)
     dbFile.OpenNewAdgDataSet(*ByRef dataSet)
  Else 
     // If the AdgConnection was not ready, you cannot immediately
     // open the file, so take alternative action here.
  EndIf </pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> Pro
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [Close Method](dcsAdgConnectionClassCloseMethod.html)
      <br />
      [Dispose Method](dcsAdgConnectionClassDisposeMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

