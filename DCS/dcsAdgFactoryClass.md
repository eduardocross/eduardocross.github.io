---
title: AdgFactory Class

Id: dcsAdgFactoryClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 2

keywords: classes [DCS 16.0 AdgFactory class
keywords: AdgFactory class
keywords: AdgFactory class, about AdgFactory class

---

The **AdgFactory** class static methods construct instances of [ IAdgObject](dcsIAdgObjectClass.html) representing database files, libraries, and members along with [IDataArea](dcsIDataAreaClass.html) for data areas. 

For a list of all members of this type, see [AdgFactory Members](dcsAdgFactoryMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> **ASNA.DataGate.Client.AdgFactory** 
<pre class="prettyprint">
        <span class="lang">[Prototype in C#]</span>
        <span>
 **public class AdgFactory | System.Object** 
        </span>
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

The **AdgFactory** methods create new [ IAdgObject](dcsIAdgObjectClass.html) instances based on a given [AdgConnection](dcsAdgConnectionClass.html) database source. **IAdgObject** is the base interface for the [ IFileObject](dcsIFileObjectClass.html), [IDirectory](dcsIDirectoryClass.html), and [ IMember](dcsIMemberClass.html) interfaces (representing database files, libraries, and members, respectively) for database object management functions.

**AdgFactory** has four methods to directly create object instances, given a path name to an existing database object, as follows:

1. [NewDirectory](dcsAdgFactoryClassNewDirectoryMethod.html) creates **IDirectory** 
				objects
2. [NewFile](dcsAdgFactoryClassNewFileMethod.html) creates new **IFileObject** 
				objects
3. [NewLibraryList](dcsAdgFactoryClassNewLibraryListMethod.html) creates 
					new **ILibraryList** 
				objects
4. [NewMember](dcsAdgFactoryClassNewMemberMethod.html) creates new **IMember** 
					objects.

[ReadXml](dcsAdgFactoryClassReadXmlMethods.html) methods creates a new **IAdgObject** instance (of type **IFileObject** , **IDirectory** , or **IMember** ) using **System.Xml.XmlReader** . The underlying type of the **IAdgObject** returned by **ReadXml** can be determined by examining the [ AdgObjectType](dcsIAdgObjectClassAdgObjectTypeProperty.html) property.

The **AdgFactory** methods create new [IDataArea](dcsIDataAreaClass.html) instances based on a given [AdgConnection](dcsAdgConnectionClass.html) database source. **IDataArea** is the interface representing data area processing functions. **AdgFactory** uses the [NewDataArea](dcsAdgFactoryClassNewDataAreaMethods.html) methods to create a new data area.

The **AdgFactory** class provides only static methods and is not intended to be instantiated as an object.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgFactory Members](dcsAdgFactoryMembers.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [AdgObjectType Property](dcsIAdgObjectClassAdgObjectTypeProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

