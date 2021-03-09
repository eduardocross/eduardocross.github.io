---
title: DdsTable.IconBackcolorField Property

Id: amfDdsTableClassIconBackcolorFieldProperty
TocParent: amfDdsTableClassPropertiesMain
TocOrder: 09

keywords: IconBackcolorField property
keywords: DdsTable.IconBackcolorField property
keywords: how to, Icon backcolor field
keywords: Icon Backcolor fields
keywords: table icon color

---

Defines the field from which the background color of the icons for the IconColumn.

#### Syntax
<pre class="prettyprint"> **BegProp IconBackcolorField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string that sets the field that the background color name or hex code for the IconColumn will come from. Defaults to "".

#### Remarks
This property requires [IconBackcolorFieldLength](amfDdsTableClassIconBackcolorFieldLengthProperty.html), . 

This property is set on each IconColumn in the [column editor](amfUnderColumnsList.html).

This control was introduced with version ASNA Mobile Support version 8.0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsTable Class](amfDdsTableClass.html) <br /> [ DdsTable Class Members](amfDdsTableClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
