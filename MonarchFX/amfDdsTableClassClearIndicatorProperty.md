---
title: DdsTable.ClearIndicator Property

Id: amfDdsTableClassClearIndicatorProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: ClearIndicator property
keywords: DdsTable.ClearIndicator property
keywords: Web server controls [ASNA Monarch], setting DdsTable ClearIndicator
keywords: how to, set DdsTable ClearIndicator
keywords: how to, get DdsTable ClearIndicator

---

Sets the IBM i clear indicator for the subfile underlying the table.

#### Syntax
<pre class="prettyprint"> **BegProp ClearIndicator Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. An integer defining the clear indicator for the subfile that provides data for the table. Defaults to 99.

#### Remarks
Defines the clear indicator for the table's underlying subfile. Set in the DdsTable tasks window.

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

