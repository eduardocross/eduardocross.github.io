---
title: DdsGeolocation.AltitudeField Property

Id: amfDdsGeolocationClassAltitudeFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 35

keywords: AltitudeField property
keywords: DdsGeolocation.AltitudeField property

---

Defienes the name of a record field used to report the Altitude of the device.

#### Syntax
<pre class="prettyprint"> **BegProp AltitudeField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of the record Field that holds the Altitude of the mobile device. Requires [DdsGeolocation.AltitudeFieldLength](amfDdsGeolocationClassAltitudeFieldLengthProperty.html) and [DdsGeolocation.AltitudeFieldDecimals](amfDdsGeolocationClassAltitudeFieldDecimalsProperty.html) 

#### Remarks
This sets a Field in a record that holds the Altitude. Reports the altitude of the device relative to the WGS84 ellipsoid (roughly sea level). Expressed in Meters. Must be used with [AltitudeFieldLength](amfDdsGeolocationClassAltitudeFieldLengthProperty.html) and [AltitudeFieldDecimals](amfDdsGeolocationClassAltitudeFieldDecimalsProperty.html) in order to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
