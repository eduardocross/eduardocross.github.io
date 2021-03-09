---
title: DdsGeolocation.ErrorCodeField Property

Id: amfDdsGeolocationClassErrorCodeFieldProperty
TocParent: amfDdsGeolocationClassProperties
TocOrder: 50

keywords: ErrorCodeField property
keywords: DdsGeolocation.ErrorCodeField property

---

Specifies the name of a <code>Packed(5,0)</code> field that receives an error code for the control:

#### Syntax
<pre class="prettyprint"> **BegProp ErrorCodeField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Specifies the name of a <code>Packed(5,0)</code> field that receives one of the following codes:

- 0 = No error.
- 99999 = Browser does not support 'navigator.geolocation' interface
- 1 = <code>PERMISSION_DENIED</code> (might be due to not running in HTTPS)
- 2 = <code>POSITION_UNAVAILABLE</code>
- 3 = <code>TIMEOUT</code>

Requires [DdsGeolocation.ErrorCodeFieldLength](amfDdsGeolocationClassErrorCodeFieldLengthProperty.html)
.

#### Remarks
This sets a <code>Packed(5,0)</code> Field in an IBM i record that receives a code indicating errors. Must be used with [ErrorCodeFieldLength](amfDdsGeolocationClassErrorCodeFieldLengthProperty.html) in order to avoid throwing an error.

This is intended for debugging purposes and should not be exposed to end users.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGeolocation Description](amfUnderstandingGeoloc.html)<br /> [ DdsGeolocation Class](amfDdsGeolocationClass.html) <br /> [ DdsGeolocation Class Members](amfDdsGeolocationClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
