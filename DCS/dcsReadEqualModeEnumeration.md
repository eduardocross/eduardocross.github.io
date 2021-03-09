---
title: ReadEqualMode Enumeration

Id: dcsReadEqualModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 25

keywords: NextEqual enumeration member
keywords: PreviousEqual enumeration member
keywords: ReadEqualMode enumeration
keywords: enumerations [DCS 16.0 ReadEqualMode

---

Defines modes of operation for the [ FileAdapter.ReadSequentialEqual](dcsFileAdapterClassReadSequentialEqualMethod.html) method.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum RangeEqualMode;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum RangeEqualMode** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum RangeEqualMode Access(*Public)** 
      </pre>

Remarks

<span>ReadEqualMode</span> defines modes for [FileAdapter.ReadSequentialEqual](dcsFileAdapterClassReadSequentialEqualMethod.html) as listed in the table below.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
            <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col align="middles" span="1" width="10%" />
            <tr>
              <th>	Member</th>
              <th>	Description</th>
              <th>	Value</th>
            </tr>
            <tr>
              <td>NextEqual
							</td>
              <td>Read the next record.
							</td>
              <td>17
							</td>
            </tr>
            <tr>
              <td>PreviousEqual
							</td>
              <td>Read the previous record. If the file has just been opened, get the last 
								record.
							</td>
              <td>18
							</td>
            </tr>
</table>

Examples

<pre class="prettyprint">
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
  custNoKey.KeyPartCount = 1;
  decimal totalSales = 0;
  decimal totalReturns = 0;
  int saleRecordsRead = 0;
  int returnRecordsRead = 0;
  bool EOF = false;
  dbFile.SeekKey(SeekMode.SetLL, custNoKey);
  while(!EOF)
  {
      try
      {
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
      catch(dgException dgEx)
      {
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
  decimal averageSalesPerYear = totalSales / saleRecordsRead;
  decimal averageReturnsPerYear = totalReturns / returnRecordsRead;
  if (saleRecordsRead &gt; 0)
      averageSalesPerYear = totalSales / saleRecordsRead;
  else
      averageSalesPerYear = 0;
  if (returnRecordsRead &gt; 0)
      averageReturnsPerYear = totalReturns / returnRecordsRead;
  else
      averageReturnsPerYear = 0; </pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CSMASTERL1", "CSMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' We read all of the records For customer 300 in order to get 
  'their net sales as well as their average yearly gross sales
  'and returns. 
  Dim custNoKey As AdgKeyTable = myDS.NewKeyTable("RCSMastL1")
  custNoKey.Row.Item("CSCustNo") = Convert.ToDecimal(300)
  custNoKey.KeyPartCount = 1
  Dim totalSales As Decimal = 0
  Dim totalReturns As Decimal = 0
  Dim saleRecordsRead As Integer = 0
  Dim returnRecordsRead As Integer = 0
  Dim EOF As Boolean = False
  dbFile.SeekKey(SeekMode.SetLL, custNoKey)
  While Not EOF
      Try
          dbFile.ReadSequentialEqual(myDS, ReadEqualMode.NextEqual, LockRequest.Read, custNoKey)
          If Convert.ToDecimal(myDS.ActiveRow.Item("CSType")) = 1 Then
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
          If dgEx.Error = dgErrorNumber.dgEaEOF Then
              EOF = True
          Else
              MsgBox("Error getting next record For customer 300:" &amp; _
                  dgEx.Message, MsgBoxStyle.Critical, "Error")
              'Exit procedure or end application here.
          End If
      End Try
      ' Compute additional results. 
  End While
  Dim netSales As Decimal = totalSales - totalReturns
  Dim averageSalesPerYear As Decimal
  Dim averageReturnsPerYear As Decimal
  If saleRecordsRead &gt; 0 Then
      averageSalesPerYear = totalSales / saleRecordsRead
  Else
      averageSalesPerYear = 0
  End If
  If returnRecordsRead &gt; 0 Then
      averageReturnsPerYear = totalReturns / returnRecordsRead
  Else
      averageReturnsPerYear = 0
  End If</pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter.ReadSequentialEqual 
					Method](dcsFileAdapterClassReadSequentialEqualMethod.html) <br />[ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

