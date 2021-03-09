---
title: AdgObjectTypes Enumeration

Id: dcsAdgObjectTypesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 2

keywords: enumerations [DCS 16.0 AdgObjectTypes
keywords: AdgObjectTypes enumeration
keywords: File enumeration member
keywords: Member enumeration member
keywords: Directory enumeration member

---

The <span> **AdgObjectTypes** </span> enumerated constant defines values for the [ AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property of [IAdgObject](dcsIAdgObjectClass.html). 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum AdgObjectTypes;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Enum AdgObjectTypes** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum AdgObjectTypes Access(*Public)** 
      </pre>

Remarks

**AdgObjectTypes** denote values which classify a database object. DCS sets the value of the **IAdgObject.AdgObjectType** property to one of these values. Currently, DCS supports libraries, files, and members only. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="39.99%" />
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

Directory
</td>
            <td colspan="1" rowspan="1">

The object is a directory.
</td>
            <td colspan="1" rowspan="1">

68
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

File
</td>
            <td colspan="1" rowspan="1">

The object is a file.
</td>
            <td colspan="1" rowspan="1">

70
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Member
</td>
            <td colspan="1" rowspan="1">

The object is a member.
</td>
            <td colspan="1" rowspan="1">

77
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DataArea
</td>
            <td colspan="1" rowspan="1">

The object is a data area.
</td>
            <td colspan="1" rowspan="1">

83
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Catalog
</td>
            <td colspan="1" rowspan="1">

Reserved value for internal DCS use only. 
</td>
            <td colspan="1" rowspan="1">

89
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IAdgObject Class<br />](dcsIAdgObjectClass.html)
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

