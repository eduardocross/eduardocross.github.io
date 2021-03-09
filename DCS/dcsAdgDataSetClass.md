---
title: AdgDataSet Class

Id: dcsAdgDataSetClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 1

keywords: classes [DCS 16.0 AdgDataSet class
keywords: AdgDataSet class
keywords: accessing a file, about AdgDataSet
keywords: AdgDataSet class, about AdgDataSet class

---

A DataGate-compatible DataSet class for record-oriented database access.

For a list of all members of this type, see [AdgDataSet Members](dcsAdgDataSetMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> **ASNA.DataGate.Client.<span>AdgDataSet</span>** 
<pre class="syntax" />

[Visual Basic] **Public MustInherit Class AdgDataSet Inherits System.Data.DataSet** 
Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

<span> **AdgDataSet** </span> is a subclass of the class. <span>System.Data.DataSet</span> is used widely throughout the .NET Framework. When used in tandem with [FileAdapter](dcsFileAdapterClass.html) **AdgDataSet** features methods to facilitate record-oriented access, while maintaining all of the integration and set-oriented features of System.Data.DataSet. 

**AdgDataSet** objects are specialized instances of System.Data. DataSet, distinguished by the composition of the data tables they contain. The **Tables** property of System.Data.DataSet is a collection of objects. In **AdgDataSet** objects, the tables referred to by the Tables property represent the formats of a DataGate file. Each table in a System.Data.DataSet contains a **Rows** collection of objects. System.Data.DataRow objects are used to model records in DCS. Records are composed of fields, and in System.Data.DataRow, field data is accessed with it's **Item** and **ItemArray** properties. Some field meta-data, or type information, is available from the **Columns** property of System.Data.DataTable.

Generally, applications need not access the System.Data.DataTable objects in **AdgDataSet** via the Tables property, etc. Rather, **AdgDataSet** provides several methods and properties for accessing particular rows of a table, such as [ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) property and [PrepareRow](dcsAdgDataSetClassPrepareRowMethodMain.html), [AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html), [AddRow](dcsAdgDataSetClassAddRowMethods.html), [InsertRow](dcsAdgDataSetClassInsertRowMethods.html), [SetActive](dcsAdgDataSetClassSetActiveMethods.html), and [DeleteRow](dcsAdgDataSetClassDeleteRowMethod.html) methods. 

Other methods and properties, such as [Formats](dcsAdgDataSetClassFormatsProperty.html), [FormatIDs](dcsAdgDataSetClassFormatIDsProperty.html), [GetFormatIndex](dcsAdgDataSetClassGetFormatIndexMethod.html), [GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html), [CurrentFormatIndex](dcsAdgDataSetClassGetFormatIndexMethod.html), and [CurrentFormatName](dcsAdgDataSetClassCurrentFormatNameProperty.html), provide information about the formats of the file modeled by **AdgDataSet** . When a format modeled by **AdgDataSet** contains a key, [NewKeyTable](dcsAdgDataSetClassNewKeyTableMethods.html) provides a method to construct a key buffer for keyed access methods.

**AdgDataSet** is an "abstract" base class, not intended for direct instantiation (<span>MustInherit in VB). **AdgDataSet** instances are returned by [FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) or by instantiating another class that inherits **AdgDataSet.** For most applications, it is sufficient to use **<code>OpenNewAdgDataSet</code>** to create the **AdgDataSet** instance, since this method creates table structures in the **AdgDataSet** to match the formats of the file to be accessed.</span>

It is generally not recommended to compose your own class to inherit **AdgDataSet** . Such a class could be directly instantiated, however. Alternately, an **AdgDataSet** sub-class created with a DCS-aware development tool, such as Visual RPG, can be directly instantiated for use with access functions like [FileAdapter.Open](dcsFileAdapterClassOpenMethod.html).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
							  [AdgDataSet Members](dcsAdgDataSetMembers.html)
							  <br />
							  [FileAdapter.OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
							  <br />
							  [AdgKeyTable Class](dcsAdgKeyTableClass.html)
							  <br />
							  [ASNA DataGate Client Namespace](dcsDataGateClientNamespace.html)
							  <br /><br />
							  <br />

