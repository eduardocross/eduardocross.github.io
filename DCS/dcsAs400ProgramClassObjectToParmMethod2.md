---
title: As400Program.ObjectToParm(object, string, int[])

Id: dcsAs400ProgramClassObjectToParmMethod2
TocParent: dcsAs400ProgramClassObjectToParmMethodMain
TocOrder: 3

---

Converts an object or value type to a parameter list value. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void ObjectToParm(
   object Value,
   string ParameterName,
   int[] ElementIndices
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub ObjectToParm( _
   ByVal Value As Object _
   ByVal ParameterName As String _
   ByVal ElementIndices() As Integer _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ObjectToParm Acess(*Public)
   DclSrParm Value Type(*Object)
   DclSrParm ParameterName Type(*String)
   DclSrParm ElementIndices Type(*Integer4) Rank(1)** 
      </pre>

Parameters

<dl>
        <dt>
 *Value* 
        </dt>
        <dd>
          The value to be set. </dd>
        <dt>
          <span> *ParameterName* 
          </span>
        </dt>
        <dd>The program parameter name in the parameter list to set the value of. </dd>
        <dt>
          <span>
 *ElementIndices* 
          </span>
        </dt>
        <dd>
         For multiple-occurrence parameters 
										only, the index of the occurrence to set.
									</dd>
</dl>

Exceptions

**ArgumentException** . Indicates that *ParameterName* , and if necessary *ElementIndices* , do not reference a valid parameter in the parameter list.

**InvalidOperationException** . Indicates that the [ Connection](dcsAs400ProgramClassConnectionProperty.html) property of **As400Program** has not been set.
Remarks

This form of **ObjectToParm** may be used to set the value of simple parameters (non-structured) with a reference to the [ ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) object. The object should be a member of the [As400Program's](dcsAs400ProgramClass.html) parameter list. The **Connection** property must be set (or the **As400Program** constructed with an [ AdgConnection](dcsAdgConnectionClass.html) object) prior to calling **ObjectToParm** .

For the method to succeed, the *value* object must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be set with an arbitrary object (such as a string), only if the object implements **System.IConvertible** and the **ToDecimal** method yields a valid conversion.<span style="mso-spacerun: yes"> </span>Most fundamental types in the System namespace implement **IConvertible** .

The *ElementIndices* parameter is ignored unless *ParameterName* refers to a "multiple-occurrence" parameter type. Multiple-occurrence parameters consist of single-dimension arrays of the parameter type. *ElementIndices* is a zero-relative index identifying the element of the array **ObjectToParm** is setting the value for.
Examples

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
      <pre>
        <span class="lang">
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
      [Connection Property](dcsAs400ProgramClassConnectionProperty.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink.StructureType Class](dcsStructureTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html)

