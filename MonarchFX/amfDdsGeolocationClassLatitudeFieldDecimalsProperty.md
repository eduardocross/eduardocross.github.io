---
title: DdsGeolocation.LatitudeFieldDecimals Property

Id: amfDdsGeolocationClassLatitudeFieldDecimalsProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 60

keywords: LatitudeFieldDecimals property
keywords: DdsGeolocation.LatitudeFieldDecimals property

---

Defines the number of decimal places recognized by the field that holds the Latitude.

#### Syntax
<pre class="prettyprint"> **BegProp LatitudeFieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the number of decimal places for the Record field that holds the Latitude. Requires [LatitudeField](amfDdsGeolocationClassLatitudeFieldProperty.html) and [LatitudeFieldLength](amfDdsGeolocationClassLatitudeFieldLengthProperty.html).

#### Remarks
Sets the number of decimal places for the field that holds the Latitude. Must be used with [LatitudeField](amfDdsGeolocationClassLatitudeFieldProperty.html) and [LatitudeFieldLength](amfDdsGeolocationClassLatitudeFieldLengthProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
