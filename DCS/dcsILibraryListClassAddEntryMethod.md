---
title: ILibraryList.AddEntry Method

Id: dcsILibraryListClassAddEntryMethod
TocParent: dcsILibraryListMethods
TocOrder: 0

keywords: AddEntry method
keywords: ILibraryList.AddEntry method
keywords: LiblPosition enumeration, used by
keywords: enumerations [DCS 16.0 LiblPosition, used by
keywords: library lists, add entries to a database
keywords: database library lists, add entries
keywords: how to, add entries to database library list

---

**AddEntry** adds a library list entry to a database in the library represented by [ILibraryList](dcsILibraryListClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void AddEntry(_
   string path _
   ASNA.DataGate.Client.LiblPosition pos _
   string refLib<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Function AddEntry(
   ByVal path As string,
   ByVal pos As [ASNA.DataGate.Client.LiblPosition](dcsLiblPositionEnumeration.html) 
   ByVal refLib As string<br />) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AddEntry Access(*Public) Type(Void)
   DclSrParm path Type(*string) 
   DclSrParm pos Type([ASNA.DataGate.Client.LiblPosition](dcsLiblPositionEnumeration.html))
   DclSrParm refLib Type(*string)** 
      </pre>

Parameters

<dl>
        <dt>
 *path* 
        </dt>
        <dd>

String. Specifies the path name of the database library to add to the library list.
</dd>
        <dt>
 *pos* 
        </dt>
        <dd>

[LiblPosition](dcsLiblPositionEnumeration.html) values indicating the position in the library list to add the new library list entry.
</dd>
        <dt>
 *refLib* 
        </dt>
        <dd>

String. Specifies the reference library. If **LiblPosition** is **Before** , **After** , or **Replace** , then this library is used for reference. If **LiblPosition** is **System** , **First** , or **Last** , then this parameter is ignored. 
</dd>
</dl>

Remarks

Use this method to create a library entry whose parent library is represented by **ILibraryList** . Note that creating such a "sub-library" is a database provider-dependent function. For example, on System i databases, only the root library "/" (also known as QSYS) can contain other libraries. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span>
See Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [ILibraryList Class Members](dcsILibraryListMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

