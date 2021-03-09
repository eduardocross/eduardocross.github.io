---
title: IDataArea.ObjectToParm(ASNA.DataGate.DataLink.ProgParm, System.Type)

Id: dcsIDataAreaClassObjectToParmMethod1

---

Converts an object to a parameter list value provided with the parameter value and type.
<pre>        <span class="lang">[C#]</span>
 **Public object ObjectToParm(
   [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) Parameter,
   object Value
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Function ObjectToParm(_ 
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) _
   ByVal Value As Object
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ObjectToParm Access(*Public) Type(Object)
   DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))
   DclSrParm Value Type(Object)** 
      </pre>

Parameters

<dl>
        <dt>
 *Parameter* 
        </dt>
        <dd>[ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html).  
						The program parameter object in the parameter list to get the value of.</dd>
        <dt>
 *Value* 
        </dt>
        <dd>			Object.  The object to be converted.</dd>
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

