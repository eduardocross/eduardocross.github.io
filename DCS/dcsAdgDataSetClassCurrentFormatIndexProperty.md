---
title: AdgDataSet.CurrentFormatIndex Property

Id: dcsAdgDataSetClassCurrentFormatIndexProperty
TocParent: dcsAdgDataSetProperties
TocOrder: 1

keywords: AdgDataSet.CurrentFormatIndex property
keywords: CurrentFormatIndex property
keywords: records, index of active record format
keywords: index for active record format
keywords: active records, format index of AdgDataSet
keywords: rows, format index currently active
keywords: format index of AdgDataSet active record
keywords: how to, return format index for active record
keywords: tables, format index currently active

---

The current format index of the **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int CurrentFormatIndex { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property CurrentFormatIndex As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp CurrentFormatIndex Access(*Public) Type(*Integer) Len(4)
   BegGet** 
      </pre>

Property Value

**Integer** . The format index of the record contained by the [ ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) property.
Remarks

**CurrentFormatIndex** is related to **ActiveRow** , in that the format of the record contained by **ActiveRow** is identified by the value of **CurrentFormatIndex.** Upon construction, **ActiveRow** has no value and the value of **CurrentFormatIndex** is -1.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Members](dcsAdgDataSetMembers.html)
      <br />
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

