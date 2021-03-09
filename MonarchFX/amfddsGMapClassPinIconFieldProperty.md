---
title: DdsGMap.PinIconField Property

Id: amfddsGMapClassPinIconFieldProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinIconField property
keywords: DdsGMap.PinIconField property

---

. Specifies the name of subfile character field which will contain the URL of an image that will serve as the icon to mark the address. 

#### Syntax
<pre class="prettyprint"> **BegProp PinIconField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the character field containing the pin icon URL. Requires [DdsGMap.PinIconFieldLength](amfDdsGMapClassPinIconFieldLengthProperty.html).

#### Remarks
This sets the field that will contain the URL for an icon to be used on the map pins. The field in question must be populated with string data and [PinIconFieldLength](amfDdsGMapClassPinIconFieldLengthProperty.html) must also be set to avoid throwing an error.

This property overrides [PinIcon](amfDdsGMapClassPinIconProperty.html).

This property applies only when the [Marks](amfddsGMapClassMarksProperty.html) property for the DdsGMap is set to <code>Pin</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
