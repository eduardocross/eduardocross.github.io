---
title: ILibraryList Members

Id: dcsILibraryListMembers
TocParent: dcsILibraryListClass
TocOrder: 0

keywords: members [DCS 16.0 ILibraryList class
keywords: ILibraryList class, all members

---

[ILibraryList Overview](dcsILibraryListClass.html) 
Public Properties

<br />

<table class="dtTABLE" id="table4" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [CurrentSystemLibs](dcsILibraryListClassCurrentSystemLibsProperty.html)
</td>
            <td colspan="1" rowspan="1">

Returns a string array containing a list of the current system and user portion of the directories in the library list represented by **ILibraryList** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [CurrentUserLibs](dcsILibraryListClassCurrentUserLibsProperty.html)
</td>
            <td colspan="1" rowspan="1">

Sets or returns a string array containing a list of the user portion of the directories in the current library list represented by **ILibraryList** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [SystemConfig](dcsILibraryListClassSystemConfigProperty.html)
</td>
            <td colspan="1" rowspan="1">

Sets or returns a string array containing a list of the system and user portion of the available directories in the library list represented by **ILibraryList** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [UserConfig](dcsILibraryListClassUserConfigProperty.html)
</td>
            <td colspan="1" rowspan="1">

Sets or returns a string array containing a list of the user portion of the available directories in the library list represented by **ILibraryList** .
</td>
          </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [AddEntry](dcsILibraryListClassAddEntryMethod.html)
</td>
            <td colspan="1" rowspan="1">

Adds a library list entry to a database in the library represented by **ILibraryList** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [EnumerateCurrentSystem](dcsILibraryListClassEnumerateCurrentSystemMethod.html)
</td>
            <td colspan="1" rowspan="1">

Enumerates the object contents of the system and user portion of the library list represented by **ILibraryList** , with the supplied [ AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="../Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [EnumerateCurrentUser](dcsILibraryListClassEnumerateCurrentUserMethod.html)
</td>
            <td colspan="1" rowspan="1">

Enumerates the object contents of the user portion of the library list represented by **ILibraryList** , with the supplied [ AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [RemoveEntry](dcsILibraryListClassRemoveEntryMethod.html)
</td>
            <td colspan="1" rowspan="1">

Removes a library list entry from a database in the library represented by **ILibraryList** .
</td>
          </tr>
</table>

See Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)

