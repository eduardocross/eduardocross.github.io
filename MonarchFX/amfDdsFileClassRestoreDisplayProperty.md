---
title: DdsFile.RestoreDisplay Property

Id: amfDdsFileClassRestoreDisplayProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 171

keywords: RestoreDisplay property
keywords: DdsFile.RestoreDisplay property
keywords: Reset key, text
keywords: attention keys, Reset key text
keywords: function keys, Reset key text
keywords: how to, set reset key text
keywords: how to, get reset key text

---

Sets whether data being shown on a display by this display file is saved at the time the file is suspended (made temporarily inactive) so that another display file can show different data on the same device. If the data for this file is saved, it is restored to the display of the device when the file is used again. This mimics the IBM i <code>CRTDSPF</code> parameter <code>RSTDSP</code>.

#### Syntax
<pre class="prettyprint"> **BegProp RestoreDisplay Access(*Public) Type(*Boolean) 
   BegGet;   BegSet** </pre>

#### Property Value
Boolean. If <code>True</code>, the data in the DdsFile will be saved when the file is suspended. If <code>False</code> the data will not be saved.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 8, Windows 10

#### See Also
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
