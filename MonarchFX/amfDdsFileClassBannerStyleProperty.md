---
title: DdsFile.BannerStyle Property

Id: amfDdsFileClassBannerStyleProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 40

keywords: BannerStyle property
keywords: DdsFile.BannerStyle property
keywords: enumerations [ASNA.onarach.WebDspF], BannerStyles, used by
keywords: BannerStyles enumeration, used by
keywords: function keys, controlling display position
keywords: attention keys, controlling display position
keywords: full banner
keywords: vertical banner
keywords: horizontal banner
keywords: function keys, hiding all except Enter and Reset
keywords: attention keys, hiding all except Enter and Reset
keywords: function keys, setting banner style
keywords: function keys, getting banner style
keywords: attention keys, setting banner style
keywords: attention keys, getting banner style
keywords: aidkeys, setting banner style
keywords: aidkeys, getting banner style
keywords: web controls, setting banner style
keywords: web controls, getting banner style
keywords: display files, setting banner style
keywords: display files, getting banner style
keywords: Reset key
keywords: Enter key
keywords: Reset key, special treatment
keywords: Enter key, special treatment

---

Gets or sets how the function key banner on the page will display. **Horizontal** is the default.

#### Syntax
<pre class="prettyprint"> **BegProp BannerStyle Access(*Public) Type([ASNA.Monarch.WebDspF.BannerStyles](amfBannerStylesEnumeration.html))
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.BannerStyles** that represents how the function keys banner is to display on the page.

#### Remarks
The **BannerStyle** property determines whether the keys will display as either a full banner, horizontal vertical, hidden, or invisible. The default is **horizontal** . When **Hidden** is selected, this hides all function keys **except** for the "enter" and "reset" keys. **Invisible** hides the entire banner, and is most useful for conserving screen real estate on mobile platforms.

To set this property at design-time, click to the right of the BannerStyle property and select the banner style from the drop-down list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
