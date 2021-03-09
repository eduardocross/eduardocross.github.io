---
title: DdsTable.HeadingFieldLength Property

Id: amfDdsTableClassHeadingFieldLengthProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: HeadingFieldLength property
keywords: DdsTable.HeadingFieldLength property
keywords: Web server controls [ASNA MobileRPG], DdsTable HeadingFieldLength
keywords: how to, set DdsTable HeadingFieldLength
keywords: how to, get DdsTable HeadingFieldLength

---

Gets or sets an integer containing the Name of a column's HeadingFieldLength.

#### Syntax
<pre class="prettyprint"> **BegProp HeadingFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. ets the length of the Record field from which the data for the Text will be drawn. Requires [HeadingFieldName](amfDdsTableClassHeadingFieldProperty.html)..

#### Remarks
Sets the length of the field the data for the heading will be drawn from. Must be used with [HeadingFieldName](amfDdsTableClassHeadingFieldProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsTable Class](amfDdsTableClass.html)</dd>
        <dd>[DdsTable Class Members](amfDdsTableClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

