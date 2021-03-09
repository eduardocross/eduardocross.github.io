---
title: SourceProfile.Register Method

Id: dcsSourceProfileClassRegisterMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 6

keywords: Register method
keywords: SourceProfile.Register method
keywords: Windows registry, register database names
keywords: database names, create and update registry
keywords: registered database names, create and update
keywords: connections, database named registered
keywords: database connections, registry database name created or updated
keywords: how to, update registered name of database
keywords: how to, create registered name of database

---

## <span style="font-color:red">Deprecated</span>
Replaced by [DatabaseName.Register](DCSDataBaseNameClassRegisterMethod.html)

Saves the contents of the **SourceProfile** object to the system registry as a database name.
<span style="MARGIN-BOTTOM: 0.8em" />
      <pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Register();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub Register()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSub Register Access(*Public)** 
      </pre>

Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
								Exception Type
							</th>
            <th colspan="1" rowspan="1">
								Condition
							</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException
</td>
            <td colspan="1" rowspan="1">

See table below.
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property. 
<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
								Value of dgException.Error
							</th>
            <th colspan="1" rowspan="1">
								Condition
							</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The database name string (specified by the SourceProfile constructor) contains an invalid character. Path delimiter characters ('/' and '\') are not permitted in database names, unless used with "*PUBLIC"; for example "*PUBLIC/MyDB" is a valid database name, but "Copyof/MyDB" is not.
</td>
          </tr>
</table>

Example <p>The following example retrieves a database name called "Asna 400 db" (in the process of constructing the SourceProfile object), changes the user and password, and then saves the changes by calling Register. 
<pre class="prettyprint">  Using ASNA.DataGate.Providers
  DclfldName(AsnaDbName) Type(SourceProfile)
  AsnaDbName = *New SourceProfile("Asna 400 db")
  AsnaDbName.User = "NewUser"
  AsnaDbName.Password = "NewPasswd"
  AsnaDbName. Register()			</pre>

Examples 

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* When we specify false with this constructor, we're
   * telling Datagate not to get information from the
   * registry. Thus we can use it to create an entirely
   * new database name. */
  SourceProfile newDbProfile = new SourceProfile("New database", false);
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' When we specIfy false with this constructor, we're
  ' telling Datagate not to get inFormation from the
  ' registry. Thus we can use it to create an entirely
  ' new database name. 
  Dim newDbProfile As New SourceProfile("New database", False)
  newDbProfile.Server = "valid ip address"
  newDbProfile.User = "User1"
  newDbProfile.Password = "password" ' ' Note- not very secure.
  newDbProfile.Port = 5047
  newDbProfile.PoolingTimeout = 0
  newDbProfile.PlatformAttribute = "*DATALINK"
  newDbProfile.Text = "New database at valid ip address, on port 5047."
  ' Register the database name.
  newDbProfile.Register()
</pre>

Requirements

**Namespace: [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)** 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [Unregister Method](dcsSourceProfileClassUnregisterMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

