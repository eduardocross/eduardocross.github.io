---
title: DdsSubfileControl.DblClickTargetValue Property

Id: amfDdsSubfileControlClassDblClickTargetValueProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 14

keywords: SubfileDrop property
keywords: DdsSubfileControl.SubfileDrop property
keywords: subfiles, conditional indicator expression controlling truncated display
keywords: web controls, conditional indicator expression controlling truncated display
keywords: how to, set conditional indicator expression to control truncated display
keywords: how to, get conditional indicator expression controlling truncated display
keywords: subfile records, conditional indicator expression controlling truncated display
keywords: subfile usage, conditional indicator expression controlling truncated display

---

Gets or sets the value that the target field is to be set to. 

#### Syntax
<pre class="prettyprint"> **BegProp DblClickTargetValue Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string value that provides the value of the field to set be modified (by the [DblClickTargetField](amfDdsSubfileControlClassDblClickTargetField.html) property) when a double-click event is detected.

#### Remarks
This property requires the DblClickTargetField to contain the name of a valid field in the corresponding record.

To set this property at design-time, right click the **DblClickTargetValue** property and enter the conditional indicators. <br />

This property was added with Wings 5.2.<br />

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
