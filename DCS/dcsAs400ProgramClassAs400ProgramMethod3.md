---
title: As400Program(AdgConnection, string)

Id: dcsAs400ProgramClassAs400ProgramMethod3
TocParent: dcsAs400ProgramClassAs400ProgramMethodMain
TocOrder: 2

---

Construct an instance of the **As400Program** object and set the [Connection](dcsAs400ProgramClassConnectionProperty.html) and [ProgramPath](dcsAs400ProgramClassProgramPathProperty.html) properties.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public As400Program(
   AdgConnection Connection,
   string ProgramPath
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal Connection As [AdgConnection](dcsAdgConnectionClass.html) _
   ByVal ProgramPath As String _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegConstructor Acess(*Public)
   DclSrParm Connection Type(AdgConnection)
   DclSrParm ProgramPath Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Connection* 
          </span>
        </dt>
        <dd>An [AdgConnection](dcsAdgConnectionClass.html) object used to set the 
						value of the **Connection**  property. </dd>
        <dt>
 *ProgramPath* 
        </dt>
        <dd>A string used to set the value of the **ProgramPath**  property.</dd>
</dl>

Exceptions

[ASNA.DataGate.Common.dgException](dcsdgExceptionClass.html) is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
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

This constructor invokes the [ default constructor](dcsAs400ProgramClassAs400ProgramMethod1.html) and then sets property values using the given parameters. The value of the **Connection** property is set with the *Connection* parameter, and the value of the **ProgramPath** property is set with the *ProgramPath* parameter. The parameter list is initialized to length zero.

If *Connection* is set with a null value or is an **AdgConnection** instance that is unconnected or incompatible with **As400Program** , an exception is raised. Use [AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html) to open a connection to an IBM i database provider prior to setting **Connection** . The value of the *ProgramPath* parameter is not validated by this constructor.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Here, "ProdDB" is an initialized AdgConnection and
   * Call400 is a valid IBM i program file. */
  As400Program prog = new As400Program(ProdDB, "*Libl/Call400");</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Here, "ProdDB" is an initialized AdgConnection and
  ' Call400 is a valid IBM i program file.
  Dim prog As New As400Program(ProdDB, "*Libl/Call400");</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  /* Here, "ProdDB" is an initialized AdgConnection and
   * Call400 is a valid IBM i program file. */
  DclFld prog Type(As400Program)
  prog = *New As400Program(ProdDB, "*Libl/Call400")</pre>

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

