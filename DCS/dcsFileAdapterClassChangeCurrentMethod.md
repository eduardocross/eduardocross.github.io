---
title: FileAdapter.ChangeCurrent Method

Id: dcsFileAdapterClassChangeCurrentMethod
TocParent: dcsFileAdapterMethods
TocOrder: 1

keywords: records, update current
keywords: update, current record
keywords: update current record
keywords: how to, update current record
keywords: database files, update current record
keywords: files, update current record
keywords: ChangeCurrent method
keywords: FileAdapter.ChangeCurrent method

---

Updates the current database file record with the contents of the specified [ AdgDataSet.ActiveRow ](dcsAdgDataSetClassActiveRowProperty.html)property.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void ChangeCurrent(
   [AdgDataSet](dcsAdgDataSetClass.html) ds
};** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub ChangeCurrent( _
   ByVal ds As [AdgDataSet](dcsAdgDataSetClass.html) _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSub ChangeCurrent Access(*Public)
   DclSrParm ds Type([AdgDataSet](dcsAdgDataSetClass.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *ds* 
        </dt>
        <dd>The DataSet object ( **ASNA.DataGate.Client.AdgDataSet** ) used to 
						update the database file record.
					</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

FileAdapter open method has not been called (file is not open).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException
</td>
            <td colspan="1" rowspan="1">

See table below.
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of
							<br />
							dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTUPD
</td>
            <td colspan="1" rowspan="1">

The file was not opened for update. To use **ChangeCurrent** , the [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) property must be set to a value which includes the [ AccessMode.Change](dcsAccessModeEnumeration.html) flag prior to opening the file.
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

dgEaNOCURR
</td>
            <td colspan="1" rowspan="1">

There is not a current record associated with the file. If the file is open for "network blocking", the current record position on the server is unknown.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBUSYREC
</td>
            <td colspan="1" rowspan="1">

Record is in use or locked by another process. You cannot access the requested record because it is being used by another database process. Certain DataGate providers may provide further details of the conflicting process in the Message and Text members of dgException.
</td>
          </tr>
</table>

Remarks

<span> **ChangeCurrent** </span> updates the contents of the current record of an open file. The current record is usually the record most recently accessed (by <code>read</code> or <code>seek</code> method). On database providers such as the IBM i, the record must be locked for update and upon completion of <span> **ChangeCurrent** </span>, the record is unlocked. Locking the record for update is performed by reading or seeking to the record without specifying a "no lock" option.
Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Change;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }
  /* We read the first record of the file... */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);
  myDS.SetActive(myDS.GetFormatName(0), 0); 
  /* ...and make the customer name all caps. */
  string CustName = System.Convert.ToString(myDS.ActiveRow["CMName"]);
  CustName = CustName.ToUpper();
  myDS.ActiveRow["CMName"] = CustName;
  try
  {
      /* Here we update the record. */
      dbFile.ChangeCurrent(myDS);
  }
  catch (dgException dgEx)
  {
      MessageBox.Show("Error updating record: " + dgEx.Message, "Error.");
      // Exit routine or take alternative action here.
      test.Actual = "Catch occured.";
  }

  dbFile.Close();
  db.Close();</pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read Or AccessMode.Change

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, MsgBoxStyle.OKOnly, "Error")
      'Exit procedure or end application here.
  End Try
  ' We read the first record of the file... 
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default)
  myDS.SetActive(myDS.GetFormatName(0), 0)
  ' ...and make the customer name all caps. 
  Dim CustName As String
  CustName = System.Convert.ToString(myDS.ActiveRow.Item("CMName"))
  CustName = CustName.ToUpper()
  myDS.ActiveRow.Item("CMName") = CustName
  Try
      ' Here we update the record. 
      dbFile.ChangeCurrent(myDS)
  Catch dgEx As dgException
      MsgBox("Error updating record: " + dgEx.Message, MsgBoxStyle.OKOnly, "Error")
      ' Exit routine or take alternative action here.
  End Try
</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

