---
title: IDataArea.AppendParm Method

Id: dcsIDataAreaClassAppendParmMethod

keywords: AppendParm method
keywords: IDataArea.AppendParm method
keywords: program parameters, append parameter to
keywords: parameter lists, append parameter to
keywords: append parameter to program parameter list
keywords: parameters, append program parameter list
keywords: how to, append parameter to program parameter list

---

Appends a parameter to the parameter list for the program.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public void AppendParm(
   [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) Parameter
);** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public Sub AppendParm( _
   ByVal Parameter As [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html) _
)** 
      </pre>
      <pre class="prettyPrint">
        <span class="lang">[Visual RPG]</span>
 **BegSr AppendParm Acess(*Public)
   DclSrParm Parameter Type([ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html))** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *Parameter* 
          </span>
        </dt>
        <dd><span />
          <span>  <font>An instance of **ASNA.DataGate.DataLink.ProgParm**  class that represents the program parameter to append. </span>  </dd>
</dl>

See Also

[IDataArea Class](dcsIDataAreaClass.html) <br /> [IDataArea Class Members](dcsIDataAreaMembers.html) <br /> [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html) <br /> [ASNA.DataGate.DataLink.ProgParm Class](dcsProgParmClass.html) <br /> 
