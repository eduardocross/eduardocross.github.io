---
title: DdsGMap.SelectedPinIcon Property

Id: amfddsGMapClassSelectedPinIconProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: SelectedPinIcon property
keywords: DdsGMap.SelectedPinIcon property

---

Contains a URL for the icon to display for selected pins. 

#### Syntax
<pre class="prettyprint"> **BegProp SelectedPinIcon Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets a URL for the icon to use to indicate an selected pin. Defaults to Marker_Green.png ![](images/marker_green.png). 

#### Remarks
This sets a particular icon to use when a pin is displayed and selected.

This property is overriden by [SelectedPinIconField](amfddsGMapClassSelectedPinIconFieldProperty.html).

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pins</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
