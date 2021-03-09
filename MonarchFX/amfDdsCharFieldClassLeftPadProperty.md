---
title: DdsCharField.LeftPad Property

Id: amfDdsCharFieldClassLeftPadProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 57

keywords: LeftPad property
keywords: DdsCharField.LeftPad property
keywords: Web server controls [ASNA.Monarch], field LeftPad
keywords: how to, set field control LeftPad
keywords: how to, get field control LeftPad
keywords: display files, setting field control LeftPad
keywords: display files, getting field control LeftPad
keywords: web controls, setting field control LeftPad
keywords: web controls, getting field control LeftPad
keywords: field controls, LeftPad

---

Prepends the field data with blanks or zeroes to fill out the length of field LeftPad.

#### Syntax
<pre class="syntax"> **BegProp LeftPad Access(*Public) Type(*Enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Values include: Blanks, Zeroes, and None. Defaults to **None** . 

#### Remarks
**LeftPad** is used to add blanks or zeroes to the full length of a field before the actual data, often for formatting reasons. This property is the equivalent of the DDS Keywords CHECK(RB), CHECK(RZ), and AUTO(RAB), AUTO(RAZ). It is invoked in Monarch and Wings handling of those keywords.

To set this property at design time, click on the right side of the property window and select true or false from the drop down.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Members](amfDdsCharFieldClassMembers.html) <br /> [ ValuesStyle Property](amfDdsDataFieldClassValuesStyleProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
