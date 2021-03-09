---
title: DdsCharField.AutoPostBackKey Property

Id: amfDdsCharFieldClassAutoPostBackKeyProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 20

keywords: AutoPostBackKey property
keywords: DdsCharField.AutoPostBackKey property
keywords: web controls, setting AutoPostBack aidkey
keywords: web controls, getting AutoPostBack aidkey
keywords: how to, set AutoPostBack aidkey
keywords: how to, get AutoPostBack aidkey
keywords: display files, AutoPostBack aidkey
keywords: Web server controls [ASNA.Monarch], AutoPostBack aidkey
keywords: field controls, AutoPostBack aidkey

---

Gets or sets the aidkey to return to the server when [ AutoPostBack](amfDdsCharFieldClassAutoPostBackProperty.html) is True.

#### Syntax
<pre class="syntax"> **BegProp AutoPostBackKey Access(*Public) Type(ASNA.Monarch.WebDspF.AidKey) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidKey** . One of the enumeration values containing the function key value to return to the server when **AutoPostBack** is true.

#### Remarks
Nothing will occur if the key is not enabled for the current format.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
