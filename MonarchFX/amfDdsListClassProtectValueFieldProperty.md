---
title: DdsList.ProtectValueField Property

Id: amfDdsListClassProtectValueFieldProperty
TocParent: amfDdsListClassProperties
TocOrder: 84

keywords: ProtectValueFieldproperty
keywords: DdsList.ProtectValueFieldproperty

---

Sets an indicator expression (or *True) which determines whether the fields in this record are protected.

#### Syntax
<pre class="prettyprint"> **BegProp ProtectValueField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Accepts either an indicator expression or special value (*True).

#### Remarks
When this property is set ***True** , all input-capable value fields in the record will become read-only (protected). New fields that are added may not be protected unless this property is reinvoked.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
