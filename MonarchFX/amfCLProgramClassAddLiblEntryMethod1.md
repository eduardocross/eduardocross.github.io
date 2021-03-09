---
title: CLProgram.AddLiblEntry(String)

Id: amfCLProgramClassAddLiblEntryMethod1
TocParent: amfCLProgramClassAddLiblEntryMethods
TocOrder: 10

---

This method adds a library name to the user portion of the library list.

#### Syntax
<pre class="syntax"> **BegSr AddLiblEntry Access(*Public) Type(Void)
   DclSrParm *libraryName*  Type(*String) Len(45)** </pre>

#### Parameters
<dl>
        <dt>
          <code> *libraryName* </code>
        </dt>
        <dd>

String. Specifies the name of the library being added to the user portion of the library list.
</dd>
</dl>

#### Remarks
This method adds the specified library name to the user portion of the library list after the current library list entry (if it exists) for the process in which the command was entered. Up to 250 libraries may exist in the user portion of the library list. Only one library name is added at a time with this method.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ AddLiblEntry Methods](amfCLProgramClassAddLiblEntryMethods.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
