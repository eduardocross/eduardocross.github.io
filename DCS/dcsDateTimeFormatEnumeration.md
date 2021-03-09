---
title: DateTimeFormat Enumeration

Id: dcsDateTimeFormatEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 8

keywords: enumerations [DCS 16.0 DateTimeFormat
keywords: DateTimeFormat enumeration
keywords: fields, date/time format constants
keywords: date/time format of field constants
keywords: how to, determine date/time format of field constants
keywords: DMY enumeration member
keywords: EUR enumeration member
keywords: HMS enumeration member
keywords: ISO enumeration member
keywords: JIS enumeration member
keywords: JUL enumeration member
keywords: MDY enumeration member
keywords: USA enumeration member
keywords: YMD enumeration member

---

The <span> **DateTimeFormat** </span> enumerated constant defines values on the type of date and time being accessed. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum DataTimeFormat;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum DataTimeFormat** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DataTimeFormat Access(*Public)** 
      </pre>

Remarks

Used by the [DateTime](dcsFieldTypeClassDateTimeProperty.html) property of [FieldType](dcsFieldTypeClass.html) objects.

<span> **DateTimeFormat** </span> defines values in which you can select one of the choices. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="8%" style="FONT-WEIGHT: bold" />
            <col span="1" width="40%" />
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

DMY
</td>
            <td colspan="1" rowspan="1">

Day/Month/Year. For date, dd/mm/yy.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

EUR
</td>
            <td colspan="1" rowspan="1">

IBM European Standard. For date, dd.mm.yyyy. For time, hh:mm:ss.
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="height: 47px">

HMS
</td>
            <td colspan="1" rowspan="1" style="height: 47px">

Hours/Minutes/Seconds. For time, hh:mm:ss.
</td>
            <td colspan="1" rowspan="1" style="height: 47px">

10
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ISO
</td>
            <td colspan="1" rowspan="1">

International Standards Organization. For date, yyyy-mm-dd. For time, hh:mm:ss.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

JIS
</td>
            <td colspan="1" rowspan="1">

Japanese Industrial Standard Christian Era. For date, yyyy-mm-dd. For time, hh:mm:ss.
</td>
            <td colspan="1" rowspan="1">

5
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

JUL
</td>
            <td colspan="1" rowspan="1">

Julian. For date, yy/ddd.
</td>
            <td colspan="1" rowspan="1">

9
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

MDY
</td>
            <td colspan="1" rowspan="1">

Month/Day/Year. For date, mm/dd/yy.
</td>
            <td colspan="1" rowspan="1">

7
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

USA
</td>
            <td colspan="1" rowspan="1">

IBM USA Standard. For date, mm/dd/yyyy. For time, hh:mm AM.
</td>
            <td colspan="1" rowspan="1">

3
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

YMD
</td>
            <td colspan="1" rowspan="1">

Year/Month/Day. For date, yy/mm/dd.
</td>
            <td colspan="1" rowspan="1">

6
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      [DateTime Property](dcsFieldTypeClassDateTimeProperty.html)
      <br />
      [FieldType Class](dcsFieldTypeClass.html)

