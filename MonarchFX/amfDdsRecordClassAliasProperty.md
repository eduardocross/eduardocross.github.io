---
title: DdsRecord.Alias Property

Id: amfDdsRecordClassAliasProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 10

keywords: Alias property
keywords: DdsRecord.Alias property
keywords: web controls, setting alternate format name for compiler
keywords: web controls, getting alternate format name for compiler
keywords: subfiles, setting alternate format name for compiler
keywords: subfiles, getting alternate format name for compiler
keywords: subfile controls, setting alternate format name for compiler
keywords: subfile controls, getting alternate format name for compiler
keywords: subfile records, setting alternate format name for compiler
keywords: subfile records, getting alternate format name for compiler
keywords: records, setting alternate format name for subfile for compiler
keywords: records, getting alternate format name for subfile for compiler
keywords: formats, setting alternate name for compiler
keywords: formats, getting alternate name for compiler
keywords: how to, set alternate record format name for compiler
keywords: how to, get alternate record format name for compiler
keywords: display files, alternate record format name for compiler

---

Gets or sets an alternate format name to be used by the compiler.

#### Syntax
<pre class="prettyprint"> **BegProp Alias Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The alternate format name for the record. This value must be different from all other alternative names and from all DDS field names in the record format.

#### Remarks
When the program is compiled the alternative name is brought into the program instead of the DDS record (ID) name.

To set this property at design-time, click to the right of the property and enter the alternate name for the field.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
