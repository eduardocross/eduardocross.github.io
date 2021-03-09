---
title: As400Program.AppendParm Method

Id: dcsAs400ProgramClassAppendParmMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 0

keywords: AppendParm method
keywords: As400Program.AppendParm method
keywords: program parameters, append parameter to
keywords: parameter lists, append parameter to
keywords: append parameter to program parameter list
keywords: parameters, append program parameter list
keywords: how to, append parameter to program parameter list

---

Appends a parameter to the parameter list for the program.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void AppendParm(
   [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) Parameter
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub AppendParm( _
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AppendParm Acess(*Public)
   DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Parameter* 
          </span>
        </dt>
        <dd>
          <span />
          <span> An instance of **ASNA.DataGate.DataLink.ProgParm**  class that represents the program parameter to append. </span>  </dd>
</dl>

Exceptions

ArgumentException. A **ProgParm** in the array has the same name as another parameter in the parameter list.<span />
Remarks

To create a program parameter list, <span> **ProgParm** </span> objects should be added with the <span> **AppendParm** </span> or [AppendParms](dcsAs400ProgramClassAppendParmsMethod.html) method in the order of their occurrence in the program parameter list. <span> **AppendParm** </span> appends a single <span> **ProgParm** </span> object to the parameter list.

The **ProgParm** appended to the list may optionally be named via the <span>name</span> parameter of the [DataLink.ProgParmType](dcsProgParmTypeClassProgParmTypeConstructor.html) and [DataLink.StructuredType](dcsStructureTypeClass.html) constructors. If the <span> **ProgParm** </span> is named and a previously appended **ProgParm** has the same name, an ArgumentException is raised. 

**Note** that the parameter list may be constructed with this method before the [ Connection](dcsAs400ProgramClassConnectionProperty.html) property has been set, but the values of the parameters may not be accessed with [ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html) and [ParmToObject Method](dcsAs400ProgramClassParmToObjectMethodMain.html) until <span> **Connection** </span> has a value.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( new ProgParm(
        new ProgParmType("CustName", 0, FieldType.NewChar(40)),
        DataDirection.InputOutput
  ));
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", new int[]{} );
  prog.Execute();
  //Fetch the returned value.
  CustName = Convert.ToString(
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", 
        new int[]{}));  </pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, prog is an initialized As400Program.
  ' We add the field "CustName" to the parm list, and a local
  ' string variable by the same name into it.  After calling the
  ' program, we then set the local variable to the returned
  ' value in the parms list.
  prog.AppendParm( New ProgParm( _
        New ProgParmType("CustName", 0, FieldType.NewChar(40)), _
        DataDirection.InputOutput _
  ))
  ' Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", New Integer(){} )
  prog.Execute()
  ' Fetch the returned value.
  CustName = Convert.ToString( _
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", _
        New Integer(){}))</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, prog is an initialized As400Program.
   * We add the field "CustName" to the parm list, and a local
   * string variable by the same name into it.  After calling the
   * program, we then set the local variable to the returned
   * value in the parms list. */
  prog.AppendParm( *New ProgParm( +
        *New ProgParmType("CustName", 0, FieldType.NewChar(40)), +
        DataDirection.InputOutput + 
  ))
  //Store the value to pass in.
  prog.ObjectToParm( CustName, "CustName", *Nothing *As *Integer4[] )
  prog.Execute()
  //Fetch the returned value.
  CustName = Convert.ToString( +
        prog.ParmToObject(System.Type.GetType("System.String"), "CustName", +
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
      [AppendParms Method](dcsAs400ProgramClassAppendParmsMethod.html)
      <br />
      [Connection Property](dcsAs400ProgramClassConnectionProperty.html)
      <br />
      [ObjectToParm Methods](dcsAs400ProgramClassObjectToParmMethodMain.html)
      <br />
      [ParmToObject Methods](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink.StructuredType Class](dcsStructureTypeClass.html)
      <br />
      [StructuredType Class 
					Constructors](dcsStructureTypeClass.html)
      <p />

