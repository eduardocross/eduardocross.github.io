---
title: RangeFirst Enumeration

Id: dcsRangeFirstEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 22

keywords: Exclude enumeration member
keywords: Include enumeration member
keywords: Top enumeration member
keywords: RangeFirst enumeration
keywords: enumerations [DCS 16.0 RangeFirst

---

Defines parameter values for [FileAdapter](dcsFileAdapterClass.html) range access methods.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum RangeFirst;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum RangeFirst** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum RangeFirst Access(*Public)** 
      </pre>

#### Remarks
**RangeFirst** enumeration values modify the usage of key value parameters describing the lower limit of a range in **FileAdapter** range access methods. For example, specifying *Exclude* for the **RangeFirst** parameter indicates that the lower limit of the range should not include records whose key value is equal to the "first key" parameter. Note that the *Top* value indicates that the lower limit should always include the first record of the file (and thus the "first key" parameter can be ignored).

**RangeFirst** is specified as a parameter for the [ DeleteRange](dcsFileAdapterClassDeleteRangeMethod.html), [ReadRange](dcsFileAdapterClassReadRangeMethod.html), and [SeekRange](dcsFileAdapterClassSeekRangeMethod.html) methods of [ FileAdapter](dcsFileAdapterClass.html).

**RangeFirst** defines values in which you can select one of the choices.
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

Exclude
</td>
            <td >

Exclude the first record in the range.
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

Include the first record in the range.
</td>
            <td >

1
</td>
          </tr>
          <tr>
            <td >

Top
</td>
            <td >

Start at the top of the file.
</td>
            <td >

2
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
  dbFile.AccessMode = AccessMode.RWCD;

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

  /* We erase all records with a customer number equal to
   * or greater than 5000 and less than, but not
   * equal to, 6000. */
  AdgKeyTable OneKey = myDS.NewKeyTable("RCMMastL1");
  OneKey.Row["CMCustNo"] = 5000;
  AdgKeyTable TwoKey = myDS.NewKeyTable("RCMMastL1");
  TwoKey.Row["CMCustNo"] = 6000;
  try
  {
      dbFile.DeleteRange(OneKey, RangeFirst.Include, TwoKey, RangeLast.Exclude);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting records 5000-6000 :" +
          dgEx.Message, "Error");
  }

  dbFile.Close();
  db.Close();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.RWCD

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, "Error")
      'Exit procedure or end application here.
  End Try

  ' We erase all records with a customer number equal to
  ' or greater than 5000 and less than, but not
  ' equal to, 6000. 
  Dim OneKey As AdgKeyTable = myDS.NewKeyTable("RCMMastL1")
  OneKey.Row.Item("CMCustNo") = 5000
  Dim TwoKey As AdgKeyTable = myDS.NewKeyTable("RCMMastL1")
  TwoKey.Row.Item("CMCustNo") = 6000
  Try
      dbFile.DeleteRange(OneKey, RangeFirst.Include, TwoKey, RangeLast.Exclude)
  Catch dgEx As dgException
      MsgBox("Error deleting records 5000-6000 :" &amp; _
          dgEx.Message, MsgBoxStyle.Critical, "Error")
  End Try

  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

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
      </span>
      <br />
      <span>
        [ReadRange Method](dcsFileAdapterClassReadRangeMethod.html)
        <br />
      </span>
      <span>
        [SeekRange Method](dcsFileAdapterClassSeekRangeMethod.html)
      </span>

