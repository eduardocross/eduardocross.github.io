---
title: FileAdapter.FileLength Property

Id: dcsFileAdapterClassFileLengthProperty
TocParent: dcsFileAdapterProperties
TocOrder: 5

keywords: FileLength property,
keywords: FileAdapter.FileLength property

keywords: number of, records in open database file
keywords: database files, number of deleted and non-deleted records in open file

---

The number of deleted and non-deleted records in the open database file. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public long FileLength { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property FileLength As Long** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp FileLength Type(*Integer) Len(8) Access(*Public)** 
      </pre>

Property Value

Integer. Returns the number of deleted and non-deleted records in the file. 
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  FileAdapter dbFile = new FileAdapter();
  dbFile.Connection = new AdgConnection("*Public/DG NET Local");
  dbFile.FileName = "*Libl/CMASTNEW";
  dbFile.MemberName = "CMMASTER";
  AdgDataSet myDS = null;
  dbFile.Open(myDS); /* Will not initialize the data set. */

  /* Figure out the number of records which were logically 
   * deleted but are still taking up space on the physical file.
   * FileLength returns the number of deleted and non-deleted 
   * records stored on a physical file, while RecordCount returns
   * the number of non-deleted records only. */
  long deletedRecords = dbFile.FileLength - dbFile.RecordCount;
  MessageBox.Show("Number of deleted records still taking up space in file \"" 
      + dbFile.FileName + "\" is " + deletedRecords.ToString());
  dbFile.Close();
  dbFile.Connection.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim dbFile As New FileAdapter
  dbFile.Connection = New AdgConnection("*Public/DG NET Local")
  dbFile.FileName = "*Libl/CMASTNEW"
  dbFile.MemberName = "CMMASTER"
  Dim myDS As AdgDataSet = Nothing
  dbFile.Open(myDS) ' Will not initialize the data set. 

  ' Figure the number of records which were logically 
  ' deleted but are still taking up space on the physical file.
  ' FileLength returns the number of deleted and non-deleted 
  ' records stored on a physical file, while RecordCount returns
  ' the number of non-deleted records only. 
  Dim deletedRecords As Long
  deletedRecords = dbFile.FileLength - dbFile.RecordCount
  MsgBox("Number of deleted records still taking up space in file """ &amp; _
      dbFile.FileName &amp; """ is " &amp; deletedRecords.ToString())
  dbFile.Close()
  dbFile.Connection.Close()
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
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)  

