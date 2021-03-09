---
title: InitMemberOptions Enumeration

Id: dcsInitMemberOptionsEnumeration
TocParent: dcsDataGateClientEnumerations
TocOrder: 1

keywords: enumerations [DCS 16.0 InitMemberOptions
keywords: InitMemberOptions enumeration
keywords: WithDefaults enumeration member
keywords: WithDeleted enumeration member
keywords: database file members, initialize record types
keywords: database files, initialize records in database file member
keywords: records, initialize database file member
keywords: record types, initialize database file member
keywords: how to, initialize records in database file member
keywords: ASNA.DataGate.Client.InitMemberOptions

---

<span> **InitMemberOptions** </span> contains the values used by [ IMember.Initialize](dcsIMemberClassInitializeMethod.html) to specify the type of records to initialize a database member with. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum InitMemberOptions;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum InitMemberOptions** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum InitMemberOptions Access(*Public)** 
      </pre>

Remarks

**InitMemberOptions** is a parameter of the **IMember.Initialize** method. It specifies the type of records added to an existing database member by the method. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="50%" />
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
            <td colspan="1" rowspan="1">

WithDefaults 
</td>
            <td colspan="1" rowspan="1">

Initialize each record's fields with default values, if defined. Numeric fields that do not have a default value are set to zero and character fields that do not have a default value are set to "blanks". 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithDeleted 
</td>
            <td colspan="1" rowspan="1">

Initialize with deleted records. The data of deleted records is not accessible. 
</td>
            <td colspan="1" rowspan="1">

1 
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

