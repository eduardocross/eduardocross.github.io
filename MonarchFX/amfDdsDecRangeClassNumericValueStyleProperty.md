---
title: DdsDecRange.NumericValueStyle Property

Id: amfDdsDecRangeClassNumericValueStyleProperty
TocParent: amfDdsDecRangeClassPropertiesMain

keywords: NumericValueStyle property
keywords: DdsDecRange.NumericValueStyle property
keywords: web controls, setting NumericValueStyle
keywords: web controls, getting NumericValueStyle
keywords: how to, set NumericValueStyle
keywords: how to, get NumericValueStyle
keywords: display files, NumericValueStyle
keywords: Web server controls [ASNA.Monarch], NumericValueStyle
keywords: field controls, NumericValueStyle

---

Sets how the numeric value will be displayed.

#### Syntax
<pre class="prettyprint"> **BegProp NumericValueStyle Access(*Public) Type(enum.NumericValueStyle) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
NumericValueStyle Enumeration. Options include

- Hidden
- Center
- Left
- Right (default)

#### Remarks
This sets the location of the numeric value (if shown) within the control. If the [InteractionStyle](amfddsdecrangeClassInteractionStyleProperty.html)=<code>Slider</code> option is selected, the <code>Center</code> option will be silently ignored.

To set this property at design-time, click to the right of the property and enter the desired value.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDecRange Class](amfDdsDecRangeClass.html) <br /> [ DdsDecRange Class Members](amfDdsDecRangeClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

