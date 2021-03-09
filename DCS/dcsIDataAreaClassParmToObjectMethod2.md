---
title: IDataArea.ParmToObject(ASNA.DataGate.DataLink.ProgParm, System.Type, integer)

Id: dcsIDataAreaClassParmToObjectMethod2

---

Returns an object of a specific type from the program parameter list provided with the program parameter object in the parameter list to get the value of, the type of the object returned by the method, and a zero-relative index identifying the element of the array to get the value of.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public object ParmToObject(
   [ASNA.DataGate.Client](DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a> Parameter,
   System.Type ReturnType,
   int Element
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function ParmToObject(_ 
   ByVal Parameter As <a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a> _
   ByVal ReturnType As System.Type_
   ByVal Element As Integer
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ParmToObject Access(*Public) Type(Object)
   DclSrParm Parameter Type(<a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a>)
   DclSrParm ReturnType Type(System.Type)
   DclSrParm Element Type(*Integer)** 
      </pre>

Parameters

<dl>
        <dt>
 *Parameter* 
        </dt>
        <dd><a href="DCS160-F1071E27-0001DD">ASNA.DataGate.DataLink.ProgParm</a>.  
						The program parameter object in the parameter list to get the value of.</dd>
        <dt>
 *ReturnType* 
        </dt>
        <dt />
        <dd>			System.Type.  The requested type of the object returned by the method. </dd>
        <dt>
 *Element* 
        </dt>
        <dd>					Integer. For paths including multiple-occurrence parameters, a zero-relative 
											index identifying the element of the array to get the value of. </dd>
</dl>

Requirements

**Namespace:** <a href="dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDataArea Class](dcsIDataAreaClass.html)
      <br />
      [IDataArea Class Members](dcsIDataAreaMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

