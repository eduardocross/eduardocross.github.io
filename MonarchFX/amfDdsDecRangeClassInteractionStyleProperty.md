---
title: DdsDecRange.InteractionStyle Property

Id: amfDdsDecRangeClassInteractionStyleProperty
TocParent: amfDdsDecRangeClassPropertiesMain

keywords: InteractionStyle property
keywords: DdsDecRange.InteractionStyle property
keywords: web controls, setting InteractionStyle
keywords: web controls, getting InteractionStyle
keywords: how to, set InteractionStyle
keywords: how to, get InteractionStyle
keywords: display files, InteractionStyle
keywords: Web server controls [ASNA.Monarch], InteractionStyle
keywords: field controls, InteractionStyle

---

Defines the style of interaction for an instance of DdsDecRange control.

#### Syntax
<pre class="prettyprint"> **BegProp InteractionStyle Access(*Public) Type(enum) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
Emumeration that sets the display and interaction style of the DdsDecRange. Options are:

- Buttons
- Slider

#### Remarks
This property determines which interactive elements the control will have: either buttons or a slider. If the <code>Slider</code> is selected, the [NumericValueStyle](amfddsdecrangeClassNumericValueStyleProperty.html) option <code>Center</code> will be silently ignored and hidden.

To set this property at design-time, click to the right of the property and enter the alternate name for the field.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsDecRange Class](amfDdsDecRangeClass.html) <br /> [ DdsDecRange Class Members](amfDdsDecRangeClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
<!-- last one -->

