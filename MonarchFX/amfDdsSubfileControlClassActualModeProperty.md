---
title: DdsSubfileControl.ActualMode Property

Id: amfDdsSubfileControlClassActualModeProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 5

keywords: ActualMode property
keywords: DdsSubfileControl.ActualMode property
keywords: subfiles, getting drop or subfile fold mode
keywords: web controls, getting subfile drop or subfile fold mode
keywords: how to, get control subfile drop or subfile fold mode
keywords: subfile records, getting subfile drop or subfile fold mode
keywords: subfile usage, getting subfile drop or subfile fold mode

---

Gets the subfile drop or fold state of the subfile control.

#### Syntax
<pre class="prettyprint"> **BegProp ActualMode Access(*Public) Type(*SflModes)
   BegGet;** </pre>

#### Property Values
SflModes values indicating the state of the subfile. A 0 if the subfile is Folded, a 1 if the subfile is in Truncated mode, or 2 if neither folded or truncated mode (None).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
