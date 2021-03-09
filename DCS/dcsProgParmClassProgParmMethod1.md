---
title: ProgParm(ProgParmType, DataDirection)

Id: dcsProgParmClassProgParmMethod1
TocParent: dcsProgParmClassProgParmMethodMain
TocOrder: 0

keywords: enumerations [DCS 16.0 DataDirection, used by
keywords: DataDirection enumeration, used by

---

Construct a representation of a simple iSeries program parameter.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ProgParm(<br />   ProgParmType ppt,<br />   DataDirection dir<br />)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Sub New( _<br />   ByVal ppt As [ProgParmType](dcsProgParmTypeClass.html) _<br />   ByVal dir As [DataDirection](dcsDataDirectionEnumeration.html)<br />)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)<br />   DclSrParm ppt Type(ProgParmType)<br />   DclSrParm dir Type(DataDirection)** 
      </pre>

Parameters

<dl>
        <dt>
 *ppt* 
        </dt>
        <dd>
          [ProgParmType](dcsProgParmTypeClass.html). The data type description 
						of the simple program parameter. </dd>
        <dt>
 *dir* 
        </dt>
        <dd>
          [ASNA.DataGate.Common.DataDirection](dcsDataDirectionEnumeration.html). 
								The declared input/output orientation of the parameter.</dd>
</dl>

Remarks

**ProgParm** constructors define the metadata and input/output orientation of a single iSeries program parameter. In this form, *ppt* contains the type description for the simple (non-structured) parameter.

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

Value data moves from DCS to data provider prior to iSeries program call and from data provider to DCS after return from iSeries program call. 
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

Careful use of the *dir* parameter can improve the performance of iSeries program calls in DCS. For example, by specifying **DataDirection.None** (for a parameter not used by your program nor the iSeries program), the network bandwidth required for passing that parameter across the client/server link is decreased.

**ProgParm** constructors do not allow the initialization of the parameter value data. Values may only be set in the **ProgParm** object after it has been added to the [As400Program](dcsAs400ProgramClass.html) parameter list (via [AppendParm](dcsAs400ProgramClassAppendParmMethod.html) or [AppendParms](dcsAs400ProgramClassAppendParmsMethod.html)). Use the [ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html) method to set the value *data* of the **ProgParm** .
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* Create paramerter list to send to the program being called.
   * The first two parameters catch return values, the last will tell the
   * external program to shut down if the value is '1'. */
  char Quit400App = '1';

  ProgParm[] parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input)
  };

  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");
  prog.AppendParms(parms); //Use our parm list defined above.
  //Here, we make sure our variables are passed as the parms in ther parm list.
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  //Now we execute the call to the As400Program, "Call400".
  prog.Execute();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Create paramerter list to send to the program being called. 
  ' The first two parameters catch return values, the last will tell the
  ' external program to shut down if the value is '1'. 
  Dim Quit400App As Char = "1"

  Dim parms As ProgParm()
  parms = new ProgParm(){ _
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output), _
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output), _
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input) _
  }

  Dim prog As New As400Program(ProdDB, "*Libl/Call400")
  prog.AppendParms(parms) 'Use our parm list defined above.
  'Here, we make sure our variables are passed as the parms in ther parm list.
  prog.ObjectToParm(Quit400App, "Quit400App", New Integer() {})
  'Now we execute the call to the As400Program, "Call400".
  prog.Execute() </pre>

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

