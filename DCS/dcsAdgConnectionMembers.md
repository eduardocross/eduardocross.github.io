---
title: AdgConnection Members

Id: dcsAdgConnectionMembers
TocParent: dcsAdgConnectionClass
TocOrder: 0

keywords: members [DCS 16.0 AdgConnection class
keywords: AdgConnection class, all members

---

[AdgConnection Overview](dcsAdgConnectionClass.html) 
Public Constructors

<br />

<table class="dtTABLE" id="table4" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 77.71%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ AdgConnection](dcsAdgConnectionConstructorsMain.html) 

</td> <td colspan="1" rowspan="1"> <p>Overloaded. Initializes a new instance of the **AdgConnection** class, assigning an initial value to the **SourceProfile** property.
</td>
          </tr>
</table>

Public Properties

<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ CurrentUserLibl](dcsAdgConnectionCurrentUserLiblProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Set-only property used to change the current library list of an open database connection.
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The [SourceProfile](dcsSourceProfileClass.html) object describing the currently open database connection, or if the<span> **AdgConnection** </span> object is in the 'Closed' state, the database connection to be opened when the **Open** method is called.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ State](dcsAdgConnectionClassStateProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The **System.Data.ConnectionState** value corresponding to the current state of the connection, 'Open' (1) or 'Closed' (0).
</td>
          </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="table2" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) 
</td>
            <td colspan="1" rowspan="1">

Overloaded method that begins an automatic database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) with combinations of transaction locking level, name, and command options parameters specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) 
</td>
            <td colspan="1" rowspan="1">

Overloaded method that begins a manual database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) object with combinations of transaction locking level, name, and command options parameters specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Clone](dcsAdgConnectionClassCloneMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns a copy of the **AdgConnection** object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Close](dcsAdgConnectionClassCloseMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Closes the connection to the database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Dispose](dcsAdgConnectionClassDisposeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Releases the resources used by the object. If in the 'Open' state, the **Close** method is invoked.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Equals](dcsAdgConnectionClassEqualsMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **True** if the S **ourceProfile** properties of the objects being compared refer to the same object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ GetHashCode](dcsAdgConnectionClassGetHashCodeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Invokes the GetHashCode method of the **SourceProfile** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ op_Equality](dcsAdgConnectionclassopEqualityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **True** if the references being compared refer to the same object. Otherwise, returns the value of the **Equals** method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ op_InEquality](dcsAdgConnectionClassopInequalityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns the opposite value returned by **op_Equality** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Open](dcsAdgConnectionClassOpenMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Opens a database connection.
</td>
          </tr>
</table>

See Also

[AdgConnection Class](dcsAdgConnectionClass.html) <br /> [SourceProfile Class](dcsSourceProfileClass.html) <br /> [IAdgTransaction Class](dcsIAdgTransactionClass.html) 
