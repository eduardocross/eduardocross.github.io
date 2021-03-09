---
title: DdsGMap.PinTagField Property

Id: amfddsGMapClassPinTagFieldProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinTagField property
keywords: DdsGMap.PinTagField property

---

Specifies the name of a subfile <code>CHAR(1)</code> field which will be used to add a tag to the marker for the address.

#### Syntax
<pre class="prettyprint"> **BegProp PinTagField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of a subfile <code>CHAR(1)</code> field which will be used to add a tag to the marker for the address.

#### Remarks
This ets developers set a tag to be displayed along with a pin.

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pins</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
