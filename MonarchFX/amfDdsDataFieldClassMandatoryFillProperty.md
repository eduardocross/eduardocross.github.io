---
title: DdsDataField.MandatoryFill Property

Id: amfDdsDataFieldClassMandatoryFillProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 59

keywords: MandatoryFill property
keywords: DdsDataField.MandatoryFill property
keywords: MandatoryFill Property Editor, setting values
keywords: CHECK(MF)

keywords: CHECK(MF) Support
keywords: Mandatory Fill
keywords: field controls, Mandatory Fill
keywords: indicator expressions, Mandatory Fill
keywords: conditioning expressions, Mandatory Fill

---

Specifies that, if True, when any part of the field is altered, each position in the field must have a character entered in it. Blanks are considered valid characters for this purpose.

#### Syntax
<pre class="prettyprint"> **BegProp MandatoryFill Access(*Public) Type(Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If true, each position of the field must contain a character for processing to continue. 

#### Remarks
Implemented in 8.0 tp support the CHECK(MF) keyword function.

User will be prompted via dialog to complete the field if changes are made and there are positions unfilled.

This property does not allow optional indicators, and therefore cannot be conditioned.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
