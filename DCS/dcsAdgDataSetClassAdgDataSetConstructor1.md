---
title: AdgDataSet(String)

Id: dcsAdgDataSetClassAdgDataSetConstructor1
TocParent: dcsAdgDataSetClassConstructorsMain
TocOrder: 1

---

Initialize the <span> **AdgDataSet** </span> base class.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AdgDataSet(
   string name
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal name As String _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)
   DclSrParm name Type(*String)** 
      </pre>
      <span/>

Parameters

<dl>
        <dt>
 *name* 
        </dt>
        <dd>	The name of the new DataSet object.  This parameter initializes the
							 property.</dd>
</dl>

Exceptions

None.
Remarks

The constructor of **AdgDataSet** should not be called directly, since the class is abstract. Rather it must be called by a class that inherits and implements the abstract methods of the class.

Most applications should create **AdgDataSet** instances via the [ FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) method. The **AdgDataSet** object returned by this method is properly initialized for accessing a particular file. Alternately, DCS-aware development tools, such as Visual RPG, can create **AdgDataSet** classes. These classes can be instantiated directly and used with access functions, such as [FileAdapter.Open.](dcsFileAdapterClassOpenMethod.html)
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />

