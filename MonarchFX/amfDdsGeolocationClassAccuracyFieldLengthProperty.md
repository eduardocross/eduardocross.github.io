---
title: DdsGeolocation.AccuracyFieldLength Property

Id: amfDdsGeolocationClassAccuracyFieldLengthProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 15

keywords: AccuracyFieldLength property
keywords: DdsGeolocation.AccuracyFieldLength property

---

Defines the length of the field that holds the accuracy of the Latitude and Longitude.

#### Syntax
<pre class="prettyprint"> **BegProp AccuracyFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the length of the Record field that holds the accuracy of the Latitude and Longitude. Requires [AccuracyField](amfDdsGeolocationClassAccuracyFieldProperty.html) and [AccuracyFieldDecimals](amfDdsGeolocationClassAccuracyFieldDecimalsProperty.html).

#### Remarks
Sets the length of the field that holds the accuracy of the Latitude and Longitude. Must be used with [AccuracyField](amfDdsGeolocationClassAccuracyFieldProperty.html) and [AccuracyFieldDecimals](amfDdsGeolocationClassAccuracyFieldDecimalsProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
