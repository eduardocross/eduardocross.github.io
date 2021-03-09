---
title: DdsBaseDate.Visible Property

Id: amfDdsBaseDateClassVisibleProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 250

keywords: Visible property
keywords: DdsBaseDate.Visible property
keywords: Web server controls [ASNA.Monarch], field visibility
keywords: how to, set field control visibility
keywords: how to, get field control visibility
keywords: display files, setting field control visibility
keywords: display files, getting field control visibility
keywords: web controls, setting field control visibility
keywords: web controls, getting field control visibility
keywords: field controls, visibility

---

Gets or sets a boolean value that indicates whether a date field is visible on the page.

#### Syntax
<pre class="syntax"> **BegProp Visible Access(*Public) Type(*Boolean) Modifier(*Overrides)
   BegGet;  BegSet** 
      </pre>

#### Property Values
Boolean value set **True** if the field is visible on the page; otherwise **False** .

#### Remarks
Conditional indicators can be set to control the visibility of the field. The evaluation of these conditional indicators can control the boolean value setting of this property (see [ DdsField.VisibleCondition Property](amfDdsFieldClassVisibleConditionProperty.html)).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br />[ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html)<br />[ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ DdsField.VisibleCondition Property](amfDdsFieldClassVisibleConditionProperty.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
