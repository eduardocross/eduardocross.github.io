---
title: DdsButton.ButtonStyle Property

Id: amfDdsButtonClassButtonStyleProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 12

keywords: ButtonStyle property
keywords: DdsButton.ButtonStyle property
keywords: ButtonStyles enumeration, used by
keywords: enumerations [ASNA.Monarch.WebDspF], ButtonStyles, used by
keywords: Web server controls [ASNA.Monarch], dds button style
keywords: how to, set dds button style
keywords: how to, get dds button style
keywords: display files, setting dds button style
keywords: display files, getting dds button style
keywords: web controls, setting dds button style
keywords: web controls, getting dds button style
keywords: dds button, style
keywords: field controls, dds button, style

---

Gets or sets the style used to specify the type of button control, **Button** , **Icon, Image** , or **Link** .

#### Syntax
<pre class="syntax"> **BegProp ButtonStyle Access(*Public) Type(ASNA.Monarch.WebDspF.ButtonStyles)
   BegGet;  BegSet** </pre>

#### Property Values
[ ASNA.Monarch.WebDspF.ButtonStyles](amfButtonStylesEnumeration.html). One of the valid enumeration values that indicates the style of button control for the field. The default is **Button** .

#### Remarks
To set this property at design time, click on the arrow on the right side of the property window and choose one of the options shown in the drop-down box: **Button** , **Icon, Image** , or **Link** . 

Selecting the Icon option will activate (and require) the [IconID property](amfDdsButtonClassIconIdProperty.html).

**Caution &#8211;** The [OnMouseOverImage](amfDdsButtonClassOnMouseOverImageProperty.html) property is only compatible with the **Image** option. Attempting to use it with either **Button** or **Link** will result in no image being shown

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [DdsButton Class](amfDdsButtonClass.html) <br /> [ DdsButton Class Members](amfDdsButtonClassMembers.html) <br /> [ ButtonStyles Enumeration](amfButtonStylesEnumeration.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
