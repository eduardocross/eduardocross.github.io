---
title: IAdgObject.DateCreated Property

Id: dcsIAdgObjectClassDateCreatedProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 4

keywords: DateCreated property
keywords: IAdgObject.DateCreated property
keywords: how to, return object creation timestamp recorded by database provider
keywords: timestamps, recorded by database provider when object was created
keywords: database objects, return database providers creation timestamp

---

**DateCreated** is a timestamp recorded by the database provider when the database object is created.
<pre>        <span class="lang">[C#]</span>
 **Public System.DateTime DateCreated { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DateCreated As System.DateTime** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DateCreated Access(*Public) Type(System.DateTime)
   BegGet** 
      </pre>

Property Value

**System.DateTime** . ReadOnly. If **IAdgObject** was obtained via [IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html) the time the object was created. 
Remarks

Database providers record a timestamp of when a database object is created. In the current version of DCS, this timestamp is only reflected by **DateCreated** when **IAdgObject** is obtained through the **IDirectory.Enumerate** method. The value of **DateCreated** in instances constructed in any other way is **DateTime.Min** .
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

