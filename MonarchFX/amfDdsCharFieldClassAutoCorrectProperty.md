---
title: DdsCharField.AutoCorrect Property

Id: amfDdsCharFieldClassAutoCorrectProperty
TocParent: amfDdsCharFieldClassPropertiesMain
TocOrder: 09

keywords: AutoCorrect property
keywords: DdsCharField.AutoCorrect property
keywords: web controls, generating AutoCorrect
keywords: how to, generate AutoCorrect
keywords: display files, generating AutoCorrect
keywords: Web server controls [ASNA.Monarch], AutoCorrect
keywords: field controls, AutoCorrect

---

Gets or sets a boolean value that if true, employs automatic spelling correction on all text elements. (Defaults to False.)

#### Syntax
<pre class="syntax"> **BegProp AutoCorrect Access(*Public) Type(*Boolean) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. True will cause text elements in the control to be automatically spell checked. False will leave autocorrect disabled.

#### Remarks
This property was introduced with Monarch and Wings 6.0. Along with [AutoCapitalize](amfDdsCharfieldClassAutoCapitalizeProperty.html), it is a common feature of mobile applications.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Class Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
