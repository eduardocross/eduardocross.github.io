---
title: DdsGeolocation.LongitudeField Property

Id: amfDdsGeolocationClassLongitudeFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 65

keywords: LongitudeField property
keywords: DdsGeolocation.LongitudeField property

---

Defines the name of a record field used to report the Longitude.

#### Syntax
<pre class="prettyprint"> **BegProp LongitudeField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of the record Field that holds the Longitude of the mobile device. Requires [DdsGeolocation.LongitudeFieldLength](amfDdsGeolocationClassLongitudeFieldLengthProperty.html) and [DdsGeolocation.LongitudeFieldDecimals](amfDdsGeolocationClassLongitudeFieldDecimalsProperty.html) 

#### Remarks
This defines a field that holds the Longitude. Reports the Longitude of the device. Positive Longitudes are east of the Prime Meridian (Greenwich, England), while negative Longitudes fall west of it. The measurements are bounded by +/- 90°, and expressed in Decimal Degrees. Must be used with [LongitudeFieldLength](amfDdsGeolocationClassLongitudeFieldLengthProperty.html) and [LongitudeFieldDecimals](amfDdsGeolocationClassLongitudeFieldDecimalsProperty.html) in order to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
