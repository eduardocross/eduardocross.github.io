---
title: SeekMode Enumeration

Id: dcsSeekModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 29

keywords: Equal enumeration member
keywords: First enumeration member
keywords: Greater enumeration member
keywords: Last enumeration member
keywords: SetGE enumeration member
keywords: SetGT enumeration member
keywords: SetLL enumeration member
keywords: SeekMode enumeration
keywords: enumerations [DCS 16.0 SeekMode

---

Defines modes of operation for the [FileAdapter.SeekKey](dcsFileAdapterClassSeekKeyMethod.html) and [FileAdapter.SeekRRN](dcsFileAdapterClassSeekRRNMethod.html) methods.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum SeekMode;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum SeekMode** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum SeekMode Access(*Public)** 
      </pre>

Remarks

The **SeekMode** enumeration is used as a parameter by the [ SeekKey](dcsFileAdapterClassSeekKeyMethod.html) and [SeekRRN](dcsFileAdapterClassSeekRRNMethod.html) methods of the [FileAdapter](dcsFileAdapterClass.html) class. It defines operational modes for these methods as listed in the table below.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
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

Equal 
</td>
            <td colspan="1" rowspan="1">

Seeks the record with a key equal to the search argument. 
</td>
            <td colspan="1" rowspan="1">

13 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

First 
</td>
            <td colspan="1" rowspan="1">

First record in the file without regard to the value of search argument. 
</td>
            <td colspan="1" rowspan="1">

5 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Greater 
</td>
            <td colspan="1" rowspan="1">

Seeks the position in the file at the first record in the file that is greater than the value of search argument. 
</td>
            <td colspan="1" rowspan="1">

14 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Last 
</td>
            <td colspan="1" rowspan="1">

Seeks the position in the file after the last record in the file without regard to the value of search argument. 
</td>
            <td colspan="1" rowspan="1">

6 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SetGE 
</td>
            <td colspan="1" rowspan="1">

Seeks the position in a file at the next record that has a key that is greater than or equal to the search argument. 
</td>
            <td colspan="1" rowspan="1">

15 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SetGT 
</td>
            <td colspan="1" rowspan="1">

Seeks the position in a file at the next record that has a key that is greater the search argument. 
</td>
            <td colspan="1" rowspan="1">

46 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SetLL 
</td>
            <td colspan="1" rowspan="1">

Seeks the position in a file at the next record that has a key that is less than to the search argument. 
</td>
            <td colspan="1" rowspan="1">

47 
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [SeekKey Method](dcsFileAdapterClassSeekKeyMethod.html)
      <br />
      [SeekRRN Method](dcsFileAdapterClassSeekRRNMethod.html) <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

