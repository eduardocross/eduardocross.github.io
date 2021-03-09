---
title: DuplicateOptions Enumeration

Id: dcsDuplicateOptionsEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 13

keywords: DuplicateOptions enumeration
keywords: enumerations [DCS 16.0 DuplicateOptions
keywords: Members enumeration member
keywords: Data enumeration member
keywords: None enumeration member

---

<span> **DuplicateOptions** </span> defines values directing the operation of the [ Duplicate](dcsIAdgObjectClassDuplicateMethod.html) method of [IAdgObject](dcsIAdgObjectClass.html). 
<pre>        <span class="lang">[C#]</span>
 **[Flags] public enum DuplicateOptions;** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **&lt;Flags&gt; Public Enum DuplicateOptions** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DuplicateOptions Access(*Public) Attributes(Flags)** 
      </pre>

Remarks

The **Duplicate** method is used to copy an existing database object. One or more of the values of **DuplicateOptions** may be specified in the *options* parameter of **Duplicate** to engage provider-dependent features of the method as listed in the table below. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="center" span="1" valign="middle" width="12%" style="FONT-WEIGHT: bold" />
            <col span="1" width="50%" />
            <col align="center" span="1" valign="middle" width="10%" />
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

Members 
</td>
            <td colspan="1" rowspan="1">

Duplicate members. If the target of the copy is a file, duplicate the members of the file as well. Data of the members duplicated is not copied unless **Data** is also specified. This option must be specified for IBM i database providers or **Duplicate** will throw an exception. Database providers not supporting this option may throw exceptions when this value is set. 
</td>
            <td colspan="1" rowspan="1">

1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Data 
</td>
            <td colspan="1" rowspan="1">

Duplicate data. If the target of the copy is a file, duplicate file members with data. This option is ignored unless **Members** is also specified. 
</td>
            <td colspan="1" rowspan="1">

2 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

None 
</td>
            <td colspan="1" rowspan="1">

Default features only; members and data are not duplicated. 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Duplicate Method](dcsIAdgObjectClassDuplicateMethod.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

