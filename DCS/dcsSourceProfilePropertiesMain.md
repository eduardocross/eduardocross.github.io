---
title: SourceProfile Properties

Id: dcsSourceProfilePropertiesMain
TocParent: dcsSourceProfileClass
TocOrder: 3

keywords: properties [DCS 16.0 SourceProfile class
keywords: SourceProfile class, properties

---

[SourceProfile Overview](dcsSourceProfileClass.html) 
Public Properties

<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" >
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ DatabaseName](dcsSourceProfileClassDatabaseNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The database name (or identifier) of this set of connection parameters.
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ InitialLibl](dcsSourceProfileClassInitialLiblProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Retrieves the current database’s initial library list.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Label](dcsSourceProfileClassLabelProperty.html) 
</td>
            <td colspan="1" rowspan="1">

For host platforms that support multiple databases, the label of the database to connect to. This is the name of the actual database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Password](dcsSourceProfileClassPasswordProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Password is a write-only property specifying the password for the user profile indicated by the User property. This property should only be set if the user profile has an associated password, and only after setting the **User** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [PasswordType](dcsSourceProfileClassPasswordTypeProperty.html)
</td>
            <td colspan="1" rowspan="1">

This property specifies the authentication method for initiating database sessions with the **Password** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ PlatformAttribute](dcsSourceProfileClassPlatformAttributeProperty.html) 
</td>
            <td colspan="1" rowspan="1">

This property is used when accessing SQL Server databases, and must be set to "*SQL" in this case. Older, unsupported versions of Acceler8DB may also assign the "library name" of the APPC partner program to this property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ PoolingTimeout](dcsSourceProfileClassPoolingTimeoutProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The amount of time (in minutes) in which a connection will remain idle in the pool until it is closed and removed from the pool. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Port](dcsSourceProfileClassPortProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The TCP/IP port number used to initiate the connection to the database server platform. This is the port that the server is configured to "listen" to for incoming connections (by default, Acceler8DB servers listen to port 5042).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Qualifier](dcsSourceProfileClassQualifierProperty.html) 
</td>
            <td colspan="1" rowspan="1">

This is a reserved property and should not be set by the user.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Server](dcsSourceProfileClassServerProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The network name of the server that contains the database (either a DNS hostname or TCP/IP address).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="height: 70px">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ Text](dcsSourceProfileClassTextProperty.html) 
</td>
            <td colspan="1" rowspan="1" style="height: 70px">

This property may be used to hold any comments about the database connection parameters. It can be used, for example, as a longhand name for the SourceProfile.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ User](dcsSourceProfileClassUserProperty.html) 
</td>
            <td colspan="1" rowspan="1">

A user/profile name for authenticating access to the server platform.
</td>
          </tr>
</table>

See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)
      <br />
      [ASNA DataGate Providers Namespace](dcsDataGateProvidersNamespace.html) 

