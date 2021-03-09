---
title: IAdgObject.DateReferenced Property

Id: dcsIAdgObjectClassDateReferencedProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 6

keywords: DateReferenced property
keywords: IAdgObject.DateReferenced property
keywords: how to, return object last referenced timestamp recorded by database provider
keywords: timestamps, recorded by database provider when object was last referenced
keywords: database objects, return database providers last referenced timestamp

---

**DateReferenced** is a timestamp recorded by the database provider when the database object is referenced.
<pre>        <span class="lang">[C#]</span>
 **Public System.DateTime DateReferenced { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DateReferenced As System.DateTime** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DateReferenced Access(*Public) Type(System.DateTime)
   BegGet** 
      </pre>

Property Value <p> **System.DateTime** . Read only. If **IAdgObject** was obtained via [IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html), the time the object was most recently referenced. 
Remarks

Database providers record a timestamp of when a database object was most recently referenced by any session. In the current version of DCS, this timestamp is only reflected by **DateReferenced** when **IAdgObject** is obtained through the **IDirectory.Enumerate** method. The value of **DateReferenced** in instances constructed in any other way is **DateTime.Min** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IDirectory.Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

