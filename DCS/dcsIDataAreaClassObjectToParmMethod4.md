---
title: IDataArea.ObjectToParm(System.Type, string, integer[])

Id: dcsIDataAreaClassObjectToParmMethod4

---

Converts an object to a data area value provided with the parameter type, value, and the indices in the path to the parameter.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public object ObjectToParm(
   Object Value,
   string ParameterName,
   int[] ElementIndices
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ObjectToParm(_ 
   ByVal Value As Object_
   ByVal ParameterName As String_
   ByVal ElementIndices[] As Integer
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ObjectToParm Access(*Public) Type(Object)
   DclSrParm Value Type(Object)
   DclSrParm ParameterName Type(*String)
   DclSrParm ElementIndices Type(*Integer) Rank(1)** 
      </pre>

Parameters

<dl>
        <dt>
 *Value* 
        </dt>
        <dt />
        <dd>	Object.  The object to be converted. </dd>
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

