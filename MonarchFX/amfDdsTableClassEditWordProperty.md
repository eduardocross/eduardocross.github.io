---
title: DdsTable.EditWord Property

Id: amfDdsTableClassEditWordProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: EditWord property
keywords: DdsTable.EditWord property
keywords: Web server controls [ASNA Monarch], setting DdsTable EditWord
keywords: how to, set DdsTable EditWord
keywords: how to, get DdsTable EditWord
keywords: web controls, setting DdsTable EditWord
keywords: web controls, getting DdsTable EditWord

---

Gets or sets a string containing an edit word to punctuate numeric fields according to the standard RPG rules for edit words.

#### Syntax
<pre class="prettyprint"> **BegProp EditWord Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Gets or sets a string containing an edit word to punctuate numeric fields. 

#### Remarks
To set this property at design time, click on the right side of the property window and enter a valid edit word as listed in the [EditWord Table](sharedEditWordTable.html) that gives you the desired display. 

An EditWord allows you to include spaces, commas, decimal points, and dollar signs. You can also output negative sign or CR when a numeric field has a negative value, suppress unwanted zeroes, and include constants. At design-time, the edit word can not to be surrounded by an apostrophe.

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

