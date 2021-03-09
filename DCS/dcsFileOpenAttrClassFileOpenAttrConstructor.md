---
title: FileOpenAttr(string)

Id: dcsFileOpenAttrClassFileOpenAttrConstructor
TocParent: dcsFileOpenAttrConstructors
TocOrder: 0

---

Initialize the **FileOpenAttr** base class.
<pre class="prettyprint">       <span class="lang">[C#]</span>
 **Public FileOpenAttr();** 
      </pre>
            <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub New()**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)** 
      </pre>

Exceptions

None.
Remarks

The constructor of **FileOpenAttr** should not be called directly, since the class is abstract. Rather it must be called by a class that inherits and implements the abstract methods of the class.

Most applications should create **FileOpenAttr** instances via the [ FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) method. The **FileOpenAttr** object returned by this method is properly initialized for accessing a particular file. Alternately, DCS-aware development tools, such as Visual RPG, can create **FileOpenAttr** classes. These classes can be instantiated directly and used with access functions, such as [ FileAdapter.Open](dcsFileAdapterClassOpenMethod.html).
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileOpenAttr Class](dcsAdgDataSetClass.html)
      <br />
      [FileOpenAttr Class Members](dcsAdgDataSetMembers.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

