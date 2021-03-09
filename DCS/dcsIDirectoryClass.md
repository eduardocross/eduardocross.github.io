---
title: IDirectory Interface

Id: dcsIDirectoryClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 11

keywords: classes [DCS 16.0 IDirectory class
keywords: interfaces [DCS 16.0 IDirectory class
keywords: IDirectory class
keywords: IDirectory class, about IDirectory class
keywords: database files, about libraries
keywords: database libraries, about IDirectory class

---

**IDirectory** models an object management interface to the database library object. 

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

ASNA.DataGate.Client.IAdgObject<br /> **ASNA.DataGate.Client.<span>IDirectory</span>** 
<pre class="prettyprint">
        <span class="lang">[Prototype in C#]<br /></span>                                <span> public interface IDirectory | Inherits IAdgObject</span>
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Prototype in Visual RPG for VS 2008]<br /></span>                                <span> BegInterface IDirectory access (*public) implements (IAdgObject)</span>
      </pre>

Thread Safety

In DCS implementations of **IDirectory** , instance members are not guaranteed to be thread safe.
Remarks

The **IDirectory** class models the library object of the database server. In addition to the generic object management methods and properties of [IAdgObject](dcsIAdgObjectClass.html) the **IDirectory** class provides additional functions specific to library objects.

A valid **IDirectory** reference may be obtained from DCS in one of the following ways:

- The [AdgFactory.NewDirectory](dcsAdgFactoryClassNewDirectoryMethod.html) method instantiates a new instance of **IDirectory** given a path name and [AdgConnection](dcsAdgConnectionClass.html) reference. Such an instance is suitable for creating a new library object (via [ IAdgObject.Create](dcsIAdgObjectClassCreateMethod.html)) or for managing the attributes of an existing library.
- An instance of **IDirectory** representing an existing database library may be returned when using the [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html) method.
- An instance of **IDirectory** representing an existing database library may be obtained as a member of the array value of the [ IDirectory.ItemList](dcsIDirectoryClassItemListProperty.html) property.
- An **IDirectory** instance may be returned from the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) method (as an **IAdgObject** reference), when the XML definition describes a database library.
- The [IDirectory.CreateSubDirectory](dcsIDirectoryClassCreateSubDirectoryMethod.html) method, if successful, returns an instance of **IDirectory** representing the library it created.

**CreateSubDirectory** creates a library within an existing library. **ItemList** is an array of zero or more **IAdgObject** references ( **IDirectory** and [IFileObject](dcsIFileObjectClass.html) instances) representing the sub-libraries and files which may be contained by the database server library. Similarly, **Enumerate** calls the provided [AdgEnumerator](dcsAdgEnumeratorDelegate.html) delegate for each file and library in the library.

The [AttachRemoteDirectory](dcsIDirectoryClassAttachRemoteDirectoryMethod.html) method with the [RemotePathName](dcsIDirectoryClassRemotePathNameProperty.html) property is used to attach an existing directory to an object. The [ RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html) method is used to repair objects as specified using [RepairOptions](dcsRepairOptionsEnumeration.html) enumeration for the valid options.

[IAdgObject.AdgSubType](dcsIAdgObjectClassAdgSubTypeProperty.html) property always has a value of **Unknown** for **IDirectory** instances. Additionally, the values of the [ IAdgObject.Bases](dcsIAdgObjectClassBasesProperty.html) and [IAdgObject.Dependents](dcsIAdgObjectClassDependentsProperty.html) properties are always empty arrays.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDirectory Members](dcsIDirectoryMembers.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgSubType Property](dcsIAdgObjectClassAdgSubTypeProperty.html)
      <br />
      [Bases Property](dcsIAdgObjectClassBasesProperty.html)
      <br />
      [Dependents Property](dcsIAdgObjectClassDependentsProperty.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [NewDirectory Method](dcsAdgFactoryClassNewDirectoryMethod.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [RepairOptions Enumeration](dcsRepairOptionsEnumeration.html)
      <br />
      [AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

