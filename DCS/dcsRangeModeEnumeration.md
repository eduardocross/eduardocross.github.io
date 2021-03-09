---
title: RangeMode Enumeration

Id: dcsRangeModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 24

keywords: First enumeration member
keywords: Last enumeration member
keywords: RangeMode enumeration
keywords: enumerations [DCS 16.0 RangeMode

---

For [FileAdapter](dcsFileAdapterClass.html) range methods, defines how to access the first record in the range.
<pre class="syntax">
        <span class="lang">[C#]</span>
 **public enum RangeMode;** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual Basic] </span>
 **public Enum RangeMode** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual RPG]</span>
 **BegEnum RangeMode Access(*Public)** 
      </pre>

Remarks

<span> **RangeMode** </span> is used as a parameter for the **FileAdapter** methods which establish a range: [ReadRange](dcsFileAdapterClassReadRangeMethod.html) and [SeekRange](dcsFileAdapterClassSeekRangeMethod.html). In addition to establishing the range, these methods position the file to one end of the range based on the value of <span> **RangeMode** </span>.

For <span> **ReadRange** </span>, **RangeMode** determines whether to read the first or last record in the range.

For <span> **SeekRange** </span>, **RangeMode** determines whether to locate the file cursor on the first or last record in the range.

<span> **RangeMode** </span> defines values in which you can select one of the choices.
Members

<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col align="middles" span="1" width="10%" />
          </colgroup>
          <tr>
            <th>	Member</th>
            <th>	Description</th>
            <th>	Value</th>
          </tr>
          <tr>
            <td>

First
</td>
            <td>

The first record in a range to access.
</td>
            <td>

5
</td>
          </tr>
          <tr>
            <td>

Last
</td>
            <td>

The last record in a range to access.
</td>
            <td>

6
</td>
          </tr>
</table>

Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

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

  /* We read all records with a customer number greater
   * than, but not equal to 6000 and less than or equal
   * to, 7000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 10000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 40000;

  try
  {
      dbFile.ReadRange(myDS, RangeMode.First, 
      LockRequest.Read, OneKey, 
      RangeFirst.Exclude, TwoKey,
      RangeLast.Include);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error getting records 10000-40000 :" +
          dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  int totalSum = 0;
  int activeSum = 0;
  bool EOF = false;
  while(!EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait);
          if (Convert.ToChar(myDS.ActiveRow["CMActive"]) == '1')
              activeSum ++;
          totalSum ++;
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
          {
              //Exit procedure or end application here.
          }
      }
  }
  if (totalSum &gt; 0)
  {
      string percent = Convert.ToString((Convert.ToDecimal(activeSum)
          /Convert.ToDecimal(totalSum)) * 100);
      percent = percent.Substring(0, percent.IndexOf('.'));
      MessageBox.Show(percent + "% of the customers sampled are active.");
  }
  else
      MessageBox.Show("Unable to access any customers!");
  dbFile.Close();
  db.Close(); </pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, "Error")
      'Exit procedure or end application here.
  End Try

  ' We read all records with a customer number greater
  'than, but not equal to 6000 and less than or equal
  'to, 7000. 
  Dim OneKey As AdgKeyTable = myDS.NewKeyTable("RCMMastL1")
  OneKey.Row.Item("CMCustNo") = 10000
  Dim TwoKey As AdgKeyTable = myDS.NewKeyTable("RCMMastL1")
  TwoKey.Row.Item("CMCustNo") = 40000

  Try
      dbFile.ReadRange(myDS, RangeMode.First, _
          LockRequest.Read, OneKey, _
          RangeFirst.Exclude, TwoKey, _
          RangeLast.Include)
  Catch dgEx As dgException
      MsgBox("Error getting records 10000-40000 :" &amp; _
          dgEx.Message, "Error")
      'Exit procedure or end application here.
  End Try

  Dim totalSum As Integer = 0
  Dim activeSum As Integer = 0
  Dim EOF As Boolean = False
  While Not EOF
      Try
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait)
          If Convert.ToChar(myDS.ActiveRow.Item("CMActive")) = "1" Then
             activeSum = activeSum + 1
          End If
          totalSum = totalSum + 1
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEaEOF) Then
              EOF = True
          Else
              'Exit procedure or end application here.
          End If
      End Try
  End While

  If (totalSum &gt; 0) Then
      Dim percent As String
      percent = Convert.ToString((Convert.ToDecimal(activeSum) _
           / Convert.ToDecimal(totalSum)) * 100)
      percent = percent.Substring(0, percent.IndexOf("."))
      MsgBox(percent &amp; "% of the customers sampled are active.")
  Else
      MsgBox("Unable to access any customers!")
  End If
  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [SeekRange Method](dcsFileAdapterClassSeekRangeMethod.html)
      <br />
      [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)

