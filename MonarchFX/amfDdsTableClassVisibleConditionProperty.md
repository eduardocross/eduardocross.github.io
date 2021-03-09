---
title: DdsTable.VisibleCondition Property

Id: amfDdsTableClassVisibleConditionProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: VisibleCondition property
keywords: DdsTable.VisibleCondition property
keywords: Web server controls [ASNA MobileRPG], DdsTable VisibleCondition
keywords: how to, set DdsTable VisibleCondition
keywords: how to, get DdsTable VisibleCondition

---

Gets or sets a conditional indicator expression that will be evaluated to determine the conditions under which the table is visible and rendered.

#### Syntax
<pre class="prettyprint"> **BegProp VisibleCondition Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the conditional indicator expression that will be evaluated to determine whether the table is visible and rendered.

#### Remarks
To set this property at design-time, click on the right of the property in the properties window and enter the conditional indicator expression that will determine whether the table is visible and rendered. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) for more information.

Special case insensitive string values may be used to set the condition to either TRUE or FALSE. "*True" means to make the control visible unconditionally. "*False" means to make the control invisible unconditionally.

Note: If the [ Visible](amfDdsPanelClassVisibleProperty.html) property is FALSE, the control will be invisible regardless of the result of the **VisibleCondition** expression. If the result **VisibleCondition** expression is FALSE, the control will be invisible regardless of the state of the **Visible** property. If the **VisibleCondition** property value is empty (no expression given), then the control's visible state relies upon the **Visible** property only.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsTable Class](amfDdsTableClass.html)</dd>
        <dd>[DdsTable Class Members](amfDdsTableClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

