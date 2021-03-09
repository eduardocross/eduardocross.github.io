---
title: DdsDataField.Alias Property

Id: amfDdsDataFieldClassAliasProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 10

keywords: Alias property
keywords: DdsDataField.Alias property
keywords: web controls, setting alternate field name for compiler
keywords: web controls, getting alternate field name for compiler
keywords: how to, set alternate field name for compiler
keywords: how to, get alternate field name for compiler
keywords: display files, alternate field name for compiler
keywords: Web server controls [ASNA.Monarch], field alias name
keywords: field controls, alias

---

Gets or sets an alternate field name for the field. 

#### Syntax
<pre class="prettyprint"> **BegProp Alias Access(*Public) Type(*String)
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
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
