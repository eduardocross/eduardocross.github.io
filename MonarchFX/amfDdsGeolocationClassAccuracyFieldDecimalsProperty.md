---
title: DdsGeolocation.AccuracyFieldDecimals Property

Id: amfDdsGeolocationClassAccuracyFieldDecimalsProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 10

keywords: AccuracyFieldDecimals property
keywords: DdsGeolocation.AccuracyFieldDecimals property

---

Defines the number of decimal places recognized by the field that holds the accuracy of the Latitude and Longitude.

#### Syntax
<pre class="prettyprint"> **BegProp AccuracyFieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Sets the number of decimal places for the Record field that holds the accuracy of the Latitude and Longitude. Requires [AccuracyField](amfDdsGeolocationClassAccuracyFieldProperty.html) and [AccuracyFieldLength](amfDdsGeolocationClassAccuracyFieldLengthProperty.html).

#### Remarks
Sets the number of decimal places for the field that holds the accuracy of the Latitude and Longitude. Must be used with [AccuracyField](amfDdsGeolocationClassAccuracyFieldProperty.html) and [AccuracyFieldLength](amfDdsGeolocationClassAccuracyFieldLengthProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
