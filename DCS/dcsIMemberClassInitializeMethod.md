---
title: IMember.Initialize Method

Id: dcsIMemberClassInitializeMethod
TocParent: dcsIMemberMethods
TocOrder: 1

keywords: Initialize method
keywords: IMember.Initialize method
keywords: InitMemberOptions enumeration, used by
keywords: enumerations [DCS 16.0 InitMemberOptions, used by
keywords: database file members, initialize records
keywords: database files, initialize records in database file member
keywords: records, initialize database file member
keywords: record types, initialize database file member
keywords: how to, initialize records in database file member

---

Initialize a specific number of records in the database file member represented by **IMember** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Initialize(<br />    [InitMemberOptions](dcsInitMemberOptionsEnumeration.html) Options ,
   long Records
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Sub Initialize(_
   ByVal Options As [InitMemberOptions](dcsInitMemberOptionsEnumeration.html)_<br />   ByVal Records As System.Int64<br /> ) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Initialize Access(*Public) Type(Void)<br />   DclSrParm Options Type([InitMemberOptions](dcsInitMemberOptionsEnumeration.html))<br />   DclSrParm Records Type(System.Int64)** 
      </pre>

Parameters

<dl>
        <dt />
</dl>

*Options* 
<dl>
        <dd>

[InitMemberOptions](dcsInitMemberOptionsEnumeration.html). The kind of record initialization to perform.
</dd>
</dl>

*Records* 
<dl>
        <dd>

**System.Int64** . A non-negative number of records to add to the database object.
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1" style="height: 23px">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1" style="height: 23px">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this **IMember** instance does not locate a valid database object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOLOCK, or dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The database provider could not obtained the requisite lock(s) to perform this function, including an "exclusive" lock on the database member object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database provider encountered a system-level error. Details provided in the **dgException.Message** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVFTOP
</td>
            <td colspan="1" rowspan="1">

This method is not supported for the type of file containing the member object represented by **IMember** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTIMPL
</td>
            <td colspan="1" rowspan="1">

One or more of the following conditions exist:

- *Options* does <u>not</u> specify the **InitMemberOptions.WithDeleted** 
								value, but the database provider does not support this method unless the option 
								is specified.
- The database provider does not support this method.

</td>
          </tr>
</table>

Remarks

**Initialize** adds records of a certain type to the database member represented by **IMember** . The number of records initialized is specified by *Records* . *Options* specifies the type of records added to the member (see **InitMemberOptions** ).
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [InitMemberOptions Enumeration](dcsInitMemberOptionsEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

