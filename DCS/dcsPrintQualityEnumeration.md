---
title: PrintQuality Enumeration

Id: dcsPrintQualityEnumeration

keywords: Draft enumeration member
keywords: Low enumeration member
keywords: Medium enumeration member
keywords: High enumeration member
keywords: PrintQuality enumeration
keywords: enumerations [DCS 16.0 PrintQuality
keywords: printing, quality, constants
keywords: quality, constants
keywords: printer device parameters, quality constants

---

The **PrintQuality** enumerated constant defines values on the print quality.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum PrintQuality;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum PrintQuality** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum PrintQuality Access(*Public)** 
      </pre>

Remarks

**PrintQuality** defines values in which you can select one of the choices. 
Members

<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
          <col span="1" width="70%" />
          <col align="middles" span="1" width="10%" />
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

Draft
</td>
            <td colspan="1" rowspan="1">

Draft quality - the lowest print quality will be used (the least dots per inch). Note, however, that this is the fastest print mode.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Low
</td>
            <td colspan="1" rowspan="1">

Low quality - a low print quality will be used. Note, however, that this is a fairly fast print mode.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Medium
</td>
            <td colspan="1" rowspan="1">

Medium quality - a medium print quality will be used. Note, however, that this is a fairly slow print mode.
</td>
            <td colspan="1" rowspan="1">

3
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

High
</td>
            <td colspan="1" rowspan="1">

High quality - the highest print quality available for the specified printer will be used (the most dots per inch). Note, however, this is the slowest print mode.
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

