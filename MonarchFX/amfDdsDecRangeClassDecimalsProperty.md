---
title: DdsDecRange.Decimals Property

Id: amfDdsDecRangeClassDecimalsProperty
TocParent: amfDdsDecRangeClassPropertiesMain

keywords: Decimals property
keywords: DdsDecRange.Decimals property
keywords: web controls, setting Alias aidkey
keywords: web controls, getting Alias aidkey
keywords: how to, set Alias aidkey
keywords: how to, get Alias aidkey
keywords: display files, Alias aidkey
keywords: Web server controls [ASNA.Monarch], Alias aidkey
keywords: field controls, Alias aidkey

---

Gets or sets the field name for the compiler to use for externally described files.

#### Syntax
<pre class="prettyprint"> **BegProp Decimals Access(*Public) Type(ASNA.Monarch.WebDspF.AidKey) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the alternate name for the field. This value must be different from all other alternative names and from all DDS field names in the record format.

#### Remarks
When the program is compiled, the alternative name is brought into the program instead of the DDS field name.

To set this property at design-time, click to the right of the property and enter the desired value.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDecRange Class](amfDdsDecRangeClass.html) <br /> [ DdsDecRange Class Members](amfDdsDecRangeClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

