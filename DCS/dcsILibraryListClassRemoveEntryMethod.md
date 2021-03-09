---
title: ILibraryList.RemoveEntry Method

Id: dcsILibraryListClassRemoveEntryMethod
TocParent: dcsILibraryListMethods
TocOrder: 3

keywords: RemoveEntry method
keywords: ILibraryList.RemoveEntry method
keywords: library lists, remove entry from a database
keywords: database library lists, remove entries
keywords: how to, remove entries from database library list

---

**RemoveEntry** removes a library list entry from a database in the library represented by [ILibraryList](dcsILibraryListClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void RemoveEntry(_
   string path<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Function RemoveEntry(
   ByVal path As string<br />) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr RemoveEntry Access(*Public) Type(Void)
   DclSrParm path Type(*string)** 
      </pre>

Parameters

<dl>
        <dt>
 *path* 
        </dt>
        <dd>

String. Specifies the path name of the database library to remove from the library list.
</dd>
</dl>

Remarks

A library list entry can not be removed if it's on an active user's library list. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See 
Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [ILibraryList Members](dcsILibraryListMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

