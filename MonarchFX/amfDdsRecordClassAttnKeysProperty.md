---
title: DdsRecord.AttnKeys Property

Id: amfDdsRecordClassAttnKeysProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 20

keywords: AttnKeys property
keywords: DdsRecord.AttnKeys property
keywords: Aid Property Dialog, setting attention key values
keywords: available aid keys
keywords: aidkeys, setting values
keywords: aidkeys, getting values
keywords: aidkeys, setting response indicators
keywords: aidkeys, getting response indicators
keywords: web controls, setting attention key values
keywords: web controls, getting attention key values
keywords: subfiles, setting attention key values
keywords: subfiles, getting attention key values
keywords: subfile controls, setting attention key values
keywords: subfile controls, getting attention key values
keywords: subfile records, setting attention key values
keywords: subfile records, getting attention key values
keywords: records, setting attention key values
keywords: records, getting attention key values
keywords: how to, set attention key values
keywords: how to, get attention key values
keywords: conditioning expressions, attention keys
keywords: response indicators, setting for attention keys
keywords: response indicators, getting for attention keys
keywords: display files, response indicators for attention keys
keywords: display files, attention keys
keywords: attention keys

---

Gets or sets the keys the user can press, the message to be displayed, and the response indicators to turn on. No input data is transmitted from the Browser.

This is a Conditional Property and is subject to specific rules outlined in the [Conditional Property Overview](amfconConditionalPropertiesOverview.html).

#### Syntax
<pre class="prettyprint"> **BegProp AttnKeys Access(*Public) Type(ASNA.Monarch.WebDspF.AidProperty)
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidProperty** containing the attention key settings in a semicolon( **;** ) separated list.

#### Remarks
The **AttnKeys** property contains all attention key settings in a semicolon( **;** ) separated list of function key, 'text' and response **:** option indicators.

For example: **F3 'Cancel' 03 ;F4 'Exit' 04;** 

This property is mainly used to control processing within the application to control flow within the form since NO input data is transmitted from the browser. Use the [ FuncKeys](amfDdsRecordClassFuncKeysProperty.html) property to specify function keys that transfer input to the Browser.

To set this property at design-time, click on the right of the **AttnKeys** property and the **Aid Property Dialog** will display as shown below. Enter the Text and resulting option indicators in the row corresponding to the key to apply to.

![](Images/zzDdsRecordAttnKeys.jpg) 

This is a Conditional Property and is subject to specific rules outlined in the [Conditional Property Overview](amfconConditionalPropertiesOverview.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ DdsRecord.FuncKeys Property](amfDdsRecordClassFuncKeysProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
