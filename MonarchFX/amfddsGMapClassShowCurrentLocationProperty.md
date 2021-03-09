---
title: DdsGMap.ShowCurrentLocation Property

Id: amfddsGMapClassShowCurrentLocationProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: ShowCurrentLocation property
keywords: DdsGMap.ShowCurrentLocation property

---

Gets or sets a boolean that determines whether the DdsGmap will show the current location of the user's device.

#### Syntax
<pre class="prettyprint"> **BegProp ShowCurrentLocation Access(*Public) Type(*bool)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If **true** , the device's location will be reported to Google Maps and appear on the DdsGMap. 

#### Remarks
This property will usually create a static location pin on your DdsGMap.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMaplClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
