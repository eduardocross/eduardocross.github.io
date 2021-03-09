---
title: DdsDataField.AutoPostBackKey Property

Id: amfDdsDataFieldClassAutoPostBackKeyProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 30

keywords: AutoPostBackKey property
keywords: DdsDataField.AutoPostBackKey property
keywords: web controls, setting AutoPostBack aidkey
keywords: web controls, getting AutoPostBack aidkey
keywords: how to, set AutoPostBack aidkey
keywords: how to, get AutoPostBack aidkey
keywords: display files, AutoPostBack aidkey
keywords: Web server controls [ASNA Monarch], AutoPostBack aidkey
keywords: field controls, AutoPostBack aidkey

---

Gets or sets the aidkey to return to the server when [ AutoPostBack](amfDdsDataFieldClassAutoPostBackProperty.html) is True. 

#### Syntax
<pre class="prettyprint"> **BegProp AutoPostBackKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKey) Modifier(*MustOverride)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidKey** . One of the enumeration values containing the function key value to return to the server when **AutoPostBack** is true.

#### Remarks
Nothing will occur if the key is not enabled for the current format.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 10

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
