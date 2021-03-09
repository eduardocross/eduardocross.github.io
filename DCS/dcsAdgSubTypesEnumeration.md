---
title: AdgSubTypes Enumeration

Id: dcsAdgSubTypesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 3

keywords: enumerations [DCS 16.0 AdgSubTypes
keywords: AdgSubTypes enumeration
keywords: Unknown enumeration member
keywords: DataAreaLgl enumeration member
keywords: DataAreaChr enumeration member
keywords: DataAreaDec enumeration member
keywords: Join enumeration member
keywords: Local enumeration member
keywords: Merge enumeration member
keywords: NetPrint enumeration member
keywords: OlePrint enumeration member
keywords: Physical enumeration member
keywords: SqlLogical enumeration member
keywords: Remote enumeration member
keywords: Simple enumeration member
keywords: System enumeration member
keywords: Array enumeration member

---

The **AdgSubTypes** enumerated constant defines values for the [IAdgObject.AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html) property of an object. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum AdgSubTypes;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Enum AdgSubTypes** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegEnum AdgSubTypes Access(*Public)** 
      </pre>

Remarks

**AdgSubTypes** defines values in which you can select one of the choices. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="30%" />
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

Unknown
</td>
            <td colspan="1" rowspan="1">

The sub type is unknown.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DataAreaLgl
</td>
            <td colspan="1" rowspan="1">

This object is of type System.Boolean.
</td>
            <td colspan="1" rowspan="1">

66
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DataAreaChr
</td>
            <td colspan="1" rowspan="1">

This object is of type System.String or System.Char[].
</td>
            <td colspan="1" rowspan="1">

67
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DataAreaDec
</td>
            <td colspan="1" rowspan="1">

This object is of type System.Decimal.
</td>
            <td colspan="1" rowspan="1">

68
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Join
</td>
            <td colspan="1" rowspan="1">

This is a Join Logical file.
</td>
            <td colspan="1" rowspan="1">

74
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Local
</td>
            <td colspan="1" rowspan="1">

This is a Local Directory.
</td>
            <td colspan="1" rowspan="1">

76
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Merge
</td>
            <td colspan="1" rowspan="1">

This is a Merge Logical file.
</td>
            <td colspan="1" rowspan="1">

77
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NetPrint
</td>
            <td colspan="1" rowspan="1">

This is a .Net print file.
</td>
            <td colspan="1" rowspan="1">

78
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OlePrint
</td>
            <td colspan="1" rowspan="1">

This is a Ole print file. 
</td>
            <td colspan="1" rowspan="1">

79
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Physical
</td>
            <td colspan="1" rowspan="1">

This is a Physical file. 
</td>
            <td colspan="1" rowspan="1">

80
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

SqlLogical
</td>
            <td colspan="1" rowspan="1">

This is a SQL Logical file. 
</td>
            <td colspan="1" rowspan="1">

81
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Remote
</td>
            <td colspan="1" rowspan="1">

This is a Remote Directory. 
</td>
            <td colspan="1" rowspan="1">

82
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Simple
</td>
            <td colspan="1" rowspan="1">

This is a Simple Logical file. 
</td>
            <td colspan="1" rowspan="1">

83
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

System
</td>
            <td colspan="1" rowspan="1">

This is a system object. 
</td>
            <td colspan="1" rowspan="1">

89
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Array
</td>
            <td colspan="1" rowspan="1">

This object is an array. 
</td>
            <td colspan="1" rowspan="1">

91
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IAdgObject.AdgSubType Property](dcsIAdgObjectClassAdgSubTypeProperty.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

