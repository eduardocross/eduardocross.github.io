---
title: IAdgObject.SortByName Property

Id: dcsIAdgObjectClassSortByNameProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 15

keywords: SortByName property
keywords: IAdgObject.SortByName property
keywords: IComparer, return instances for database object case sensitive string comparision
keywords: how to, return IComparer instances for case sensitive database object string comparision

---

**SortByName** returns an **IComparer** instance suitable for comparing instances of [IAdgObject](dcsIAdgObjectClass.html) based on the value returned by their [ToString](dcsIAdgObjectClassToStringMethod.html) method. String comparison is conducted using **System.Collections.Comparer.Default** .
<pre>        <span class="lang">[C#]</span>
 **Public interface IComparer SortByName { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public interface ReadOnly Property SortByName As IComparer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp SortByName Access(*Public) Type(IComparer)
   BegGet** 
      </pre>

Property Value

**System.Collections.IComparer** . Each access of the property returns a new **IComparer** .
Remarks

**SortByName** returns an **IComparer** instance suitable for comparing instances of **IAdgObject** based on the value returned by their [ToString](dcsIAdgObjectClassToStringMethod.html) method. String comparison is conducted using **System.Collections.Comparer.Default** . Thus, the string comparison is based on the thread's culture settings for character casing, etc.

The property always returns a new instance of IComparer.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ToString Method](dcsIAdgObjectClassToStringMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

