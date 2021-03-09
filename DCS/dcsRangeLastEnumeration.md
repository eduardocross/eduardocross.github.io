---
title: RangeLast Enumeration

Id: dcsRangeLastEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 23

keywords: Bottom enumeration member
keywords: Exclude enumeration member
keywords: Include enumeration member
keywords: SameAsFirst enumeration member
keywords: RangeLast enumeration
keywords: enumerations [DCS 16.0 RangeLast

---

Defines parameter values for [FileAdapter](dcsFileAdapterClass.html) range access methods.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum RangeLast;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum RangeLast** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum RangeLast Access(*Public)**  </pre>

Remarks

**RangeLast** enumeration values modify the usage of key value parameters describing the upper limit of a range in **FileAdapter** range access methods. For example, specifying *Include* for the **RangeLast** parameter indicates that the upper limit of the range should include records whose key value is equal to the "last key" parameter. Note that the *Bottom* value indicates that the upper limit should always include the last record of the file (and thus the "last key" parameter can be ignored).

**RangeLast** is specified as a parameter for the [ DeleteRange](dcsFileAdapterClassDeleteRangeMethod.html), [ReadRange](dcsFileAdapterClassReadRangeMethod.html), and [SeekRange](dcsFileAdapterClassSeekRangeMethod.html) methods of FileAdapter. 

**RangeLast** defines values in which you can select one of the choices.
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
            <td >

Bottom
</td>
            <td >

The bottom or last record in the file.
</td>
            <td >

4
</td>
          </tr>
          <tr>
            <td >

Exclude
</td>
            <td >

Exclude the last record in the range.
</td>
            <td >

0
</td>
          </tr>
          <tr>
            <td >

Include
</td>
            <td >

Include the last record in the range.
</td>
            <td >

1
</td>
          </tr>
          <tr>
            <td >

SameAsFirst
</td>
            <td >

The same record as specified in the RangeFirst parameter of the DeleteRange or ReadRange methods.
</td>
            <td >

8
</td>
          </tr>
</table>

Examples

<pre class="prettyprint">
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

  MessageBox.Show(Convert.ToDecimal((activeSum/totalSum) * 100) + 
      "% of the customers sampled are active.");
  dbFile.Close();
  db.Close(); </pre>
      <pre class="prettyprint">
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
  ' than, but not equal to 6000 and less than or equal
  ' to, 7000. 
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
          dgEx.Message, MsgBoxStyle.Critical, "Error")
      'Exit procedure or end application here.
  End Try

  Dim totalSum As Integer = 0
  Dim activeSum As Integer = 0
  Dim EOF As Boolean = False
  While Not EOF
      Try
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoWait)
          If (Convert.ToChar(myDS.ActiveRow.Item("CMActive")) = "1") Then
              activeSum = activeSum + 1
              totalSum = totalSum + 1
          End If
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEaEOF) Then
              EOF = True
          Else
              'Exit procedure or end application here.
          End If
      End Try
  End While

  MsgBox(Convert.ToDecimal((activeSum / totalSum) * 100) &amp; _
      "% of the customers sampled are active.")
  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      <span>
        [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
        <br />
        [DeleteRange Method](dcsFileAdapterClassDeleteRangeMethod.html)
        <br />
        [FileAdapter Class](dcsFileAdapterClass.html)
        <br />
      </span>
      <span>
        [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)
        <br />
      </span>
      <span>
        [SeekRange Method](dcsFileAdapterClassSeekRangeMethod.html)
      </span>

