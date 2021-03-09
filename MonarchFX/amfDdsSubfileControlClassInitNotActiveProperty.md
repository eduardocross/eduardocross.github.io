---
title: DdsSubfileControl.InitNotActive Property

Id: amfDdsSubfilecontrolClassInitNotActiveProperty
TocParent: amfDdsSubfileControlClassPropertiesMain
TocOrder: 51

keywords: InitNotActive property
keywords: DdsSubfileControl.InitNotActive property
keywords: how to, control added record behavior
keywords: subfiles, determine if data is rendered to browser
keywords: subfile fields, controlling data displayed
keywords: subfile records, controlling data displayed
keywords: web controls, controlling data rendered to browser
keywords: subfile usage, InitNotActive
keywords: subfile usage, controlling data rendering

---

Gets or sets a boolean value that, when "true", causes records added to the subfile to be non-active when initializing the subfile records (because expression for InitializeRecords evaluates to true) - meaning that they are not part of the subfile yet until the records are written to, or the user enters values into them. The default is **False** .

#### Syntax
<pre class="prettyprint"> **BegProp InitNotActive Access(*Protected) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
**True** if records added to the subfile are non-active until they are written to, or have values emtered by the user. 

**False** if new records are immediately active.

#### Remarks
To set this property at design-time, click on the right of the **InitNotActive** property and select ** *True* ** or ** *False* ** from the drop-down box.

This property supports the SFLRNA keyword.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfileControl Class](amfDdsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfDdsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
