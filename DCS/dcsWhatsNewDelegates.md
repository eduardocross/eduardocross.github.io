---
title: New Delegates

Id: dcsWhatsNewDelegates
TocParent: dcsDataGateClientNamespace
TocOrder: 2

keywords: whats new [DCS 16.0 delegates
keywords: new [DCS 16.0 delegates
keywords: new delegates [DCS 16.0]

---

This document contains a list and brief description of the DataGate Component Suite delegates. 

###  **[AdgEnumerator Delegate](dcsAdgEnumeratorDelegate.html)** 
This delegate is provided to the [ IDirectory.Enumerate](dcsIDirectoryClassEnumerateMethod.html) method for processing [ IAdgObject](dcsIAdgObjectClass.html) references corresponding to the contents of a database library. This delegate is also used in the [ ILibraryList.EnumerateCurrentSystem](dcsILibraryListClassEnumerateCurrentSystemMethod.html) and [ILibraryList.EnumerateCurrentUser](dcsILibraryListClassEnumerateCurrentUserMethod.html) methods for processing [ILibraryList](dcsILibraryListClass.html) references corresponding to the contents of a library list.

**[AdgObserver Delegate](dcsAdgObserverDelegate.html)** 

This delegate is a simple diagnostic and progress information processor, used by some DCS methods to providing feedback to the user program. The information is provided in a simple text message. [ IDirectory.RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html) and [ IFileObject.RepairFile](dcsIFileObjectClassRepairFileMethod.html) methods include the **AdgObserver** delegate in their parameter lists.[XmlInfoEventHandler Delegate](dcsIFileObjectClassRepairFileMethod.htm" />

**<a href="dcsXmlInfoEventHandlerDelegate.html)** 

This delegate provides a feedback channel and is defined strictly for use as an optional parameter with the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethod2.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html) methods. If desired, the user can define an implementation for this delegate to monitor the operation of these methods. The methods will periodically call the delegate to report a milestone of a certain detail level (see [XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html)).
<br />

See Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html) 
				<br />[IDirectory Class](dcsIDirectoryClass.html)
				<br />[IFileObject Class](dcsIFileObjectClass.html) 
				<br />[ILibraryList Class](dcsILibraryListClass.html)
				<br />[XmlInfoEventArgs Class](dcsXmlInfoEventArgsClass.html)

---

