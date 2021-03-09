---
title: CLProgram.AddLiblEntry(string,LiblPosition,string)

Id: amfCLProgramClassAddLiblEntryMethod2
TocParent: amfCLProgramClassAddLiblEntryMethods
TocOrder: 20

keywords: LiblPosition enumeration, used by

---

This method adds a library name to the user portion of the library list (as specified by *position* and *referenceLibraryName* ) for the process in which the command was entered.

#### Syntax
<pre class="syntax"> **BegSr AddLiblEntry Access(*Public) Type(Void)
   DclSrParm *libraryName*  Type(*String)
   DclSrParm *position*  Type(ASNA. AtaGate.Client.LiblPosition)
   DclSrParm *referenceLibraryName*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *libraryName* </code>
        </dt>
        <dd>

String. Specifies the name of the library being added to the user portion of the library list.
</dd>
        <dt>
          <code> *position* </code>
        </dt>
        <dd>

**ASNA.DataGate.Client.LiblPosition** specifying the position in the user portion of the library list where the *libraryName* is to be added relative to the position of the *referenceLibraryName* . If *position* is **First** or **Last** , the *referenceLibraryName* is ignored. If *position* is **Before** , **After** , or **Replace** , then the *libraryName* is placed before, after, or replaces the referenceLibraryName parameter respectively.
</dd>
        <dt>
          <code> *referenceLibraryName* </code>
        </dt>
        <dd>

String. The name of a library that already exists in the user portion of the library list. The library specified in the *libraryName* parameter is added relative to the position of this library. If *position* is **First** or **Last** , then this parameter is ignored.
</dd>
</dl>

#### Remarks
This method adds the specified library name to the user portion of the library list (as specified by <code> *position* </code> and <code> *referenceLibraryName)* </code> for the process in which the command was entered. Up to 250 libraries may exist in the user portion of the library list. Only one library name is added at a time with this method. The user can specify whether the library is added to the beginning or to the end of the library list. In addition to this, the user can specify whether the library is added before, after, or replaces an existing library in the library list.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ AddLiblEntry Methods](amfCLProgramClassAddLiblEntryMethods.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
