---
title: DdsGeolocation.AltitudeAccuracyField Property

Id: amfDdsGeolocationClassAltitudeAccuracyFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 20

keywords: AltitudeAccuracyField property
keywords: DdsGeolocation.AltitudeAccuracyField property

---

Defines the name of a record field used to report the the accuracy to which the Altitude is reported.

#### Syntax
<pre class="prettyprint"> **BegProp AltitudeAccuracyField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of an IBM i number field that holds the accuracy of the Altitude. Requires [DdsGeolocation.AltitudeAccuracyFieldLength](amfDdsGeolocationClassAltitudeAccuracyFieldLengthProperty.html) and [DdsGeolocation.AltitudeAccuracyFieldDecimals](amfDdsGeolocationClassAltitudeAccuracyFieldDecimalsProperty.html) 

#### Remarks
This sets a CharField in an IBM i record that holds the accuracy of the Altitude. Expressed in Meters. It must be used with [AltitudeAccuracyFieldLength](amfDdsGeolocationClassAltitudeAccuracyFieldLengthProperty.html) and [AltitudeAccuracyFieldDecimals](amfDdsGeolocationClassAltitudeAccuracyFieldDecimalsProperty.html) in order to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
