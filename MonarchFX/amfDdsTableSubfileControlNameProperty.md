---
title: DdsTable.SubfileControlName Property

Id: amfDdsTableClassSubfileControlNameProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SubfileControlName property
keywords: DdsTable.SubfileControlName property
keywords: Web server controls [ASNA MobileRPG], setting DdsTable SubfileControlName
keywords: how to, set DdsTable SubfileControlName
keywords: how to, get DdsTable SubfileControlName

---

Gets or sets a string containing the name of the subfile control that holds the [SubfileName](amfDdsTableClassSubfileNameProperty.html).

#### Syntax
<pre class="prettyprint"> **BegProp SubfileControlName Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string containing the name of the subfile control that holds the [SubfileName](amfDdsTableClassSubfileNameProperty.html).

#### Remarks
This required property works with [SubfileName](amfDdsTableClassSubfileNameProperty.html) to define the subfile tfrom which MobileRPG will draw the data for the DdsTable.

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

