---
title: DdsField.VisibleCondition Property

Id: amfDdsFieldClassVisibleConditionProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 60

keywords: Web server controls [ASNA.Monarch], setting field control visibility conditions
keywords: field controls, visibility conditions
keywords: how to, set field control visiblility conditions
keywords: how to, get field control visiblility conditions
keywords: web controls, setting field control visibility conditions
keywords: web controls, getting field control visibility conditions
keywords: display files, setting field control visibility conditions
keywords: display files, getting field control visibility conditions
keywords: indicator expressions, field control visibility
keywords: conditioning expressions, field control visibility
keywords: VisibleCondition property
keywords: DdsField.VisibleCondition property

---

Gets or sets the *RPG indicator* expression that, when evaluated, determines if the field should be visible.

#### Syntax
<pre class="prettyprint"> **BegProp VisibleCondition Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
**String** containing the *RPG indicator* expression that, when evaluated, determines if the field should be visible.

#### Remarks
To set this property, click on the right hand side of the property window and enter the conditional indicators that will determine the visibility of the control. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

Special case insensitive string values may be used to set the condition to either TRUE or FALSE. "*True" means to make the control visible unconditionally. "*False" means to make the control invisible unconditionally.

Note: If the [ Visible](amfDdsFieldClassVisibleProperty.html) property is FALSE, the control will be invisible regardless of the result of the **VisibleCondition** expression. If the result **VisibleCondition** expression is FALSE, the control will be invisible regardless of the state of the **Visible** property. If the **VisibleCondition** property value is empty (no expression given), then the control's visible state relies upon the **Visible** property only.
<!--mine -->

#### Example
<pre class="example">ControlName.VisibleCondition = "(46 &amp; !47)"
ControlName.VisibleCondition = "!(13 | !15)"
ControlName.VisibleCondition = "*true"
ControlName.VisibleCondition = *false"</pre>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsField Class](amfDdsFieldClass.html) <br clear="none" /> [ DdsField.Visible Property](amfDdsFieldClassVisibleProperty.html) <br clear="none" /> [ Derived classes](amfDdsFieldClassDerivedClasses.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br clear="none" /> [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) 
