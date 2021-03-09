---
title: DdsButton.IconID Property

Id: amfDdsButtonClassIconIdProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 21

keywords: IconID property
keywords: DdsButton.IconID property
keywords: IconID enumeration, used by
keywords: enumerations [ASNA.Monarch.WebDspF], IconID, used by
keywords: how to, set dds Icon ID
keywords: how to, get dds Icon ID
keywords: display files, setting dds Icon ID
keywords: display files, getting dds Icon ID
keywords: web controls, setting dds Icon ID
keywords: web controls, getting dds Icon ID
keywords: dds button, style
keywords: field controls, dds button, Icon ID

---

Gets or sets the ID to be used in the Icon-style button or link.

#### Syntax
<pre class="syntax"> **BegProp IconID Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. One of the over two hundred or so valid string values (determined by the [default collection](amfIconIdCollection.html)) that indicates the icon to be used for the field. If accessed via the Property Tasks or Visual Studio Properties window, the [Icon Selection](amfIconSelection.html) screen will appear to help streamline the process.

#### Remarks
This feature was introduced in Wings 6.1 and Mobile RPG 6.1. It requires a [Buttonstyle](amfDdsButtonClassButtonStyleProperty.html) or [LinkStyle](amfDdsLinkClassLinkStyleProperty.html) of **Icon** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [DdsButton Class](amfDdsButtonClass.html) <br /> [ DdsButton Class Members](amfDdsButtonClassMembers.html) <br /> [ ButtonStyles Enumeration](amfButtonStylesEnumeration.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
