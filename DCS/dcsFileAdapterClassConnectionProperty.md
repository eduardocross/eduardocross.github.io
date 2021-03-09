---
title: FileAdapter.Connection Property

Id: dcsFileAdapterClassConnectionProperty
TocParent: dcsFileAdapterProperties
TocOrder: 1

keywords: Connection property
keywords: FileAdapter.Connection property
keywords: how to, connect files to a database server
keywords: database files, connection to a database server
keywords: files, connection to a database server
keywords: connection to a database server
keywords: database servers, connection to

---

The current **AdgConnection** associated with this **FileAdapter** .
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public AdgConnection Connection{ get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property Connection As [AdgConnection](dcsAdgConnectionClass.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Connection Access(*Public) Type(AdgConnection)** 
      </pre>

Property Value

Integer. Returns or sets an instance of [AdgConnection](dcsAdgConnectionClass.html) which represents a connection to a database server.
Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  /* Initialize a new fileadapter. Since the AdgConnection is needed
   * only for this file adapter, it is created and destroyed using the
   * FileAdapter's Connection property. */
  FileAdapter dbFile = new FileAdapter();
  dbFile.Connection = new AdgConnection("*Public/DG NET Local");
  dbFile.FileName = "*Libl/CMASTNEWL2";
  dbFile.MemberName = "CMMASTERL2";
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Find first record beginning with M. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMName"] = "M";
  dbFile.SeekKey(SeekMode.SetLL, keyTbl);

  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);
  string firstMCustomer = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close(); /* Close file. */
  dbFile.Connection.Close(); /* Close database. */</pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Initialize a new fileadapter. Since the AdgConnection is needed
  ' only for this file adapter, it is created and destroyed using the
  ' FileAdapter's Connection property. 
  Dim dbFile As New FileAdapter
  dbFile.Connection = New AdgConnection("*Public/DG NET Local")
  dbFile.FileName = "*Libl/CMASTNEWL2"
  dbFile.MemberName = "CMMASTERL2"
  dbFile.AccessMode = AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' Find first record beginning with M. 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL2")
  keyTbl.Row.Item("CMName") = "M"
  dbFile.SeekKey(SeekMode.SetLL, keyTbl)

  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)
  Dim firstMCustomer As String = myDS.ActiveRow.Item("CMName").ToString()

  dbFile.Close() ' Close file. 
  dbFile.Connection.Close() ' Close database. </pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

