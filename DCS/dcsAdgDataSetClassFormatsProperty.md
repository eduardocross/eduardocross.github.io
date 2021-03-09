---
title: AdgDataSet.Formats Property

Id: dcsAdgDataSetClassFormatsProperty
TocParent: dcsAdgDataSetProperties
TocOrder: 4

keywords: AdgDataSet.Formats property
keywords: Formats property
keywords: record formats, number of in an AdgDataSet
keywords: number of, record formats in an AdgDataSet
keywords: how to, determine number of record formats in an AdgDataSet
keywords: format identifiers, number of record formats in an AdgDataSet
keywords: binary format identifiers associated with an AdgDataSet, number of

---

The number of formats in this **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int Formats { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Formats As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Formats Access(*Public) Type(*Integer) Len(4)
   BegGet** 
      </pre>

Property
 Value

Integer. The count of formats in this **AdgDataSet** . 
Remarks

An **AdgDataSet** object is a reflection of a DataGate file, including its record formats. The number of record formats in the file upon which the **AdgDataSet** is based is given by the **Formats** property. This number is the upper bound for integer indices used to identify formats in **AdgDataSet** methods such as [ GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

