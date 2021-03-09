---
title: IAdgObject.ToString Method

Id: dcsIAdgObjectClassToStringMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 9

keywords: ToString method
keywords: IAdgObject.ToString method
keywords: path names, return for database objects
keywords: database objects, return path names for

---

**ToString** returns the path name of the database object represented by [IAdgObject Class](dcsIAdgObjectClass.html).
<pre>        <span class="lang">[C#]</span>
 **Public string IAdgObject ToString(<br /> );** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Function ToString() As string** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ToString Access(*Public) Type(*String)** 
      </pre>

Returns

The path name of the database object represented by **IAdgObject** .
Exceptions

None.
Remarks

The path name of an object uniquely identifies it in a database hierarchy. The path name is given as a parameter to the factory methods of **IAdgObject** ([AdgFactory.NewDirectory](dcsAdgFactoryClassNewDirectoryMethod.html), [AdgFactory.NewFile](dcsAdgFactoryClassNewFileMethod.html), or [ AdgFactory.NewMember](dcsAdgFactoryClassNewMemberMethod.html)).

For **IAdgObject** instances created with the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) method, the path name is initialized as the concatenation of the path of the container object, and the object name given in the XML description of the object. The path name of **IAdgObject** cannot be otherwise initialized or changed.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [NewDirectory Method](dcsAdgFactoryClassNewDirectoryMethod.html)
      <br />
      [NewFile Method](dcsAdgFactoryClassNewFileMethod.html)
      <br />
      [NewMember Method](dcsAdgFactoryClassNewMemberMethod.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

