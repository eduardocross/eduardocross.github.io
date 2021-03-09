---
title: Dependent.PathName Property

Id: dcsDependentClassPathNameProperty
TocParent: dcsDependentProperties
TocOrder: 2

keywords: Dependent.PathName property
keywords: PathName property
keywords: dependent objects, return full path name
keywords: path names, return location of dependent objects
keywords: how to, return full path name of dependent objects

---

**PathName** is the full path name of the dependent database object. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string PathName{ get;}** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property PathName As String<br />** </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp PathName Access(*Public) Type(*String)
   BegGet** 
      </pre>

Property Value

**String** . Read-Only. The full path name of the dependent database object. 
Remarks

The path name of the dependent database object specifies its location in the database.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />
      [Dependent Class](dcsDependentClass.html)
      <br />
      [Dependent Members](dcsDependentMembers.html)

