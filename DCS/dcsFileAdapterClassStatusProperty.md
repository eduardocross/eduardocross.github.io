---
title: FileAdapter.Status Property

Id: dcsFileAdapterClassStatusProperty
TocParent: dcsFileAdapterProperties
TocOrder: 12

keywords: enumerations [DCS 16.0 FileAdapter.AdapterStatus, used by
keywords: FileAdapter.AdapterStatus enumeration, used by
keywords: Status property
keywords: FileAdapter.Status property
keywords: database files, state of
keywords: files, open state of
keywords: how to, determine open state of database file
keywords: open state of file

---

<span>Indicates the status of the file; whether it is open or closed. </span> 
<pre>        <span class="lang">[C#]</span>
 **public FileAdapter.AdapterStatus Status { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Status As [FileAdapter.AdapterStatus](dcsFileAdapterAdapterStatusEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Status Type(FileAdapter.AdapterStatus) Access(*Public)
   BegGet** 
      </pre>

Property Value

[FileAdapter.AdapterStatus](dcsFileAdapterAdapterStatusEnumeration.html). Returns a value indicating whether the file is Open(1) or Closed(0).
Remarks

The value of **Status** is one of the **FileAdapter.AdapterStatus** values.
Examples

Here we want to use a fileAdapter object named "dbFile" but are unsure as to whether or not it's been initialized, so we check for null and use the Status property to make sure its opened and open it if it isn't.
<pre>        <span class="lang">
 **[C#]** 
        </span>
  if (dbFile == null)
      dbFile = new FileAdapter();
  if (dbFile.Status == FileAdapter.AdapterStatus.Closed)
  {
      dbFile.Connection = myAdgConnection;
      dbFile.FileName = fileName;
      dbFile.MemberName = memberName;
      dbFile.OpenNewAdgDataSet(out myDataSet);
  }
  </pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  If dbFile Is Nothing Then
      dbFile = New FileAdapter
  End If
  If dbFile.Status = FileAdapter.AdapterStatus.Closed Then
      dbFile.Connection = myAdgConnection
      dbFile.FileName = fileName
      dbFile.MemberName = memberName
      dbFile.OpenNewAdgDataSet(myDataSet)
  End If
</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [FileAdapter.AdapterStatus 
					Enumeration](dcsFileAdapterAdapterStatusEnumeration.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)  

