---
title: DdsSubfileControl.SflMode Property

Id: amfDdsSubfileControlClassSflModeProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 100

keywords: SflMode property
keywords: DdsSubfileControl.SflMode property
keywords: controling subfile drop and subfile fold
keywords: subfiles, indicating drop and subfile fold
keywords: web controls, indicating subfile drop and subfile fold
keywords: how to, set control subfile drop and subfile fold mode
keywords: how to, get control subfile drop and subfile fold mode
keywords: subfile records, indicating subfile drop and subfile fold
keywords: subfile usage, indicating subfile drop and subfile fold

---

Gets or sets the name of the field in which the state of the subfile will be contained. 

#### Syntax
<pre class="prettyprint"> **BegProp SflMode Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String value containing the name of the field in which the state (0 folded or 1 truncated) of the subfile will be contained.

#### Remarks
A field must be specified to hold the value. The field will contain 0 if the subfile is in folded mode or a 1 if the subfile is in truncated mode.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
