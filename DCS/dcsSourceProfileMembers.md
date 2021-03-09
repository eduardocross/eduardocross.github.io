---
title: SourceProfile Members

Id: dcsSourceProfileMembers
TocParent: dcsSourceProfileClass
TocOrder: 0

keywords: members [DCS 16.0 SourceProfile class
keywords: SourceProfile class, all members

---

[SourceProfile Overview](dcsSourceProfileClass.html) 
Public Constructors

<br />

<table class="dtTABLE" id="table4" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ SourceProfile Property](dcsSourceProfileConstructorsMain.html) 
</td>
            <td colspan="1" rowspan="1">

Overloaded. Initializes a new instance of the <span>SourceProfile</span> class.
</td>
          </tr>
</table>

Public Fields

<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1" style="height: 69px">

![public property" src="../Images/property.bmp" width="16" border="0](../Images/fields.bmp" x-maintain-ratio="TRUE" style="WIDTH:24px; HEIGHT:12px" width="24" height="12" border="0" /> [MaxSystemLibl](dcsMaxSystemLiblEnumeration.html) 
</td>
            <td colspan="1" rowspan="1" style="height: 69px">

The maximum number of library list entries used by all processes, which open this database as the system portion of their library list - 15. This field is read-only.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

![](Images/fields.bmp" x-maintain-ratio="TRUE" style="WIDTH:24px; HEIGHT:12px" width="24" height="12" border="0) [MaxUserLibl](dcsMaxUserLiblEnumeration.html) 
</td>
            <td colspan="1" rowspan="1">

The maximum number of new processes allowed in the user portion of the library list for a database - 25. This field is read-only.
</td>
          </tr>
</table>

Public Properties

<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" >
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ DatabaseName](dcsSourceProfileClassDatabaseNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The database name (or identifier) of this set of connection parameters.
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ InitialLibl](dcsSourceProfileClassInitialLiblProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Retrieves the current database’s initial library list.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Label](dcsSourceProfileClassLabelProperty.html) 
</td>
            <td colspan="1" rowspan="1">

For host platforms that support multiple databases, the label of the database to connect to. This is the name of the actual database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Password](dcsSourceProfileClassPasswordProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Password is a write-only property specifying the password for the user profile indicated by the User property. This property should only be set if the user profile has an associated password, and only after setting the **User** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16) [PasswordType](dcsSourceProfileClassPasswordTypeProperty.html)
</td>
              <td colspan="1" rowspan="1">

This property specifies the authentication method for initiating database sessions with the **Password** property.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ PlatformAttribute](dcsSourceProfileClassPlatformAttributeProperty.html) 
</td>
              <td colspan="1" rowspan="1">

This property is used when accessing SQL Server databases, and must be set to "*SQL" in this case. Older, unsupported versions of Acceler8DB may also assign the "library name" of the APPC partner program to this property.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ PoolingTimeout](dcsSourceProfileClassPoolingTimeoutProperty.html) 
</td>
              <td colspan="1" rowspan="1">

The amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool. 
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Port](dcsSourceProfileClassPortProperty.html) 
</td>
              <td colspan="1" rowspan="1">

The TCP/IP port number used to initiate the connection to the database server platform. This is the port that the server is configured to "listen" to for incoming connections (by default, Acceler8DB servers listen to port 5042).
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Qualifier](dcsSourceProfileClassQualifierProperty.html) 
</td>
              <td colspan="1" rowspan="1">

This is a reserved property and should not be set by the user.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Server](dcsSourceProfileClassServerProperty.html) 
</td>
              <td colspan="1" rowspan="1">

The network name of the server that contains the database (either a DNS hostname or TCP/IP address).
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ Text](dcsSourceProfileClassTextProperty.html) 
</td>
              <td colspan="1" rowspan="1">

This property may be used to hold any comments about the database connection parameters. It can be used, for example, as a longhand name for the SourceProfile.
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ User](dcsSourceProfileClassUserProperty.html) 
</td>
              <td colspan="1" rowspan="1">

A user/profile name for authenticating access to the server platform.
</td>
            </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px; height: 401px;" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Clone](dcsSourceProfileClassCloneMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns a copy of the <span>SourceProfile</span> object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Equals](dcsSourceProfileClassEqualsMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **true** if the [SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) objects being compared refer to the same object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ GetHashCode](dcsSourceProfileClassGetHashCodeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Invokes the <span>GetHashCode</span> method of the [SourceProfile constructor](dcsSourceProfileConstructorsMain.html).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ GetNames](dcsSourceProfileClassGetNamesMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns the currently registered database names available for use in a program.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ op_Equality](dcsSourceProfileClassop_EqualityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **true** if the references being compared refer to the same object. Otherwise, returns the value of the **Equals** method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ op_InEquality](dcsSourceProfileClassop_InequalityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns the opposite value returned by **op_Equality** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Register](dcsSourceProfileClassRegisterMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Saves the contents of the SourceProfile object to the system registry as a database name.<span style="MARGIN-BOTTOM: 0.8em"> </span>
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Unregister](dcsSourceProfileClassUnregisterMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes a registered database name from the system registry.
</td>
          </tr>
</table>

See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

