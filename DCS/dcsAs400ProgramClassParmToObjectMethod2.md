---
title: As400Program.ParmToObject(System.Type, string, integer[])

Id: dcsAs400ProgramClassParmToObjectMethod2
TocParent: dcsAs400ProgramClassParmToObjectMethodMain
TocOrder: 3

---

Returns an object of a specific type from the program parameter list.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public object ParmToObject(
   Type ReturnType,
   string ParameterName,
   int[] ElementIndices
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ParmToObject( _
   ByVal ReturnType As Type, _
   ByVal ParameterName As String, _
   ByVal ElementIndices[] As Integer _
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ParmToObject Access(*Public) Type(Object)
   DclSrParm ReturnType Type(Type)
   DclSrParm ParameterName Type(*String)
   DclSrParm ElementIndices Type(*Integer) Len(4) Rank(1)** 
      </pre>

Parameters

<dl>
        <dt>
 *ReturnType* 
        </dt>
        <dd>System.Type.  The requested type of the object returned by the method. </dd>
        <dt>
 *ParameterName* 
        </dt>
        <dd>The name or path of the program parameter object in the parameter list. </dd>
        <dt>
 *ElementIndices* 
        </dt>
        <dd>For paths including multiple-occurrence parameters only, the indices in the 
										path to the parameter.</dd>
</dl>

Exceptions

<span> **ArgumentException** .</span> Indicates that *ParameterName* , and if necessary *ElementIndices* , do not reference a valid parameter in the parameter list.

<span> **InvalidOperationException** .</span> Indicates that the **Connection** property of **As400Program** has not been set.
Remarks

This form of **ParmToObject** may be used to get the value of both simple and structured parameters, using the optional parameter naming scheme allowed by [ProgParmType](dcsProgParmTypeClass.html) and [StructureType](dcsStructureTypeClass.html). The constructor for these classes allows the program parameters they represent to be given a string identifier. This identifier may have significance to the application, but it also may be used by this **ParmToObject** method to identify and retrieve the parameter after it has been added to the [As400Program](dcsAs400ProgramClass.html) parameter list.

For simple parameters (constructed with **ProgParmType** ), *ParameterName* refers to the name given to the [ ProgParmType’s constructor](dcsProgParmTypeClassProgParmTypeConstructor.html). *ElementIndices* is ignored unless the simple parameter is a multiple-occurrence (single-dimension array) parameter. In this case, *ElementIndices* should be an integer array of at least one element. The first element in indices must be a zero-relative number identifying the element in the array to be returned by **ParmToObject** .

For complex parameters (constructed with [ StructureType's constructor](dcsStructureTypeClass.html)), *ParameterName* refers to a path to a particular member of the data structure. This name should be in the form of string tokens separated by the character ‘.’, as in "x.y.z". Each token to the left of ‘.’ is the name of a structure containing a member named on the right of ‘.’. The leftmost string token refers to the name of the outermost structure or the [ProgParm](dcsProgParmClass.html) object contained in the **As400Program** parameter list. The rightmost token must refer to the name of a simple parameter type (constructed with <span> **ProgParmType** </span>) which is the member whose value is to be returned.

If the complex parameter path includes data types defined as multiple-occurrence types, then *ElementIndices* must contain an array of integers. The elements of indices refer to positions in the multiple occurrence types. For example, suppose a parameter consists of a multiple occurrence data structure, and one of the data structure’s members is a multiple occurrence character field type. To access the value of one of the character fields, *ElementIndices* must be an array of at least length 2. The first element of the array would reference an occurrence of the outer structure, and the second element of the array would refer to the particular character field to set.

If no multiple occurrence types are included in the path given by *ParameterName* , *ElementIndices* may be specified as an integer array of length zero.

The outermost <span> **ProgParm** </span> object identified by *ParameterName* and *ElementIndices* should be a member of the **As400Program’s** parameter list. The [Connection](dcsAs400ProgramClassConnectionProperty.html) property must be set (or the **As400Program** constructed with an [AdgConnection](dcsAdgConnectionClass.html) object) prior to calling <span> **ParmToObject** </span>.

For the method to succeed, the type specified by *ReturnType* must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be returned as an arbitrary object (such as a string), only if the object implements <span> **System.IConvertible** </span>, and the <span> **ChangeType** </span> method yields a valid conversion. Most fundamental types in the System namespace implement <span>IConvertible</span>.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[3];
  Parms[0] = new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output);
  Parms[1] = new ProgParm(
        new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output);
  Parms[2] = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input);
  prog.AppendParms(Parms);
  prog.ObjectToParm(Parms[2], Quit400App, 0);

  prog.Execute();
  /* After calling the last two values in the parameter list
   * will have new values in it.  To read them, we set our local 
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString(
        prog.ParmToObject(System.Type.GetType("System.String"),
        "CustName",
        0));
  TimeOfDay = Convert.ToDecimal(
        prog.ParmToObject(System.Type.GetType("System.Decimal"),
        "TimeOfDay",
        0));</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, Prog is an initialized As400Program object, 
  ' and CustName, TimeOfDay, and Quit400App are valid
  ' string, decimal, and char types respectively.
  Dim Parms(2) As ProgParm
  Parms(0) = New ProgParm( _
        New ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output)
  Parms(1) = New ProgParm( _
        New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output)
  Parms(2) = New ProgParm( _
        New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input)
  Prog.AppendParms(Parms)
  Prog.ObjectToParm(Parms(2), Quit400App, 0)
  Prog.Execute()
  ' After calling the last two values in the parameter list
  ' will have new values in it.  To read them, we set our local 
  ' variables to the returned values in the parameters list.
  CustName = Convert.ToString( _
        Prog.ParmToObject(System.Type.GetType("System.String"), _
        "TimeOfDay", _
        0))
  TimeOfDay = Convert.ToDecimal( _
        Prog.ParmToObject(System.Type.GetType("System.Decimal"), _
        "TimeOfDay", _
        0))</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, Prog is an initialized As400Program object, 
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  DclArray Parms Type(ProgParm) Dim(3)
  Parms[0] = *New ProgParm( +
        *New ProgParmType("CustName", 0, FieldType.NewChar(40)), DataDirection.Output)
  Parms[1] = *New ProgParm( +
        *New ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)), DataDirection.Output)
  Parms[2] = *New ProgParm( +
        *New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), DataDirection.Input)
  prog.AppendParms(Parms)
  prog.ObjectToParm(Parms[2], Quit400App, 0)
  prog.Execute()
  /* After calling the last two values in the parameter list
   * will have new values in it.  To read them, we set our local 
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString( +
        prog.ParmToObject(System.Type.GetType("System.String"), +
        "CustName", +
        0))
  TimeOfDay = Convert.ToDecimal( +
        prog.ParmToObject(System.Type.GetType("System.Decimal"), +
        "TimeOfDay", +
        0)) </pre>

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
      [ProgParmType Constructor](dcsProgParmTypeClassProgParmTypeConstructor.html)
      <br />
      [ASNA.DataGate.DataLink.StructureType Class](dcsStructureTypeClass.html)
      <br />
      [StructureType 
					Constructor](dcsStructureTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html)

