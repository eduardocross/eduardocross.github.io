---
title: DdsGeolocation.ErrorMessageField Property

Id: amfDdsGeolocationClassErrorMessageFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 53

keywords: ErrorMessageField property
keywords: DdsGeolocation.ErrorMessageField property

---

Specifies the name of a <code>CHAR</code> field that receives a string with details of the error encountered.

#### Syntax
<pre class="prettyprint"> **BegProp ErrorMessageField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Name of a <code>CHAR</code> field that receives a string with details of the error encountered.

Requires [DdsGeolocation.ErrorMessageFieldLength](amfDdsGeolocationClassErrorMessageFieldLengthProperty.html).

#### Remarks
This sets a <code>CHAR</code> Field in an IBM i record that receives a message (in string form) describing an error. Must be used with [ErrorMessageFieldLength](amfDdsGeolocationClassErrorMessageFieldLengthProperty.html) in order to avoid throwing an error.

This is intended for debugging purposes and should not be exposed to end users.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
