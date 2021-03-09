---
title: As400Program.ObjectToParm(ProgParm, object)

Id: dcsAs400ProgramClassObjectToParmMethod4
TocParent: dcsAs400ProgramClassObjectToParmMethodMain
TocOrder: 0

---

Converts an object or value type to a parameter list value.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void ObjectToParm(
   ProgParm Parameter,
   object Value
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub ObjectToParm( _
   ByVal Parameter As ProgParm _
   ByVal Value As Object _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ObjectToParm Acess(*Public)
   DclSrParm Parameter Type(ProgParm)
   DclSrParm Value Type(*Object)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Parameter* 
          </span>
        </dt>
        <dd>
          [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html).  The 
						value to be set.</dd>
        <dt>
 *Value* 
        </dt>
        <dd>The name of the program parameter object in the parameter list.
							</dd>
</dl>

Exceptions

**ArgumentException** . Thrown if *parameter* is a complex parameter (constructed with an instance of [StructureType](dcsStructureTypeClass.html)).

**InvalidOperationException** . Indicates that the [ Connection](dcsAs400ProgramClassConnectionProperty.html) property of **As400Program** has not been set.
Remarks

This form of **ObjectToParm** may be used to set the value of simple parameters (non-structured) with a reference to the **ProgParm** object. The object should be a member of the [ As400Program's](dcsAs400ProgramClass.html) parameter list. The **Connection** property must be set (or the **As400Program** constructed with an [AdgConnection](dcsAdgConnectionClass.html) object) prior to calling **ObjectToParm** .

For the method to succeed, the *Value* object must have a valid conversion to the underlying parameter type. For example, a parameter for a decimal number can be set with an arbitrary object (such as a string), only if the object implements **System.IConvertible** and the **ToDecimal** method yields a valid conversion. Most fundamental types in the System namespace implement IConvertible.

This method of **ObjectToParm** should not be used if *Parameter* is a "multiple-occurrence" parameter type. Instead, use a method that allows the index of the multiple-occurrence parameter to be specified.
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
      <pre class="prettyprint">
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

