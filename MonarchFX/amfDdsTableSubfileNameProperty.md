---
title: DdsTable.SubfileName Property

Id: amfDdsTableClassSubfileNameProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SubfileName property
keywords: DdsTable.SubfileName property
keywords: Web server controls [ASNA MobileRPG], setting DdsTable SubfileName
keywords: how to, set DdsTable SubfileName
keywords: how to, get DdsTable SubfileName

---

Gets or sets a string containing the Name of the subfile record format used for the table data.

#### Syntax
<pre class="prettyprint"> **BegProp SubfileName Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the Name of the subfile record format used for the table data.

#### Remarks
This required property works with [SubfileControlName](amfDdsTableClassSubfileControlNameProperty.html) to define the subfile from which MobileRPG will draw the data for the DdsTable.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsTable Class](amfDdsTableClass.html)</dd>
        <dd>[DdsTable Class Members](amfDdsTableClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

