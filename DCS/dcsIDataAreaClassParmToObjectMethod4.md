---
title: IDataArea.ParmToObject(System.Type, string, integer[])

Id: dcsIDataAreaClassParmToObjectMethod4

---

Returns an object of a specific type from the program parameter list provided with the type of the object returned by the method, the name or path of the program parameter object in the parameter list, and the indices in the path to the parameter.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public object ParmToObject(
   System.Type ReturnType,
   string ParameterName,
   int[] ElementIndices
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ParmToObject(_ 
   ByVal ReturnType As System.Type_
   ByVal ParameterName As String_
   ByVal ElementIndices[] As Integer
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ParmToObject Access(*Public) Type(Object)
   DclSrParm ReturnType Type(Type)
   DclSrParm ParameterName Type(*String)
   DclSrParm ElementIndices Type(*Integer) Rank(1)** 
      </pre>

Parameters

<dl>
        <dt>
 *ReturnType* 
        </dt>
        <dt />
        <dd>	System.Type.  The requested type of the object returned by the method. </dd>
        <dt>
 *ParameterName* 
        </dt>
        <dd>			The name or path of the program data area. </dd>
        <dt>
 *ElementIndices* 
        </dt>
        <dd>					Integer. For paths including multiple-occurrence parameters, the indices in the 
											path to the data area. </dd>
</dl>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDataArea Class](dcsIDataAreaClass.html)
      <br />
      [IDataArea Class Members](dcsIDataAreaMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

