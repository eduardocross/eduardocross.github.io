---
title: DbcsFormat Enumeration

Id: dcsDbcsFormatEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 9

keywords: enumerations [DCS 16.0 DbcsFormat
keywords: DbcsFormat enumeration
keywords: shift control characters
keywords: Either enumeration member
keywords: Graphic enumeration member
keywords: None enumeration member
keywords: Only enumeration member
keywords: Open enumeration member

---

The <span> **DbcsFormat** </span> enumerated constant defines values on whether shift-control characters appear internally on the IBM i. This enumeration is used by the [ Dbcs](dcsFieldTypeClassDbcsProperty.html) property for [FieldType](dcsFieldTypeClass.html) objects.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum DbcsFormat;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum DbcsFormat** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DbcsFormat Access(*Public)** 
      </pre>

Remarks

<span>Dbcs</span> defines values in which you can select one of the choices. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
            <colgroup span="1">
              <col align="middles" span="1" width="8%" style="FONT-WEIGHT: bold" />
              <col span="1" width="40%" />
              <col span="1" width="5%" />
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

Either
</td>
              <td colspan="1" rowspan="1">

Double byte (with shift-control) or single byte.
</td>
              <td colspan="1" rowspan="1">

4
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Graphic
</td>
              <td colspan="1" rowspan="1">

Double byte only (no shift-control).
</td>
              <td colspan="1" rowspan="1">

5
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

None
</td>
              <td colspan="1" rowspan="1">

Shift-control characters do not appear.
</td>
              <td colspan="1" rowspan="1">

0
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Only
</td>
              <td colspan="1" rowspan="1">

Double byte only (with shift-control).
</td>
              <td colspan="1" rowspan="1">

3
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Open
</td>
              <td colspan="1" rowspan="1">

Mixed single byte/double byte (with shift-control).
</td>
              <td colspan="1" rowspan="1">

2
</td>
            </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
        [AdgDataSet Class](dcsAdgDataSetClass.html)
        <br />
        [Dbcs Property](dcsFieldTypeClassDbcsProperty.html)
        <br />
        [FieldType Class](dcsFieldTypeClass.html)
        <br />
        [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

