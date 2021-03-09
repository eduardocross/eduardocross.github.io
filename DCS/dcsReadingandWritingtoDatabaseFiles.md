---
title: Reading and Writing to Database Files

Id: dcsReadingandWritingtoDatabaseFiles
TocParent: dcsAccessingaFileMain
TocOrder: 2

keywords: accessing a file, reading and writing to database files
keywords: database files, reading to
keywords: database files, writing to
keywords: writing to database files
keywords: reading to database files

---

The following example in AVR <span>opens a database file</span> for "read" access as before and then reads the first record in the file.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
  using ASNA.DataGate.Client;
  using ASNA.DataGate.Common;
  ...
  AdgConnection Cx;
  FileAdapter DBFile;
  AdgDataSet Ds;
  Cx = new AdgConnection("ASNA Local DB");
  Cx.Open();
  DbFile = new FileAdapter(Cx,"/cmmaster","*first");
  DbFile.OpenNewAdgDataSet( ref Ds );
  DbFile.ReadSequential (Ds, ReadSequentialMode.Next, LockRequest.Default);
  Console.WriteLine("CMCustNo = " + Ds.ActiveRow["CMCustNo"]);</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
  Imports ASNA.DataGate.Client
  Imports ASNA.DataGate.Common
  ...
  Dim Cx As AdgConnection
  Dim DbFile As FileAdapter
  Dim Ds As AdgDataSet
  Cx = New AdgConnection("ASNA Local DB")
  Cx.Open() 
  DbFile = New FileAdapter(Cx,"/cmmaster","*first")
  DbFile.OpenNewAdgDataSet( ByRef Ds )
  DbFile.ReadSequential(Ds, ReadSequentialMode.Next, LockRequest.Default)
  Console.WriteLine("CMCustNo = " + Ds.ActiveRow["CMCustNo"])</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
  Using ASNA.DataGate.Client
  Using ASNA.DataGate.Common
  ...
  Dclfld Name(Cx) Type(AdgConnection)
  Dclfld Name(DbFile) Type FileAdapter
  Dclfld Name(Ds) Type(AdgDataSet)
  Cx = *New AdgConnection("ASNA Local DB")
  Cx.Open()
  DbFile = *New FileAdapter(Cx,"/cmmaster","*first")
  DbFile.OpenNewAdgDataSet( *ByRef Ds )
  DbFile.ReadSequential(Ds, ReadSequentialMode.Next, LockRequest.Default)
  Console.WriteLine("CMCustNo = " + Ds.ActiveRow["CMCustNo"])</pre>

Upon the successful completion of the DbFile.[ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) method in this example, the database file cursor represented by DbFile will rest on the first record of the file. Also, the data contained in the first record is available via the <span> **AdgDataSet** </span> object referred to by the <span> *Ds* </span> variable. The most recent record read into **AdgDataSet** is accessible via its [ActiveRow ](dcsAdgDataSetClassActiveRowProperty.html) property. In the last line of the example, the value of a field in the record (CMCustNo) is referenced from the <span> **ActiveRow** </span> property and displayed in a message box.

Other <span>FileAdapter</span> methods provide the record-oriented "read" access functions familiar to RPG and AS/400 programmers, including reading by key and reading by RRN. Keyed-access is explained in more detail in the Advanced Topics section (coming soon). 

To update a database file record, the [ ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html) method of FileAdapter is used. First, the record to be updated is read as in the previous example. Then the fields whose values are to be changed are accessed by name as above. 

The following example illustrates one procedure for **updating a file** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
  AdgConnection cx; 
  FileAdapter dbFile;
  AdgDataSet ds;
  cx = new AdgConnection("ASNA Local DB");
  cx.Open();
  dbFile = new FileAdapter(cx, "/cmmaster", "*first");
  dbFile.AccessMode = AccessMode.Change + AccessMode.Read;
  dbFile.OpenNewAdgDataSet(ds);
  dbFile.ReadSequential(ds, ReadSequentialMode.Next, LockRequest.Default);
  ds.ActiveRow.Item("CMCustNo") = 101;
  dbFile.ChangeCurrent(ds);
  dbFile.Close();
  cx.Close();</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
  Dim cx As AdgConnection
  Dim dbFile As FileAdapter
  Dim ds As AdgDataSet
  cx = New AdgConnection("ASNA Local DB")
  cx.Open()
  dbFile = New FileAdapter(cx, "/cmmaster", "*first")
  dbFile.AccessMode = AccessMode.Change + AccessMode.Read
  dbFile.OpenNewAdgDataSet(ds)
  dbFile.ReadSequential(ds, ReadSequentialMode.Next, LockRequest.Default)
  ds.ActiveRow.Item("CMCustNo") = 101
  dbFile.ChangeCurrent(ds)
  dbFile.Close()
  cx.Close()</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
  Dclfld Name(Cx) Type(AdgConnection)
  Dclfld Name(DbFile) Type(FileAdapter)
  Dclfld Name(Ds) Type(AdgDataSet)
  cx = *New AdgConnection("ASNA Local DB")
  cx.Open()
  dbFile = *New FileAdapter(cx, "/cmmaster", "*first")
  dbFile.AccessMode = AccessMode.Change + AccessMode.Read
  dbFile.OpenNewAdgDataSet(ds)
  dbFile.ReadSequential(ds, ReadSequentialMode.Next, LockRequest.Default)
  ds.ActiveRow.Item("CMCustNo") = 101
  dbFile.ChangeCurrent(ds)
  dbFile.Close()
  cx.Close()</pre>

This example simply opens and reads the first record as in the previous example, then sets the value of the CMCustNo field before calling the [ ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html) method to send the change to the server. Note that we have set the [AccessMode](dcsFileAdapterClassAccessModeProperty.html) property of the **FileAdapter** object prior to calling the [ OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) method. This informs the server that records in the opened file are to be read and updated. If not set explicitly, the <span> **AccessMode** </span> property value is Read, for read-only access.

The procedure for adding new records to database files follows a similar pattern, but the <span> **DataRow** </span> object representing the record to be inserted must be initialized according to the file format it represents. New **DataRow** objects to be added to a file are initialized with the [ PrepareRow ](dcsAdgDataSetClassPrepareRowMethodMain.html)method of **AdgDataSet** . This method is passed an index identifying the format of the record to be added, so that the new **DataRow** can be initialized with field objects of the appropriate name and type. Note that fields are initialized with the value <span>System.DBNull.Value</span>. Unless the corresponding database field supports "null values", the **DataRow** field value must be set explicitly by your program before the record is added to the database or an exception will occur. After setting field values in the new record you must append it to the dataset using a method such as [ AddPreparedRowAndSetActive](dcsAdgDataSetClassAddPreparedRowAndSetActiveMethod.html). Once the prepared row is the active row in the **AdgDataSet** , the [ FileAdapter.AddRecord](dcsFileAdapterClassAddRecordMethod.html) method can be called to add the new record to the database file.

The following example illustrates an appropriate sequence for **adding a database record** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
  using ASNA.DataGate.Client;
  using ASNA.DataGate.Common;
  ...
  AdgConnection cx;
  FileAdapter dbFile;
  AdgDataSet ds;
  cx.Open();
  dbFile.AccessMode = AccessMode.RWCD;
  dbFile.OpenNewAdgDataSet(ds);
  newRow DataRow;
  newRow = ds.PrepareRow(0);
  newRow["CMCustNo"] = 1;
  newRow["CMName"] = "Important Co.";
  newRow["CMAddr1"] = "1 Business Way";
  newRow["CMAddr2"] = "";
  newRow["CMCity"] = "Portland";
  newRow["CMState"] = "FL";
  newRow["CMPostCode"] = "21012";
  newRow["CMActive"] = "1";
  newRow["CMFax"] = 1232344567;
  newRow["CMPhone"] = "(234)456-6789";
  ds.AddPreparedRowAndSetActive(0);
  dbFile.AddRecord(ds);
  dbFile.Close();
  cx.Close();</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic]</span>
  Imports ASNA.DataGate.Client
  Imports ASNA.DataGate.Common
  ...
  Dim cx As New AdgConnection("ASNA Local DB")
  Dim dbFile As New FileAdapter(cx, "cmmaster", "*first")
  Dim ds As AdgDataSet
  cx.Open()
  dbFile.AccessMode = AccessMode.RWCD
  dbFile.OpenNewAdgDataSet(ds)
  Dim newRow As DataRow
  newRow = ds.PrepareRow(0)
  newRow("CMCustNo") = 1
  newRow("CMName") = "Important Co."
  newRow("CMAddr1") = "1 Business Way"
  newRow("CMAddr2") = ""
  newRow("CMCity") = "Portland"
  newRow("CMState") = "FL"
  newRow("CMPostCode") = "21012"
  newRow("CMActive") = "1"
  newRow("CMFax") = 1232344567
  newRow("CMPhone") = "(234) 456-6789"
  ds.AddPreparedRowAndSetActive(0)
  dbFile.AddRecord(ds)
  dbFile.Close()
  cx.Close()</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
  Using ASNA.DataGate.Client
  Using ASNA.DataGate.Common
  ...
  Dclfld Name(Cx) Type(AdgConnection&lt;)
  Dclfld Name(DbFile) Type(FileAdapter)
  Dclfld Name(Ds) Type(AdgDataSet)
  Cx = *New AdgConnection("ASNA Local DB")
  Cx.Open()
  dbFile.AccessMode = AccessMode.RWCD
  dbFile.OpenNewAdgDataSet(ds)
  DCLFLD Name (newRow) Type(DataRow)
  newRow = ds.PrepareRow(0)
  newRow("CMCustNo") = 1newRow("CMName") = "Important Co."
  newRow("CMAddr1") = "1 Business Way"
  newRow("CMAddr2") = ""
  newRow("CMCity") = "Portland"
  newRow("CMState") = "FL";
  newRow("CMPostCode") = "21012"
  newRow("CMActive") = "1"
  newRow("CMFax") = 1232344567
  newRow("CMPhone") = "(234)456-6789"
  ds.AddPreparedRowAndSetActive(0)
  dbFile.AddRecord(ds)
  dbFile.Close()
  cx.Close()</pre>

See Also

[AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [Database File Records and 
				AdgDataSet](dcsDatabaseFileRecordsandAdgDataSet.html)
      <br />
      [Efficient File Access](dcsEfficientFileAccess.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Verifying Results with 
				Exception Handling](dcsVerifyingResultswithExceptionHandling.html)
      <br />
      [Using the FileAdapter Class](dcsUsingtheFileAdapterClass.html)

