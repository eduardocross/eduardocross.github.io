---
title: DdsField.Color Property

Id: amfDdsFieldClassColorProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 10

keywords: Web server controls [ASNA.Monarch], setting field color
keywords: how to, set field control color
keywords: how to, get field control color
keywords: display files, setting field control color
keywords: display files, getting field control color
keywords: web controls, setting field control color
keywords: web controls, getting field control color
keywords: field controls, color
keywords: indicator expressions, controlling color
keywords: conditioning expressions, controlling color
keywords: Color property
keywords: Color Property Editor, setting values
keywords: DdsField.Color property

---

Gets or sets a new instance of a [ ColorProperty](amfColorPropertyClass.html) object containing the conditional values that control the color of the field.

#### Syntax
<pre class="prettyprint"> **BegProp Color Access(*Public) Type(<a>ColorProperty</a>)
   BegGet;  BegSet** </pre>

#### Property Values
**ColorProperty** object containing the conditional values to control the color for the field.

#### Remarks
To set the **Color** property, click on the right side of the property window and the **Color Property Editor** window will display as shown below. Enter the color value and conditional indicator that when evaluated to true, will cause the selected color to be used.

Enter the *Value* representing the color (must be a valid [Conditional Properties Overview](http://msdn2.microsoft.com/en-us/library/system.drawing.color.aspx"> System.Drawing.Color</a>) to be selected, and also the condition under which that color will be used. For example, in the display below: " **Green:!61** and **DarkBlue:61** " means the value Green is selected if *IN61 is *OFF, while DarkBlue is selected if *IN61 is *ON.

See <a href="amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

![](Images/zzcolorpropertyEditor.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsField Class](amfDdsFieldClass.html) <br /> [ Derived classes](amfDdsFieldClassDerivedClasses.html) <br />[ ColorProperty Class](amfColorPropertyClass.html)<br />[Conditional Properties Overview](http://msdn2.microsoft.com/en-us/library/system.drawing.color.aspx">System.Drawing.Color</a>) <br /><a href="amfconConditionalPropertiesOverview.html)<br />[ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
