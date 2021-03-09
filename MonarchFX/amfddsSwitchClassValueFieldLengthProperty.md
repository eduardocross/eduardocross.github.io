---
title: DdsSwitch.ValueFieldLength Property

Id: amfDdsSwitchClassValueFieldLengthProperty
TocParent: amfDdsSwitchClassPropertiesMain
TocOrder: 46

keywords: ValueFieldLength property
keywords: DdsSwitch.ValueFieldLength property
keywords: how to, set switch value field characters
keywords: switches, Value field length
keywords: switches, field length

---

Gets or sets the length (in characters) of the DdsSwitch's Value Field.

#### Syntax
<pre class="prettyprint"> **BegProp ValueFieldLength Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. A number that sets the character length for the [ValueField](amfDdsSwitchClassValueFieldProperty.html). Defaults to '1'.

#### Remarks
To avoid throwing an error, the values of [ValueField](amfDdsSwitchClassValueFieldProperty.html), [ValueOn](amfDdsSwitchClassValueOnProperty.html), and [ValueOff](amfDdsSwitchClassValueOffProperty.html) must all match the length defined by this property.

This control was introduced with version ASNA Mobile Support version 8.0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSwitch Class](amfDdsSwitchClass.html) <br /> [DdsSwitch Class Members](amfDdsSwitchClassMembers.html) <br />[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
