---
title: DdsGMap.PinLabelField Property

Id: amfddsGMapClassPinLabelFieldProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: PinLabelField property
keywords: DdsGMap.PinLabelField property

---

Defines the name of a record field used to report the address Pin Label data.

#### Syntax
<pre class="prettyprint"> **BegProp PinLabelField Access(*Public) Type(*strong)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the record field used to report the pin label data. Requires [DdsGMap.PinLabelFieldLength](amfDdsGMapClassPinLabelFieldLengthProperty.html).

#### Remarks
This sets the field that data used to populate the map's pin labels comes from. The field in question must be populated with string data and [PinLabelFieldLength](amfDdsGMapClassPinLabelFieldLengthProperty.html) must also be set to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
