---
title: AdgConnection Properties

Id: dcsAdgConnectionPropertiesMain
TocParent: dcsAdgConnectionClass
TocOrder: 3

keywords: properties [DCS 16.0 AdgConnection class
keywords: AdgConnection class, properties

---

[AdgConnection Overview](dcsAdgConnectionClass.html) 
Public Properties

<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ CurrentUserLibl](dcsAdgConnectionCurrentUserLiblProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Set-only property used to change the current library list of an open database connection.
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The [SourceProfile](dcsSourceProfileClass.html) object describing the currently open database connection, or if the **AdgConnection** object is in the 'Closed' state, the database connection to be opened when the [ Open](dcsAdgConnectionClassOpenMethod.html) method is called.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/property.bmp" width="16" height="16" border="0" /> [ State](dcsAdgConnectionClassStateProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The **System.Data.ConnectionState** value corresponding to the current state of the connection, 'Open' (1) or 'Closed' (0).
</td>
          </tr>
</table>

See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Members](dcsAdgConnectionMembers.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA DataGate Client Namespace](dcsDataGateClientNamespace.html)

