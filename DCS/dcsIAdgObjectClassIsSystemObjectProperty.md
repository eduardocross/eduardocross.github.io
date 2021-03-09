---
title: IAdgObject.IsSystemObject Property

Id: dcsIAdgObjectClassIsSystemObjectProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 8

keywords: IsSystemObject property
keywords: IAdgObject.IsSystemObject property
keywords: how to, identify system objects
keywords: system objects, identify

---

**IsSystemObject** indicates if the existing database object represented by **IAdgObject** is a "system" object, when **IAdgObject** is obtained through [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html).
<pre>        <span>[C#]</span>
 **Public bool IsSystemObject { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property IsSystemObject As boolean** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp IsSystemObject Access(*Public) Type(*Boolean)
   BegGet** 
      </pre>

Property Value <p> **Boolean** . ReadOnly. **True** if the database provider designates the object as a system object. 
Exceptions

None
Remarks

A database provider may designate some objects as "system" objects. In the current version of DCS, this designation is only reflected by **IsSystemObject** when the **IAdgObject** reference is obtained through the **IDirectory.Enumerate** method. The value of **IsSystemObject** in **IAdgObject** instances constructed in any other way is always **False** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IAdgObject Class Members](dcsIAdgObjectMembers.html)
      <br />
      [IDirectory.Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

