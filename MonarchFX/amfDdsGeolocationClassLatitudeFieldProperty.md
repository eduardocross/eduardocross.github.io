---
title: DdsGeolocation.LatitudeField Property

Id: amfDdsGeolocationClassLatitudeFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 55

keywords: LatitudeField property
keywords: DdsGeolocation.LatitudeField property

---

Defines the name of a field used to report the Latitude of the device.

#### Syntax
<pre class="prettyprint"> **BegProp LatitudeField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of an IBM i number field that holds that holds the Latitude of the mobile device. Requires [DdsGeolocation.LatitudeFieldLength](amfDdsGeolocationClassLatitudeFieldLengthProperty.html) and [DdsGeolocation.LatitudeFieldDecimals](amfDdsGeolocationClassLatitudeFieldDecimalsProperty.html) 

#### Remarks
This sets a Field in an IBM i record that holds the Latitude. Reports the Latitude of the device. Positive Latitudes are north of the equator, while negative latitudes fall south of it. The measurements are bounded by +/- 90°, and expressed in Decimal Degrees. Must be used with [LatitudeFieldLength](amfDdsGeolocationClassLatitudeFieldLengthProperty.html) and [LatitudeFieldDecimals](amfDdsGeolocationClassLatitudeFieldDecimalsProperty.html) in order to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
