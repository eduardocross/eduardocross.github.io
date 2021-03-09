---
title: As400Program.Execute Method

TocParent: dcsAs400ProgramMethodsMain
TocOrder: 3

keywords: Execute method
keywords: As400Program.Execute method
keywords: iSeries computers, execute programs
keywords: IBM i programs, execute
keywords: how to, execute IBM i programs
keywords: execute programs, IBM i
keywords: database servers, execute IBM i programs

---

Runs the database program.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Execute();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub Execute()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Execute Acess(*Public)** 
      </pre>

Exceptions

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InvalidOperationException 
</td>
            <td colspan="1" rowspan="1">

The [ProgramPath](dcsAs400ProgramClassProgramPathProperty.html) property has not been set or contains a zero-length string. 
</td>
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of
							<br />
							dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpMEMEXCEPTION 
</td>
            <td colspan="1" rowspan="1">

An IBM i memory exception occurred (an exception in the MCH36xx series). Generally this indicates a bad pointer in the called program. Examine the job log for details. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPGMNOTFND 
</td>
            <td colspan="1" rowspan="1">

The value specified for the **ProgramPath** property does not refer to a valid program object. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The value specified for the **ProgramPath** property is not a valid database object path (did you forget a library name or *LIBL?). 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpPGMERR 
</td>
            <td colspan="1" rowspan="1">

The number of parameters in the parameter list exceeds the maximum allowed by DataGate. Currently the maximum is 36. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The IBM i server encountered a system error. Details may be available via the [ SystemError](dcsdgExceptionClassSystemErrorField.html) and [Text](dcsDisconnectingfromaDatabase.html) fields of dgException. 
</td>
          </tr>
</table>

Remarks

The **Execute** method invokes the program on the database server. If the program requires parameters, they should be added to the parameter list (with [AppendParm Method](dcsAs400ProgramClassAppendParmMethod.html) and [AppendParms](dcsAs400ProgramClassAppendParmsMethod.html)) prior to calling **Execute** . If any parameters are "input" parameters, their value should be set (with [ ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html)) first. The [ Connection](dcsAs400ProgramClassConnectionProperty.html) and [ProgramPath](dcsAs400ProgramClassProgramPathProperty.html) properties must be set (directly or by [ As400Program constructor](dcsAs400ProgramClassAs400ProgramMethodMain.html)) prior to calling **Execute** .

The name of the program, as specified by the **ProgramPath** property, is validated by this method. If a program cannot be found at the specified location, dgException is raised with the [ Error](dcsdgExceptionClassErrorField.html) property set to dgEpPGMNOTFND.

If an i Series system exception occurs in the called program, dgException is raised with the Error property set to dgEsAS400ERROR. System details of the exception will be available in the **Text** , **SystemError** , and [ErrorClass](dcsdgExceptionClassErrorClassField.html) fields of dgException.

Upon successful return from **Execute** , the values of any "output" parameters passed to the program will be available with the [ ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html) method.
<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[]
  {
      new ProgParm(new ProgParmType("CustName", 0, FieldType.NewChar(40)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
      DataDirection.Output),
      new ProgParm(new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
      DataDirection.Input)
  };
  prog.AppendParms(Parms);
  prog.ObjectToParm(Quit400App, "Quit400App", new int[]{});
  prog.Execute();
  CustName = Convert.ToString(
     prog.ParmToObject(System.Type.GetType("System.String"),
     "CustName",
     new int[]{}));
  TimeOfDay = Convert.ToDecimal(
     prog.ParmToObject(System.Type.GetType("System.Decimal"),
     "TimeOfDay",
     new int[]{}));              </pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, Prog is an initialized As400Program object,
  ' and CustName, TimeOfDay, and Quit400App are valid
  ' string, decimal, and char types respectively.
  Dim Parms As ProgParm()
  Parms = New ProgParm(){ _
     New ProgParm(New ProgParmType("CustName", 0, FieldType.NewChar(40)), _
     DataDirection.Output), _
     New ProgParm(New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), _
     DataDirection.Output), _
     New ProgParm(New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), _
     DataDirection.Input) _
  }
  prog.AppendParms(Parms)
  prog.ObjectToParm(Quit400App, "Quit400App", New Integer(){})
  prog.Execute()
  CustName = Convert.ToString( _
     prog.ParmToObject(System.Type.GetType("System.String"), _
     "TimeOfDay", _
     New Integer(){}))
  TimeOfDay = Convert.ToDecimal( _
     prog.ParmToObject(System.Type.GetType("System.Decimal"), _
     "TimeOfDay", _
     New Integer(){}))
</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  DclArray Parms Type(ProgParm) Rank(1)
  Parms = *New ProgParm[]{ +
      *New ProgParm(*New ProgParmType("CustName", 0, FieldType.NewChar(40)), +
      DataDirection.Output), +
      *New ProgParm(*New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), +
      DataDirection.Output), +
      *New ProgParm(*New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), +
      DataDirection.Input) +
  }
  prog.AppendParms(Parms)
  prog.ObjectToParm(Quit400App, "Quit400App", *Nothing *As *Integer4[])
  prog.Execute()
  CustName = Convert.ToString( +
     prog.ParmToObject(System.Type.GetType("System.String"), +
     "CustName", +
     *Nothing *As *Integer4[]))
  TimeOfDay = Convert.ToDecimal( +
     prog.ParmToObject(System.Type.GetType("System.Decimal"), +
     "TimeOfDay", +
     *Nothing *As *Integer4[]))</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [As400Program Class Members](dcsAs400ProgramMembers.html)
      <br />
      [AppendParm Method](dcsAs400ProgramClassAppendParmMethod.html)
      <br />
      [AppendParms Method](dcsAs400ProgramClassAppendParmsMethod.html)
      <br />
      [Connection Property](dcsAs400ProgramClassConnectionProperty.html)
      <br />
      [As400ProgramClass 
					Constructors](dcsAs400ProgramClassAs400ProgramMethodMain.html)
      <br />
      [ObjectToParm Method](dcsAs400ProgramClassObjectToParmMethodMain.html)
      <br />
      [ParmToObject Method](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ProgramPath Property](dcsAs400ProgramClassProgramPathProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

