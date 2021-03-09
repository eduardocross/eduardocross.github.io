---
title: DdsGMap.AddressField Property

Id: amfDdsGMapClassAddressFieldProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: AddressField property
keywords: DdsGMap.AddressField property

---

Defines the name of a record field used to report the address data.

#### Syntax
<pre class="prettyprint"> **BegProp AddressField Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the record field used to report the address data. Requires [DdsGMap.AddressFieldLength](amfDdsGMapClassAddressFieldLengthProperty.html).

#### Remarks
This sets the field that data used to populate the map comes from. The field in question must be populated with addresses to be interpreted correctly and [DdsGMap.AddressFieldLength](amfDdsGMapClassAddressFieldLengthProperty.html) must also be set to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfDdsGMapClass.html) <br /> [ DdsGMap Class Members](amfDdsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
