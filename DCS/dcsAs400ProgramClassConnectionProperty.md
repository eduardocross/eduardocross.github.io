---
title: As400Program.Connection Property

Id: dcsAs400ProgramClassConnectionProperty
TocParent: dcsAs400ProgramPropertiesMain
TocOrder: 0

keywords: Connection property
keywords: As400Program.Connection property

keywords: database connections, hosting AdgConnection specified
keywords: database servers, hosting connection specified
keywords: how to, specify database host connection for program

---

The **AdgConnection** object of the database server hosting the program to be called. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public [AdgConnection](dcsAdgConnectionClass.html) Connection { set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public WriteOnly Property Connection As [AdgConnection](dcsAdgConnectionClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Connection Access(*Public) Type([AdgConnection](dcsAdgConnectionClass.html))
   BegSet** 
      </pre>

Property Value

[AdgConnection](dcsAdgConnectionClass.html). Set-Only. Represents the connection to the database server hosting the program.
Exceptions

[ASNA.DataGate.Common.dgException](dcsdgExceptionClass.html) is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
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

The reference being assigned to **Connection** is null, or is an **AdgConnection** object whose [ State](dcsAdgConnectionClassStateProperty.html) property is not equal to System.Data.ConnectionState.Open (see Remarks).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVSQLOP
</td>
            <td colspan="1" rowspan="1">

The value of **Connection** is not a valid connection for use with As400Program.
</td>
          </tr>
</table>

Remarks

To run the program on a particular database server, set the **Connection** property with an [AdgConnection](dcsAdgConnectionClass.html) object containing an open connection to the machine. If **As400Program** was instantiated with the [default constructor](dcsAs400ProgramClassAs400ProgramMethod1.html) (no parameters), this property must be set before adding program parameters or calling the [AdgConnection.Open](dcsAs400ProgramClassExecuteMethod.htm ">Execute</a> method.

**Connection** is a set-only property. If **Connection** is set with a null value or is an **AdgConnection** instance that is unconnected or incompatible with **As400Program** , an exception is raised. Use <a href="dcsAdgConnectionClassOpenMethod.html) to open a connection to an IBM i database provider prior to setting **Connection.** 
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  As400Program prog = new As400Program();
  prog.Connection = new AdgConnection("*Public/DG NET IBM i");
  prog.ProgramPath = "*Libl/Call400";</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim prog As New As400Program()
  prog.Connection = New AdgConnection("*Public/DG NET IBM i")
  prog.ProgramPath = "*Libl/Call400"</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  DclFld prog Type(As400Program) New()
  prog.Connection = *New AdgConnection("*Public/DG NET IBM i")
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
      [AdgConnection Class](dcsAs400ProgramClassExecuteMethod.htm ">Execute Method</a>
      <br />
      <a href="dcsAdgConnectionClass.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

