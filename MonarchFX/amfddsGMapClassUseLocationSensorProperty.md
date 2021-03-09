---
title: DdsGMap.UseLocationSensor Property

Id: amfDdsGMapClassUseLocationSensorProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords:  UseLocationSensor property
keywords: DdsGMap.UseLocationSensor property

---

Gets or sets a boolean value that determines whether the [map control](amfDdsGMapClass.html) has access to the mobile device's location sensor.

#### Syntax
<pre class="prettyprint"> **BegProp UseLocationSensor Access(*Public) Type(*bool)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. Sets whether the mobile device's location sensor will be accessed by the GoogleMaps API. Defaults to **No** .

#### Remarks
The **UseLocationSensor** property is often set via end-user dialog, as the GoogleMaps API cannot legally access a mobile device's location sensor without the user's explicit permission. If this property is set to FALSE, it will rule out active route guidance through Google Maps or Google Navigation. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfDdsGMapClass.html) <br /> [ DdsGMap Class Members](amfDdsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
