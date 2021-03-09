---
title: ILibraryList.CurrentSystemLibs Property

Id: dcsILibraryListClassCurrentSystemLibsProperty
TocParent: dcsILibraryListProperties
TocOrder: 0

keywords: CurrentSystemLibs property
keywords: ILibraryList.CurrentSystemLibs property
keywords: directories, setting user portion of directories in current library list
keywords: directories, getting user portion of directories in current library list
keywords: library lists, setting user portion of directories in
keywords: library lists, getting user portion of directories in
keywords: how to, set user portion of directories in the current library list
keywords: how to, get user portion of directories in the current library list
keywords: directories, setting system portion of directories in current library list
keywords: directories, getting system portion of directories in current library list
keywords: library lists, setting system portion of directories in
keywords: library lists, getting system portion of directories in
keywords: how to, set system portion of directories in the current library list
keywords: how to, get system portion of directories in the current library list

---

**CurrentSystemLibs** returns a string array containing a list of the current system and user portion of the directories in the library list represented by **ILibraryList** . 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **protected string[] CurrentSystemLibs { get;}** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Protected Property CurrentSystemLibs As String()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp CurrentSystemLibs Type(*string) Access(*Protected) Rank(1)
     BegGet;** 
      </pre>

Return Value

**String array** . Read-only. A string array containing a list of the system and user portion of the directories in the library list represented by **ILibraryList** .
Remarks

Use [CurrentUserLibs](dcsILibraryListClassCurrentUserLibsProperty.html) property to set and return just the user portion of the library list.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [ILibraryList Class Members](dcsILibraryListMembers.html)
      <br />
      [CurrentUserLibs Property](dcsILibraryListClassCurrentUserLibsProperty.html)
      <br />
      [AdgConnection.CurrentUserLibl](dcsAdgConnectionCurrentUserLiblProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

