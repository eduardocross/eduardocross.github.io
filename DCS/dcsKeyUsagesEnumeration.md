---
title: KeyUsages Enumeration

Id: dcsKeyUsagesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 18

keywords: KeyUsages enumeration
keywords: enumerations [DCS 16.0 KeyUsages
keywords: ASCEND enumeration member
keywords: DESCEND enumeration member
keywords: ABSVALUE enumeration member
keywords: SIGNED enumeration member
keywords: UNSIGNED enumeration member
keywords: DIGIT enumeration member
keywords: ZONE enumeration member

---

Key definition properties which apply to a key field.<span style="MARGIN-BOTTOM: 0.8em" />
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum KeyUsages;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum KeyUsages** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum KeyUsages Access(*Public)** 
      </pre>

Remarks

These properties are used when defining a key with the parameters of the [ FileAdapter.OpenSimpleQuery](dcsFileAdapterClassOpenSimpleQueryMethod.html) method. DCS also uses **KeyUsages** for internal file definition methods. Most values of **KeyUsages** can be combined to specify more than one value. *ASCEND* and *DESCEND* cannot be combined in the same **KeyUsages** value. The following table lists each value and the effect on key fields to which it is applied.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col span="1" width="10%" />
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

ASCEND
</td>
            <td colspan="1" rowspan="1">

index value is sequence in ascending order.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DESCEND
</td>
            <td colspan="1" rowspan="1">

<p>Index value is sequenced in decending order.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ABSVALUE
</td>
            <td colspan="1" rowspan="1">

Index value is interpreted as the absolute value of the format field.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SIGNED
</td>
            <td colspan="1" rowspan="1">

Index value is interpreted as the signed value of the format field.
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

UNSIGNED
</td>
            <td colspan="1" rowspan="1">

Index value is interpreted as the unsigned value of the format field.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DIGIT
</td>
            <td colspan="1" rowspan="1">

Each byte of index value masks the rightmost 4 bits only.
</td>
            <td colspan="1" rowspan="1">

16
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ZONE
</td>
            <td colspan="1" rowspan="1">

Each byte of index value masks the leftmost 4 bits only.
</td>
            <td colspan="1" rowspan="1">

32
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ALTSEQ
</td>
            <td colspan="1" rowspan="1">

This is a reserved value for ASNA internal use only.
</td>
            <td colspan="1" rowspan="1">

64
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SEPARATOR
</td>
            <td colspan="1" rowspan="1">

This is a reserved value for ASNA internal use only.
</td>
            <td colspan="1" rowspan="1">

128
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [File Adapter Class](dcsFileAdapterClass.html)
      <br />
      [OpenSimpleQuery Method](dcsFileAdapterClassOpenSimpleQueryMethod.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

