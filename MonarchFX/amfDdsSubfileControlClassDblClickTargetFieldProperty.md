---
title: DdsSubfileControl.DblClickTargetField Property

Id: amfDdsSubfileControlClassDblClickTargetFieldProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 13

keywords: DblClickTargetField property
keywords: DdsSubfileControl.DblClickTargetField property
keywords: subfiles, conditional indicator expression controlling doubleclick
keywords: web controls, conditional indicator expression controlling truncated display
keywords: how to, set conditional indicator expression to control truncated display
keywords: how to, get conditional indicator expression controlling truncated display
keywords: subfile records, conditional indicator expression controlling truncated display
keywords: subfile usage, conditional indicator expression controlling truncated display

---

Gets or sets the name of the field to be modified when double-click is detected. 

#### Syntax
<pre class="prettyprint"> **BegProp DblClickTargetField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string value containing the name of the field to be modified when a double-click event is detected in the subfile area.

#### Remarks
By default, no value is generated for this property during migration; it must be specified manually. To set this property at design-time, right click the **DblClickTargetField** property and enter the name of the field to be modified into the text box.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
