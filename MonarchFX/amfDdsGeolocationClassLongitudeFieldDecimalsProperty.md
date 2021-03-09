---
title: DdsGeolocation.LongitudeFieldDecimals Property

Id: amfDdsGeolocationClassLongitudeFieldDecimalsProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 70

keywords: LongitudeFieldDecimals property
keywords: DdsGeolocation.LongitudeFieldDecimals property

---

Defines the number of decimal places recognized by the field that holds the Longitude.

#### Syntax
<pre class="prettyprint"> **BegProp LongitudeFieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the number of decimal places for the Record field that holds the Longitude. Requires [LongitudeField](amfDdsGeolocationClassLongitudeFieldProperty.html) and [LongitudeFieldLength](amfDdsGeolocationClassLongitudeFieldLengthProperty.html).

#### Remarks
Sets the number of decimal places for the field that holds the Longitude. Must be used with [LongitudeField](amfDdsGeolocationClassLongitudeFieldProperty.html) and [LongitudeFieldLength](amfDdsGeolocationClassLongitudeFieldLengthProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
