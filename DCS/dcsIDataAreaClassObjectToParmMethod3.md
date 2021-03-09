---
title: IDataArea.ObjectToParm(System.Type, string)

Id: dcsIDataAreaClassObjectToParmMethod3

---

Converts an object to a data area value provided with the parameter type and value.
<pre>        <span class="lang">[C#]</span>
 **Public object ObjectToParm(
   Object Value,
   string ParameterName,
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Function ObjectToParm( _
   ByVal Value As Object, _
   ByVal ParameterName As String, _
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ObjectToParm Access(*Public) Type(Object)
   DclSrParm Value Type(Object)
   DclSrParm ParameterName Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *Value* 
        </dt>
        <dd>Object.  The object to be converted. </dd>
        <dt>
 *ParameterName* 
        </dt>
        <dd>		The name or path of the program data area.</dd>
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

