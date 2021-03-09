---
title: DdsFile.CssEnterClass Property

Id: amfDdsFileClassCssEnterClassProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 60

keywords: CssEnterClass property
keywords: DdsFile.CssEnterClass property
keywords: Reset key, css class
keywords: Enter key, css class
keywords: cascading style sheets, reset key
keywords: cascading style sheets, enter key
keywords: how to, set css class for Enter key
keywords: how to, get css class for Enter key
keywords: how to, set css class for Reset key
keywords: how to, get css class for Reset key
keywords: web controls, setting enter key cascading style sheet
keywords: web controls, getting enter key cascading style sheet
keywords: web controls, setting reset key cascading style sheet
keywords: web controls, getting reset key cascading style sheet
keywords: display files, setting enter key cascading style sheet
keywords: display files, getting enter key cascading style sheet
keywords: display files, setting reset key cascading style sheet
keywords: display files, getting reset key cascading style sheet
keywords: CSS, enter key
keywords: CSS, reset key

---

Gets or sets the name of the cascading style sheet class that controls the appearance of the "enter" and "reset" keys.

#### Syntax
<pre class="prettyprint"> **BegProp CssEnterClass Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
**String** containing the name of the cascading style sheet class that controls the appearance of the "enter" and "reset" keys.

#### Remarks
The **CssEnterClass** property can be used to set the appearance of the "enter" and "reset" keys to distinguish it from the other function keys. You can also set the [ BannerStyle](amfDdsFileClassBannerStyleProperty.html) property to **Hidden** to hide all functions keys **except** "enter" and "reset".

To set this property at design-time, enter a Css class name for the "enter" and "reset" keys. The CssEnterClass value you enter (along with the **BannerStyle** setting) will be immediately apparent on the display.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [BannerStyle Property](amfDdsFileClassBannerStyleProperty.html) <br clear="none" />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
