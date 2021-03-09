---
title: DdsLink.VisibleCondition Property

Id: amfDdsLinkClassVisibleConditionProperty
TocParent: amfDdsLinkClassPropertiesMain
TocOrder: 180

keywords: VisibleCondition property
keywords: DdsLink.VisibleCondition property
keywords: Hyperlink, visible condition
keywords: hyperlink fields, visible condition
keywords: hyperlink field visibility
keywords: how to, set hyperlink visible condition
keywords: how to, get hyperlink visible condition
keywords: web controls, setting hyperlink visible condition
keywords: display files, setting hyperlink visible condition

---

Gets or sets a conditional indicator expression that will be evaluated to determine the conditions under which the field is visible and rendered.

#### Syntax
<pre class="prettyprint"> **BegProp VisibleCondition Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. The conditional indicator expression that will be evaluated to determine whether the field is visible and rendered.

#### Remarks
To set this property at design-time, click on the right of the property in the properties window and enter the conditional indicator expression that will determine whether the field is visible and rendered. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information.

Special case insensitive string values may be used to set the condition to either TRUE or FALSE. "*True" means to make the control visible unconditionally. "*False" means to make the control invisible unconditionally.

Note: If the [ Visible](amfDdsFieldClassVisibleProperty.html) property is FALSE, the control will be invisible regardless of the result of the **VisibleCondition** expression. If the result **VisibleCondition** expression is FALSE, the control will be invisible regardless of the state of the **Visible** property. If the **VisibleCondition** property value is empty (no expression given), then the control's visible state relies upon the **Visible** property only.

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
[DdsLink Description](amfUnderstandingLinks.html)<br /> [DdsLink Class](amfDdsLinkClass.html) <br clear="none" /> [DdsLink Class Members](amfDdsLinkClassMembers.html) <br clear="none" /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
