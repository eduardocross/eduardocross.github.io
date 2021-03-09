---
title: DdsImage.NameField Property

Id: amfDdsImageClassNameFieldProperty
TocParent: amfDdsImageClassPropertiesMain
TocOrder: 31

keywords: NameField property
keywords: DdsImage.NameField property

---

Gets or sets an IFS CharField from which to draw the name of the file the Image Control will show.

#### Syntax
<pre class="prettyprint"> **BegProp NameField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the path to the CharField for the file to be presented by the Image Control.

#### Remarks
As this product sets up an absolute NameField, this control is best used when the file to be presented on the page is unlikely to change at any forseeable point. This property requires [NameFieldLength](amdDdsImageClassNameFieldLengthProperty.html), and overrides [Name](amdDdsImageClassNameProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsImage Description](amfUnderstandingImageControls.html)<br /> [ DdsImage Class](amfDdsImageClass.html) <br /> [ DdsImage Class Members](amfDdsImageClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
