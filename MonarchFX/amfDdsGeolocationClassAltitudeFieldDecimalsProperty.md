---
title: DdsGeolocation.AltitudeFieldDecimals Property

Id: amfDdsGeolocationClassAltitudeFieldDecimalsProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 40

keywords: AltitudeFieldDecimals property
keywords: DdsGeolocation.AltitudeFieldDecimals property

---

Defines the number of decimal places recognized by the field that holds the Altitude.

#### Syntax
<pre class="prettyprint"> **BegProp AltitudeFieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the number of decimal places for the Record field that holds the Altitude. Requires [AltitudeField](amfDdsGeolocationClassAltitudeFieldProperty.html) and [AltitudeFieldLength](amfDdsGeolocationClassAltitudeFieldLengthProperty.html).

#### Remarks
Sets the number of decimal places for the field that holds the Altitude. Must be used with [AltitudeField](amfDdsGeolocationClassAltitudeFieldProperty.html) and [AltitudeFieldLength](amfDdsGeolocationClassAltitudeFieldLengthProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
