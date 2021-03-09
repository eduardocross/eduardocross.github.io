---
title: DdsRecord.FuncKeys Property

Id: amfDdsRecordClassFuncKeysProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 80

keywords: FuncKeys property
keywords: DdsRecord.FuncKeys property
keywords: Aid Property Dialog, setting function key values
keywords: available aid keys
keywords: aidkeys, setting values
keywords: aidkeys, getting values
keywords: aidkeys, setting response indicators
keywords: aidkeys, getting response indicators
keywords: web controls, setting function key values
keywords: web controls, getting function key values
keywords: subfiles, setting function key values
keywords: subfiles, getting function key values
keywords: subfile controls, setting function key values
keywords: subfile controls, getting function key values
keywords: subfile records, setting function key values
keywords: subfile records, getting function key values
keywords: records, setting function key values
keywords: records, getting function key values
keywords: how to, set function key values
keywords: how to, get function key values
keywords: conditioning expressions, function keys
keywords: response indicators, setting for function keys
keywords: response indicators, getting for function keys
keywords: display files, response indicators for function keys
keywords: display files, function keys
keywords: function keys

---

Gets or sets the keys the user can press, the message to be displayed, and the response indicators to turn on. Input data is transmitted from the Browser.

This is a Conditional Property and is subject to specific rules outlined in the [Conditional Property Overview](amfconConditionalPropertiesOverview.html).

#### Syntax
<pre class="prettyprint"> **BegProp FuncKeys Access(*Public) Type(ASNA.Monarch.WebDspF.AidProperty)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidProperty** containing the function key settings in a semicolon( **;** ) separated list.

#### Remarks
The **FuncKeys** property contains all function key settings in a semicolon( **;** ) separated list of function key, 'text' and response **:** option indicators.

For example: **F4 'PROMPT' 04;F6 'ADD' 06 : !30;F11 'Delete' 11 : !30;F12 'Cancel' 12;** 

This property is mainly used to control processing between applications since input data is transmitted from the browser. Use the [ AttnKeys](amfDdsRecordClassAttnKeysProperty.html) property to specify function keys that do not transfer input to the Browser.

**Warning &#8211;** Designers must ensure that this property defines the AidKeys set by the [AidKey](amdDdsButtonClassAidKeyProperty.html) property of each [DdsButton](amfDdsButtonClass.html) property contained by the DdsRecord. Otherwise the DdsButtons will not work.

To set this property at design-time, click on the right of the **FuncKeys** property and the **Aid Property Dialog** will display as shown below. Enter the Text and response **:** option indicators in the row corresponding to the key to apply to.

When the user presses a function key defined, the record containing the changed fields is returned to the program. If a response indicator is also specified, the response indicator is set on and passed to the program with the input data.

![](Images/zzDdsRecordFuncKeys.jpg) 

This is a Conditional Property and is subject to specific rules outlined in the [Conditional Property Overview](amfconConditionalPropertiesOverview.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ DdsRecord.AttnKeys Property](amfDdsRecordClassAttnKeysProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
