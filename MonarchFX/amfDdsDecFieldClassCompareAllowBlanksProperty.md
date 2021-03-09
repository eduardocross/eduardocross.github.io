---
title: DdsDecField.CompareAllowBlanks Property

Id: amfDdsDecFieldClassCompareAllowBlanksProperty
TocParent: amfDdsDecFieldClassPropertiesMain
TocOrder: 32

keywords: CompareAllowBlanks property
keywords: DdsDecField.CompareAllowBlanks property
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
Use the **<code>CompareAllowBlanks</code>** property to skip the Compare validation on blank fields; in Monarch the <code>CHECK(AB)</code> keyword is migrated as <code>CompareAllowBlanks = True</code>.

Added in 7.2, this feature allows the combination of keywords <code>COMP(GT 0)</code> and <code>CHECK(RB AB)</code> to behave properly in Wings and Monarch.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsCharField Class](amfDdsCharFieldClass.html) <br /> [ DdsCharField Members](amfDdsCharFieldClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DefaultValue Property](amfDdsCharFieldClassDefaultValueProperty.html) <br /> [ UnCompareAllowBlanks Property](amfDdsCharFieldClassUnCompareAllowBlanksProperty.html) <br /> [ InputStyles Property](amfDdsCharFieldClassInputStyleProperty.html) 
