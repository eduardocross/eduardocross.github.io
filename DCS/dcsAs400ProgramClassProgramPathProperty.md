---
title: As400Program.ProgramPath Method

Id: dcsAs400ProgramClassProgramPathProperty
TocParent: dcsAs400ProgramPropertiesMain
TocOrder: 2

keywords: ProgramPath property
keywords: As400Program.ProgramPath property

keywords: database connections, program path specified
keywords: how to, set program path

---

A string describing the path to the called program on the database server.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string ProgramPath { set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public WriteOnly Property ProgramPath As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ProgramPath Access(*Public) Type(*String)
   BegSet** 
      </pre>

Property Value

String. Set Only. The path to the program called on the database server. 
Remarks

Set the <span> **ProgramPath** </span> property to name the program on the database server to be called by **As400Program** . Unless <span> **As400Program** </span> was created using the constructor defining a string parameter, this property <span>must</span> be set before adding program parameters or calling the [ASNA.DataGate.Client](dcsAs400ProgramClassExecuteMethod.htm "> Execute</a> method. 

<span> **ProgramPath** </span> is a set-only property. The value of the string assigned to the property is not validated by DCS.
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

**Namespace:** <a href="dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [As400Program Class Members](dcsAs400ProgramMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsAs400ProgramClassExecuteMethod.htm ">Execute Method</a>
      <br />
      <a href="dcsDataGateClientNamespace.html)

