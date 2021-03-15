---
title: IDirectory Members

Id: dcsIDirectoryMembers
TocParent: dcsIDirectoryClass
TocOrder: 0

keywords: members [DCS 16.0 IDirectory class
keywords: IDirectory class, all members

---

[IDirectory Overview](dcsIDirectoryClass.html) 

Public Properties
<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ ItemList](dcsIDirectoryClassItemListProperty.html) 
</td>
            <td colspan="1" rowspan="1">

**ItemList** is a list of [IAdgObject](dcsIAdgObjectClass.html) references corresponding to the database object contents of an existing library.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" width="16" height="16" border="0" /> [ RemotePathName](dcsIDirectoryClassRemotePathNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

**RemotePathName** is the full path of a directory associated with the library represented by **IDirectory** , if any.
</td>
          </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="table3"  style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ AttachRemoteDirectory](dcsIDirectoryClassAttachRemoteDirectoryMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Attaches a remote directory to an database library object
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ CreateSubDirectory](dcsIDirectoryClassCreateSubDirectoryMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Creates a new library contained by the library represented by **IDirectory** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [Enumerate](dcsIDirectoryClassEnumerateMethod.html)
</td>
            <td colspan="1" rowspan="1">

Enumerate the object contents of the library represented by **IDirectory** with the supplied [AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html)
</td>
            <td colspan="1" rowspan="1">

Repair database files contained by the library, as specified by [ RepairOptions](dcsRepairOptionsEnumeration.html).
</td>
          </tr>
</table>

See Also

<dl />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)
      <br />
      [RepairOptions Enumeration](dcsRepairOptionsEnumeration.html)

