---
title: AdgConnection Methods

Id: dcsAdgConnectionMethodsMain
TocParent: dcsAdgConnectionClass
TocOrder: 2

keywords: methods [DCS 16.0 AdgConnection class
keywords: AdgConnection class, methods

---

[AdgConnection Overview](dcsAdgConnectionClass.html) 
Public Methods

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) 
</td>
            <td colspan="1" rowspan="1">

Overloaded method that begins an automatic database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) with combinations of transaction locking level, name, and command options parameters specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) 
</td>
            <td colspan="1" rowspan="1">

Overloaded method that begins a manual database transaction creating an instance of an [IAdgTransaction](dcsIAdgTransactionClass.html) object with combinations of transaction locking level, name, and command options parameters specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Clone](dcsAdgConnectionClassCloneMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns a copy of the **AdgConnection** object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Close](dcsAdgConnectionClassCloseMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Closes the connection to the database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Dispose](dcsAdgConnectionClassDisposeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Releases the resources used by the object. If in the 'Open' state, the **Close** method is invoked.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Equals](dcsAdgConnectionClassEqualsMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **True** if the [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html)<strong />properties of the objects being compared refer to the same object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ GetHashCode](dcsAdgConnectionClassGetHashCodeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Invokes the GetHashCode method of the **SourceProfile** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ op_Equality](dcsAdgConnectionclassopEqualityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns **True** if the references being compared refer to the same object. Otherwise, returns the value of the **Equals** method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ op_InEquality](dcsAdgConnectionClassopInequalityMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Returns the opposite value returned by **op_Equality** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ Open](dcsAdgConnectionClassOpenMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Opens a database connection.
</td>
          </tr>
</table>

See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)

