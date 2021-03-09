---
title: FileAdapter.SeekKey Method

Id: dcsFileAdapterClassSeekKeyMethod
TocParent: dcsFileAdapterMethods
TocOrder: 26

keywords: SeekKey method
keywords: FileAdapter.SeekKey method
keywords: SeekMode enumeration, used by
keywords: enumerations [DCS 16.0 SeekMode, used by
keywords: database files, set record pointer by key
keywords: files, set record pointer by key
keywords: records, set file pointer by key
keywords: set file record pointer by key
keywords: how to, set file record pointer by key

---

Moves the record pointer associated with the currently open file without reading records to within a range of key values.
<pre>
        <span class="lang">[C#]</span>
 **Public void SeekKey(
   SeekMode mode,
   AdgKeyTable keyTable
);** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **public Sub SeekKey( _
   ByVal mode As [SeekMode](dcsSeekModeEnumeration.html) _
   ByVal keyTable As [AdgKeyTable](dcsAdgKeyTableClass.html)
.)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr SeekKey Access(*Public)
   DclSrParm mode Type(SeekMode)
   DclSrParm keyTable Type(AdgKeyTable)** 
      </pre>

Parameters

<dl>
        <dt>
 *mode* 
        </dt>
        <dd>[SeekMode](dcsSeekModeEnumeration.html). Specifies the manner in 
						which the record is to be located using the specified key. </dd>
        <dt>
 *keyTable* 
        </dt>
        <dd>A [AdgKeyTable](dcsAdgKeyTableClass.html)  object containing the 
				key used to seek for a record.
							</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0">
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

The record access operation resulted in an end-of-file condition. This exception also occurs when the record access operation would place the current file position outside of the boundaries established by a prior [ ReadRange](dcsFileAdapterClassReadRangeMethod.html) or [SeekRange](dcsFileAdapterClassSeekRangeMethod.html) method call.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaNOTFND
</td>
            <td colspan="1" rowspan="1">

The record to be accessed was not found. It may have been deleted, it may never have existed, or the key may have been changed. If *mode* is **SetGT** or **SetLL** , the file pointer is also placed at the end of the file.
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
</table>

Remarks

**SeekKey** positions the file pointer to a particular record using the specified *keyTable* and *mode* as a point of reference. The record pointed to by **SeekKey** will contain a key value equal to, greater than or equal to, or greater than the specified *keyTable* parameter, dependent on the value of the *mode* parameter. Optionally, the file pointer may be placed on the first or last record of the file, by specifying a *mode* value of **SeekMode.First** or **SeekMode.Last** , respectively. If the record sought does not exist in the file, the method throws dgException with an Error property value of dgEaNOTFND.

When **SeekMode.SetLL** or **SeekMode.SetGT** values for *mode* are specified and the record sought is not found, the file pointer is placed at the end of the file, and then dgException is thrown.

Calling this method cancels "range mode". A prior successful call to **ReadRange** or **SeekRange** places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed. This method cancels the restriction.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* Seek the file pointer to just before Customer number 1500. */
  AdgKeyTable key = myDS.NewKeyTable("RCMMASTL1");
  key.Row["CMCustNo"] = Convert.ToDecimal(1500);
  dbFile.SeekKey(SeekMode.SetLL, key);
  /* We read the next record to get customer number 1500.*/
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName1 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to just after customer number 2000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2000);
  dbFile.SeekKey(SeekMode.SetGT, key);
  /* We read backwards one record to get customer number 2000. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
  string CustomerName2 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 2979. */
  key.Row["CMCustNo"] = Convert.ToDecimal(2979);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 2979 usually does not exist, so we should be on record
  * 3000, which we read by reading the current record (using
  * SeekMode.SetLL would have gotten us record 2900). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName3 = myDS.ActiveRow["CMName"].ToString();

  /* We set the file pointer to greater than or equal to 4000. */
  key.Row["CMCustNo"] = Convert.ToDecimal(4000);
  dbFile.SeekKey(SeekMode.SetGE, key);
  /* Record 4000 does exist, and by reading the next record we should access it. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
  string CustomerName4 = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' Seek the file pointer to just before Customer number 1500. 
  Dim key As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  key.Row.Item("CMCustNo") = Convert.ToDecimal(1500)
  dbFile.SeekKey(SeekMode.SetLL, key)
  ' We read the next record to get customer number 1500.
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default)
  Dim CustomerName1 As String
  CustomerName1 = myDS.ActiveRow.Item("CMName").ToString()

  ' We set the file pointer to just after customer number 2000. 
  key.Row.Item("CMCustNo") = Convert.ToDecimal(2000)
  dbFile.SeekKey(SeekMode.SetGT, key)
  ' We read backwards one record to get customer number 2000. 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default)
  Dim CustomerName2 As String
  CustomerName2 = myDS.ActiveRow.Item("CMName").ToString()

  ' We set the file pointer to greater than or equal to 2979. 
  key.Row.Item("CMCustNo") = Convert.ToDecimal(2979)
  dbFile.SeekKey(SeekMode.SetGE, key)
  ' Record 2979 usually does not exist, so we should be on record
  ' 3000, which we read by reading the current record (using
  ' SeekMode.SetLL would have gotten us record 2900). 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default)
  Dim CustomerName3 As String
  CustomerName3 = myDS.ActiveRow.Item("CMName").ToString()

  ' We set the file pointer to greater than or equal to 4000. 
  key.Row.Item("CMCustNo") = Convert.ToDecimal(4000)
  dbFile.SeekKey(SeekMode.SetGE, key)
  ' Record 4000 does exist, and by reading the next record we should access it. 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default)
  Dim CustomerName4 As String
  CustomerName4 = myDS.ActiveRow.Item("CMName").ToString()

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
      [SeekMode Enumeration](dcsSeekModeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

