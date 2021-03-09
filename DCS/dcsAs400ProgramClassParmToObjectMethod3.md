---
title: As400Program.ParmToObject(ProgParm, System.Type)

Id: dcsAs400ProgramClassParmToObjectMethod3
TocParent: dcsAs400ProgramClassParmToObjectMethodMain
TocOrder: 0

---

Returns an object of a specific type from the program parameter list.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public object ParmToObject(
   [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) Parameter
   Type ReturnType
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ParmToObject( _
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) _
   ByVal ReturnType As Type _
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ParmToObject Access(*Public) Type(Object)
DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))
DclSrParm ReturnType Type(Type)** 
      </pre>

Parameters

<dl>
        <dt>
 *Parameter* 
        </dt>
        <dd>
          [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html).  The 
						program parameter object in the parameter list to get the value of. </dd>
        <dt>
 *ReturnType*  
							</dt>
        <dd>System.Type.  The requested type of the object returned by the method.
							</dd>
</dl>

Returns

System.Object whose actual type is *ReturnType* .
Exceptions

**ArgumentException** . Thrown if *Parameter* is a complex parameter (constructed with an instance of [ StructureType](dcsStructureTypeClass.html)).

**InvalidOperationException** . Indicates that the **Connection** property of **As400Program** has not been set.
Remarks

This form of **ParmToObject** may be used to get the value of simple parameters (non-structured) with a reference to the **ProgParm** object. *Parameter* should be a member of the **As400Program’s** parameter list. The value being referenced by this method should not belong to a multiple-occurrence type source, since there is no provision for specifying the index. The [ Connection](dcsAs400ProgramClassConnectionProperty.html) property must be set (or the **As400Program** constructed with an [AdgConnection](dcsAdgConnectionClass.html) object) prior to calling **ParmToObject** .

For the method to succeed, the type specified by *ReturnType* must have a valid conversion from the underlying parameter type. For example, a parameter for a decimal number can be converted to an arbitrary object type (such as a string), only if the object implements **System.IConvertible** and the **ChangeType** method yields a valid conversion. Most fundamental types in the System namespace implement IConvertible.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Here, Prog is an initialized As400Program object,
   * and CustName, TimeOfDay, and Quit400App are valid
   * string, decimal, and char types respectively. */
  ProgParm[] Parms = new ProgParm[3];
  Parms[0] = new ProgParm(<br />     new ProgParmType("CustName", 0, FieldType.NewChar(40)),
  DataDirection.Output);<br />    Parms[1] = new ProgParm(<br />        new ProgParmType("TimeOfDay", 0, FieldType.NewPacked(6, 0)),
  DataDirection.Output);<br />    Parms[2] = new ProgParm(<br />        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
  DataDirection.Input);
   prog.AppendParms(Parms);
   prog.ObjectToParm(Parms[2], Quit400App, 0);
   prog.Execute(); 
  /* After calling the last two values in the parameter list
   * will have new values in it. To read them, we set our local
   * variables to the returned values in the parameters list. */
  CustName = Convert.ToString(<br />      prog.ParmToObject(System.Type.GetType("System.String"),<br />      "CustName",<br />       0));
  TimeOfDay = Convert.ToDecimal(<br />      prog.ParmToObject(System.Type.GetType("System.Decimal"),<br />      "TimeOfDay",<br />      0));</pre>
      <pre>        <span class="lang">
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
      [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html)
      <br />
      [ASNA.DataGate.DataLink.StructureType Class](dcsStructureTypeClass.html)

