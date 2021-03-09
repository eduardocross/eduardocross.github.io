---
title: Calling Stored Procedures

Id: dcsCallingStoredProcedures
TocParent: dcsTutorialsMain
TocOrder: 0

keywords: VB examples
keywords: samples programs
keywords: program call turtorial
keywords: calling stored procedures, tutorial
keywords: calling stored procedures, database connections and program paths
keywords: calling stored procedures, procedural construction of parameter lists
keywords: calling stored procedures, accessing parameter data
keywords: calling stored procedures, structured types and arrays as parameters
keywords: program call example
keywords: example programs
keywords: example programs, program call tutorial
keywords: example programs, location of installed examples
keywords: example programs, location of installed examples
keywords: turorial, program call example
keywords: turorial, database connections and program paths
keywords: turorial, procedural construction of parameter lists
keywords: turorial, accessing parameter data
keywords: turorial, structures types and arrays as parameters

---

#### Program Call Example Tutorial
DCS for Visual Studio 2019 offers an interface for calling traditional RPG programs. These called programs typically are designed to be passed parameter variable values by reference. Thus the caller can pass a variable of a certain type to the program and the program, which defines the type of the parameter variable, can read and change the value of the variable before control is returned to the caller.

Unlike IBM i file access where files are "externally described" and programs are compiled against those descriptions, the descriptions of IBM i program parameters are not readily available from the database, and thus cannot be directly compiled against. The description of called program parameters must be known and described by the DCS programmer in order for a program call to be successful. DCS allows parameters of called programs to be described procedurally. The following sections describe the objects and methods for calling programs.

IBM i called programs may define parameters as complex data structures and arrays of simple or complex types. DCS supports these parameters. Following the sections outlining parameter list construction is a section detailing the use of arrays and data structures.

Note: There are some VB examples located in the C:\Program Files\ASNA\Examples\DCS for VS 2017\VB folder. Each example is contained within a separate folder and there is a file called z_Readme.mht file in each folder containing information about the example and how to access it. Double-clicking on the solution file (.sln) will automatically open the example in Visual Studio 2019.
Contents

- Database Connections and Program Paths
- Procedural Construction of Parameter Lists
- Accessing Parameter Data
- Structured Types and Arrays as Parameters

### Database Connections and Program Paths
Before calling a program with DCS you must provide the following information: 

- The database server to connect to.
- The path of the program on the database server.
- A description of the parameters to be passed into and/or returned from the program (see [ProgParm](#Procedural_Construction_of_Parameter_Lists">Procedural_Construction_of_Parameter_Lists</a>).

#### Database Connection:
The database server is identified and connected with an object of the AdgConnection class. Very often you will use a predefined "database name" in the Open method of AdgConnection to connect to the database.
<pre>[C#]
  AdgConnection cn;
  Cn = new AdgConnection();
  cn.Open("MyAs400");</pre>
        <pre>[Visual Basic]
  Dim cn as AdgConnection
  cn = New AdgConnection
  cn.Open("MyAs400")</pre>
        <pre>[Visual RPG]
  Dclfld Name(Cn)Type(AdgConnection)
  Cn =*New AdgConnection
  Cx.Open("MyAs400")</pre>

The above code will open a database connection to the IBM i server named "MyAs400". See the DataGate Studio documentation for a discussion of database names.

#### Path of Program:
To name the path of a program you use the As400Program class, as in the following examples.
<pre class="prettyprint">[C#]
  As400Program prog;
  Prog = new As400Program(cn, "*libl/myprog");</pre>
        <pre class="prettyprint">[Visual Basic]
  Dim prog as As400Program
  prog = New As400Program(cn, "*libl/myprog")</pre>
        <pre class="prettyprint">[Visual RPG]
  Dclfld Name(Prog) Type(As400Program)			
  Prog = *New As400Program(cn, "*libl/myprog")</pre>

### Procedural Construction of Parameter Lists
To procedurally describe the parameters and attach the description to the As400Program object, three classes in the ASNA.DataGate.Client.DataLink namespace are provided:

- <a href="dcsProgParmClass.html) is the data instance of a ProgParmType or StructureType description in an As400Program object, and includes a description of how the data of the parameter will be marshalled across the client/server connection.
- [ProgParmType](dcsProgParmTypeClass.html) describes scalar parameters of the traditional IBM i database types, such as "packed", "char", etc.
- [StructureType](dcsStructureTypeClass.html) describes complex types composed of combinations of scalars, arrays and embedded complex types.

ProgParm objects reference an instance of ProgParmType or StructureType. The As400Program object references a list of ProgParm objects representing the ordered list of program parameters passed to the program. ProgParm objects are used to access the data associated with a particular parameter. To construct a parameter list procedurally using the parameter classes, construct instances of ProgParmType (and/or instances of StructureType, as will be discussed in a later section). Then append instances of ProgParm referencing the corresponding ProgParmType to the As400Program object.

In the ProgramCallSimple example, the IBM i program being called is a one-parameter program, as written in the following CL code:
<pre>
  PGM       PARM(&amp;DECPARM)
  DCL       VAR (&amp;DECPARM) TYPE(*DEC) LEN(7 2)
  CHGVAR    VAR (&amp;DECPARM) VALUE(&amp;DECPARM + 1)
  ENDPGM</pre>

This program expects to receive an input parameter of type packed decimal (precision 7, scale 2). The program adds the value 1 to the parameter before returning to the caller. In ProgramCallSimple, you will find the following code which accomplishes this.
<pre>[C#]
  ProgParmType parmType;
  parmType = new ProgParmType( "Parm1", 0, FieldType.NewPacked(7,2) );
  ProgParm countParm;
  countParm = new ProgParm( parmType, DataDirection.InputOutput );
  ...
  prog.AppendParm(countParm);</pre>
        <pre>[Visual Basic]
  Dim parmType As	ProgParmType
  parmType = New ProgParmType("Parm1", 0, FieldType.NewPacked(7, 2))
  Dim countParm As ProgParm
  countParm = New ProgParm(parmType, DataDirection.InputOutput)
  ...
  prog.AppendParm(countParm)</pre>
        <pre>[Visual RPG]
  DCLFLD Name (parmType) Type (ProgParmType)
  parmType = New ProgParmType("Parm1", 0, FieldType.NewPacked(7, 2))
  DCLFLD Name (countParm) Type (ProgParm)
  countParm = New ProgParm(parmType, DataDirection.InputOutput)
  ...
  prog.AppendParm(countParm)</pre>

ProgParmType object parmType is constructed with three parameters.

1. The first parameter names the program parameter type. This name is useful when the type is part of a StructureType but we can ignore it for now.
2. The second parameter supports the use of this type as an array – setting the value to zero marks this parameter type as a non-array.
3. The third parameter specifies the data type of the parameter; in this case the required packed decimal type. Use the ASNA.DataGate.Common.FieldType.New* methods to specify the data type.

The ProgParm object countParm is constructed by passing a reference to the previously constructed ProgParmType object and a marshalling directive. In this case, DataDirection.InputOutput tells DCS that the value of the parameter will be copied across the client/server link both prior to calling the program and then again upon return. InputOutput effectively emulates the "pass by reference" semantics of the traditional IBM i CALL command. If you know that your parameter is either an input-only or an output-only parameter (or unused), then you may specify another directive (Input, Output, or None) to improve performance by reducing the amount of data transferred on the client/server link. In this case however, the packed decimal parameter described by parmType will be used as both an input and output parameter.

The [AppendParm](dcsAs400ProgramClassAppendParmMethod.html) method of As400Program associates the ProgParm object with the program as the first parameter in the stack to be passed. In this case, countParm is the only parameter to be passed. If there were more than one, you would use successive calls to AppendParm to list the parameters in the order they would be passed to the program.

### Accessing Parameter Data
For input parameters, you will want to set the data value of the parameter before calling the program. You may only do this after appending the parameter to the As400Program object as follows.
<pre class="prettyprint">[C#]
  prog.ObjectToParm(countParm, 7.73, 0 );</pre>
        <pre class="prettyprint">[Visual Basic]
  prog.ObjectToParm(countParm, 7.73, 0);</pre>
        <pre class="prettyprint">[Visual RPG]
  prog.ObjectToParm(countParm, 7.73, 0)</pre>

The ObjectToParm method of As400Program is used to convert an object or value type to a parameter list value.

- The first parameter in this ObjectToParm call references the ProgParm object. Note that this ProgParm object must be previously inserted into the parameter list of the As400Program object via the Append method or the method will fail.
- The second parameter is the object or value type whose value will set the parameter value. In this case, the value is the fixed decimal constant ‘7.73’. Note that the parameter can generally be an arbitrary type – ObjectToParm will attempt to convert the given object or value type to the type described by the ProgParm object. Not all conversions will be sensible however. For example, if the string value "Red" were used in the above call instead of 7.73, ObjectToParm would throw an exception indicating that the value could not be converted to the specified packed decimal database type.
- The third parameter in the ObjectToParm method is a single-dimension array index. Since countParm is not an array, the index parameter is ignored. If count parm were an array, this index would specify which element of the array should be set to the specified value.

After setting the input parameter values, the IBM i program may be invoked with the Execute method of As400Program, as below.
<pre class="prettyprint">[C#]
  prog.Execute();</pre>
        <pre class="prettyprint">[Visual Basic]
  prog.Execute()</pre>
        <pre class="prettyprint">[Visual RPG]
  prog.Execute()</pre>

Execute sends all DataDirection.Input and DataDirection.InputOutput parameter values to the database server, and tells the server to invoke the program. Execute blocks, waiting for the result of the program call. When control returns to the database server from the called program, the server sends all DataDirection.Output and DataDirection.InputOutput parameter values to DCS.

Upon return from Execute, your DCS program will want to extract the output parameter values from the parameter list. In the ProgramCallSimple example, there is only one output parameter that we are interested in and it is accessed with the As400Program class’ ParmToObject method as follows:
<pre class="prettyprint">[C#]
  decimal retVal;
  retVal = (decimal) prog.ParmToObject(countParm,);
  typeof(decimal), 0);</pre>
        <pre class="prettyprint">[Visual Basic]
  Dim retVal As Decimal
  retVal = prog.ParmToObject(countParm, Type.GetType("System.Decimal"), 0)</pre>
        <pre class="prettyprint">[Visual RPG]
  Dclfld Name(retVal) Type(*Decimal)
  retVal = prog.ParmToObject(countParm,
  Type.GetType("System.Decimal"),0)</pre>

ParmToObject returns an object or value type of a specific type. As with the value parameter of ObjectToParm, this return type may be arbitrary, but there are limits to the possible conversions available. Here, we expect ParmToObject to return a **System.Decimal** value.

- The first parameter specifies the ProgParm object containing the value we want to access, *countParm* . If countParm were not in the parameter list of the prog object then an exception would be thrown.
- The second parameter specifies the type of the object or value type to be returned. Since we expect a System.Decimal to be returned, we pass that value type specification here.
- The final parameter of ParmToObject is identical to the index parameter of ObjectToParm. It is ignored by ParmToObject in this case, since countParm is not an array.

Note that in C#, an explicit cast is required to instruct the compiler that the object type returned by ParmToObject is a boxed value type (decimal).

### Structured Types and Arrays as Parameters
IBM i programs and, in particular, ILE-RPG programs, are allowed to define parameters as complex types, or "structured" types. Also, parameters may be defined as "multiple-occurrence" parameters or single-dimension arrays. A combination of structured types and arrays is allowed by defining a parameter as a "multiple occurrence data structure." DCS provides the capability to call programs defining parameters in any of these ways. The ProgramCallComplex project illustrates one example of calling an RPG program which defines its input parameter as a multiple-occurrence data structure. The program being called is given by the following ILE-RPG source code.

ILE-RPG source code:
<pre class="prettyprint">
  D TestDS   DS           Occurs(5)
  DTest1        1    5S 1
  DTest2        6    10
  DTest3       11    16P 2
  C   *Entry Plist
  C          parm         TestDs
  C          parm         OccurRes
  C    2     Occur   TestDS
  C    Test2   Ifeq   '2Fld2'
  C            movel  'ok'   OccurRes
  C            else
  C            movel  'bad'  OccurRes 3
  C            Endif
                       Return
   </pre>

This code defines two program parameters, TestDS and OccurRes.

- TestDS is a multiple-occurrence type or, conventionally, a single-dimension array of length 5. Further, each element of TestDS is a "data structure", consisting of a set of primary types. The data structure defined consists of a zoned decimal number of precision 5 and scale 1 (Test1), a 5-character fixed-width string (Test2), and a packed decimal of precision 11 and scale 2 (Test3). Thus the TestDS parameter consists of 5 consecutive occurrences of this structure.
- The OccurRes parameter is defined as a character field of 3 or more characters and is used by the program as an output parameter to return a result value.

This very simple test program merely examines the second element of the array, determines if the Test2 member of this element contains an expected value (‘2Fld2’), and returns ‘ok’ or ‘bad’ in OccurRes depending upon the result.

You can construct a parameter list for calling this program using the previously shown procedural method. In the ProgramCallComplex project, the TestDS parameter is formed using the StructureType class. StructureType is similar to ProgParmType, in that it is used to construct a ProgParm instance. StructureType is constructed with an array of objects. The objects must be of type ProgParmType (for simple types) or StructureType (for embedded structures). The following code from ProgramCallComplex illustrates the creation of the TestDS parameter.
<pre>[C#]
  // Create "TestDS" structure definition (3 members)
  object[] structMbrs = new object[3];
  structMbrs[0] = new ProgParmType("Test1", 0, FieldType.NewZoned(5, 1));
  structMbrs[1] = new ProgParmType("Test2", 0, FieldType.NewChar(5));
  structMbrs[2] = new ProgParmType("Test3", 0, FieldType.NewPacked(11, 2));
  // Add multiple-occurrence (array) definition "TestDS" to parameter list
  StructureType structType = new StructureType("TestDS", 5, structMbrs);
  parmList[0] = new ProgParm(structType, DataDirection.Input);</pre>
        <pre>[Visual Basic]
  ' Create "TestDS" structure definition (3 members)
  Dim structMbrs(2) As Object
  structMbrs(0) = New ProgParmType("Test1", 0, FieldType.NewZoned(5, 1))
  structMbrs(1) = New ProgParmType("Test2", 0, FieldType.NewChar(5))
  structMbrs(2) = New ProgParmType("Test3", 0, FieldType.NewPacked(11, 2))
  ' Add multiple-occurrence (array) definition "TestDS" to parameter list
  Dim structType As StructureType
  structType = New StructureType("TestDS", 5, structMbrs)
  parmList(0) = New ProgParm(structType, DataDirection.Input)</pre>
        <pre class="prettyprint">[Visual RPG] 
  //Create "TestDS" structure definition (3 members) 
  DCLFLD Name (structMbrs(2)) Type (*Object) 
  structMbrs(0) = New ProgParmType("Test1", 0, FieldType.NewZoned(5, 1)) 
  structMbrs(1) = New ProgParmType("Test2", 0, FieldType.NewChar(5)) 
  structMbrs(2) = New ProgParmType("Test3", 0, FieldType.NewPacked(11, 2))
  ' Add multiple-occurrence (array) definition "TestDS" to parameter list
  DCLFLD Name (structType) Type (StructureType) 
  structType = New StructureType("TestDS", 5, structMbrs) 
  parmList(0) = New ProgParm(structType, DataDirection.Input)</pre>

The first four statements construct the array of objects describing the members of the structure (Test1, Test2, and Test3).

In the next section, the structMbrs array is passed to the StructureType constructor to complete the structure definition. Notice that since this is a multiple occurrence data structure, we specify the number of occurrences here (5). 

The last statement creates a ProgParm object containing the structure definition and defines it as an "input only" parameter.

After constructing the parameter list the ProgramCallComplex program initializes the TestDS input parameter data as follows.
<pre>[C#]
  int[] secondElemRef = new int[]{1};
  prog.ObjectToParm( "2Fld2", "TestDS.Test2",
    secondElemRef );</pre>
        <pre>[Visual Basic]
  Dim secondElemRef(1) As Integer
  secondElemRef(0) = 1
  prog.ObjectToParm("2Fld2", "TestDS.Test2", secondElemRef)</pre>
        <pre class="prettyprint">[Visual RPG] 
  Dclfld Name(secondElemRef(1) Type(*Integer) 
  secondElemRef(0) = 1 
  prog.ObjectToParm("2Fld2", "TestDS.Test2",  
  secondElemRef)</pre>

Since the called program is only interested in a particular member of a data structure (Test2) and that data structure is in a particular element of the array (second element), the above code only sets the data for that element. Note that DCS chooses reasonable default "zero" values for parameter values that are not set explicitly. However, the programmer should not rely on default values to supply data used by a called program. 

In referencing the data of any parameter, DCS uses two distinguishing characteristics: 

4. the name of each member in the path to the data
5. a set of integers,representing array indices selecting array elements along the path to the data

By "path to the data" we mean navigation from the top-most parent structure name to the leaf member name. Note that structures may contain other structures (though not in RPG), and that structures and/or their members may be arrays.

In this case, TestDS is an array of 5 elements. Thus, we provide ObjectToParm with a set of indices containing one integer, the index of the element of the TestDS array to reference. The integer array passed to ObjectToParm (secondElemRef) is an array of integers of length one. We set its only element to the value 1, which denotes the zero-relative second element of the TestDS array.

To access the particular member of the TestDS element we have chosen, we use the second parameter of ObjectToParm. This string names all members in the path to the data, separated by a dot (‘.’). The first name, TestDS, is the name of the structure in the parameter list. The second name is the name of the member, Test2, to be accessed. Finally, the value for the parameter data is passed as "2Fld2", which is what the called program expects as valid input.

### See Also
<dl />
        [AdgDataSet Class](dcsAdgDataSetClass.html)
        <br />
        [FileAdapter Class](dcsFileAdapterClass.html)

