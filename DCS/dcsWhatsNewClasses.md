---
title: New Classes

Id: dcsWhatsNewClasses

keywords: whats new [DCS 16.0 classes
keywords: new classes [DCS 16.0]
keywords: new [DCS 16.0 classes

---

### Introduction
This document contains a list and brief description of the new classes. 

For additional information, refer to the namespace and class links noted in ** <u>red</u> ** within the document.

References to new methods, properties, or fields for these new classes are noted in ***bold italics*** . Additional information on these references can be found in the 'members' for each class shown in the [ ** AdgFactory Class ** ](#AlsoSee">See Also</a> section.

Reference to other classes, methods, properties, or fields are noted in ** <u>green</u> ** within the document. 

###  <a name="return">Contents</a> 
Client 
						Namespace

<a href="#AdgFactoryClass">AdgFactory Class</a> 

<a href="#AdgTableClass">AdgTable Class</a> 

<a href="#AuthorityEntryClass">AuthorityEntry Class</a> 

<a href="#DependentClass">Dependent Class</a> 

<a href="#IAdgObjectClass">IAdgObject Class</a> 

<a href="#IAdgTransactionClass">IAdgTransaction Class</a> 

<a href="#IDirectoryClass">IDirectory Class</a> 

<a href="#IFileObjectClass">IFileObject Class</a> 

<a href="#ILibraryListClass">ILibraryList Class</a> 

<a href="#IMemberClass">IMember Class</a> 

<a href="#XmlInfoEventArgsClass">XmlInfoEventArgs Class</a> 
Providers Namespace

<a href="#IPrintPropertiesClass">IPrintProperties Class</a> 

<a href="#PrintDevAttrClass">PrintDevAttr Class</a> 
<br />

### CLIENT NAMESPACE

####  <a name="AdgFactoryClass">AdgFactory Class</a> 
The <a href="dcsAdgFactoryClass.html) static methods construct instances of [ **AdgConnection** ](#IAdgObjectClass">IAdgObject</a> representing database files, libraries, library lists, and members.

The AdgFactory methods create new IAdgObject instances based on a given <a href="dcsAdgConnectionClass.html) database source. IAdgObject is the base interface for the [ AdgTable Class ](#IFileObjectClass">IFileObject</a>, <a href="#IDirectoryClass">IDirectory</a>, and <a href="#IMemberClass">IMember</a> classes (representing database files, libraries, library lists, and members, respectively) for database object management functions.

AdgFactory has four methods to directly create IDirectory, IFileObject, ILibraryList, and IMember instances, given a path name and/or connection to an existing database object. These methods are: ***NewDirectory*** , ***NewFile*** , ***NewLibraryList*** , and ***NewMember*** , respectively.

-- <a href="#return">Return to contents</a> --
<br />

####  <a name="AdgTableClass">AdgTable Class</a> 
The **<a href="dcsAdgTableClass.html)** class supports DCS infrastructure and is not intended to be used directly from your code. It is added in support of [ **AdgKeyTable Class** ](dcsAdgKeyTableClass.html).

-- [ ** AuthorityEntry Class ** ](#return">Return to contents</a> --
<br />

####  <a name="AuthorityEntryClass">AuthorityEntry Class</a> 
The <a href="dcsAuthorityEntryClass.html) describes a user or group authorization to a database directory, member, or file. An instance of AuthorityEntry is usually one of a collection of authority descriptors for the database object, such as provided by the ** *AuthorityEntries* ** property of IAdgObject.

AuthorityEntry ***constructors*** create a single authority descriptor. ***AuthorityType*** establishes the access capabilitities and limitations (add, change, exclude, management, etc.). ***Username*** establishes the user or group profile name associated with the access authority. The ***IsGroupAccount*** field indicates if the Username is a user or group profile.

-- [ ** Dependent Class ** ](#return">Return to contents</a> --
Dependent Class

Instances of <a href="dcsDependentClass.html) are returned by the ** *Dependents* ** property of [ **AdgObjectTypes** ](#IAdgObjectClass"> IAdgObject</a>. These instances enumerate logical database objects which are defined in terms of a relationship to the base physical database object, represented by IAdgObject. Database providers may place constraints on database objects that have dependents, such as not allowing the object's deletion.

The ***AdgObjectType*** property reveals the dependent object's type, defined by the <a href="dcsAdgObjectTypesEnumeration.html) enumeration. Current database providers only list database files and members as dependents.

The ***DependentType*** property determines the relationship between this dependent and its base (see [ ** DependentTypes ** ](dcsDependentTypesEnumeration.html) enumeration).

-- [ **IAdgObject** ](#return">Return to contents</a> --
<br />

####  <a name="IAdgObjectClass">IAdgObject Class</a> 
<a href="dcsIAdgObjectClass.html) is the base interface implemented by all DataGate Component Suite (DCS) class objects modeling database objects. The leaf interfaces of these classes are [ **IAdgTransaction** ](#IDirectoryClass">IDirectory</a>, <a href="#IFileObjectClass">IFileObject</a>, and <a href="#IMemberClass">IMember</a>. Each of these inherits the methods and properties of IAdgObject, so that an instance of IDirectory, IFileObject, or IMember is also an instance of IAdgObject.

Note that methods which iterate IAdgObject instances (such as ** *IDirectory.Enumerate* ** , ** *IFileObject.Members* ** ), are actually returning references to objects that implement IDirectory, IFileObject, ILibraryList, or IMember. The underlying type of an IAdgObject instance can be determined with the ***AdgObjectType*** property.

The properties and methods provided by IAdgObject represent database object management functionality common to all database objects, such as names, locations, security, allocation, and definition. Included are methods for creating, renaming, moving, duplicating, and deleting database objects. Basically, IAdgObject and its inheritors are useful for performing the following tasks:

1. *Accessing* 
				the metadata of existing database objects.
2. *Modifying* 
				certain operational attributes of existing database objects.
3. *Defining*  and *creating*  new database objects.

-- <a href="#return">Return to contents</a> --
<br />

####  <a name="IAdgTransactionClass">IAdgTransaction Class</a> 
<a href="dcsIAdgTransactionClass.html) models database transaction management objects for database providers which support transaction processing. DCS provides two types of transaction objects, automatic and manual, both of which implement IAdgTransaction.

Manual transactions objects are constructed by the [ **AdgConnection.BeginTransaction** ](dcsAdgConnectionClassBeginTransactionMethodMain.html) method. The database provider begins a transaction context upon successful construction of the transaction object. The behavior of the manual transaction with regard to the ** *Commit* ** and ** *Rollback* ** methods is database provider platform-dependent. Some providers may end the transaction context after a call to ** *Commit* ** or ** *Rollback* ** , while others may continue the transaction context after these method calls. In either case, DCS regards manual transactions as ended with a call to the ***Dispose*** method.

Automatic transactions are constructed by the [ **AdgConnection.BeginAutoTransaction** ](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) method. A transaction context is begun by the database provider upon successful construction of the transaction object. The ** *Commit* ** and ** *Rollback* ** methods of an automatic transaction object perform the same functions as those of a manual transaction object. However, after successfully accepting or cancelling database modifications, both methods of an automatic transaction end the current transaction context and begin a new transaction using the parameters of the preceding transaction. The IAdgTransaction instance assumes control of the new transaction context. An automatic transaction is intended to emulate the behavior of System i database transactions for all database platforms.

At the time of this writing, only the System i database provider supports transaction processing. 

-- [ **IDirectory Class** ](#return">Return to contents</a> --
<br />

IDirectory Class

The <a href="dcsIDirectoryClass.html) models the library object of the database server. In addition to the generic object management methods and properties of IAdgObject, the IDirectory class provides additional functions specific to library objects.

A valid IDirectory reference may be obtained from DCS in one of the following ways:

- The ***AdgFactory.NewDirectory*** method instantiates a new instance of IDirectory, given a path name and [ ** AdgConnection ** ](dcsAdgConnectionClass.html) reference.
- An instance of IDirectory representing an existing database library may be returned when using the ** *IDirectory.Enumerate* ** method.
- An instance of IDirectory representing an existing database library may be obtained as a member of the array value of the ***ItemList*** property.
- An IDirectory instance may be returned from the ***AdgFactory.ReadXml*** method (as an IAdgObject reference), when the XML definition describes a database library.
- The ***CreateSubDirectory*** method, if successful, returns an instance of IDirectory representing the library it created.

-- [ ** IFileObject Class ** ](#return">Return to contents</a> --
<br />

IFileObject Class

The <a href="dcsIFileObjectClass.html) models the file object of the database server. In addition to the generic methods and properties of [ ** AdgConnection ** ](#IAdgObjectClass">IAdgObject</a> the IFileObject class provides methods specific to file objects. 

A valid IFileObject reference may be obtained from DCS in one of the following ways:

- The ***AdgFactory.NewFile*** method instantiates a new instance of IFileObject, given a path name and <a href="dcsAdgConnectionClass.html) reference.
- An instance of IFileObject representing an existing database file may be returned when using the ***IDirectory.Enumerate*** method.
- An instance of IFileObject representing an existing database file may be obtained as a member of the array value of the ***IDirectory.ItemList*** property.
- An IFileObject instance may be returned from the ***AdgFactory.ReadXml*** method (as an IAdgObject reference), when the XML definition describes database file.
- ***IFileObject.Copy*** returns an instance of IFileObject corresponding to the new duplicate file.

-- [ ** ILibraryList Class ** ](#return">Return to contents</a> --
<br />

ILibraryList Class

The <a href="dcsILibraryListClass.html) models an object management interface to the databases' library list. A library list is an ordered set of directory names associated with each applications database connection. In addition to the generic methods and properties of [ **AdgConnection** ](#IAdgObjectClass">IAdgObject</a>, ILibraryList provides properties and methods specific to library list objects.

A valid **ILibraryList** reference may be obtained from DCS in one of the following ways:

- The ***AdgFactory.NewLibraryList*** method instantiates a new instance of ILibraryList, given an <a href="dcsAdgConnectionClass.html) reference.
- An instance of ILibraryList representing an existing database library list entry may be returned when using the ** *EnumerateCurrentSystem* ** or ***EnumerateCurrentUser*** methods.
- The array elements of ** *CurrentSystemLibs* ** , ***CurrentUserLibs*** , ** *SystemConfig* ** , and ***UserConfig*** properties are references to ILibraryList instances. These references represent the library entries contained by the Library List.

-- [ ** IMember Class ** ](#return">Return to contents</a> --
<br />

IMember Class

The <a href="dcsIMemberClass.html) models the file member object of the database server. In addition to the generic methods and properties of [ **AdgConnection** ](#IAdgObjectClass">IAdgObject</a>, IMember provides properties and methods specific to member objects.

A valid **IMember** reference may be obtained from DCS in one of the following ways:

- The ***AdgFactory.NewMember*** method instantiates a new instance of IMember, given a path name and <a href="dcsAdgConnectionClass.html) reference.
- The array elements of the ***IFileObject.Members*** property are references to IMember instances, together representing the database member objects contained by a file.
- An IMember instance may be returned from the ***AdgFactory.ReadXml*** method (as an IAdgObject reference), when the XML definition describes a database file member.

-- [ ** XmlInfoEventArgs ** ](#return">Return to contents</a> --
XmlInfoEventArgs Class

An <a href="dcsXmlInfoEventArgsClass.html) object contains the details of events reported by the ** *AdgFactory.ReadXml* ** and ** *IAdgObject.WriteXml* ** methods, through the [ **XmlInfoEventHandler** ](dcsXmlInfoEventHandlerDelegate.html) delegate.

XmlInfoEventArgs is defined for use as a parameter of the XmlInfoEventHandler delegate. The parameter reports a single event status in a DCS XML method.

-- [ **IPrintProperties Class** ](#return">Return to contents</a> --
<br />

### PROVIDERS NAMESPACE
IPrintProperties Class

Print files in DCS may have fields with an associated print control object. These print controls may have ambient properties that characterize document attributes such as "font" or "color". Access to these properties permits adjustments to report documents as they are being generated. <a href="dcsIPrintPropertiesClass.html) is the interface to run-time print control properties. Instances of IPrintProperties are allocated per print format, via the [ **FileAdapter.GetPrintProperties** ](dcsFileAdapterClassGetPrintPropertiesMethod.html) method.

IPrintProperties methods must only be used when the print file is in the open state (see [ **FileAdapter.Open** ](dcsFileAdapterClassOpenMethod.html) ). Because print controls can exist as unmanaged objects, unexpected results may occur if IPrintProperties is used after the file has been closed. 

<p>-- [Client Namespace](#return">Return to contents</a> --
<br />

PrintDevAttr Class

Under construction.

-- <a href="#return">Return to contents</a> --
See Also

<dl />
      <a href="dcsDataGateClientNamespace.html)
      <br />
      [AdgFactory Class Members](dcsAdgFactoryMembers.html) 
				<br />[AuthorityEntry Class Members](dcsAuthorityEntryMembers.html) 
				<br />[Dependent Class Members](dcsDependentMembers.html)<br />
				[IAdgObject Class Members](dcsIAdgObjectMembers.html) 
				<br />[IAdgTransaction Class Members](dcsIAdgTransactionMembers.html)<br />
				[IDirectory Class Members](dcsIDirectoryMembers.html)<br />
				[IFileObject Class Members](dcsIFileObjectMembers.html)<br />
				[ILibraryList Class Members](dcsILibraryListMembers.html)<br />
				[IMember Class Members](dcsIMemberMembers.html) 
				<br />[XmlInfoEventArgs Class Members](dcsXmlInfoEventArgsMembers.html)<br />
				[Providers Namespace](dcsDataGateProvidersNamespace.html) 
				<br />[IPrintProperties Class Members](dcsIPrintPropertiesMembers.html)

