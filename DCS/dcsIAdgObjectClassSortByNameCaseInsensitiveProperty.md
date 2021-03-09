---
title: IAdgObject.SortByNameCaseInsensitive Property

Id: dcsIAdgObjectClassSortByNameCaseInsensitiveProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 16

keywords: SortByNameCaseInsensitive property
keywords: IAdgObject.SortByNameCaseInsensitive property
keywords: IComparer, returne instances for database object case insensitive string comparision
keywords: how to, return IComparer instances for case insensitive database object string comparision

---

**SortByNameCaseInsensitive** returns an **IComparer** instance suitable for comparing instances of [ IAdgObject](dcsIAdgObjectClass.html) based on the value returned by their [ ToString](dcsIAdgObjectClassToStringMethod.html) method. String comparison is conducted using **System.Collections.CaseInsensitiveComparer** .
<pre>        <span class="lang">[C#]</span>
 **Public interface IComparer SortByNameCaseInsensitive { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public interface ReadOnly Property SortByNameCaseInsensitive As IComparer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp SortByNameCaseInsensitive Access(*Public) Type(IComparer)
   BegGet** 
      </pre>

Property Value

**System.Collections.IComparer** . Each access of the property returns a new IComparer. 
Remarks

**SortByNameCaseInsensitive** returns an **IComparer** instance suitable for comparing instances of **IAdgObject** based on the value returned by their [ToString](dcsIAdgObjectClassToStringMethod.html) method. String comparison is conducted using a **System.Collections.CaseInsensitiveComparer** instance, created with its default constructor. Thus, the case-insensitive string comparison is based on the thread's culture settings.

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

