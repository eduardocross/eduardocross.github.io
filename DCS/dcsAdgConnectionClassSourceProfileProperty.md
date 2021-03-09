---
title: AdgConnection.SourceProfile Property

Id: dcsAdgConnectionClassSourceProfileProperty
TocParent: dcsAdgConnectionPropertiesMain
TocOrder: 1

keywords: SourceProfile property
keywords: AdgConnection.SourceProfile property

keywords: database files, establish a connection
keywords: files, establish a database connection
keywords: establish database connection
keywords: how to, establish database connection
keywords: database connections, established

---

The [SourceProfile](dcsSourceProfileClass.html) object describing the currently open database connection, or if the **AdgConnection** object is in the <span>Closed</span> state, the database connection to be opened when the [ Open](dcsAdgConnectionClassOpenMethod.html) method is called.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public [SourceProfile](dcsSourceProfileClass.html) SourceProfile { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property SourceProfile As [SourceProfile](dcsSourceProfileClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp SourceProfile Access(*Public) Type([SourceProfile](dcsSourceProfileClass.html))
   BegGet** 
      </pre>

Property Value

[ASNA.DataGate.Providers.SourceProfile](dcsSourceProfileClass.html). (get/set)
Remarks

The **Open** method utilizes this property to establish a database connection with specific characteristics as required by the user. The property can be set explicitly, or via the [ AdgConnection constructor.](dcsAdgConnectionConstructorsMain.html)

Note that changing the value of this property, or changing the object referenced by this property, has no effect on the current database connection (if [ State](dcsAdgConnectionClassStateProperty.html) indicates Open). The database connection is only influenced by this property via the **AdgConnection.Open** method. 
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection Cx;
  Cx = new AdgConnection("*Public/DG NET IBM i");
  MessageBox.Show("The database name \"*Public/DG NET IBM i\" refers to a connection to "
           + Cx.SourceProfile.Server + " on port " + Cx.SourceProfile.Port.ToString());</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim Cx As AdgConnection
  Cx = New AdgConnection("*Public/DG NET IBM i")
  MsgBox ("The database name ""*Public/DG NET IBM i"" refers to a connection to " _
           + Cx.SourceProfile.Server + " on port " + Cx.SourceProfile.Port.ToString())</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  Dclfld Name(Cx) Type(AdgConnection)
  Cx = *New AdgConnection("*Public/DG NET IBM i")
  MsgBox 'The database name "*Public/DG NET IBM i" refers to a connection to ' +
           + Cx.SourceProfile.Server + " on port " + Cx.SourceProfile.Port.ToString()</pre>

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
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [State Method](dcsAdgConnectionClassStateProperty.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

