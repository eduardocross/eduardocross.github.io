---
title: DdsDateField.CompareAllowBlanks Property

Id: amfDdsDateFieldClassCompareAllowBlanksProperty
TocParent: amfDdsDateFieldClassPropertiesMain
TocOrder: 7

keywords: CompareAllowBlanks property
keywords: DdsDateField.CompareAllowBlanks property
keywords: Web server controls [ASNA.Monarch], Allow Blanks
keywords: how to, set field control to allow blanks
keywords: how to, get field control to allow blanks
keywords: display files, setting field control to allow blanks
keywords: display files, getting field control tO allow blanks
keywords: web controls, setting field control to allow blanks
keywords: web controls, getting field control to allow blanks
keywords: field controls, compare allow blanks
keywords: compare allow blanks

---

If <code>True</code>, Compare validation will be skipped when field value is blank.

#### Syntax
<pre class="syntax"> **BegProp CompareAllowBlanks Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Value
Boolean that sets whether to skip Compare validation on blank fields. Defaults to <code>False</code>

#### Remarks
Use the **<code>CompareAllowBlanks</code>** property to skip the Compare validation on blank fields, allowing a "blank" or date "low value" to be accepted even if it doesn't satisfy the Compare condition.

Added in late 8.0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsDateField Class](amfDdsDateFieldClass.html) <br /> [ DdsDateField Members](amfDdsDateFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> 
