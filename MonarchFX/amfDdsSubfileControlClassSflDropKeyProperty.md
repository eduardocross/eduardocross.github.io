---
title: DdsSubfileControl.SflDropKey Property

Id: amfDdsSubfileControlClassSflDropKeyProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 80

keywords: SflDropKey property
keywords: DdsSubfileControl.SflDropKey property
keywords: function keys, controlling subfile drop
keywords: subfiles, function key controlling subfile drop
keywords: web controls, function key controlling subfile drop
keywords: how to, set function key to control subfile drop
keywords: how to, get function key controlling subfile drop
keywords: subfile records, function key controlling subfile drop
keywords: subfile usage, function key controlling subfile drop

---

Gets or sets the function key to press to switch between a truncated and folded display of the subfile record. 

#### Syntax
<pre class="prettyprint"> **BegProp SflDropKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKeyIBM)
   BegGet;  BegSet** </pre>

#### Property Values
[ ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html). Enumeration value of the function key.

#### Remarks
This function key will allow the user to switch from a truncated display to a folded (multi-row) display of the subfile record. Pressing the key again will switch from folded back to truncated.

Since both SflFoldKey and SflDropKey set a default (SFLDROP defaults to truncated, SFLFOLD to multi-row; although these can be conditioned), and a toggle control, the two are **mutually exclusive** . If each is defined as a separate command key, SflDropKey will be used (and SflFoldKey will be ignored). 

If both SFLFOLD and SFLDROP are declared on the *same* key, the subfile condition will default to whichever of them is conditioned TRUE. If both are TRUE, the initial state will be folded; if both are FALSE, it will be dropped.

To set this property at design-time, click on the right of the **SflDropKey** property and select the function key or attention key value from the drop down list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html) 
