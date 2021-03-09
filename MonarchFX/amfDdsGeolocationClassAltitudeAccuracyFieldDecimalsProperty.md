---
title: DdsGeolocation.AltitudeAccuracyFieldDecimals Property

Id: amfDdsGeolocationClassAltitudeAccuracyFieldDecimalsProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 25

keywords: AltitudeAccuracyFieldDecimals property
keywords: DdsGeolocation.AltitudeAccuracyFieldDecimals property

---

Defines the number of decimal places recognized by the field that holds the accuracy of the Altitude.

#### Syntax
<pre class="prettyprint"> **BegProp AltitudeAccuracyFieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the number of decimal places for the Record field that holds the accuracy of the Altitude. Requires [AltitudeAccuracyField](amfDdsGeolocationClassAltitudeAccuracyFieldProperty.html) and [AltitudeAccuracyFieldLength](amfDdsGeolocationClassAltitudeAccuracyFieldLengthProperty.html).

#### Remarks
Sets the number of decimal places for the field that holds the accuracy of the Altitude. Must be used with [AltitudeAccuracyField](amfDdsGeolocationClassAltitudeAccuracyFieldProperty.html) and [AltitudeAccuracyFieldLength](amfDdsGeolocationClassAltitudeAccuracyFieldLengthProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
