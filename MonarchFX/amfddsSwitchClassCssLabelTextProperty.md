---
title: DdsSwitch.CssLabelText Property

Id: amfDdsSwitchClassCssLabelTextProperty
TocParent: amfDdsSwitchClassPropertiesMain
TocOrder: 05

keywords: CssLabelText property
keywords: DdsSwitch.CssLabelText property
keywords: how to, label switch text
keywords: switches labels
keywords: switch label

---

Gets or sets the CSS Class to apply to the Label Text.

#### Syntax
<pre class="prettyprint"> **BegProp CssLabelText Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string that sets the Cascading Style Sheet Class to apply to the label text. Defaults to "ToggleSwitchLabel".

#### Remarks
This CSS defines (among other styles) the Width of the label element. The default "ToggleSwitchLabel" defines Width as **7em** such that several labels may show their corresponding switch aligned. But if you have more than one group of switches, you may want to use different CSS for them - or even individual CSS for each label in the switch group. 

This control was introduced with version ASNA Mobile Support version 8.0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSwitch Class](amfDdsSwitchClass.html) <br /> [ DdsSwitch Class Members](amfDdsSwitchClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
