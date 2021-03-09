---
title: FileAdapter.ReadSequentialEqual Method

Id: dcsFileAdapterClassReadSequentialEqualMethod
TocParent: dcsFileAdapterMethods
TocOrder: 20

keywords: FileAdapter.ReadSequentialEqual method
keywords: ReadSequentialEqual method
keywords: enumerations [DCS 16.0 LockRequest, used by
keywords: enumerations [DCS 16.0 ReadEqualMode, used by
keywords: LockRequest enumeration, used by
keywords: ReadEqualMode enumeration, used by
keywords: database files, read records sequentially
keywords: files, read records sequentially
keywords: how to, read records sequentially
keywords: read records sequentially
keywords: records, read sequentially
keywords: files, record locking override

---

Read a database file record adjacent to the current position with a key equal to the key of the current record, or optionally, a key equal to the specified key.
<pre>        <span class="lang">[C#]</span>
 **Public void ReadSequentialEqual(
   AdgDataSet ds,
   ReadEqualMode mode,
   LockRequest lr,
   AdgKeyTable keyTable
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub ReadSequentialEqual( _
   ByVal ds As [AdgDataSet](dcsAdgDataSetClass.html) _
   ByVal mode As [ReadEqualMode](dcsReadEqualModeEnumeration.html) _
   ByVal lr As [LockRequest](dcsLockRequestEnumeration.html) _
   ByVal keyTable As [AdgKeyTable](dcsAdgKeyTableClass.html)
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr ReadSequentialEqual Access(*Public)
   DclSrParm ds Type(AdgDataSet)
   DclSrParm mode Type(ReadEqualMode)
   DclSrParm lr Type(LockRequest)
   DclSrParm keyTable Type(AdgKeyTable)** 
      </pre>

Parameters

<dl>
        <dt>
 *ds* 
        </dt>
        <dd>The DataSet object ([AdgDataSet](dcsAdgDataSetClass.html)) to which a 
						single record will be added. </dd>
        <dt>
 *mode* 
        </dt>
        <dd><a style="FONT-STYLE: normal" href="dcsReadEqualModeEnumeration.htm">ReadEqualMode</a>. 
								Specifies the manner in which the record is to be located, relative to the 
								current position in the file (Current, Next, Previous, NextEqual, 
								PreviousEqual) or at the beginning or end of the file (First, Last). </dd>
        <dt>
 *lr* 
        </dt>
        <dd>[LockRequest](dcsLockRequestEnumeration.html). Specifies how the 
										record read is to be locked. </dd>
        <dt>
 *keyTable* 
        </dt>
        <dd>[AdgKeyTable](dcsAdgKeyTableClass.html). An optional key value to 
												search for the record.
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

FileAdapter [open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open).
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

dgEaEOF
</td>
            <td colspan="1" rowspan="1">

The record access operation resulted in an end-of-file condition. This exception also occurs when the record access operation would place the current file position outside of the boundaries established by a prior **ReadRange** or **SeekRange** method call.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTFND
</td>
            <td colspan="1" rowspan="1">

The record to be accessed was not found. It may have been deleted, it may never have existed, or the key may have been changed.
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

Reads a single record based on the file's access path, current record key value, and a read *mode* indicator. Optionally read a record with a key value equal to the specified key. Also, the behavior of this method is influenced by **FileAdapter** "range mode" (see also [ ReadRange](dcsFileAdapterClassReadRangeMethod.html) and [SeekRange](dcsFileAdapterClassSeekRangeMethod.html)).

Commonly, the **ReadSequentialEqual** method is used to read a record adjacent to the current record that has the same key value as the current record. To do this, specify the desired *mode* parameter, and set the [KeyPartCount](dcsAdgKeyTableClassKeyPartCountProperty.html) property of the **AdgKeyTable** object passed in the key parameter to zero.

To use **ReadSequentialEqual** to read a record which contains a particular key value, specify the key value in the **AdgKeyTable** object passed in the *keyTable* parameter.

**ReadSequentialEqual** is subject to the restrictions of "range mode". Calls to the **ReadRange** or **SeekRange** methods will restrict the records accessible to subsequent sequential access methods, including **ReadSequentialEqual** . If **ReadSequentialEqual** would otherwise return a record containing a key which falls outside of the current range, dgException will be thrown with an Error property value of dgEaEOF.

If the operation is successful, the record read is placed in the specified **AdgDataSet** object. The record is appended to a DataTable in the **AdgDataSet** corresponding to the record format. The record is appended as a DataRow object in the DataTable, and the [AdgDataSet.ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) property will reference this DataRow on return. If the operation is unsuccessful, no record is appended to the table, and an exception is thrown.

A successful read operation optionally locks the record read as directed by the *lr* parameter and the locking properties of the file. 
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read all of the records for customer 300 in order to get 
   * their net sales as well as their average yearly gross sales
   * and returns. */
  AdgKeyTable custNoKey = myDS.NewKeyTable("RCSMastL1");
  custNoKey.Row["CSCustNo"] = Convert.ToDecimal(300);
  custNoKey.KeyPartCount = 1; //Only use the first field of the key.
  decimal totalSales = 0;
  decimal totalReturns = 0;
  int saleRecordsRead = 0;
  int returnRecordsRead = 0;
  bool EOF = false;
  /* Because ReadSequentialEqual will return EOF if the record
   * it immediately gets is not equal to its search key, we need
   * to first seek to an equal record. */ 
  dbFile.SeekKey(SeekMode.SetLL, custNoKey);
  while(!EOF){
      try{
          dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey);
          if (Convert.ToDecimal(myDS.ActiveRow["CSType"]) == 1)
          {
              totalSales += Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              saleRecordsRead ++;
          }
          else
          {
              totalReturns -= Convert.ToDecimal(myDS.ActiveRow["CSSales01"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales02"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales03"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales04"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales05"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales06"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales07"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales08"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales09"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales10"]) +
                  Convert.ToDecimal(myDS.ActiveRow["CSSales11"]) + 
                  Convert.ToDecimal(myDS.ActiveRow["CSSales12"]);
              returnRecordsRead ++;
          }
      }
      catch(dgException dgEx){
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
          {
              EOF = true;
          }
          else
          {
              MessageBox.Show("Error getting next record for customer 300:" + 
                  dgEx.Message, "Error");
              //Exit procedure or end application here.
          }
      }
  }
  /* Compute additional results. */
  decimal netSales = totalSales - totalReturns;
  decimal averageSalesPerYear;
  if (saleRecordsRead &gt; 0)
      averageSalesPerYear = totalSales / saleRecordsRead;
  else
      averageSalesPerYear = 0;
  decimal averageReturnsPerYear;
  if (returnRecordsRead &gt; 0)
      averageReturnsPerYear = totalReturns / returnRecordsRead;
  else
      averageReturnsPerYear = 0;
  dbFile.Close();
  db.Close();
</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As AdgConnection = New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' We read all of the records for customer 300 in order to get 
  ' their net sales as well as their average yearly gross sales
  ' and returns. 
  Dim custNoKey As AdgKeyTable = myDS.NewKeyTable("RCSMastL1")
  custNoKey.Row.Item("CSCustNo") = Convert.ToDecimal(300)
  custNoKey.KeyPartCount = 1 'Only use the first field of the key.
  Dim totalSales As Decimal = 0
  Dim totalReturns As Decimal = 0
  Dim saleRecordsRead As Integer = 0
  Dim returnRecordsRead As Integer = 0
  Dim EOF As Boolean = False
  ' Because ReadSequentialEqual will return EOF If the record
  ' it immediately gets is not equal to its search key, we need
  ' to first seek to an equal record. 
  dbFile.SeekKey(SeekMode.SetLL, custNoKey)
  While Not EOF
      Try
          dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey)
          If (Convert.ToDecimal(myDS.ActiveRow.Item("CSType")) = 1) Then
              totalSales += Convert.ToDecimal(myDS.ActiveRow.Item("CSSales01")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales02")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales03")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales04")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales05")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales06")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales07")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales08")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales09")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales10")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales11")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales12"))
              saleRecordsRead = saleRecordsRead + 1
          Else
              totalReturns -= Convert.ToDecimal(myDS.ActiveRow.Item("CSSales01")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales02")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales03")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales04")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales05")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales06")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales07")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales08")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales09")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales10")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales11")) + _
                  Convert.ToDecimal(myDS.ActiveRow.Item("CSSales12"))
              returnRecordsRead = returnRecordsRead + 1
          End If
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEaEOF) Then
              EOF = True
          Else
              MsgBox("Error getting next record for customer 300:" &amp; _
                  dgEx.Message, MsgBoxStyle.OKOnly, "Error")
              'Exit procedure or end application here.
          End If
      End Try
  End While
  ' Compute additional results. 
  Dim netSales As Decimal = totalSales - totalReturns
  Dim averageSalesPerYear As Decimal

  If (saleRecordsRead &gt; 0) Then
      averageSalesPerYear = totalSales / saleRecordsRead
  Else
      averageSalesPerYear = 0
  End If
  Dim averageReturnsPerYear As Decimal
  If (returnRecordsRead &gt; 0) Then
      averageReturnsPerYear = totalReturns / returnRecordsRead
  Else
      averageReturnsPerYear = 0
  End If
  dbFile.Close()
  db.Close()
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
      [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)
      <br />
      [SeekRange Method](dcsFileAdapterClassSeekRangeMethod.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [KeyPartCount Property](dcsAdgKeyTableClassKeyPartCountProperty.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [ReadEqualMode Enumeration](dcsReadEqualModeEnumeration.html)
      <br />
      [LockRequest Enumeration](dcsLockRequestEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />

