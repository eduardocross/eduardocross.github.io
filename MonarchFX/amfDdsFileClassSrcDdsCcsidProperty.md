---
title: DdsFile.SrcDdsCcsid Property

Id: amfDdsFileClassSrcDdsCcsidProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 174

keywords: SrcDdsCcsid property
keywords: DdsFile.SrcDdsCcsid property

---

This string sets the Coded Character Set Identifier, (CCSID or Code Page) for this file.

#### Syntax
<pre class="prettyprint"> **BegProp SrcDdsCcsid Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets or gets the CCSID for the DDS Source, effectively selecting the character set to be displayed. Defaults to blank, but can be automatically populated by Monarch and Wings.

#### Remarks
This property is usually populated automatically in Monarch and Wings. It enables Wings Bidirectional support.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsFile Class](amfDdsFileClass.html) <br /> [ DdsFile Class Members](amfDdsFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
