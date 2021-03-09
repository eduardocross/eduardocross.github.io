---
title: AdgDataSet.ActiveRow Property

Id: dcsAdgDataSetClassActiveRowProperty
TocParent: dcsAdgDataSetProperties
TocOrder: 0

keywords: AdgDataSet.ActiveRow property
keywords: ActiveRow property
keywords: active row, of AdgDataSet
keywords: rows, currently active
keywords: how to, establish active row
keywords: tables, active row

---

The **DataRow** object currently established as the active row.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public  ActiveRow{ get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ActiveRow() As** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp ActiveRow Access(*Public) Type()
   BegGet** 
      </pre>

Property
 Value

**System.Data.DataRow** . The active row of the **AdgDataSet** . 
Remarks

The active row is used in several [FileAdapter](dcsFileAdapterClass.html) access methods as the record upon which an access operation is performed. **FileAdapter** read methods create a new **DataRow** to contain the record read, append the row to the **AdgDataSet** , and set it as the value of **ActiveRow** . Other **FileAdapter** methods, such as [AddRecord](dcsFileAdapterClassAddRecordMethod.html) and [ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html) use the record contained in ActiveRow to update the database file.

Though <span> **ActiveRow** </span> is a read-only property, [SetActiveRecord](dcsAdgDataSetClassSetActiveMethods.html) can be used to explicitly set a particular DataRow in the **AdgDataSet** as the value of <span> **ActiveRow** </span>. The [DeleteRow](dcsAdgDataSetClassDeleteRowMethod.html) method sets the value of **ActiveRow** to null.

Upon construction of **AdgDataSet** , the **ActiveRow** property has no value. Its value is set by <span> **FileAdapter** </span> and **AdgDataSet** methods, as explained above. An exception is thrown if <span> **ActiveRow** </span> is accessed before it has a value.
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
      [SetActiveRecord Method](dcsAdgDataSetClassSetActiveMethods.html)
      <br />
      [DeleteRow Method](dcsAdgDataSetClassDeleteRowMethod.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [AddRecord Method](dcsFileAdapterClassAddRecordMethod.html)
      <br />
      [ChangeCurrent Method](dcsFileAdapterClassChangeCurrentMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />

