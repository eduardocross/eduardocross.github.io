---
title: FileAdapter.AdapterStatus Enumeration

Id: dcsFileAdapterAdapterStatusEnumeration
TocParent: dcsDataGateClientEnumerations
TocOrder: 0

keywords: enumerations [DCS 16.0 FileAdapter.AdapterStatus
keywords: FileAdapter.AdapterStatus enumeration
keywords: database files, determine if open or closed
keywords: files, determine if open or closed
keywords: Open enumeration member
keywords: Closed enumeration member
keywords: database files, status of open 
keywords: files, status of open
keywords: status of a file

---

Indicates the status of the file: open or closed. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public FileAdapter.AdapterStatus Status { get: }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Status As FileAdapter.AdapterStatus** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Status Type(FileAdapter.AdapterStatus) Access(*Public)** 
      </pre>

Remarks

The **FileAdapter.AdapterStatus** enumeration is used as a parameter by the [ FileAdapter.Status Property](dcsFileAdapterClassStatusProperty.html) of the [FileAdapter Class](dcsFileAdapterClass.html).
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="40%" />
            <col span="1" width="5%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
									Member</th>
            <th colspan="1" rowspan="1">
									Description</th>
            <th colspan="1" rowspan="1">
									Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Open
</td>
            <td colspan="1" rowspan="1">

The file is open.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Closed
</td>
            <td colspan="1" rowspan="1">

The file is closed.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
</table>

Examples

Here we want to use a **FileAdapter** object named "dbFile" but are unsure as to whether or not it's been initialized, so we check for null and use the Status property to make sure it's opened and open it if it isn't.
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
      [FileAdapter.Status Property](dcsFileAdapterClassStatusProperty.html) <br />[FileAdapter Members](dcsFileAdapterMembers.html) <br />[ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)  

