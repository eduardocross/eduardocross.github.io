---
title: PrintTrueType Enumeration

Id: dssPrintTrueTypeEnumeration
TocParent: dssDataGateEnumerations
TocOrder: 1

keywords: Bitmap enumeration member
keywords: Download enumeration member
keywords: Subdev enumeration member
keywords: PrintTrueType enumeration
keywords: enumerations [ASNA.DataGate.Common], PrintTrueType
keywords: printing, true type fonts, constants
keywords: true type fonts, constants
keywords: printer device parameters, true type font constants

---

The <span class="hcp1"> **PrintTrueType** </span> enumerated constant defines values whether the **True Type font** will be used. 
<pre class="syntax">
        <span class="lang">[C#]</span>
 **public enum PrintTrueType;** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual Basic] </span>
 **Public Enum PrintTrueType** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual RPG]</span>
 **BegEnum PrintTrueType Access(*Public)** 
      </pre>

### Remarks 
**PrintTrueType** defines values in which you can select one of the choices. 

### Members
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1" class="fineprint">
            <col align="middles" span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="59.99%" />
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

</td> <td colspan="1" rowspan="1"> <p class="indent"> 2
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

### Requirements
<strong class="hcp7">Namespace:</strong> [ASNA DataGate](adgDataGateNamespace.html) 

<strong class="hcp9">Assembly:</strong> ASNA DataGate&#174; Client (in ASNA DataGate.Client.dll)

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows Vista Business Edition, Windows 7, Windows 8 

### See Also
[DataGate&#174; Namespace](adgDataGateNamespace.html) 
