---
title: IFileObject Interface

Id: dcsIFileObjectClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 12

keywords: classes [DCS 16.0 IFileObject class
keywords: interfaces [DCS 16.0 IFileObject interface
keywords: IFileObject class
keywords: IFileObject class, about IFileObject class
keywords: database files, about file objects

---

<span> **IFileObject** </span> models an object management interface to the database file object. 

For a list of all members of this type, see [IFileObject Members](dcsIFileObjectMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

ASNA.DataGate.Client.IAdgObject<br /> **ASNA.DataGate.Client.<span>IFileObject</span>** 
<pre class="prettyprint">
[Prototype in C#] public interface IFileObject | Inherits IAdgObject</pre>
      <pre class="prettyprint"> [Prototype in AVR] BegInterface IFileObject access(public) implements(IAdgObject)</pre>

Thread Safety

In DCS implementations of **IFileObject** , instance members are not guaranteed to be thread safe.
Remarks

The **IFileObject** class models the file object of the database server. In addition to the generic methods and properties of [ IAdgObject](dcsIAdgObjectClass.html) the **IFileObject** class provides methods specific to file objects. 

A valid **IFileObject** reference may be obtained from DCS in one of the following ways:

- The [AdgFactory.NewFile](dcsAdgFactoryClassNewFileMethod.html) method instantiates a new instance of **IFileObject** given a path name and [AdgConnection](dcsAdgConnectionClass.html) reference. Such an instance is suitable for creating a new file object (via [ IAdgObject.Create](dcsIAdgObjectClassCreateMethod.html)), or for access to the attributes of an existing file.
- An instance of **IFileObject** representing an existing database file may be returned when using the [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html) method.
- An instance of **IFileObject** representing an existing database file may be obtained as a member of the array value of the [ IDirectory.ItemList](dcsIDirectoryClassItemListProperty.html) property.
- An **IFileObject** instance may be returned from the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) method (as an **IAdgObject** reference) when the XML definition describes a database file.
- [IFileObject.Copy](dcsIFileObjectClassCopyMethod.html) returns an instance of **IFileObject** corresponding to the new duplicate file.

**Copy** allows the file corresponding to **IFileObject** to be copied to a target library and with a new name. [ MemberCount](dcsIFileObjectClassMemberCountProperty.html) property returns the non-negative number of member objects contained by the file. This number is equal to the length of the array value of the [Members](dcsIFileObjectClassMembersProperty.html) property, which is a list of the members rendered as [IMember](dcsIMemberClass.html) instances.

[ReadDefinition](dcsIFileObjectClassReadDefinitionMethod.html), [ WriteDefinition](dcsIFileObjectClassWriteDefinitionMethod.html), [ ReadCreationAttributes](dcsIFileObjectClassReadCreationAttributesMethod.html), and [ WriteCreationAttributes](dcsIFileObjectClassWriteCreationAttributesMethod.html) provide the means to express database file definitions as XML documents.

The diagnostic test and repair facilities of certain database providers are accessible with the [RepairFile](dcsIFileObjectClassRepairFileMethod.html) method.

The value of [AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) for **IFileObject** instances is always **File** . The value of [AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html) can be used to determine the classification of the file, e.g. logical, physical, etc. [Bases](dcsIAdgObjectClassBasesProperty.html) is always an empty collection for physical files. [Dependents](dcsIAdgObjectClassDependentsProperty.html) may be non-empty only for physical files.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IFileObject Members](dcsIFileObjectMembers.html)
      <br />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [NewFile Method](dcsAdgFactoryClassNewFileMethod.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [ItemList Property](dcsIDirectoryClassItemListProperty.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [Dependents Property](dcsIAdgObjectClassDependentsProperty.html)
      <br />
      [Bases Property](dcsIAdgObjectClassBasesProperty.html)
      <br />
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [AdgSubType Property](dcsIAdgObjectClassAdgSubTypeProperty.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

