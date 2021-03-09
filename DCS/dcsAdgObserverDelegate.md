---
title: AdgObserver Delegate

Id: dcsAdgObserverDelegate
TocParent: dcsWhatsNewDelegates
TocOrder: 1

keywords: delegates [DCS 16.0 AdgObserver
keywords: AdgObserver delegate

keywords: repair database files in library, feedback
keywords: database library lists, repair database files, feedback
keywords: database libraries, repair database files, feedback
keywords: database files, repair files in library, feedback
keywords: how to, repair database files in library, feedback
keywords: how to, invoke automatic diagnostic and repair function for library files, feedback
keywords: database files, repair single file, feedback
keywords: repair single database file, feedback
keywords: how to, repair database file, feedback
keywords: how to, invoke automatic diagnostic and repair function for a file, feedback

---

Defines a "call-back" method to report progress information to the user program as certain DCS methods operate.

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 
<pre class="prettyprint">
&lt;Serializable&gt; **Public Delegate AdgObserver** </pre>

Remarks

This delegate is a simple diagnostic and progress information processor, used by some DCS methods to provid feedback to the user program. The information is provided in a simple text message. The following methods include the **AdgObserver** delegate in their parameter lists:

- [IDirectory.RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html)
- IFileObject.InspectFile - This method is reserved for internal use by DCS and should not be invoked by user programs .
- [IFileObject.RepairFile](dcsIFileObjectClassRepairFileMethod.html)

DCS only calls the delegate during the operation of one of the above methods. DCS does not handle exceptions raised by the delegate's code. Please see the documentation for these methods for complete details of their behavior with the delegate. Generally, use of these delegates by DCS methods is optional to the user program. When a method defines **AdgObserver** in the parameter list but no feedback is desired, a null reference may be specified. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDirectory.RepairObjects Method](dcsIDirectoryClassRepairObjectsMethod.html)
      <br />
      [IFileObject.RepairFile Method](dcsIFileObjectClassRepairFileMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

