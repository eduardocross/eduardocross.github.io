---
title: DataTypes Enumeration

Id: dcsDataTypesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 7

keywords: DataTypes enumeration
keywords: enumerations [DCS 16.0 DataTypes
keywords: types of data fields
keywords: fields, types of data
keywords: data types, constants
keywords: Binary enumeration member
keywords: Boolean enumeration member
keywords: Char enumeration member
keywords: Date enumeration member
keywords: DBCS enumeration member
keywords: DontCare enumeration member
keywords: Float enumeration member
keywords: Hex enumeration member
keywords: Integer enumeration member
keywords: MaxType enumeration member
keywords: NoType enumeration member
keywords: Packed enumeration member
keywords: Print enumeration member
keywords: Structured enumeration member
keywords: Time enumeration member
keywords: Timestamp enumeration member
keywords: Unicode enumeration member
keywords: Zoned enumeration member

---

The <span> **DataTypes** </span> enumerated constant defines values on the types of fields available. This enumeration is used by the [DataType](dcsFieldTypeClassDataTypeProperty.html) property for [FieldType](dcsFieldTypeClass.html) objects.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum DataTypes;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum DataTypes** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DataTypes Access(*Public)** 
      </pre>

Remarks

Packed, zoned and binary types are numeric fields containing decimal numbers which are expressed in digits and decimals. Float and integer types are defined in bytes.

<span> **DataTypes** </span> defines values in which you can select one of the choices. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0" width="85%">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold" width="10%" />
            <col span="1" width="40%" />
            <col align="middles" span="1" width="5%" />
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

Binary
</td>
            <td colspan="1" rowspan="1">

Field is binary.
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Boolean
</td>
            <td colspan="1" rowspan="1">

Field is a Boolean, true/false.
</td>
            <td colspan="1" rowspan="1">

15
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Char
</td>
            <td colspan="1" rowspan="1">

Field is character.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Date
</td>
            <td colspan="1" rowspan="1">

Field is a date. 
</td>
            <td colspan="1" rowspan="1">

7
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DBCS 
</td>
            <td colspan="1" rowspan="1">

Field is a double byte character field. 
</td>
            <td colspan="1" rowspan="1">

12
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DontCare
</td>
            <td colspan="1" rowspan="1">

Field is of any type.
</td>
            <td colspan="1" rowspan="1">

14
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Float 
</td>
            <td colspan="1" rowspan="1">

Field is float.
</td>
            <td colspan="1" rowspan="1">

5
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Hex 
</td>
            <td colspan="1" rowspan="1">

Field is hexadecimal.
</td>
            <td colspan="1" rowspan="1">

10
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Integer
</td>
            <td colspan="1" rowspan="1">

Field is an integer. 
</td>
            <td colspan="1" rowspan="1">

6
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

MaxType
</td>
            <td colspan="1" rowspan="1">

The total number of valid values for the Type property. 
</td>
            <td colspan="1" rowspan="1">

17
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NoType
</td>
            <td colspan="1" rowspan="1">

Field has no type.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Packed
</td>
            <td colspan="1" rowspan="1">

Field is packed.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Print
</td>
            <td colspan="1" rowspan="1">

Field is a print field. 
</td>
            <td colspan="1" rowspan="1">

11
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Structured
</td>
            <td colspan="1" rowspan="1">

Field is structured.
</td>
            <td colspan="1" rowspan="1">

13
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Time
</td>
            <td colspan="1" rowspan="1">

Field is time.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Timestamp
</td>
            <td colspan="1" rowspan="1">

Field is a timestamp.
</td>
            <td colspan="1" rowspan="1">

9
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Unicode
</td>
            <td colspan="1" rowspan="1">

Field is a Unicode data type. 
</td>
            <td colspan="1" rowspan="1">

16
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Zoned
</td>
            <td colspan="1" rowspan="1">

Field is packed.
</td>
            <td colspan="1" rowspan="1">

3
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [DataType Property](dcsFieldTypeClassDataTypeProperty.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

