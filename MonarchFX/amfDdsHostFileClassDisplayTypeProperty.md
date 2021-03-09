---
title: DdsHostFile.DisplayType Property

Id: amfDdsHostFileClassDisplayType Property
TocParent: amfDdsHostFileClassPropertiesMain
TocOrder: 03

keywords: DisplayType property
keywords: DdsHostFile.DisplayType  property

---

Determines how the hosted file will be presented on the screen.

#### Syntax
<pre class="prettyprint"> **BegProp DisplayType Access(*Public) Type(*string)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the manner that the file will be presented in the Web Display. Defaults to **Link** .

- **Link**  &#8212; A link that opens on the current page
- **LinkInNew**  &#8212; A link that opens on a new page
- **EmbeddedFrame**  &#8212; An embedded frame that appears on the current page 
		  (note that this may take considerably more screen-space)

#### Remarks
Set this property by locating it in the Properties window for the control, then choosing the desired display type from the dropdown list.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsHostFile Description](amfUnderstandingHostFiles.html)<br /> [ DdsHostFile Class](amfDdsHostFileClass.html) <br /> [ DdsHostFile Class Members](amfDdsHostFileClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
