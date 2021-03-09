---
title: DdsGMap.PinLabelType Property

Id: amfddsGMapClassPinLabelTypeProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinLabelType property
keywords: DdsGMap.PinLabelType property

---

Defines the way pin label data is displayed. Defaults to <code>tooltip</code>

#### Syntax
<pre class="prettyprint"> **BegProp PinLabelType Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the manner in which the pin label is dispayed. Options include:- ToolTip
- OpenedPopUp
- ClosedPopUp

#### Remarks
This sets the way in which the label data for a pin is displayed.

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pins</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
