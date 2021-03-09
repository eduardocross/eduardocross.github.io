---
title: DdsDecRange.Alias Property

Id: amfDdsDecRangeClassAliasProperty
TocParent: amfDdsDecRangeClassPropertiesMain

keywords: Alias property
keywords: DdsDecRange.Alias property
keywords: web controls, setting Alias
keywords: web controls, getting Alias
keywords: how to, set Alias
keywords: how to, get Alias
keywords: display files, Alias
keywords: Web server controls [ASNA.Monarch], Alias
keywords: field controls, Alias

---

Gets or sets the field name for the compiler to use for externally described files.

#### Syntax
<pre class="prettyprint"> **BegProp Alias Access(*Public) Type(string) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the alternate name for the field. This value must be different from all other alternative names and from all DDS field names in the record format.

#### Remarks
When the program is compiled, the alternative name is brought into the program instead of the DDS field name.

To set this property at design-time, click to the right of the property and enter the alternate name for the field.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDecRange Class](amfDdsDecRangeClass.html) <br /> [ DdsDecRange Class Members](amfDdsDecRangeClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

