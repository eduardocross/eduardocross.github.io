---
title: DdsField.InvertFontColor Property

Id: amfDdsFieldClassInvertFontColorProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 34

keywords: Web server controls [ASNA.Monarch], setting field control font color

keywords: InvertFontColor property
keywords: InvertFontColor Property Editor, setting values
keywords: DdsField.InvertFontColor property

---

Gets or sets whether to invert the font and background colors of the field.

#### Syntax
<pre class="prettyprint"> **BegProp InvertFontColor Access(*Public) Type(Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
**Boolean.** If True, colors for the font and background are inverted. If the background color is transparent, "white" will be used instead.

#### Remarks
To set the **InvertFontColor** property, click on the right hand side of the property window and select True or False.

This property allows migration of the DISPTR:RI keyword.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsField Class](amfDdsFieldClass.html) <br clear="none" />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
