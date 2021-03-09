---
title: ProgParm(StructureType, DataDirection)

Id: dcsProgParmClassProgParmMethod2
TocParent: dcsProgParmClassProgParmMethodMain
TocOrder: 1

keywords: enumerations [DCS 16.0 DataDirection, used by
keywords: DataDirection enumeration, used by

---

Construct a representation of a complex iSeries program parameter.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ProgParm(<br />   StructureType st,<br />   DataDirection dir<br />)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Sub New( _<br />   ByVal st As [StructureType](dcsStructureTypeClass.html) _<br />   ByVal dir As [DataDirection](dcsDataDirectionEnumeration.html) _<br />)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)<br />   DclSrParm st Type(StructureType)<br />   DclSrParm dir Type(DataDirection)** 
      </pre>

Parameters

<dl>
        <dt>
 *st* 
        </dt>
        <dd>
          [StructureType](dcsStructureTypeClass.html). The data type 
						description of the structured program parameter. </dd>
        <dt>
 *dir* 
        </dt>
        <dd>
          [ASNA.DataGate.Common.DataDirection](dcsDataDirectionEnumeration.html). 
								The declared input/output orientation of the parameter.</dd>
</dl>

Remarks

**ProgParm** constructors define the metadata and input/output orientation of a single iSeries program parameter. In this form, *st* contains the type description for the complex (structured) parameter.

*dir* defines the parameter as an "input" or "output" parameter, or both. This optimizes the movement of parameter value data across the client/server link as detailed by the following table:
<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold;WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of *dir* </th>
            <th colspan="1" rowspan="1">
							Data Movement
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Input 
</td>
            <td colspan="1" rowspan="1">

Value data moves from DCS to data provider prior to iSeries program call only. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Output 
</td>
            <td colspan="1" rowspan="1">

Value data moves from data provider to DCS after return from iSeries program call only. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InputOutput 
</td>
            <td colspan="1" rowspan="1">

Value data moves from DCS to data provider prior to iSeries program call, and from data provider to DCS after return from iSeries program call. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

None 
</td>
            <td colspan="1" rowspan="1">

No parameter value data is transferred. 
</td>
          </tr>
</table>

<br />

Careful use of the *dir* parameter can improve the performance of iSeries program calls in DCS. For example, by specifying **DataDirection.None** (for a parameter not used by your program nor by your iSeries program), the network bandwidth required for passing that parameter across the client/server link is decreased.

<span> **ProgParm** </span> constructors do not allow the initialization of the parameter value data. Values may only be set in the **ProgParm** object after it has been added to the [As400Program](dcsAs400ProgramClass.html) parameter list (via [AppendParm](dcsAs400ProgramClassAppendParmMethod.html) or [ AppendParms](dcsAs400ProgramClassAppendParmsMethod.html)). Use the [ ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html) and [SetParmsZeroValue](dcsAs400ProgramClassSetParmsZeroValueMethod.html) methods to set the value *data* of the **ProgParm** .
Requirements

**Namespace:** [ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ProgParm Class](dcsProgParmClass.html)
      <br />
      [ProgParm Class Members](dcsProgParmMembers.html)
      <br />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [AppendParm Method](dcsAs400ProgramClassAppendParmMethod.html)
      <br />
      [AppendParms Method](dcsAs400ProgramClassAppendParmsMethod.html)
      <br />
      [ObjectToParm Method](dcsAs400ProgramClassObjectToParmMethodMain.html)
      <br />
      [DataDirection Enumeration](dcsDataDirectionEnumeration.html)
      <br />
      [ASNA.DataGate.DataLink Namespace](dcsDataGateDataLinkNamespace.html)
      <br />
      [Calling Stored Procedures](dcsCallingStoredProcedures.html)

