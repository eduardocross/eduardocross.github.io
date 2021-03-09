---
title: PrintTrueType Enumeration

Id: dcsPrintTrueTypeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 21

keywords: Bitmap enumeration member
keywords: Download enumeration member
keywords: Subdev enumeration member
keywords: PrintTrueType enumeration
keywords: enumerations [DCS 16.0 PrintTrueType
keywords: printing, true type fonts, constants
keywords: true type fonts, constants
keywords: printer device parameters, true type font constants

---

The <span> **PrintTrueType** </span> enumerated constant defines values whether the **True Type font** will be used. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum PrintTrueType;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum PrintTrueType** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum PrintTrueType Access(*Public)** 
      </pre>

Remarks

**PrintTrueType** defines values in which you can select one of the choices. 
Members

<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
            <col align="middles" span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="59.99%" />
            <col span="1" width="10%" />
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

Bitmap
</td>
              <td colspan="1" rowspan="1">

Print True Type font as graphics.
</td>
              <td colspan="1" rowspan="1">

1
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Download
</td>
              <td colspan="1" rowspan="1">
											Download True Type fonts as soft fonts.
										</td>
              <td colspan="1" rowspan="1">

2
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Subdev
</td>
              <td colspan="1" rowspan="1">

Substitute device fonts for True Type fonts.
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

