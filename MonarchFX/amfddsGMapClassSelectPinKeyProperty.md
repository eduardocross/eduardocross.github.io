---
title: DdsGMap.SelectPinKey Property

Id: amfddsGMapClassSelectPinKeyProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: SelectPinKey property
keywords: DdsGMap.SelectPinKey property

---

Sets the **Function Key** that will 

#### Syntax
<pre class="prettyprint"> **BegProp SelectPinKey Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. All available F-keys are listed. 

#### Remarks
This property determines which Function Key is fired when a map pin is selected. It must be a designated Function key, rather than an Attention Key. Additionally, the Function Key must be declared in the [AidKeys](amfDdsFileClassAidKeysProperty.html) property of the DdsFile, DdsSubfile, or DdsRecord it appears in.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMaplClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
