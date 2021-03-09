---
title: DdsTable.FieldDecimals Property

Id: amfDdsTableClassFieldDecimalsProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: FieldDecimals property
keywords: DdsTable.FieldDecimals property
keywords: Web server controls [ASNA Monarch], setting DdsTable Field Decimals
keywords: how to, set DdsTable FieldDecimals
keywords: how to, get DdsTable FieldDecimals
keywords: DdsTable Field Decimals

---

Gets or sets an integer defining the number of decimal spaces in a group of a DdsTable's numeric columns.

#### Syntax
<pre class="prettyprint"> **BegProp FieldDecimals Access(*Public) Type(*Int)
   BegGet;  BegSet** </pre>

#### Property Values
Int. An integer containing the that defines the number of decimals places present in the numeric field.

#### Remarks
This property is only used by Columns of type: BinaryColumn, PackedColumn, and ZonedColumn.

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

