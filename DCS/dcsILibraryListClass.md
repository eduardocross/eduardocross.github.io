---
title: ILibraryList Interface

Id: dcsILibraryListClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 13

keywords: classes [DCS 16.0 ILibraryList class
keywords: interfaces [DCS 16.0 ILibraryList class
keywords: ILibraryList class
keywords: ILibraryList class, about ILibraryList class
keywords: library lists, about
keywords: database files, about libraries
keywords: database libraries, about ILibraryList class

---

**ILibraryLists** models an object management interface to the databases' library list. A library list is an ordered set of directory names associated with each applications database connection.

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

ASNA.DataGate.Client.IAdgObject<br /> **ASNA.DataGate.Client.<span>ILibraryList</span>** 
<pre class="prettyprint">
  [Prototype in C#] public interface ILibraryList</pre>
      <pre class="prettyprint"> [Prototype in
  Visual RPG] BegInterface ILibraryList access (*public)</pre>

Thread Safety

In DCS implementations of **ILibraryList** , instance members are not guaranteed to be thread safe.
Remarks

The **ILibraryList** class models the library list object of the database server containing an ordered set of directory names associated with each applications database connection.

A valid **ILibraryList** reference may be obtained from DCS with:

- The [AdgFactory.NewLibraryList](dcsAdgFactoryClassNewLibraryListMethod.html)
					method that instantiates a new instance of **ILibraryList** , given 
					an [AdgConnection](dcsAdgConnectionClass.html)
				reference.
- An instance of **ILibraryList** representing an existing databases' library list may be returned when using the [ EnumerateCurrentSystem](dcsILibraryListClassEnumerateCurrentSystemMethod.html) method.
- An instance of **ILibraryList** representing an existing databases' library list for the user may be returned when using the [EnumerateCurrentUser](dcsILibraryListClassEnumerateCurrentUserMethod.html) method.

**EnumerateCurrentSystem** and **EnumerateCurrentUser** calls the provided [AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate for each object contents of the system and user portion of the library list, or for each object contents of the user portion of the library list, respectively.

[AddEntry](dcsILibraryListClassAddEntryMethod.html) method adds a single library list entry using [LiblPosition](dcsLiblPositionEnumeration.html) enumeration to specify the position in the library list to add the new library list entry. [ RemoveEntry](dcsILibraryListClassRemoveEntryMethod.html) method removes a single entry from the library list.

[CurrentSystemLibs](dcsILibraryListClassCurrentSystemLibsProperty.html) property returns a string array of the current library list established for the database for both the system and user portion of the library list.

[CurrentUserLibs](dcsILibraryListClassCurrentUserLibsProperty.html) property sets or returns a string array of the current library list established for the database for the user portion of the library list.

[SystemConfig](dcsILibraryListClassSystemConfigProperty.html) property sets or returns a string array containing a list of the system and user portion of the available directories in the library list.

[UserConfig](dcsILibraryListClassUserConfigProperty.html) property sets or returns a string array containing a list of the user portion of the available directories in the library list.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ILibraryList Members](dcsILibraryListMembers.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgFactory.NewLibraryList](dcsAdgFactoryClassNewLibraryListMethod.html)
      <br />
      [LiblPosition Enumeration](dcsLiblPositionEnumeration.html)
      <br />
      [AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

