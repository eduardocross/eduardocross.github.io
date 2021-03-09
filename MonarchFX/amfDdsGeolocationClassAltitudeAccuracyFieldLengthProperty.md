---
title: DdsGeolocation.AltitudeAccuracyFieldLength Property

Id: amfDdsGeolocationClassAltitudeAccuracyFieldLengthProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 30

keywords: AltitudeAccuracyFieldLength property
keywords: DdsGeolocation.AltitudeAccuracyFieldLength property

---

Defines the length of the field that holds the accuracy of the Altitude.

#### Syntax
<pre class="prettyprint"> **BegProp AltitudeAccuracyFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length of the Record field that holds the accuracy of the Altitude. Requires [AltitudeAccuracyField](amfDdsGeolocationClassAltitudeAccuracyFieldProperty.html) and [AltitudeAccuracyFieldDecimals](amfDdsGeolocationClassAltitudeAccuracyFieldDecimalsProperty.html).

#### Remarks
Sets the length of the field that holds the accuracy of the Altitude. Must be used with [AltitudeAccuracyField](amfDdsGeolocationClassAltitudeAccuracyFieldProperty.html) and [AltitudeAccuracyFieldDecimals](amfDdsGeolocationClassAltitudeAccuracyFieldDecimalsProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
