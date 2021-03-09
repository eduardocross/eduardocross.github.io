---
title: FileAdapter.OpenSimpleQuery Method

Id: dcsFileAdapterClassOpenSimpleQueryMethod
TocParent: dcsFileAdapterMethods
TocOrder: 15

keywords: FileAdapter.OpenSimpleQuery method
keywords: OpenSimpleQuery method
keywords: KeyUsages enumeration, used by
keywords: enumerations [DCS 16.0 KeyUsages, used by

keywords: database files, open a file for query
keywords: open a file for query
keywords: files, open for query

---

Open a database file for access using the specified query and the specified [AdgDataSet](dcsAdgDataSetClass.html).
<pre>        <span class="lang">[C#]</span>
 **Public void OpenSimpleQuery(
   ref AdgDataSet Ds,
   string QueryFile,
   string Query,
   string[] KeyNames,
   KeyUsages[] KeyFlags
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub OpenSimpleQuery( _
   ByRef Ds As [AdgDataSet](dcsAdgDataSetClass.html) _
   ByVal QueryFile As String _
   ByVal Query As String _
   ByVal KeyNames As String() _
   ByVal KeyFlags As [ASNA.DataGate.Common.KeyUsages](dcsKeyUsagesEnumeration.html)() _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr OpenSimpleQuery Access(*Public)
   DclSrParm Ds Type(AdgDataSet) By(*reference)
   DclSrParm QueryFile Type(*String)
   DclSrParm Query Type(*String)
   DclSrParm KeyNames Type(*String) Rank(1)
   DclSrParm KeyFlags Type(KeyUsages) Rank(1)** 
      </pre>

Parameters

<dl>
        <dt>
 *Ds* 
        </dt>
        <dd>The DataSet object ( **AdgDataSet)**  created to match the opened 
						file. </dd>
        <dt>
 *QueryFile* 
        </dt>
        <dd>		The name of the query file. </dd>
        <dt>
 *Query* 
        </dt>
        <dd>				The selection expression used to determine which records are to be made 
										available for processing. </dd>
        <dt>
 *KeyNames* 
        </dt>
        <dd>A string array containing the name(s) of key fields used to sort the query 
												records. Each key field array item must have a corresponding *KeyFlags*  item 
												which provides the key fields' sorting order (ascending descending, or absolute 
												value for numeric fields). </dd>
        <dt>
 *KeyFlags* 
        </dt>
        <dd>		An array of type [ASNA.DataGate.Common.KeyUsages](dcsKeyUsagesEnumeration.html)
														describing how the keys will be used. **KeyUsage**  enumerations 
														can be added or ORed together where required (e.g., ABSVALUE and DESCEND). Each *KeyFlags*  array item must have a corresponding *KeyNames*  item.
													</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOLDSERVER
</td>
            <td colspan="1" rowspan="1">

The file cannot be opened because the operation is not supported by the version of the database provider of the [AdgConnection](dcsAdgConnectionClass.html) object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The [FileName](dcsFileAdapterClassFileNameProperty.html) or [ MemberName](dcsFileAdapterClassMemberNameProperty.html) properties refer to an invalid database file name.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVDMOP
</td>
            <td colspan="1" rowspan="1">

The operation is not allowed because the database is opened for monitor access only.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFRMTID
</td>
            <td colspan="1" rowspan="1">

A "level check" operation was requested, and the check discovered a difference between an expected format and the actual format of the file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED
</td>
            <td colspan="1" rowspan="1">

The database provider called an "exit point" program to validate the operation and the program denied the requested operation.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC
</td>
            <td colspan="1" rowspan="1">

The database provider has found a registration for an "exit point" program to validate the operation but the database provider is not currently licensed for that capability.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING
</td>
            <td colspan="1" rowspan="1">

The database provider has found a registration for an "exit point" program to validate the operation but no such program could be found.
</td>
          </tr>
</table>

Remarks

**OpenSimpleQuery** opens the file and creates an **AdgDataSet** instance. This **AdgDataSet** is suitable for passing to **FileAdapter** access methods where file record data is processed. The **AdgDataSet** returned by **OpenSimpleQuery** is guaranteed to reflect record formats of the query file.

Selection expressions are evaluated during file open time. Therefore, a runtime error will be generated during the opening of the file when a selection expression error is encountered.

The selection criteria is specified as a single expression describing the values used to determine which records are selected. Any logical expression formed using relational operators can be specified (such as equal and/or not equal). The syntax of this expression is identical to that used for defining select/omit expressions when creating a logical file. 

Note that the length of the <span> *KeyNames* </span> and <span> *KeyFlags* </span> array parameters should be equal.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read; 
  AdgDataSet myDS = null;

  string[] keys = new string[]{"CMCUSTNO"};
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND};

  /* Read the first customer name listed for Texas. */
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();
  /* First close the file to avoid throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();
</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing

  Dim keys As String() = New String() {"CMCUSTNO"}
  Dim usages As KeyUsages() = New KeyUsages() {KeyUsages.ASCEND}

  ' Read the first customer name listed for Texas. 
  dbFile.OpenSimpleQuery(myDS, "*UNIQUE", "CMSTATE=""TX""", keys, usages)
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read)
  Dim FirstInTexas As String = myDS.ActiveRow.Item("CMName").ToString()
  ' First close the file to avoid throwing an exception... 
  dbFile.Close()
  ' Read the first customer name listed in Tennessee. 
  dbFile.OpenSimpleQuery(myDS, "*UNIQUE", "CMSTATE=""TN""", keys, usages)
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read)
  Dim FirstInTennessee As String = myDS.ActiveRow.Item("CMName").ToString()

  dbFile.Close()
  db.Close()</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [FileName Property](dcsFileAdapterClassFileNameProperty.html)
      <br />
      [MemberName Property](dcsFileAdapterClassMemberNameProperty.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [ASNA.DataGate.Common.KeyUsages Enumeration](dcsKeyUsagesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

