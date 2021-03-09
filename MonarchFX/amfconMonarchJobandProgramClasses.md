---
title: Monarch Job and Program classes

Id: amfconMonarchJobandProgramClasses
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 60

keywords: ASNA.Monarch, execution context
keywords: ASNA.Monarch, Monarch Job and Program classes
keywords: concepts, ASNA.Monarch execution context
keywords: concepts, ASNA.Monarch Monarch Job and Program classes
keywords: concepts, ASNA.Monarch.Programs
keywords: concepts, ASNA.Monarch MyJob
keywords: concepts, ASNA.Monarch jobs
keywords: concepts, ASNA.Monarch CL programs

keywords: ASNA Monarch concepts, execution context
keywords: ASNA Monarch concepts, Monarch Job and Program classes
keywords: ASNA Monarch concepts, programs
keywords: ASNA Monarch concepts, MyJob
keywords: ASNA Monarch concepts, jobs
keywords: ASNA Monarch concepts, CL programs
keywords: ASNA.Monarch.Program class, using
keywords: Job class, concepts
keywords: Job class, activation manager
keywords: MyJob, concepts
keywords: MyJob, about
keywords: activation manager, about
keywords: activation manager, ActivationGroupAttribute
keywords: activation manager, CallerActivationGroupAttribute
keywords: activation manager, NewActivationGroupAttribute
keywords: activation group, _Star_caller
keywords: activation group attributes, _Star_caller
keywords: activation group, _Star_default
keywords: activation group attributes, _Star_default
keywords: activation group, _Star_new
keywords: activation group attributes, _Star_new
keywords: activation group name
keywords: activation group attributes, group name
keywords: activation group attributes, getting group name
keywords: startup program, about
keywords: Program class, concepts
keywords: CLProgram class, concepts
keywords: CLPrograms, about
keywords: Program class, _Star_Entry
keywords: _Star_Entry
keywords: _Star_Entry, calling
keywords: _Star_Entry, parameters
keywords: _Star_Entry, procedures
keywords: _Star_Entry, migrating
keywords: OS400 concepts, Job class
keywords: OS400 concepts, Program class
keywords: OS400 concepts, CLProgram class
keywords: OS400 concepts, startup programs
keywords: OS400 concepts, programs
keywords: OS400 concepts, CL programs
keywords: OS400 concepts, _Star_Entry
keywords: OS400 concepts, local data areas
keywords: OS400 concepts, library lists
keywords: ASNA.Monarch.Program, concepts
keywords: ASNA.Monarch.Job, concepts
keywords: ASPX sessions, workstation files

---

The Monarch Execution Context portion of the framework includes the [ ASNA.Monarch.Job](amfJobClass.html) class that supplements a process (or thread) in the implementation of the concept of a job. The **Job** class provides an environment for Monarch programs to run under. Its main functions are maintaining program activation and a connection to the database server. The Job class also provides facilities to support certain IBM i concepts, like when overriding file parameters or local data areas.

#### Programs 
When an application is migrated from IBM i; each program is transformed into an AVR class. In Monarch context, these classes are still referred to as " **Programs** ". A Program is a class that conforms to certain conventions allowing it to be the target of a <code> **CALLB** </code> operation. The class has to implement the <code> ***Entry** </code> procedure (see topic below for more information). To allow the retaining of state across program calls, the class should derive from the [ ASNA.Monarch.Program](amfProgramClass.html) class that works in conjunction with the **ASNA.Monarch.Job** class.

Besides the <code> ***Entry** </code> procedure, a Monarch program typically has a <code> **constructor** </code> and a <code> **dispose** </code> subroutine. In the <code> **constructor** </code>, the program opens all the files that were marked as being implicitly opened, that is, those not tagged as user controlled. The constructor is also responsible for initializing any data structure subfields requiring values other than zeros or blanks. The **dispose** subroutine provides the opportunity to close files and release any unmanaged resources.

The **Job** maintains an ***activation manager*** responsible for handling the activations of programs according to the <code>[ ActivationGroup](amfActivationGroupAttributeClass.html)</code> custom attribute defined in the <code> **BegClass** </code> of the program. The <code> **ActivationGroup** </code> attribute takes a string as a parameter that can be one of the following:

- *Name*  &#8211; A user provided name identifying the
        activation group to use for the program.
- *Default &#8211; A predefined activation
        group called *Default. Programs not marked
        with an ActivationGroup attribute are allocated in this
        group.
- *New &#8211; This special value indicates
        that the program is to be run in a new activation group.
        Monarch will create a new unique name for the group.
- *Caller &#8211; This special value states that
        the program will be allocated in the same activation group
        as the program calling this program.

An example of the <code>ActivationGroup</code> attribute for each type (highlighted bold) follows:
<pre class="prettyprint">BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) + 
			Attributes(ActivationGroup( "myGroupName" ))
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) +
			Attributes(ActivationGroup( "*Default" ))
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) + 
			Attributes(ActivationGroup( "*New" ))  
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) +
			Attributes(ActivationGroup( "*Caller" )) </pre>

Instead of using hard-coded string literals for the special values, the class provides the following three constants:

- ActivationGroupAttribute.Caller
- ActivationGroupAttribute.Default
- ActivationGroupAttribute.New

An example using each of these is shown below:
<pre class="example">BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) + 
			Attributes(ActivationGroup( ActivationGroupAttribute.Default ))
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) + 
			Attributes(ActivationGroup( ActivationGroupAttribute.New ))
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) +
			Attributes(ActivationGroup( ActivationGroupAttribute.Caller ))</pre>

Monarch also defines a couple of attributes to use as a "shorthand" for the cases of <code>*New</code> and <code>*Caller</code>, these are: [ NewActivationGroupAttribute](amfNewActivationGroupAttributeClass.html) and [ CallerActivationGroupAttribute](amfCallerActivationGroupAttributeClass.html). Using this shorthand, you could code something like this (both shown):
<pre class="example">BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) +
			Attributes(NewActivationGroup())
BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public ) +
			Attributes(CallerActivationGroup ())</pre>

The "<code>*Entry Procedure</code>" figure in the next section shows a program marked to run inthe activation group "<code>HardWater</code>".

#### The <code>*Entry</code> Procedure
As part of the migration process of a program, Monarch converts the mainline C-Specs into a procedure called <code>* **Entry** </code> in the generated class.
<pre class="prettyprint">BegClass Custcalc Extends(ASNA.Monarch.Program Access( *Public ) +
			Attributes(ActivationGroup("HardWater"))
   . . .
  DclFld Cust#    Type ( *Packed ) Len( 9,0 )   
  DclFld Cust#Ch  Type ( *Char   ) Len( 9   )
  DclFld SalesCh  Type ( *Char   ) Len( 13  )
  DclFld ReturnCh Type ( *Char   ) Len( 13  )

  BegProc *Entry Access ( *Public )
    DclSrParm Cust#Ch  By ( *Reference ) Options( *NoPass )   
    DclSrParm SalesCh  By ( *Reference ) Options( *NoPass )
    DclSrParm ReturnCh By ( *Reference ) Options( *NoPass )
    . . .
  EndProc</pre>

The <code>* **Entry** </code> Figure above shows the generated <code>* **Entry** </code>. Notice how the Parms in the *ENTRY PLIST become the parameters to the <code>* **Entry** </code> procedure.

#### MyJob
Each application has to be associated with a job. This is achieved via the <code>MyJob</code> class that extends **ASNA.Monarch.Job** . This class is generated by Monarch and is available to be augmented. MyJob is responsible for two main tasks: provide a connection to the databases and invoke the startup program in the application.

**MyJob.MyDatabase** and optionally **MyJob.MyPrinterDB** are defined in MyJob. MyDatabase is used for externally described data structures, for data file and data area access, and to call programs back on the server. MyPrinterDB is used to access print files. These database connections are used in two distinct forms; the commands refer to them to obtain their external definitions at compile time, and they are used at runtime to connect to the server.

When a program has to access the database at runtime, or any other of the members of the MyJob class or its base, it is necessary to obtain a reference to the instance associated with this job. This is done using the [ MonarchJob](amfProgramClassMonarchJobProperty.html) property provided by the base class **ASNA.Monarch.Program** . An example follows.
<pre class="prettyprint">BegClass Custcalc Extends(ASNA.Monarch.Program Access( *Public ))
    . . .
    BegConstructor Access ( *Public )
        . . .
        Open CSMASTERL1  DB (MonarchJob.Database)    
        Open CMMASTERL1  DB (MonarchJob.Database)  
    EndConstructor</pre>

As we will see in a later chapter, web applications are run in a multi-threaded environment, the <code> *MonarchJob* </code> property gets the instance object of the MyJob class associated with the particular thread running the program.

The <code> *MonarchJob* </code> property has a type of ASNA.Monarch.Job, if you need to refer to members in the class that you added to <code> *MyJob* </code>, then you should cast the value of <code>MonarchJob</code> using the <code>*AS</code> operator. This example shows how to access a field called <code>MyField</code>.
<pre class="prettyprint">BegClass Custcalc Extends(ASNA.Monarch.Program) Access( *Public )
. . .
  BegSr exampleSR  Access( *Public )
      DclFld X Type ( *Char  ) Len( 10 )
             X = (MonarchJob *AS MyJob).MyField
    . . .
EndClass</pre>

Alternatively, you can use the Job's built-in [LDC](amfJobClassLDCField.html) (local data collection) to provide access to objects and values to ASNA.Monarch.Program classes.

#### Startup Program
One of the main functions of <code> ***MyJob*** </code> is to get the program call sequence going. This is done by invoking the first program in the sequence of calls. This is known as the <code> **startup** </code> program.

A console program's **My Job** is typically also responsible for processing the command line. The following figure shows a <code>MyJob</code> sample where the startup program called is <code>CUSTPRTS</code>.
<pre class="prettyprint">BegClass MyJob Extends(ASNA.Monarch.Job) Access( *Public )
. . .
    BegSr ExecuteStartupProgram Access( *Protected )
        DclSrParm CustNumber Type ( *Char  ) Len( 9 )
        DclFld SendMsg       Type ( *Char  ) Len( 3 )
        Connect MyDatabase    
        Connect MyPrinterDB
        Move 'NO '  SendMsg
        Call CUSTPRTS
        DclParm    CustNumber
        DclParm    SendMsg
        EndPrograms()
     EndSr

     BegSr Main Shared(*Yes) Access(*Public)
         DclSrParm Args Type(*String) Rank(1)
         DclFld job Type(MyJob) New()
         checkParms(Args)
         job.ExecuteStartupProgram(Args[0])
     EndSr

EndClass</pre>

The Main subroutine receives the parameters from the command line in the <code> *Args* </code> array. After being validated, the job's <code> *ExecuteStartupProgram* </code> is called passing the first argument as a parameter. In this case it represents a customer number. The <code> *ExecuteStartupProgram* </code> routine connects to the databases and invokes the <code>CUSTPRTS</code> program. When <code>CUSTRPRTS</code> (and all the programs it calls) end, the [ EndPrograms](amfJobClassEndProgramsMethod.html) method of **ASNA.Monarch.Job** is called to deactivate any program that is still active and then the Dispose method of ASNA.Monarch.Job is called. This method is typically overwritten to close databases and release any other resource kept by the job.

#### Additional Embedded SQL Code
The following MyJob.vr shows a typical program with the additional code highlighted for the SQL connection established for processing embedded SQL. Notice the <code><span style="color: red">/Error</span></code> statements generated as a reminder to change the code if MS SQL Server is used.

For additional detail and other Monarch Framework classes that support embedded SQL, refer to [SQL Migration Overview](amfconSQLStatementExamples.html).
<pre class="prettyprint">Using System
Using MyCompany.MyApplication
DclNamespace MyCompany.MyApplication.GroupAll_Job
BegClass MyJob Extends(ASNA.Monarch.WebJob) Access(*Public)
  DclDB Name(MyDatabase) DBName("*Public/DG NET Local")Access(*Public)
  DclDB Name(MyPrinterDB) DBName("DG Net Local")Access(*Public)
  // additional declarative
  DclFld ADO_Connection Type(System.Data.Odbc.OdbcConnection) Access(*Public)
/Error When using MS SQL Server, replace System.Data.Odbc.OdbcConnection with +
/System.Data.SqlClient.SqlConnection

BegFunc getDatabase Type(ASNA.isualRPG.Runtime.Database) Access(*Protected) Modifier(*Overrides)
    LeaveSR MyDatabase
EndFunc
BegFunc getPrinterDB Type(ASNA.isualRPG.Runtime.Database) Access(*Protected) Modifier(*Overrides)
    LeaveSR MyPrinterDB
EndFunc

 // additional property
BegFunc getADO_Connection Type(System.Data.Common.DbConnection) Access(*Protected) Modifier(*Overrides)
   LeaveSR ADO_Connection
EndFunc BegSr Dispose Access(*Public) Modifier(*Overrides)
    DclSrParm disposing Type(*Boolean)
    If disposing
        Disconnect MyDatabase
        Disconnect MyPrinterDB
// additional dispose of ADO_Connection
        ADO_Connection.Close()
        ADO_Connection.Dispose()
    EndIf
   *Base.Dispose(Disposing)
EndSr
BegSr ExecuteStartupProgram Access(*Protected) Modifier(*Overrides)
      Connect MyDatabase
      Connect MyPrinterDB

 // additional code for ExecuteStartupProgram for the ADO connection
      DclFld connectStr Type(*String)   
      connectStr=string.Format("Driver={{ClientAccessODBCDriver(32-bit)}}; +
         "++"System={0};DBQ={1},*USRLIBL;Uid={2};Pwd={3}", +
         MyDatabase.Server, +
         MyDatabase.DBName, +
         MyDatabase.User, +
         /* Add your password here */ )
/Error When using MS SQL Server, replace connectStr assignment with "Data Source={0};Initial +
    Catalog={1};Integrated Security=True"

        ADO_Connection = *New System.Data.Odbc.OdbcConnection( connectStr )
/Error When using MS SQL Server, replace *New System.Data.Odbc.OdbcConnection with *New System.Data.SqlClient.SqlConnection

        ADO_Connection.Open()
        CallD 'MyCompany.MyApplication.Db0720'
EndSr
EndClass </pre>

#### <code>CLProgram</code>
Usage of CL can be divided into two major categories: **System Administration** and **Application Coordination** .

The administration of the system involves operations like the creation of user profiles and the save/restore procedures. These activities are not considered part of the application itself and Monarch does not attempt to facilitate such activities. Normal Windows<sup>&#174;</sup> techniques should be employed to affect these kinds of activities.

CL is used to setup the environment for RPG programs to run. The Monarch Framework, through [CL Program](amfCLProgramClass.html) class, provides support for CL program procedures in these areas:

- Sets up the Library List. The Library
        List is an ordered set of directory names associated with
        each application's database connection.
- Overrides database file. File Overrides
        are commands to replace the database file named in a CL
        procedure or program or to change certain parameters of the
        existing database file. These overrides can be applied to
        <code>DBFile</code>, <code>PrintFile</code>, or a <code>WorkStnFile</code> object. This may be
        especially useful for files that have been renamed or moved
        since the procedure or program was created. It can also be
        used to access a file member other than the first
        member.
- Maintain application parameters in data
        area. This covers several areas. 
		 <br />A 
 **local data area**  is created for each job in
        the system. The system creates a local data area, which is
        initially filled with blanks, with a length of 1024 and
        type <code>*CHAR</code>. When you submit a job, the value of the
        submitting job's local data area is copied into the
        submitted job's local data area. You can use this
        local data area to pass information to a procedure or
        program without the use of a parameter list.
        <br />Associated with each job are a set of 
 **job properties or attributes** . These
        attributes can be programmatically accessed in CL via the
        <code>RTVJOBA</code> commands. Another of these attributes is a series
        of 8 switches that can be "<code>on</code>" or "<code>off</code>." RPG programs also
        have access to these switches via the <code>*INUx</code>
        indicators.

#### Next: [Display File Concepts](amfconDisplayFiles.html)

#### Previous: [Control Execution Context](amfconExecutionContext.html)

#### See Also
[ SQL Migration Overview](amfconSQLStatementExamples.html)<br /> [Job Class](amfJobClass.html)<br /> [Job.Database Property](amfJobClassDatabaseProperty.html) <br /> [Job.PrinterDB Property](amfJobClassPrinterDBProperty.html)<br /> [Program Class](amfProgramClass.html)<br /> [CLProgram Class](amfCLProgramClass.html)<br /> [ActivationGroupAttribute Class](amfActivationGroupAttributeClass.html)<br /> [NewActivationGroupAttribute Class](amfNewActivationGroupAttributeClass.html)<br /> [CallerActivationGroupAttribute Class](amfCallerActivationGroupAttributeClass.html) 
