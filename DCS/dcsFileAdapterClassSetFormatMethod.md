---
title: FileAdapter.SetFormat Method

Id: dcsFileAdapterClassSetFormatMethod
TocParent: dcsFileAdapterMethods
TocOrder: 29

keywords: SetFormat method
keywords: FileAdapter.SetFormat method
keywords: records, specify format
keywords: records, restrict by specific format
keywords: formats, restrict records by
keywords: formats, specific
keywords: specify record by format
keywords: restrict record by format
keywords: how to, specify record by format
keywords: how to, restrict record by format
keywords: multiformat files, specify records by format
keywords: multiformat files, restrict records by specific format

---

For multiformat read access, calling this method causes the read methods to fetch only those records with the given format.
<pre>        <span class="lang">[C#]</span>
 **Public void SetFormat(
   string Format
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub SetFormat( _
   ByVal Format As String _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr SetFormat Access(*Public)
   DclSrParm Format Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *format* 
        </dt>
        <dd>A string that names the format to which to restrict record reads.
					</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
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

FileAdapter [Open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open). 
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

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException. 
</td>
          </tr>
</table>

Remarks

The default behavior of **FileAdapter** is to read all formats. Use this method to change an open file to read only records of the given format. To switch back to "read all records" mode, use the [ ResetFormat](dcsFileAdapterClassResetFormatMethod.html) method. This method has no effect if the file is not a multiformat file.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Read only records from format one. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/SalesMem", "SalesMem");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Write;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Add a record to format 0, "RCustMast". */
  /* Get new customer number to avoid adding a duplicate key. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);
  decimal newCustNo = Convert.ToDecimal(myDS.ActiveRow["CMCustNo"]) + 100m;

  DataRow newRecord = myDS.PrepareRow("RCustMast");
  /* Create a customer record. */

  newRecord["CMCustNo"] = newCustNo;
  newRecord["CMName"] = "Amalgamated Software of North America";
  newRecord["CMAddr1"] = "9901 IH-10 West, Suite 1000";
  newRecord["CMCity"] = "San Antonio";
  newRecord["CMState"] = "TX";
  newRecord["CMCntry"] = "US";
  newRecord["CMPostCode"] = "78230";
  newRecord["CMActive"] = "1";
  newRecord["CMPhone"] = "2104080212";

  myDS.AddPreparedRowAndSetActive(0);
  dbFile.SetFormat("RCustMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key value \"" + 
            newRecord["CMName"].ToString() +
          "\" already in this 
            file.", "Error");
      dbFile.Close();
      db.Close();
      //Exit procedure or take other action here to 
            avoid adding next record.
  }
  /* Now add a record to format 1, "RSalesMast". */
  DataRow newRecord2 = myDS.PrepareRow("RSalesMast");

  /* Create a record of sales for 2004. */
  newRecord2["CSCustNo"] = newRecord["CMCustNo"];
  newRecord2["CSYear"] = 2004m;
  newRecord2["CSType"] = 1m;
  newRecord2["CSSales01"] = 100m;
  newRecord2["CSSales02"] = 200m;
  newRecord2["CSSales03"] = 300m;
  newRecord2["CSSales04"] = 400m;
  newRecord2["CSSales05"] = 500m;
  newRecord2["CSSales06"] = 600m;
  newRecord2["CSSales07"] = 500m;
  newRecord2["CSSales08"] = 400m;
  newRecord2["CSSales09"] = 200m;
  newRecord2["CSSales10"] = 100m;
  newRecord2["CSSales11"] = 1m;
  newRecord2["CSSales12"] = 0m;

  myDS.AddPreparedRowAndSetActive(1);
  dbFile.SetFormat("RSalesMast");
  try
  {
      dbFile.AddRecord(myDS);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error != dgErrorNumber.dgEaDUPKEY)
          throw dgEx; /* If the 
            exception wasn't thrown due to a duplicate key, throw it again. */
      MessageBox.Show("Key " + 
            newRecord["CSName"].ToString() + " already in this file.", "Error");
  }

  dbFile.Close();
  db.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  'Read only records from format one.
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/SalesMem", "SalesMem")
  dbFile.AccessMode = AccessMode.Read Or AccessMode.Write
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' Add a record to format 0, "RCustMast".
  ' Get new customer number to avoid adding a duplicate key.
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read)
  Dim newCustNo As Decimal
  newCustNo = Convert.ToDecimal(myDS.ActiveRow.Item("CMCustNo")) + 100

  Dim newRecord As DataRow = myDS.PrepareRow("RCustMast")
  ' Create a customer record.

  newRecord.Item("CMCustNo") = newCustNo
  newRecord.Item("CMName") = "Amalgamated Software of North America"
  newRecord.Item("CMAddr1") = "9901 IH-10 West, Suite 1000"
  newRecord.Item("CMCity") = "San Antonio"
  newRecord.Item("CMState") = "TX"
  newRecord.Item("CMCntry") = "US"
  newRecord.Item("CMPostCode") = "78230"
  newRecord.Item("CMActive") = "1"
  newRecord.Item("CMPhone") = "2104080212"

  myDS.AddPreparedRowAndSetActive(0)
  dbFile.SetFormat("RCustMast")
  Try
      dbFile.AddRecord(myDS)
  Catch dgEx As dgException
      If (dgEx.Error &lt;&gt; dgErrorNumber.dgEaDUPKEY) Then
          Throw dgEx ' If the 
            exception wasn't thrown due to a duplicate key, throw it again.
      End If
      MsgBox("Key value """ + 
            newRecord.Item("CMName").ToString() &amp; _
          """ already in this 
            file.")
      dbFile.Close()
      db.Clone()
      'Exit procedure or take other action here to 
            avoid adding next record.
  End Try
  ' Now add a record to format 1, "RSalesMast".
  Dim newRecord2 As DataRow = myDS.PrepareRow("RSalesMast")

  ' Create a record of sales for 2004.
  newRecord2.Item("CSCustNo") = newRecord.Item("CMCustNo")
  newRecord2.Item("CSYear") = 2004
  newRecord2.Item("CSType") = 1
  newRecord2.Item("CSSales01") = 100
  newRecord2.Item("CSSales02") = 200
  newRecord2.Item("CSSales03") = 300
  newRecord2.Item("CSSales04") = 400
  newRecord2.Item("CSSales05") = 500
  newRecord2.Item("CSSales06") = 600
  newRecord2.Item("CSSales07") = 500
  newRecord2.Item("CSSales08") = 400
  newRecord2.Item("CSSales09") = 200
  newRecord2.Item("CSSales10") = 100
  newRecord2.Item("CSSales11") = 1
  newRecord2.Item("CSSales12") = 0

  myDS.AddPreparedRowAndSetActive(1)
  dbFile.SetFormat("RSalesMast")
  Try
      dbFile.AddRecord(myDS)
  Catch dgEx As dgException
      If (dgEx.Error &lt;&gt; dgErrorNumber.dgEaDUPKEY) Then
          Throw dgEx ' If the 
            exception wasn't thrown due to a duplicate key, throw it again.
      End If
      MsgBox("Key " &amp; newRecord.Item("CSName").ToString() 
            &amp; _
          " already in this file.", 
            MsgBoxStyle.OKOnly, "Error")
  End Try

  dbFile.Close()
  db.Close()</pre>

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
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [ResetFormat Method](dcsFileAdapterClassResetFormatMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

