---
title: As400Program.GetParmByName Method

Id: dcsAs400ProgramClassGetParmByNameMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 4

keywords: GetParmByName method
keywords: As400Program.GetParmByName method
keywords: parameter lists, retrieve parameter named
keywords: program parameters, retrieve parameter named
keywords: retrieve parameter from program parameter list by name
keywords: parameters, retrieve from parameter list by name
keywords: how to, retrieve parameters from program parameter list by name

---

Returns the [ProgParm](dcsProgParmClass.html) object in the parameter list named by string.
<pre>        <span class="lang">[C#]</span>
 **protected [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) GetParmByName(
   string name
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Protected Function GetParmByName( _
   ByVal name As String _
) As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetParmByName Access(*Protected) Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))
   DclSrParm name Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
          <span style="FONT-STYLE: italic">name</span>
        </dt>
        <dd>String identifying a **ASNA.DataGate.DataLink.ProgParm**  object in 
						the parameter list.
					</dd>
</dl>

Return Value

A **ProgParm** object in the **As400Program** parameter list with *name* or null if no object is found.
Remarks

<span> **ProgParm** </span> objects can optionally be identified with a string in the constructor of [ StructureType](dcsStructureTypeClass.html) and [ ProgParmType](dcsProgParmTypeClassProgParmTypeConstructor.html). When added to **As400Program** with [ AppendParm](dcsAs400ProgramClassAppendParmMethod.html) or [AppendParms](dcsAs400ProgramClassAppendParmsMethod.html), the *name* uniquely identifies the parameter in the list. <span> **GetParmByName** </span> allows retrieval of a parameter in the **As400Program** parameter list by its *name* . 

If no parameter with the given *name* exists in the parameter list, <span> **GetParmByName** </span> returns a null value. <span> **GetParmByName** </span> does not remove the parameter from the parameter list.
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
      [AppendParms Method](dcsAs400ProgramClassAppendParmsMethod.html)
      <br />
      [ProgParm Class](dcsProgParmClass.html)
      <br />
      [ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [ProgParmType Class 
					Constructor](dcsProgParmTypeClassProgParmTypeConstructor.html)
      <br />
      [StructureType Class](dcsStructureTypeClass.html)
      <br />
      [StructureType Class 
					Constructor](dcsStructureTypeClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

