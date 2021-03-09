---
title: DdsPanel.VisibleCondition Property

Id: amfDdsPanelClassVisibleConditionProperty
TocParent: amfDdsPanelClassProperties
TocOrder: 110

keywords: VisibleCondition property
keywords: DdsPanel.VisibleCondition property
keywords: conditioning expressions, setting for panel
keywords: visibility, setting conditional expression
keywords: panel visibility, setting conditional expression
keywords: how to, set panel visible conditional expression
keywords: web controls, setting panel visible conditional expression
keywords: display files, setting panel visible conditional expression

---

Gets or sets a conditional indicator expression that will be evaluated to determine the conditions under which the panel is visible and rendered.

#### Syntax
<pre class="prettyprint"> **BegProp VisibleCondition Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the conditional indicator expression that will be evaluated to determine whether the panel is visible and rendered.

#### Remarks
To set this property at design-time, click on the right of the property in the properties window and enter the conditional indicator expression that will determine whether the panel is visible and rendered. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information.

Special case insensitive string values may be used to set the condition to either TRUE or FALSE. "*True" means to make the control visible unconditionally. "*False" means to make the control invisible unconditionally.

Note: If the [ Visible](amfDdsPanelClassVisibleProperty.html) property is FALSE, the control will be invisible regardless of the result of the **VisibleCondition** expression. If the result **VisibleCondition** expression is FALSE, the control will be invisible regardless of the state of the **Visible** property. If the **VisibleCondition** property value is empty (no expression given), then the control's visible state relies upon the **Visible** property only.

#### Example
<pre class="example">ControlName.VisibleCondition = "(46 &amp; !47)"
ControlName.VisibleCondition = "!(13 | !15)"
ControlName.VisibleCondition = "*true"
ControlName.VisibleCondition = *false"
</pre>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsPanel Description](amfUnderstandingPanels.html)<br /> [DdsPanel Class](amfDdsPanelClass.html) <br clear="none" /> [DdsPanel Class Members](amfDdsPanelClassMembers.html) <br clear="none" /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
