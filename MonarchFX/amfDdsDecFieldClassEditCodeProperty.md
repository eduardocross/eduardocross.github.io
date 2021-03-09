---
title: DdsDecField.EditCode Property

Id: amfDdsDecFieldClassEditCodeProperty
TocParent: amfDdsDecFieldClassPropertiesMain
TocOrder: 50

keywords: EditCode property
keywords: DdsDecField.EditCode property
keywords: Web server controls [ASNA.Monarch], field edit code
keywords: how to, set field control edit code
keywords: how to, get field control edit code
keywords: display files, setting field control edit code
keywords: display files, getting field control edit code
keywords: web controls, setting field control edit code
keywords: web controls, getting field control edit code
keywords: field controls, edit code

---

Gets or sets a string containing an edit code to punctuate numeric fields according to the standard RPG edit code rules.

#### Syntax
<pre class="prettyprint"> **BegProp EditCode Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing an edit code to punctuate numeric fields as noted in the first column of the [Edit Code Table](sharedEditCodeTable.html).

#### Remarks
**EditCode** allows you to punctuate numeric fields, including $ signs, commas, periods, minus sign, and floating minus according to the standard RPG edit code rules. To set this property at design time, click on the right side of the property window and enter a valid edit code as listed in the [Edit Code Table](sharedEditCodeTable.html) that gives you the desired display. For example, entering a **J** in the **EditCode** property will display .00, giving you commas, decimals points, and a minus sign when necessary.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl><dd>[DdsDecField
    Class](amfDdsDecFieldClass.html)</dd>
    <dd>[
    DdsDecField Class Members](amfDdsDecFieldClassMembers.html)</dd>
    <dd>[
    ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

