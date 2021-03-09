---
title: DdsGMap.PinIconFieldLength Property

Id: amfDdsGMapClassPinIconFieldLengthProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinIconFieldLength property
keywords: DdsGMap.PinIconFieldLength property

---

Gets or sets an integer value that defines the length of the PinIconField from which the icon to be displayed in the [map control](amfDdsGMapClass.html) pins is drawn.

#### Syntax
<pre class="prettyprint"> **BegProp PinIconFieldLength Access(*Public) Type(*int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length (in characters) of the subfile character field from which the Pin Labels for the map will be drawn. 

#### Remarks
This sets the length of the pin icon field. It must be used in conjunction with [PinIconField](amfDdsGMapClassPinIconFieldProperty.html).

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pin</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfDdsGMapClass.html) <br /> [ DdsGMap Class Members](amfDdsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
