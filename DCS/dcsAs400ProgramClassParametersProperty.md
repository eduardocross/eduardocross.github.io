---
title: As400Program.Parameters Property

Id: dcsAs400ProgramClassParametersProperty
TocParent: dcsAs400ProgramPropertiesMain
TocOrder: 1

keywords: Parameters property
keywords: As400Program.Parameters property

keywords: program parameters, access to parameter list
keywords: parameter lists, access to program parameters
keywords: access parameter list of program parameters
keywords: parameters, program parameter list access
keywords: how to, access program parameter list

---

Contains the description and value of parameters as required by the called program.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public [ProgParm](dcsProgParmClass.html)[] Parameters { get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Parameters As [ProgParm](dcsProgParmClass.html) ()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Parameters Access(*Public) Type([ProgParm](dcsProgParmClass.html)) Rank(1)
   BegGet** 
      </pre>

Property Value

**ASNA.DataGate.DataLink.ProgParm** array. Read-Only copy of the array of **ProgParm** object references composing the parameter list of the program.
Remarks

The **Parameters** property allows access to the parameter list created with the [AppendParm](dcsAs400ProgramClassAppendParmMethod.html) method. The list is in the form of an array of **ProgParm** objects where the first element in the array corresponds to the first element in the parameter list. 

The array returned by this property is a copy of the array used by **As400Program** . However, the objects referenced by the array elements are the actual **ProgParm** objects used. The **Parameters** property is read-only; parameters may be added to the parameter list with the <span> **AppendParm** </span> method only.
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
      [AppendParm Method](dcsAs400ProgramClassAppendParmMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />
      [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html)

