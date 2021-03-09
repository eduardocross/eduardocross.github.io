---
title: IAdgObject Class

Id: dcsIAdgObjectClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 9

keywords: IAdgObject class
keywords: interfaces [DCS 16.0 base IAdgObject class
keywords: classes [DCS 16.0 IAdgObject class
keywords: IAdgObject class, about IAdgObject class
keywords: database objects, about database files
keywords: database files, about database objects

---

**IAdgObject** is the base interface implemented by all DataGate Component Suite (DCS) class objects modeling database objects. The leaf interfaces of these classes are [IDirectory](dcsIDirectoryClass.html), [IFileObject](dcsIFileObjectClass.html), and [ IMember](dcsIMemberClass.html). Each of these inherits the methods and properties of **IAdgObject** , so that an instance of **IDirectory** , **IFileObject** , or **IMember** is also an instance of **IAdgObject** .

Note that methods which iterate **IAdgObject** instances (such as [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html)), are actually returning references to objects that implement **IDirectory** , **IFileObject** , or **IMember** . The underlying type of an **IAdgObject** instance can be determined with the [ AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property. 

For a list of all members of this type, see [IAdgObject Members](dcsIAdgObjectMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

ASNA.DataGate.Client.IAdgObject
<pre>&lt;Serializable&gt; **Public interface IAdgObject** </pre>

Thread Safety

Implementations of **IAdgObject** are safe for multithreaded operations.
Remarks

When a DCS method or property returns an instance of **IAdgObject** , the instance returned is also an instance of **IDirectory** , **IFileObject** , or **IMember** . The programmer may operate on the instance through the methods of **IAdgObject** , or may use the methods of the underlying implementation, by assigning the returned instance to the proper object variable. The [AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property of **IAdgObject** is used to determine if the underlying implementation is **IDirectory** , **IFileObject** , or **IMember** .

The properties and methods provided by **IAdgObject** represent database object management functionality common to all database objects, such as names, locations, security, allocation, and definition. Included are methods for creating, renaming, moving, duplicating, and deleting database objects. Basically, **IAdgObject** and its inheritors are useful for performing the following tasks:

1. *Accessing* 
				the metadata of existing database objects.
2. *Modifying* 
				certain operational attributes of existing database objects.
3. *Defining*  and *creating*  new database objects.

**IAdgObject** instances are created either directly, via the methods of [AdgFactory](dcsAdgFactoryClass.html) ([NewFile](dcsAdgFactoryClassNewFileMethod.html), [NewDirectory](dcsAdgFactoryClassNewDirectoryMethod.html), [ NewMember](dcsAdgFactoryClassNewMemberMethod.html), [ReadXml](dcsAdgFactoryClassReadXmlMethods.html)) or from the methods of other **IAdgObject** instances representing database "container" objects ( **IDirectory.Enumerate** , [ IFileObject.Members](dcsIFileObjectClassMembersProperty.html)).

Generally, property values representing the metadata of an existing database object are provided on-demand and are cached. That is, DCS will query the database provider for the value of the property only once in the lifetime of the **IAdgObject** instance, and return the same value each time the property value is read. New or changed metadata can be accessed by obtaining a new instance of **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Members](dcsIAdgObjectMembers.html)
      <br />
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [Enumerate Method ](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [Members Property](dcsIFileObjectClassMembersProperty.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [NewFile Method](dcsAdgFactoryClassNewFileMethod.html)
      <br />
      [NewDirectory Method](dcsAdgFactoryClassNewDirectoryMethod.html)
      <br />
      [NewMember Method](dcsAdgFactoryClassNewMemberMethod.html) 
				<br />[ReadXml Method](dcsAdgFactoryClassReadXmlMethods.html)<br />
				[ASNA DataGate Client Namespace](dcsDataGateClientNamespace.html)

