---
title: DdsSwitch.LabelTextField Property

Id: amfDdsSwitchClassLabelTextFieldProperty
TocParent: amfDdsSwitchClassPropertiesMain
TocOrder: 09

keywords: LabelTextField property
keywords: DdsSwitch.LabelTextField property
keywords: how to, label switch text field
keywords: switches label fields
keywords: switch label textfield

---

Gets or sets a string that defines the field from which the text for the label will be drawn.

#### Syntax
<pre class="prettyprint"> **BegProp LabelTextField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string that sets the field that the text for the switch's label will come from. Defaults to "".

#### Remarks
This property requires [LabelTextFieldLength](amfddsSwitchClassLabelTextFieldLengthProperty.html), and overrides [LabelText](amfddsSwitchClassLabelTextProperty.html). 

This control was introduced with version ASNA Mobile Support version 8.0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSwitch Class](amfDdsSwitchClass.html) <br /> [ DdsSwitch Class Members](amfDdsSwitchClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
