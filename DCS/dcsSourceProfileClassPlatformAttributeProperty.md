---
title: SourceProfile.PlatformAttribute Property

Id: dcsSourceProfileClassPlatformAttributeProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 5

keywords: PlatformAttribute property
keywords: SourceProfile.PlatformAttribute property
keywords: platform attributes, _Star_SQLOLEB
keywords: platform attributes, _Star_DATALINK
keywords: how to, set platform attribute of database engine
keywords: how to, return platform attribute of database engine
keywords: platform attributes, set/return for database engine
keywords: database engines, platform attribute for

---

The platform-specific attribute of the database (e.g. "*SQLOLEB" for SqlServer). 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string PlatformAttribute { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property PlatformAttribute As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp PlatformAttribute Type(*String) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property
 Value

String. Returns or sets a platform-specific attribute of the database engine.
Remarks

The **PlatformAttribute** property is used to distinguish between different database engines that can reside on the same machine. For instance, both DataGate for Windows and SQL Server can reside on the same machine. When accessing SQL Server databases, **PlatformAttribute** must be set to "*SQLOLEB". The setting of assumed "*DATALINK" is used for DataGate for Windows and DataGate for iSeries. Any value other than "*SQLOLEB" is presumed to be "*DATALINK". 
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* Register the database name "My Local" to specify the local database. */
  SourceProfile newDbProfile = new SourceProfile("My Local", false);
  newDbProfile.Server = "*LOCAL";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Label = "DG 7 Database";
  newDbProfile.PoolingTimeout = 0;
  /* Specify *DATALINK since we're connecting to the datagate engine. */
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Register the database name "My Local" to specIfy the local database. 
  Dim newDbProfile As New SourceProfile("My Local", False)
  newDbProfile.Server = "*LOCAL"
  newDbProfile.User = "User1"
  newDbProfile.Password = "password" ' Note- not very secure. 
  newDbProfile.Label = "DG 7 Database"
  newDbProfile.PoolingTimeout = 0
  ' SpecIfy *DATALINK since we're connecting to the datagate engine. 
  newDbProfile.PlatFormAttribute = "*DATALINK"
  newDbProfile.Text = "New database at valid ip address, on port 5047."
  ' Register the database name. 
  newDbProfile.Register()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro </span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateClientNamespace.html)

