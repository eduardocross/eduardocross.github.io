---
title: DdsTable.VerticalMargin Property

Id: amfDdsTableClassVerticalMarginProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: VerticalMargin property
keywords: DdsTable.VerticalMargin property
keywords: Web server controls [ASNA MobileRPG], setting DdsTable Vertical Margin
keywords: how to, set DdsTable Vertical Margin
keywords: how to, get DdsTable Vertical Margin

---

Sets a fixed vertical margin for the table, allowing better framing and scrolling.

#### Syntax
<pre class="prettyprint"> **BegProp VerticalMargin Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. An integer that sets the vertical area of the browser or screen to exclude from the table. This value will include header and footer bars created with [DdsBars](amfDdsBarClass.html). This value can be rendered in any measurement recognized by .NET, including px, em, or percentage. Default value is NULL, default unit is pixels.

#### Remarks
When this property is invoked, the DdsTable will calculate the maximum viewable area of the screen or browser it is being displayed in, then deduct the value of this property. This will determine the height of the DdsChart. This technique also enables much more elegant scrolling.

Overrides the Height property.

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

