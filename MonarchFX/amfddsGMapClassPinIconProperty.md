---
title: DdsGMap.PinIcon Property

Id: amfddsGMapClassPinIconProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinIcon property
keywords: DdsGMap.PinIcon property

---

Contains a URL used for the Pin's icons when they're not selected. 

#### Syntax
<pre class="prettyprint"> **BegProp PinIcon Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets a URL for the icon to use to indicate an unselected pin. Defaults to Marker.png ![](images/marker.png). 

#### Remarks
This sets a particular icon to use when a pin is displayed.

This property is overriden by [PinIconField](amfddsGMapClassPinIconFieldProperty.html).

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pins</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
