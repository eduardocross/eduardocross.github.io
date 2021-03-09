---
title: As400Program(AdgConnection)

Id: dcsAs400ProgramClassAs400ProgramMethod2
TocParent: dcsAs400ProgramClassAs400ProgramMethodMain
TocOrder: 1

---

Construct an instance of the **As400Program** object and set the [ Connection](dcsAs400ProgramClassConnectionProperty.html) property.
<pre>
        <span class="lang">[C#]</span>
 **public As400Program(
   AdgConnection Connection
);** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal Connection As [AdgConnection](dcsAdgConnectionClass.html) _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Acess(*Public)
   DclSrParm Connection Type(AdgConnection)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Connection* 
          </span>
        </dt>
        <dd>An [AdgConnection](dcsAdgConnectionClass.html) object used to 
			set the value of the **Connection**  Property.</dd>
</dl>

Exceptions

[ASNA.DataGate.Common.dgException](dcsdgExceptionClass.html) is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 10%" />
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

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The reference being assigned to *Connection* is null, or is an **AdgConnection** object whose [State](dcsAdgConnectionClassStateProperty.html) property is not equal to System.Data.ConnectionState.Open (see Remarks). 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVSQLOP
</td>
            <td colspan="1" rowspan="1">

The value of *Connection* is not a valid connection for use with As400Program. 
</td>
          </tr>
</table>

Remarks

This constructor invokes the [default constructor](dcsAs400ProgramClassAs400ProgramMethod1.html) then sets the value of the [ Connection](dcsAs400ProgramClassConnectionProperty.html) property with the *Connection* parameter. The **As400Program** object is created without a program path. The parameter list is initialized to length zero. The [ ProgramPath](dcsAs400ProgramClassProgramPathProperty.html) property will be set to a zero-length string.

If *Connection* is set with a null value, or is an **AdgConnection** instance which is unconnected or incompatible with **As400Program** , an exception is raised. Use [ AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html) to open a connection to an IBM i database provider prior to setting **Connection** . Before adding parameters or calling programs with an instance created with this constructor, the **ProgramPath** property must be set.
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  //Here, "ProdDB" is an initialized AdgConnection.
  As400Program prog = new As400Program(ProdDB);
  prog.ProgramPath = "*Libl/Call400";</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, "ProdDB" is an initialized AdgConnection.
  Dim prog As New As400Program(ProdDB)
  prog.ProgramPath = "*Libl/Call400"</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  // Here, "ProdDB" is an initialized AdgConnection.
  DclFld prog Type(As400Program)
  prog = *New As400Program(ProdDB)
  prog.ProgramPath = "*Libl/Call400"</pre>

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
      [ProgramPath Property](dcsAs400ProgramClassProgramPathProperty.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

