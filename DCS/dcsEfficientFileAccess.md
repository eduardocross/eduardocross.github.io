---
title: Efficient File Access

Id: dcsEfficientFileAccess
TocParent: dcsAccessingaFileMain
TocOrder: 3

keywords: file access, efficient
keywords: efficient file access
keywords: accessing a file, efficient file access
keywords: how to, access a file efficiently

---

Previously, we saw how a file can be read using the [ FileAdapter](dcsFileAdapterClass.html) and [AdgDataSet](dcsAdgDataSetClass.html) objects. FileAdapter’s [ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) method is the best way to read each record of a file in succession. For large files, using this method to find a particular record of interest can be inefficient. The [ReadRandomRRN](dcsFileAdapterClassReadRandomRRNMethod.html), [ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html), [ ReadRange](dcsFileAdapterClassReadRangeMethod.html), and [ReadSequentialEqual](dcsFileAdapterClassReadSequentialEqualMethod.html) methods are provided for this reason.

**ReadRandomRRN** reads a record specified by relative record number (RRN). **ReadRandomRRN** may not be implemented by all DCS database providers, but it allows "random" access to files that may be otherwise non-indexed. On the other hand, **ReadRandomKey** , **ReadRange** , and **ReadSequentialEqual** are methods for reading files that are indexed by key data. To use these, one or more data keys must be initialized and passed to the method.

In DCS, key and record data are modeled as **DataRow** objects. **DataColumn** objects in the **DataColumnCollection** of the **DataTable** corresponding to the record format or key contain the basic type information for each field. The [ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) property of **AdgDataSet** is a reference to the **DataRow** object representing the data in the record accessed. 

Likewise, a **DataRow** object can represent a key. Generally, to obtain a **DataRow** object for a particular record format’s key you would use the [NewKeyTable](dcsAdgDataSetClassNewKeyTableMethods.html) method of **AdgDataSet.** Use this method on the **AdgDataSet** object returned by the [OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) method of **FileAdapter** . **NewKeyTable** returns an [AdgKeyTable](dcsAdgKeyTableClass.html) object reference containing the **DataRow** object for the key.

The [Row](dcsAdgKeyTableClassRowProperty.html) property of **AdgKeyTable** references this **DataRow** . As with the [ PrepareRow](dcsAdgDataSetClassPrepareRowMethodMain.html) methods of **AdgDataSet** , the **DataRow** referenced by **AdgKeyTable** will be initialized with "null values". Before using the new key in a **ReadRandomKey** method call, the **Value** properties should be set to reflect the key being sought, as in the following example.
<pre>        <span class="lang">[C#]</span>
  AdgConnection cx;
  FileAdapter DbFile;
  AdgDataSet Ds;
  AdgKeyTable KeyTbl;
  Cx = new AdgConnection("ASNA Local DB");
  Cx.Open();
  DbFile = new FileAdapter(Cx,"Asna_example_files/custmast","*first");
  DbFile.AccessMode = AccessMode.RWCD;
  DbFile.OpenNewAdgDataSet( ref Ds );
  KeyTbl = Ds.NewKeyTable(ds.GetFormatName(0));
  KeyTbl.Row["CMCustNo"] = 500;
  DbFile.ReadRandomKey( Ds, ReadRandomMode.GTEQ, LockRequest.Default, KeyTbl );
  Console.WriteLine( "CMCustNo = " + Ds.ActiveRow["CMCustNo"] ) ;</pre>
      <pre>        <span class="lang">[Visual Basic]</span>
  Dim Cx As AdgConnection
  Dim DbFile As FileAdapter
  Dim Ds As AdgDataSet
  Dim Keytbl As AdgKeyTable
  Cx = New AdgConnection("ASNA Local DB")
  Cx.Open()
  DbFile = New FileAdapter(Cx,"Asna_example_files/custmast","*first")
  DbFile.AccessMode = AccessMode.RWCD
  DbFile.OpenNewAdgDataSet( ByRef Ds )
  KeyTbl = Ds.NewKeyTable(ds.GetFormatName(0))
  KeyTbl.Row["CMCustNo"] = 500
  DbFile.ReadRandomKey( Ds, ReadRandomMode.GTEQ, LockRequest.Default, KeyTbl )
  Console.WriteLine( "CMCustNo = " + Ds.ActiveRow["CMCustNo"] )</pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
  Dclfld Name(Cx) Type(AdgConnection)
  Dclfld Name(DbFile) Type(FileAdapter)
  Dclfld Name(Ds) Type (AdgDataSet)
  Dclfld Name (KeyTbl) Type(AdgKeyTable)
  Cx = *New AdgConnection("ASNA Local DB")
  Cx.Open()
  DbFile = *New FileAdapter(Cx,"Asna_example_files/custmast","*first")
  DbFile.AccessMode = AccessMode.RWCD
  DbFile.OpenNewAdgDataSet( *ByRef Ds )
  KeyTbl = Ds.NewKeyTable(ds.GetFormatName(0))
  KeyTbl.Row["CMCustNo"] = 500
  DbFile.ReadRandomKey( Ds, ReadRandomMode.GTEQ, LockRequest.Default, KeyTbl )
  Console.WriteLine( "CMCustNo = " + Ds.ActiveRow["CMCustNo"] )</pre>

In the above example, we access a file using the **ReadRandomKey** method. This particular file has one key field named "CMCustNo". The **NewKeyTable** method is called on the **AdgDataSet** returned from **OpenNewAdgDataSet.** **NewKeyTable** is passed the format name of the only format of the file. Note that we use the [GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html) method of **AdgDataSet** to avoid hard-coding the format name. The returned **AdgKeyTable** object contains one **DataRow** object consisting of only one database field value for the CMCustNo field. This key field is initialized with the integer value 500 in this example. Next, **ReadRandomKey** is called passing the key value in the **AdgKeyTable** object. Also note that the [ ReadRandomMode.GTEQ](dcsReadRandomModeEnumeration.html) is passed to **ReadRandomKey** . This specifies that we would like to read the next record containing the given key, or otherwise the next record containing a key greater than the given key.
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [PrepareRow Methods](dcsAdgDataSetClassPrepareRowMethodMain.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ReadSequential Method](dcsFileAdapterClassReadSequentialMethod.html)
      <br />
      [ReadRandomRRN Method](dcsFileAdapterClassReadRandomRRNMethod.html)
      <br />
      [ReadRandomKey Method](dcsFileAdapterClassReadRandomKeyMethod.html)
      <br />
      [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)
      <br />
      [ReadSequentialEqual 
					Method](dcsFileAdapterClassReadSequentialEqualMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [Row Property](dcsAdgKeyTableClassRowProperty.html)
      <br />
      [ReadRandomMode Enumeration](dcsReadRandomModeEnumeration.html)
      <br />
      [Reading and Writing to Database 
					Files](dcsReadingandWritingtoDatabaseFiles.html)
      <br />
      [Verifying Results with 
					Exception Handling](dcsVerifyingResultswithExceptionHandling.html)
      <br />
      [Using the FileAdapter Class](dcsUsingtheFileAdapterClass.html)
      <br />
      [Database File Records and 
					AdgDataSet](dcsDatabaseFileRecordsandAdgDataSet.html)

