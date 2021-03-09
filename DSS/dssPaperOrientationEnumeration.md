---
title: PaperOrientation Enumeration

Id: dssPaperOrientationEnumeration
TocParent: dssDataGateEnumerations
TocOrder: 0

keywords: Portrait enumeration member
keywords: Landscape enumeration member
keywords: enumerations [ASNA.DataGate.Common], PaperOrientation
keywords: PaperOrientation enumeration
keywords: printing, orientation, constants
keywords: print orientation, constants
keywords: printer device parameters, orientation constants

---

The <span class="hcp1"> **PaperOrientation** </span> enumerated constant defines values on the orientation of the paper. 
<pre class="syntax">
        <span class="lang">[C#]</span>
 **public enum PaperOrientation;** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual Basic] </span>
 **Public Enum PaperOrientation** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual RPG]</span>
 **BegEnum PaperOrientation Access(*Public)** 
      </pre>

### Remarks 
**PaperOrientation** defines values in which you can select one of the choices. 

### Members
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
            <colgroup span="1" class="fineprint">
              <col align="middles" span="1" width="10%" style="FONT-WEIGHT: bold" />
              <col span="1" width="59.99%" />
              <col align="middles" span="1" width="10%" />
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
              <td colspan="1" rowspan="1" style="height: 21px">

Portrait
</td>
              <td colspan="1" rowspan="1" style="height: 21px">

Portrait orientation, i.e., the height is greater than the width.
</td>
              <td colspan="1" rowspan="1" style="height: 21px">

1
</td>
            </tr>
            <tr>
              <td colspan="1" rowspan="1">

Landscape
</td>
              <td colspan="1" rowspan="1">

Landscape orientation, i.e., the width is greater than the height.
</td>
              <td colspan="1" rowspan="1">

2
</td>
            </tr>
</table>

### Requirements
<strong class="hcp7">Namespace:</strong> [ASNA DataGate](adgDataGateNamespace.html) 

<strong class="hcp9">Assembly:</strong> ASNA DataGate&#174; Client (in ASNA DataGate.Client.dll)

** **Platforms:** ** Windows Server 2008 R2, Windows Server 2012, Windows Vista Business Edition, Windows 7, Windows 8 

### See Also
[ DataGate&#174; Namespace](adgDataGateNamespace.html) 
