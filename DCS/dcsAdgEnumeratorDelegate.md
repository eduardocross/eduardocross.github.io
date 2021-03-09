---
title: AdgEnumerator Delegate

Id: dcsAdgEnumeratorDelegate
TocParent: dcsWhatsNewDelegates
TocOrder: 0

keywords: delegates [DCS 16.0 AdgEnumerator
keywords: AdgEnumerator delegate
keywords: how to, enumerate database contents of library, delegate
keywords: database files, enumerate object contents of, delegate
keywords: database file members, enumerate object contents of, delegate
keywords: database libraries, enumerate object contents of, delegate

---

A delegate provided to the [IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html) method for processing [IAdgObject](dcsIAdgObjectClass.html) references corresponding to the contents of a database library. This delegate is also used in the [ILibraryList.EnumerateCurrentSystem](dcsILibraryListClassEnumerateCurrentSystemMethod.html) and [ILibraryList.EnumerateCurrentUser](dcsILibraryListClassEnumerateCurrentUserMethod.html) methods for processing [ILibraryList](dcsILibraryListClass.html) references corresponding to the contents of a library list.

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 
<pre class="prettyprint">
[ C# ] **Public delegate void AdgEnumerator (IAdgObject iAdgObject);** </pre>
      <pre class="prettyprint">
[ AVR.NET ] **DclDelegate AdgEnumerator Access(*public)
  DclSrParm iAdgObject Type(IAdgObject)** </pre>

Remarks

The **IDirectory.Enumerate** and **ILibraryList** enumerate methods are similar in that they reference an **IAdgObject** . **IDirectory.Enumerate** process each file and library object within a single library represented by **IDirectory** , while the **ILibraryList** enumerate methods process each file and library object with the entire library list represented by **ILibraryList** (directory names associated with each applications database connection). 

### IDirectory.Enumerate
The user program defines a method with this prototype, then passes a reference to it in **IDirectory.Enumerate** . The delegate is repeatedly called from **IDirectory.Enumerate** for each file and library object contained by the library represented by **IDirectory** . Only after the delegate has been called for each object in the library does **IDirectory.Enumerate** return to the caller. 

The *iAdgObject* parameter is an **IAdgObject** reference representing a file or library object contained by the library. Currently, only certain properties and methods of *iAdgObject* may be used prior to the completion of **IDirectory.Enumerate** (that is, from within the delegate's code). See [ToString](#allowed">IAdgObject Methods and Properties</a> below.
<br />

### ILibraryList.EnumerateCurrentSystem
The user program defines a method with this prototype, then passes a reference to it in **ILibraryList.EnumerateCurrentSystem** . The delegate is repeatedly called from **EnumerateCurrentSystem** for each file and library object contained by the system and user portion of the library list represented by **ILibraryList** . Only after the delegate has been called for each object in the library list does **EnumerateCurrentSystem** return to the caller. 

The *iAdgObject* parameter is an **IAdgObject** reference representing a library list entry object contained by the system and user portion of the library list. Currently, only certain properties and methods of *iAdgObject* may be used prior to the completion of **EnumerateCurrentSystem** (that is, from within the delegate's code). See <a href="#allowed">IAdgObject Methods and Properties</a> below. 

### ILibraryList.EnumerateCurrentUser
The user program defines a method with this prototype, then passes a reference to it in **ILibraryList.EnumerateCurrentUser** . The delegate is repeatedly called from **EnumerateCurrentUser** for each file and library object contained by the user portion of the library list represented by **ILibraryList** . Only after the delegate has been called for each object in the library list does **EnumerateCurrentSystem** return to the caller. 

The *iAdgObject* parameter is an **IAdgObject** reference representing a library list entry object contained by the user portion of the library list. Currently, only certain properties and methods of *iAdgObject* may be used prior to the completion of **EnumerateCurrentSystem** (that is, from within the delegate's code). See <a href="#allowed">IAdgObject Methods and Properties</a> below.

###  <a name="allowed">IAdgObject Methods and Properties</a> 
The following is a list of **IAdgObject** methods and properties that can be invoked on *iAdgObject* from within the delegate code:
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 20%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							IAdgObject<br />
							Method/Property
						</th>
            <th colspan="1" rowspan="1">
							IDirectory<br />
							Enumerate
						</th>
            <th colspan="1" rowspan="1">
							ILibraryList<br />
							EnumerateCurrentSystem
						</th>
            <th colspan="1" rowspan="1">
							ILibraryList<br />
							EnumerateCurrentUser
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<a href="dcsIAdgObjectClassToStringMethod.html) method (the object path name)
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ObjectID](dcsIAdgObjectClassObjectIDProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ParentID](dcsIAdgObjectClassParentIDProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes, except root library will be zero.
</td>
            <td colspan="1" rowspan="1">

Yes, except root library will be zero.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Text](dcsIAdgObjectClassTextProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[IsSystemObject](dcsIAdgObjectClassIsSystemObjectProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[DateCreated](dcsIAdgObjectClassDateCreatedProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[DateModified](dcsIAdgObjectClassDateModifiedProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[DateReferenced](dcsIAdgObjectClassDateReferencedProperty.html) property
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
            <td colspan="1" rowspan="1">

Yes
</td>
          </tr>
</table>

<br />

Invoking any method or property on *iAdgObject* other than those listed above from within the delegate code produces unpredictable results or abnormal termination of the **enumerate** call.

Note that following completion of **enumerate** , no restrictions are placed on the **IAdgObject** references given by *iAdgObject* . Thus if the user program must invoke a method or property other than those listed above, it may save the references given by *iAdgObject* and invoke the restricted method or property upon completion of **enumerate** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [EnumerateCurrentSystem 
					Method](dcsILibraryListClassEnumerateCurrentSystemMethod.html)
      <br />
      [EnumerateCurrentUser 
					Method](dcsILibraryListClassEnumerateCurrentUserMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

