---
title: As400Program.ObjectToParm(ProgParm, object, int)

Id: dcsAs400ProgramClassObjectToParmMethod1
TocParent: dcsAs400ProgramClassObjectToParmMethodMain
TocOrder: 1

---

Converts an object or value type to a parameter list value. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void ObjectToParm(
   [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) Parameter,
   object Value,
   int Element
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub ObjectToParm( _
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) _
   ByVal Value As Object _
   ByVal Element As Integer _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ObjectToParm Access(*Public)
   DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))
   DclSrParm Value Type(*Object)
   DclSrParm Element Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Parameter* 
          </span>
        </dt>
        <dd>
          <span />
          [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html).  
						The value to be set. </dd>
        <dt>
 *Value* 
        </dt>
        <dd>The name or path of the program parameter object in the parameter list. </dd>
        <dt>
          <span>
 *Element* 
          </span>
        </dt>
        <dd>
          <span />For paths including multiple-occurrence parameters only, the indices in the path to the parameter.
									</dd>
</dl>

Exceptions

**ArgumentException** . Indicates that name, and if necessary indices, do not reference a valid parameter in the parameter list. 

**InvalidOperationException** . Indicates that the **Connection** property of **As400Program** has not been set.
Remarks

This form of **ObjectToParm** may be used to set the value of both simple and structured parameters using the optional parameter naming scheme allowed by [ProgParmType](dcsProgParmTypeClass.html) and [StructureType](dcsStructureTypeClass.html). The constructor for these classes allows the program parameters they represent to be given a string identifier. This identifier may have significance to the application, but it also may be used by this method to identify and retrieve the parameter after it has been added to the [As400Program](dcsAs400ProgramClass.html) parameter list.

For simple parameters (constructed with **ProgParmType** ), *Value* refers to the name given to the [ ProgParmType’s constructor](dcsProgParmTypeClassProgParmTypeConstructor.html). Indices is ignored unless the simple parameter is a multiple-occurrence (single-dimension array) parameter. In this case, indices should be an integer array of at least one element. The first element in indices must be a zero-relative number identifying the element in the array to be set by **ObjectToParm** .

For complex parameters (constructed with [ StructureType's constructor](dcsStructureTypeClass.html)), *Value* refers to a path to a particular member of the data structure and should be in the form of string tokens separated by the character ‘.’, as in "x.y.z". Each token to the left of ‘.’ is the name of a structure containing a member named on the right of ‘.’. The leftmost string token refers to the name of the outermost structure, or the **ProgParm** object contained in the **As400Program** parameter list. The rightmost token must refer to the name of a simple parameter type (constructed with **ProgParmType** ) which is the member whose value is to be set.

If the complex parameter path includes data types defined as multiple-occurrence types, then the indices property must contain an array of integers. The elements of indices refer to positions in the multiple occurrence types. For example, suppose a parameter consists of a multiple occurrence data structure and one of the data structure’s members is a multiple occurrence character field type. To set the value of one of the character fields, indices must be an array of at least length 2. The first element of the array would reference an occurrence of the outer structure, and the second element of the array would refer to the particular character field to set.

If no multiple occurrence types are included in the path given by name, indices may be specified as an integer array of length zero.

The outermost **ProgParm** object identified by name and indices should be a member of the **As400Program’s** parameter list. The [Connection](dcsAs400ProgramClassConnectionProperty.html) property must be set (or the **As400Program** constructed with an [ AdgConnection](dcsAdgConnectionClass.html) object) prior to calling **ObjectToParm** .

For the method to succeed, the type specified by *ReturnType* must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be set with an arbitrary object (such as a string), only if the object implements **System.IConvertible** , and the **ToDecimal** method yields a valid conversion. Most fundamental types in the System namespace implement IConvertible.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  /* Here, "prog" is an initialized As400Program object.
   * The first two lines creates a IBM i character data type whose
   * length is one, and then appends it to "prog"'s parameter list. */
  ProgParm QuitParm = new ProgParm(
        new ProgParmType("Quit400App", 0, FieldType.NewChar(1)),
        DataDirection.InputOutput );
  prog.AppendParm(QuitParm);
  char QuitChar = '1';
  /* This next line assigns the .NET value, CustName, to the
   * IBM i data type of the same name in the parameter list. */
  prog.ObjectToParm(QuitParm, QuitChar, 0);
</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, "prog" is an initialized As400Program object.
  ' The first two lines creates a IBM i character data type whose
  ' length is one, and then appends it to "prog"'s parameter list. */
  Dim QuitParm As New ProgParm( _
        New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), _
        DataDirection.InputOutput )
  prog.AppendParm(QuitParm)
  Dim QuitChar As Char
  QuitChar = "1"
  ' This next line assigns the .NET value, CustName, to the
  ' IBM i data type of the same name in the parameter list. */
  prog.ObjectToParm(QuitParm, QuitChar, 0)</pre>
      <pre>
        <span class="lang">
 **[Visual RPG]** 
  </span>/* Here, "prog" is an initialized As400Program object.
   * The first two lines creates a IBM i character data type whose
   * length is one, and then appends it to "prog"'s parameter list. */
  DclFld QuitParm Type(ProgParm)
  QuitParm = *New ProgParm( +
        *New ProgParmType("Quit400App", 0, FieldType.NewChar(1)), +
        DataDirection.InputOutput )
  prog.AppendParm(QuitParm)
  DclFld QuitChar Type(*OneChar) Inz('1')
  /* This next line assigns the .NET value, CustName, to the
   * IBM i data type of the same name in the parameter list. */
  prog.ObjectToParm(QuitParm, QuitChar, 0)</pre>

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

