---
title: DdsDataField.PositionCursor Property

Id: amfDdsDataFieldClassPositionCursorProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 70

keywords: PositionCursor property
keywords: DdsDataField.PositionCursor property
keywords: web controls, setting field control position cursor attribute
keywords: web controls, getting field control position cursor attribute
keywords: how to, set field control position cursor attribute
keywords: how to, get field control position cursor attribute
keywords: display files, setting field control position cursor attribute
keywords: display files, getting field control position cursor attribute
keywords: Web server controls [ASNA.Monarch], field control position cursor attribute
keywords: field controls, position cursor attribute

---

Gets or sets a string containing the position cursor attribute value for the field.

#### Syntax
<pre class="prettyprint"> **BegProp PositionCursor Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the position cursor attribute for the field.

#### Remarks
Set this property to position the cursor to the first character of the field you are defining. You can specify this property for several fields and the cursor will position to the first display field with this attribute ( **DspAtr(PC)** ). If none of the Monarch Controls has a PositionCursor Indicator set then the first input capable control *in the order in which they were defined in the ASPX* is the default control to receive focus.

To set this property at design-time, click to the right of the property and enter the cursor attribute.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
