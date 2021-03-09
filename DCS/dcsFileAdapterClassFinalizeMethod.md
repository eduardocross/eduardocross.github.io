---
title: FileAdapter.Finalize Method

Id: dcsFileAdapterClassFinalizeMethod
TocParent: dcsFileAdapterMethods
TocOrder: 10

keywords: how to, release managed resources
keywords: release managed resources
keywords: resources, release managed
keywords: managed resources, release
keywords: FileAdapter.Finalize method
keywords: Finalize method,

---

Releases managed resources and performs other cleanup operations.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **protected override void Finalize();** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Overrides Sub Finalize()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Finalize Access(*Public) Modifier(*Overrides)**    </pre>

Exceptions

None. 
Remarks

The garbage collector calls <code> **Finalize** </code> when the current object is ready to be finalized. Note that **Finalize** does not "close" the **FileAdapter** . If the <span> **FileAdapter** </span> represents an open database file, its [Close](dcsFileAdapterClassCloseMethod.html) or [Dispose](dcsFileAdapterClassDisposeMethod.html) method should be called prior to finalization, or database provider resources may not be properly released.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

[FileAdapter Class](dcsFileAdapterClass.html) <br /> [ FileAdapter Class Members](dcsFileAdapterMembers.html) <br /> [Close Method](dcsFileAdapterClassCloseMethod.html) <span><br /> [Dispose Method](dcsFileAdapterClassDisposeMethod.html) <br /> </span> <span>[ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)</span>
