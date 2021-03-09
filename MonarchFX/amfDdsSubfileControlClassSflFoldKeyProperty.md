---
title: DdsSubfileControl.SflFoldKey Property

Id: amfDdsSubfileControlClassSflFoldKeyProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 90

keywords: SflFoldKey property
keywords: DdsSubfileControl.SflFoldKey property
keywords: function keys, controlling subfile fold
keywords: subfiles, function key controlling subfile fold
keywords: web controls, function key controlling subfile fold
keywords: how to, set function key to control subfile fold
keywords: how to, get function key controlling subfile fold
keywords: subfile records, function key controlling subfile fold
keywords: subfile usage, function key controlling subfile fold

---

Gets or sets the function key to press to switch between a folded and truncated display of the subfile record. 

#### Syntax
<pre class="prettyprint"> **BegProp SflFoldKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKeyIBM)
   BegGet;  BegSet** </pre>

#### Property Values
[ ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html). Enumeration value of the function key.

#### Remarks
This function key will allow the user to switch from a folded (multi-row) display to a truncated display of the subfile record. Pressing the key again will switch from truncated back to folded.

Since both SflFoldKey and SflDropKey set a default (SFLDROP defaults to truncated, SFLFOLD to multi-row; although these can be conditioned), and a toggle control, the two are **mutually exclusive** . If each is defined as a separate command key, SflDropKey will be used (and SflFoldKey will be ignored). 

If both SFLFOLD and SFLDROP are declared on the *same* key, the Subfile's condition will default to whichever of them is conditioned TRUE. If both are TRUE, the initial state will be folded; if both are FALSE, it will be dropped.

To set this property at design-time, click on the right of the **SflFoldKey** property and select the function key or attention key value from the drop-down list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html) 
