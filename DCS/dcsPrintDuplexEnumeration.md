---
title: PrintDuplex Enumeration

Id: dcsPrintDuplexEnumeration

keywords: Simplex enumeration member
keywords: Vertical enumeration member
keywords: Horizontal enumeration member
keywords: PrintDuplex enumeration
keywords: enumerations [DCS 16.0 PrintDuplex
keywords: printing, duplex, constants
keywords: duplex, constants
keywords: printer device parameters, duplex constants

---

The **PrintDuplex** enumerated constant defines values on duplex (double-sided) printing. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum PrintDuplex;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum PrintDuplex** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum PrintDuplex Access(*Public)** 
      </pre>

Remarks

**PrintDuplex** defines values in which you can select one of the choices.
Members

<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
          <col span="1" width="60%" />
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

Simplex
</td>
            <td colspan="1" rowspan="1">

Print single-sided.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Vertical
</td>
            <td colspan="1" rowspan="1">

Print duplex with vertical binding.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Horizontal
</td>
            <td colspan="1" rowspan="1">

Print duplex with horizontal binding.
</td>
            <td colspan="1" rowspan="1">

3
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

