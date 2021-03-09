---
title: DdsFile.FuncKeys Property

Id: amfDdsFileClassFuncKeysProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 140

keywords: FuncKeys property
keywords: DdsFile.FuncKeys property
keywords: Aid Property Dialog, setting function key values
keywords: function keys, setting
keywords: function keys, getting
keywords: function keys, setting message
keywords: function keys, getting message
keywords: function keys, setting response indicators
keywords: function keys, getting response indicators
keywords: aidkeys, setting
keywords: aidkeys, getting
keywords: aidkeys, setting message
keywords: aidkeys, getting message
keywords: aidkeys, setting response indicators
keywords: aidkeys, getting response indicators
keywords: web controls, setting function keyse
keywords: web controls, getting function keyse
keywords: web controls, setting function key message
keywords: web controls, getting function key message
keywords: web controls, setting function key response indicators
keywords: web controls, getting function key response indicators
keywords: display files, setting function keys
keywords: display files, getting function keys
keywords: display files, setting function key message
keywords: display files, getting function key message
keywords: display files, setting function key response indicators
keywords: display files, getting function key response indicators

---

Gets or sets which keys the user can press, the message to be displayed, and the response indicators to turn on. Input data is transmitted from the Browser.

#### Syntax
<pre class="prettyprint"> **BegProp FuncKeys Access(*Public) Type(ASNA.Monarch.WebDspF.AidProperty)
   BegGet;  BegSet** </pre>

#### Property Value
**ASNA.Monarch.WebDspF.AidProperty** containing the function key settings in a semicolon( **;** ) separated list.

#### Remarks
The **FuncKeys** property contains all function key settings in a semicolon( **;** ) separated list of: function key, 'text' and conditional property (response **:** option indicators).

For example: **F5 'Add' 07 :!99;F6 'Update' *NONE : 09;** 

This property is mainly used to control processing between applications since input data is transmitted from the browser. Use the [ AttnKeys](amfDdsFileClassAttnKeysProperty.html) property to specify function keys that do not transfer input to the Browser.

To set this property at design-time, click on the right of the **FuncKeys** property and the **Aid Property Dialog** will display. Enter the Text and resulting option indicators in the row corresponding to the key to apply to as shown below.

![](Images/zzFuncKeys.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ DdsFile.AttnKeys Property](amfDdsFileClassAttnKeysProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [Overview of Aid Keys](amfconOverviewofAidKeys.html) 
