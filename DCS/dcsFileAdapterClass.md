---
title: FileAdapter Class

Id: dcsFileAdapterClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 8

keywords: classes [DCS 16.0 FileAdapter class
keywords: FileAdapter class
keywords: FileAdapter class, about FileAdapter class
keywords: accessing a file, about FileAdapter
keywords: database files, about FileAdapter class
keywords: files, about FileAdapter class

keywords: records, about FileAdapter class

---

The **FileAdapter** class provides record-level database access methods and open file status information. 

For a list of all members of this type, see [FileAdapter Members](dcsFileAdapterMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> ASNA.DataGate.Client.<span>FileAdapter</span>
<pre class="prettyprint">&lt;Serializable&gt; **Public Class FileAdapter** </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

<span> **FileAdapter** </span> models an open database file, and when used in conjunction with the [ AdgConnection](dcsAdgConnectionClass.html) class, can be used to read, write, update, and delete database records. The **FileAdapter** class maintains a "file pointer" or a server-side indicator of the current position for record operations on the file.

Several "open" methods perform the function of opening a file for access operations. These methods define an [AdgDataSet](dcsAdgDataSetClass.html) parameter, which is bound to the open file to contain database records. Generally, the access methods and properties of **FileAdapter** are unavailable before the file is open. The [ Status](dcsFileAdapterClassStatusProperty.html) property can be used to determine if a file is currently closed or is already open. An [Open](dcsFileAdapterClassOpenMethod.html) method call reopens a database file closed by a preceding [ Close](dcsFileAdapterClassCloseMethod.html) method call.

The **Open** method is used to open a file with a preexisting **AdgDataSet** object. In general, this method should be reserved for use by development environments such as Visual RPG, which generate strongly-typed data sets at compile-time.

[OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) opens a database file member specified by the [ Connection](dcsFileAdapterClassConnectionProperty.html), [FileName](dcsFileAdapterClassFileNameProperty.html), and [MemberName](dcsFileAdapterClassMemberNameProperty.html) properties. A new **AdgDataSet** object is created and returned as an output parameter reference.

Before calling an open method, properties may be set to modify the access or availability of the open file. The [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) property may be set with the values of [AccessMode enumeration](dcsAccessModeEnumeration.html) to indicate how the open file will be accessed. [ OpenAttributes](dcsFileAdapterClassOpenAttributesProperty.html) references the [FileOpenAttr](dcsFileOpenAttrClass.html) object, which is used to specify many properties of open files. For example, the [FileOpenAttr.FormatIDs](dcsFileOpenAttrClassFormatIDsProperty.html) property may be assigned an array of format identifiers used in a "level-check" operation to verify that the format of the file is the format expected.

The record access methods of the **FileAdapter** class are used to read and write records to an open file. However, **FileAdapter’s** [SeekRange](dcsFileAdapterClassSeekRangeMethod.html), [ SeekRRN](dcsFileAdapterClassSeekRRNMethod.html), and [SeekKey](dcsFileAdapterClassSeekKeyMethod.html) methods may be used to change the file pointer without reading or changing the file. The [DeleteCurrent](dcsFileAdapterClassDeleteCurrentMethod.html), [ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html), and [ ReleaseCurrent](dcsFileAdapterClassReleaseCurrentMethod.html) methods operate upon the "current record", or the record last read from or written to the file.

Several indicator properties may be used to determine the side effects of a preceding access operation on the **FileAdapter** object. [ ExactSeek](dcsFileAdapterClassExactSeekProperty.html) is set to **true** if a seek operation results in placing the file pointer on a record containing a specified key or RRN. [ RRN](dcsFileAdapterClassRRNProperty.html) contains the "relative-record number" of the last record accessed, if the database provider supports this information. [ CurrentFormatIndex](dcsFileAdapterClassCurrentFormatIndexProperty.html) identifies the format of the record most recently accessed.

The [SetFormat](dcsFileAdapterClassSetFormatMethod.html) method is available for multiformat read access. Calling this method causes the read methods to fetch only those records with the given format. To read all record formats, specify a null or empty string. [ FormatRequested](dcsFileAdapterClassFormatRequestedProperty.html) is the record format for reading multiformat file records.

To improve the efficiency of sequential access to files residing on network database servers, specify the [ FileOpenAttr.BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) property of the **OpenAttributes** property. Even more efficiency can be achieved with the proper use of the "range" methods, [SeekRange](dcsFileAdapterClassSeekRangeMethod.html), [ReadRange](dcsFileAdapterClassReadRangeMethod.html), and [ DeleteRange](dcsFileAdapterClassDeleteRangeMethod.html).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)  <br />[AdgDataSet Class](dcsAdgDataSetClass.html)<br />[AdgDataSet Class Members](dcsAdgDataSetMembers.html)<br />[FileOpenAttr Class](dcsFileOpenAttrClass.html)<br />[FileOpenAttr Class Members](dcsFileOpenAttrClassMembers.html)<br />[FormatIDs Property](dcsFileOpenAttrClassFormatIDsProperty.html)<br />[BlockingFactor Property](dcsFileOpenAttrClassBlockingFactorProperty.html)<br />[ASNA DataGate Client Namespace](dcsDataGateClientNamespace.html) 

