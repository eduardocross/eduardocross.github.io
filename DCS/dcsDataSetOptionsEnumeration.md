---
title: DataSetOptions Enumeration

Id: dcsDataSetOptionsEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 6

keywords: enumerations [DCS 16.0 DataSetOptions
keywords: DataSetOptions enumeration

---

The <span> **DataSetOptions** </span> enumeration names are reserved for AVR for Visual Studio 2019 use so you must use the associated numeric value. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum DataSetOptions;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Enum DataSetOptions** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DataSetOptions Access(*Public)** 
      </pre>

Remarks

Currently the symbolic names are reserved for AVR for Visual Studio 2019 use, so you must use the associated numeric value.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="12%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col align="middles" span="1" width="8%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

FieldAsAttributes
</td>
            <td colspan="1" rowspan="1">

Use the field as the attributes when creating the dataset object.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OmitKeys
</td>
            <td colspan="1" rowspan="1">

Omit the keys when creating the dataset object.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [GetAdgDataSet Method](dcsIFileObjectClassGetAdgDataSetMethod.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

