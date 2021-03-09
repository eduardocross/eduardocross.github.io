---
title: DdsDataField.MandatoryEnter Property

Id: amfDdsDataFieldClassMandatoryEnterProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 57

keywords: MandatoryEnter property
keywords: DdsDataField.MandatoryEnter property
keywords: MandatoryEnter Property Editor, setting values
keywords: CHECK(ME)

keywords: CHECK(ME) Support
keywords: Mandatory Enter
keywords: field controls, Mandatory Enter
keywords: indicator expressions, Mandatory Enter
keywords: conditioning expressions, Mandatory Enter

---

Specifies that, if True, the user must enter a value in the field.

#### Syntax
<pre class="prettyprint"> **BegProp MandatoryEnter Access(*Public) Type(Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If this property evaluates to True, at least one (1) character of data must be typed into the field. A blank is valid for these purposes.

#### Remarks
Implemented in 8.0 tp support the CHECK(ME) keyword function.

This validation is run when the user presses a Function Key or Enter, if the users presses an Attention Key instead, no validation is performed on the field and no data is sent to the program.

This check is enforced always, regardless of any other field being modified or not.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDataField Class](amfDdsDataFieldClass.html) <br /> [ DdsDataField Class Members](amfDdsDataFieldClassMembers.html) <br /> [ Derived Classes](amfDdsDataFieldDerivedClasses.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
