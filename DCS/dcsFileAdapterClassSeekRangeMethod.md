---
title: FileAdapter.SeekRange Method

Id: dcsFileAdapterClassSeekRangeMethod
TocParent: dcsFileAdapterMethods
TocOrder: 27

keywords: SeekRange method
keywords: FileAdapter.SeekRange method
keywords: RangeFirst enumeration, used by
keywords: RangeLast enumeration, used by
keywords: RangeMode enumeration, used by
keywords: enumerations [DCS 16.0 RangeFirst, used by
keywords: enumerations [DCS 16.0 RangeLast, used by
keywords: enumerations [DCS 16.0 RangeMode, used by
keywords: database files, set record pointer by key range
keywords: files, set record pointer by key range
keywords: records, set file pointer by key range
keywords: set file record pointer by key range
keywords: how to, set file record pointer by key range

---

Moves the record pointer associated with the currently open file without reading records to within a range of key values. 
<pre>
        <span class="lang">[C#]</span>
 **Public void SeekRange(
   RangeMode mode,
   AdgKeyTable firstKey,
   RangeFirst rangeFirst,
   AdgKeyTable lastKey,
   RangeLast rangeLast
);** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public Sub SeekRange( _
   ByVal mode As [RangeMode](dcsRangeModeEnumeration.html) _
   ByVal firstKey As [AdgKeyTable](dcsAdgKeyTableClass.html) _
   ByVal rangeFirst As [RangeFirst](dcsRangeFirstEnumeration.html) _
   ByVal lastKey As [AdgKeyTable](dcsAdgKeyTableClass.html) _
   ByVal rangeLast As [RangeLast](dcsRangeLastEnumeration.html) _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr SeekRange Access(*Public)
   DclSrParm mode Type(RangeMode)
   DclSrParm firstKey Type(AdgKeyTable)
   DclSrParm rangeFirst Type(RangeFirst)
   DclSrParm lastKey Type(AdgKeyTable)
   DclSrParm rangeLast Type(RangeLast)** 
      </pre>

Parameters

<dl>
        <dt>
 *mode* 
        </dt>
        <dd>[RangeMode](dcsRangeModeEnumeration.html). Specifies the manner in 
						which the file pointer is to be positioned using the specified keys. **RangeMode.First** 
						places the pointer on the record using the *firstKey*  parameter, while **RangeMode.Last**  places the pointer on the record using the *lastKey* 
						parameter. </dd>
        <dt>
 *firstKey* 
        </dt>
        <dd>An [AdgKeyTable](dcsAdgKeyTableClass.html) instance specifying a 
								key defining the lower limit of the range. </dd>
        <dt>
 *rangeFirst* 
        </dt>
        <dd>[RangeFirst](dcsRangeFirstEnumeration.html). Specifies how the *firstKey* 
										parameter is interpreted in determining the lower limit of the range. </dd>
        <dt>
 *lastKey* 
        </dt>
        <dd>An [AdgKeyTable](dcsAdgKeyTableClass.html) instance specifying a 
												key defining the upper limit of the range. </dd>
        <dt>
 *rangeLast* 
        </dt>
        <dd>[RangeLast](dcsRangeLastEnumeration.html). Specifies how the *lastKey* 
			parameter is interpreted in determining the upper limit of the range.</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
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

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
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
            <td colspan="1" rowspan="1">dgEOLDSERVER
						</td>
            <td colspan="1" rowspan="1">

The operation is not supported by the version of the database provider of the [AdgConnection](dcsAdgConnectionClass.html) object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">dgEaEOF
						</td>
            <td colspan="1" rowspan="1">The record access operation resulted in an end-of-file condition.
						</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">dgEaNOTFND
						</td>
            <td colspan="1" rowspan="1">No record could be found with the specified key. The record may have been 
							deleted, it may never have existed, or the key may have been changed.
						</td>
          </tr>
</table>

Remarks

The [ReadRange](dcsFileAdapterClassReadRangeMethod.html) and **SeekRange** methods initiate a "range mode" for accessing records from an open file. Under this mode, subsequent **FileAdapter** sequential read methods ([ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) and [ReadSequentialEqual](dcsFileAdapterClassReadSequentialEqualMethod.html)) restrict access to only records with keys that fall in the range specified by the key parameters. This mode allows DCS programs to more efficiently access a certain set of records, especially when combined with the network record blocking feature (see [FileOpenAttr.BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html)).

The *firstKey* and *lastKey* parameters specify the range, along with the *rangeFirst* and *rangeLast* mode parameters. If the *lastKey* value specifies a key value which sorts prior to the *firstKey* value, the range specifies an empty set of records. Special values for the *rangeFirst* and *rangeLast* parameters allow the range to be extended to the beginning of the file ( **RangeFirst.To** ) and the end of the file ( **RangeLast.Bottom** ). When one of these values is specified, the corresponding key value parameter is ignored.

**SeekRange** positions the file cursor on the first or last record in the range, as specified by the *mode* parameter ( **RangeMode.First** or **RangeMode.Last** , respectively). If the range specifies an empty set of records, this method throws dgException with the Error property set to dgEaNOTFND.

Note that if **FileAdapter** was already in range mode, this method will cancel it and initiate a new range mode as specified.
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

  /* The code below will find all of the sales for all 
   * customers with a number from 300 to 1400, 
   * and read all the customer numbers from lowest to highest. */
  AdgKeyTable key1 = myDS.NewKeyTable("RCSMASTL1");
  key1.Row["CSCUSTNO"] = Convert.ToDecimal(300);
  key1.KeyPartCount = 1;
  AdgKeyTable key2 = myDS.NewKeyTable("RCSMASTL1");
  key2.Row["CSCUSTNO"] = Convert.ToDecimal(1400);
  key2.KeyPartCount = 1;
  dbFile.SeekRange(RangeMode.First, key1, RangeFirst.Include, key2, RangeLast.Include);

  /* Read until we go past record 1421. */
  bool EOF = false;
  decimal Total = 0;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          for (int j=1; j &lt;= 12; j++)
          {
              string number = j.ToString();
              if (number.Length &lt; 2)
                  number = "0" + number;
              Total += Convert.ToDecimal(myDS.ActiveRow["CSSALES" + number]); 
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              throw dgEx; //Throw exception if we didn't expect it.
          }
      }
  }
  MessageBox.Show("Total sales for customers 300 to 1400 totalled " 
      + Total.ToString() + ".", "Result");

  dbFile.Close();
  db.Clone();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' The code below will find all of the sales for all 
  ' customers with a number from 300 to 1400, 
  ' and read all the customer numbers from lowest to highest. 
  Dim key1 As AdgKeyTable = myDS.NewKeyTable("RCSMASTL1")
  key1.Row.Item("CSCUSTNO") = Convert.ToDecimal(300)
  key1.KeyPartCount = 1
  Dim key2 As AdgKeyTable = myDS.NewKeyTable("RCSMASTL1")
  key2.Row.Item("CSCUSTNO") = Convert.ToDecimal(1400)
  key2.KeyPartCount = 1
  dbFile.SeekRange(RangeMode.First, key1, RangeFirst.Include, key2, RangeLast.Include)

  ' Read until we go past record 1421. 
  Dim EOF As Boolean = False
  Dim Total As Decimal = 0
  While Not EOF
      Try
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait)
          For j As Integer = 1 To 12
              Dim number As String = j.ToString()
              If number.Length &lt; 2 Then
                  number = "0" + number
              End If
              Total += Convert.ToDecimal(myDS.ActiveRow.Item("CSSALES" + number))
          Next
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEaEOF) Then
              EOF = True
          Else
              Throw dgEx 'Throw exception If we didn't expect it.
          End If
      End Try
  End While
  MsgBox("Total sales for customers 300 to 1400 totalled " &amp; _
  Total.ToString() + ".")

  dbFile.Close()
  db.Clone()</pre>

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
      [ReadSequential Method](dcsFileAdapterClassReadSequentialMethod.html)
      <br />
      [ReadSequentialEqual 
					Method](dcsFileAdapterClassReadSequentialEqualMethod.html)
      <br />
      [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [BlockingFactor Property](dcsFileOpenAttrClassBlockingFactorProperty.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [RangeMode Enumeration](dcsRangeModeEnumeration.html)
      <br />
      [RangeFirst Enumeration](dcsRangeFirstEnumeration.html)
      <br />
      [RangeLast Enumeration](dcsRangeLastEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

