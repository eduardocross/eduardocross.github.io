---
title: DdsGeolocation.AccuracyField Property

Id: amfDdsGeolocationClassAccuracyFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 05

keywords: AccuracyField property
keywords: DdsGeolocation.AccuracyField property

---

Defines the name of a record field used to determine the accuracy to which Latitude and Longitude are reported.

#### Syntax
<pre class="prettyprint"> **BegProp AccuracyField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets Sets the name of an IBM i number field that holds the accuracy of the Latitude and Longitude. Requires [DdsGeolocation.AccuracyFieldLength](amfDdsGeolocationClassAccuracyFieldLengthProperty.html) and [DdsGeolocation.AccuracyFieldDecimals](amfDdsGeolocationClassAccuracyFieldDecimalsProperty.html) 

#### Remarks
This sets a CharField in an IBM i record that holds the accuracy of the Latitude and Longitude. It must be used with [AccuracyFieldLength](amfDdsGeolocationClassAccuracyFieldLengthProperty.html) and [AccuracyFieldDecimals](amfDdsGeolocationClassAccuracyFieldDecimalsProperty.html) in order to avoid throwing an error.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
