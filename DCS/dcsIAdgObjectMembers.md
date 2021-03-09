---
title: IAdgObject Members

Id: dcsIAdgObjectMembers
TocParent: dcsIAdgObjectClass
TocOrder: 0

keywords: members [DCS 16.0 IAdgObject class
keywords: IAdgObject class, all members

---

[IAdgObject Overview](dcsIAdgObjectClass.html) 
Public Properties

<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html)
</td>
            <td colspan="1" rowspan="1">

Identifies the type (file, library, library list, member) of the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html)
</td>
            <td colspan="1" rowspan="1">

Identifies the secondary type of the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AuthorityEntries](dcsIAdgObjectClassAuthorityEntriesProperty.html)
</td>
            <td colspan="1" rowspan="1">

An array of [AuthorityEntry](dcsAuthorityEntryClass.html) objects, collectively describing the user authorities the database provider has assigned to the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Bases](dcsIAdgObjectClassBasesProperty.html)
</td>
            <td colspan="1" rowspan="1">

A single-dimension array of strings containing path names, denoting the set of objects upon which the database object represented by **IAdgObject** is based.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [DateCreated](dcsIAdgObjectClassDateCreatedProperty.html)
</td>
            <td colspan="1" rowspan="1">

A timestamp recorded by the database provider when the database object is created.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [DateModified](dcsIAdgObjectClassDateModifiedProperty.html)
</td>
            <td colspan="1" rowspan="1">

A timestamp recorded by the database provider when the database object is modified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [DateReferenced](dcsIAdgObjectClassDateReferencedProperty.html)
</td>
            <td colspan="1" rowspan="1">

A timestamp recorded by the database provider when the database object is referenced.
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Dependents](dcsIAdgObjectClassDependentsProperty.html)
</td>
            <td colspan="1" rowspan="1">

An array of [Dependent](dcsDependentClass.html) objects denoting the set of objects that depend upon the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [IsSystemObject](dcsIAdgObjectClassIsSystemObjectProperty.html)
</td>
            <td colspan="1" rowspan="1">

Indicates if the existing database object represented by **IAdgObject** is a "system" object, when **IAdgObject** is obtained through [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ObjectID](dcsIAdgObjectClassObjectIDProperty.html)
</td>
            <td colspan="1" rowspan="1">

Identifies the object represented by IAdgObject.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Owner](dcsIAdgObjectClassOwnerProperty.html)
</td>
            <td colspan="1" rowspan="1">

The user or group account that owns the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [OwnerIsGroup](dcsIAdgObjectClassOwnerIsGroupProperty.html)
</td>
            <td colspan="1" rowspan="1">

Specifies [Owner](dcsIAdgObjectClassOwnerProperty.html) is a group account when **True** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ParentID](dcsIAdgObjectClassParentIDProperty.html)
</td>
            <td colspan="1" rowspan="1">

Identifies a parent database object of the object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [PrimaryGroup](dcsIAdgObjectClassPrimaryGroupProperty.html)
</td>
            <td colspan="1" rowspan="1">

The primary group assigned to a database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Schema](dcsIAdgObjectClassSchemaProperty.html)
</td>
            <td colspan="1" rowspan="1">

The XML schema collection DCS uses to validate XML document fragments describing **IAdgObject** instances and the database objects they represent.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [SortByName](dcsIAdgObjectClassSortByNameProperty.html)
</td>
            <td colspan="1" rowspan="1">

Returns an **IComparer** instance suitable for comparing instances of **IAdgObject** based on the value returned by their [ ToString](dcsIAdgObjectClassToStringMethod.html) method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [SortByNameCaseInsensitive](dcsIAdgObjectClassSortByNameCaseInsensitiveProperty.html)
</td>
            <td colspan="1" rowspan="1">

Returns an **IComparer** instance suitable for comparing instances of **IAdgObject** based on the value returned by their [ ToString](dcsIAdgObjectClassToStringMethod.html) method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Text](dcsIAdgObjectClassTextProperty.html)
</td>
            <td colspan="1" rowspan="1">

The textual description or comments associated with a database object.
</td>
          </tr>
</table>

Public Methods

<br />

<table class="dtTABLE" id="table2" style="MARGIN-TOP: 4pt; MARGIN-BOTTOM: 4pt; border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Create](dcsIAdgObjectClassCreateMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Creates a new database object reflecting the current state of **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Duplicate](dcsIAdgObjectClassDuplicateMethod.html)
</td>
            <td colspan="1" rowspan="1">

Creates a duplicate of the database object represented by **IAdgObject** , with parameters for specifying the location and name of the duplicated object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [GrantAuthority](dcsIAdgObjectClassGrantAuthorityMethod.html)
</td>
            <td colspan="1" rowspan="1">

Adds a user authorization to a database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Lock](dcsIAdgObjectClassLockMethod.html)
</td>
            <td colspan="1" rowspan="1">

Engages the database provider's object locking facility to set a lock restricting access to the database object corresponding to **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [MoveTo](dcsIAdgObjectClassMoveToMethod.html)
</td>
            <td colspan="1" rowspan="1">

Moves a database library or file represented by **IAdgObject** to a specified library.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ReadBases](dcsIAdgObjectClassReadBasesMethod.html)
</td>
            <td colspan="1" rowspan="1">

Sets base object information for the **IAdgObject** by reading an XML document fragment.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Remove](dcsIAdgObjectClassRemoveMethod.html)
</td>
            <td colspan="1" rowspan="1">

Removes an existing database object from the database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Rename](dcsIAdgObjectClassRenameMethod.html)
</td>
            <td colspan="1" rowspan="1">

Renames an object without changing its location in the database.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [RevokeAuthority](dcsIAdgObjectClassRevokeAuthorityMethod.html)
</td>
            <td colspan="1" rowspan="1">

Removes a previously granted or denied user authorization to a database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ToString](dcsIAdgObjectClassToStringMethod.html)
</td>
            <td colspan="1" rowspan="1">

Returns the path name of the database object represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Unlock](dcsIAdgObjectClassUnlockMethod.html)
</td>
            <td colspan="1" rowspan="1">

Reverses the effects of a previously successful [ Lock](dcsIAdgObjectClassLockMethod.html) method call.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [WriteBases](dcsIAdgObjectClassWriteBasesMethod.html)
</td>
            <td colspan="1" rowspan="1">

Creates an XML document fragment describing the base objects of a single database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [WriteXml](dcsIAdgObjectClassWriteXmlMethods.html)
</td>
            <td colspan="1" rowspan="1">

Produces an XML document fragment representing the **IAdgObject** instance.
</td>
          </tr>
</table>

See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)

