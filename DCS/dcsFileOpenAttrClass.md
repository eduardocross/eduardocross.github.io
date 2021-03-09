---
title: FileOpenAttr Class

Id: dcsFileOpenAttrClass
TocParent: dcsASNADataGateProvidersClasses
TocOrder: 2

keywords: FileOpenAttr class
keywords: FileOpenAttr class, about FileOpenAttr class
keywords: classes [DCS 16.0 FileOpenAttr class

---

A set of properties representing attributes of an open file.

For a list of all members of this type, see [FileOpenAttr Members](dcsFileOpenAttrClassMembers.html).

[ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) <br /> ASNA.DataGate.Providers.<span>FileOpenAttr</span>
<pre>
        <span>&lt;Serializable&gt;</span>
 **Public Class** 
        <span>FileOpenAttr | Inherits System.Collections.Hashtable</span>
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

<span> **FileOpenAttr** </span> objects are parameters passed to [FileAdapter](dcsFileAdapterClass.html) open methods ([Open](dcsFileAdapterClassOpenMethod.html), [ OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html), [OpenSimpleQuery](dcsFileAdapterClassOpenSimpleQueryMethod.html)) to invoke special access functionality in the opened DataGate file. This functionality includes:

- Network-level record blocking for high-performance read access.
- "Level-check" or DataGate file record format verification.
- Multi-process shared-access behavior.
- Other provider-dependent features of open files.

Note that **FileOpenAttr** inherits from System.Collections.Hashtable. The properties in **FileOpenAttr** are stored as key/value pairs in the **Hashtable** object where the key is a string containing the property name. For example, the value of the [ FileOpenAttr.BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) property is alternatively referenced as **FileOpenAttr.Item("BlockingFactor")** . However, to enforce type safety, it is recommended to use **FileOpenAttr** get/set property methods to access values.

Upon construction, no properties are set in **FileOpenAttr** . Properties do not have values until they are explicitly set by your program. To determine if a particular property has been assigned a value, use the **ContainsKey** method of **Hashtable** . For example, if the **BlockingFactor** property has been assigned a value, **FileOpenAttr.ContainsKey("BlockingFactor")** will return a **True** value. To remove the value (and key) for a particular property use the **Remove** method of **Hashtable** .

**FileOpenAttr** members only influence the file when the object is passed into one of the open methods of **FileAdapter** . Setting properties of **FileOpenAttr** after the file has been opened has no effect on **FileAdapter** or the open file.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileOpenAttr Members](dcsFileOpenAttrClassMembers.html)
      <br />
      [BlockingFactor Property](dcsFileOpenAttrClassBlockingFactorProperty.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [OpenSimpleQuery Method](dcsFileAdapterClassOpenSimpleQueryMethod.html)
      <br />
      [ASNA DataGate Providers Namespace](dcsDataGateProvidersNamespace.html)

