---
title: ReadRandomMode Enumeration

Id: dcsReadRandomModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 26

keywords: read random mode
keywords: Equal enumeration member
keywords: Greater enumeration member
keywords: GTEQ enumeration member
keywords: ReadRandomMode enumeration
keywords: enumerations [DCS 16.0 ReadRandomMode

---

Defines modes of operation for the [ FileAdapter.ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html) and [ FileAdapter.ReadRandomRRN](dcsFileAdapterClassReadRandomRRNMethod.html) methods.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum ReadRandomMode;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum ReadRandomMode** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum ReadRandomMode Access(*Public)** 
      </pre>

Remarks

The ReadRandomMode Enumeration&gt; enumeration is used as a parameter by the [ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html) and [ReadRandomRRN](dcsFileAdapterClassReadRandomRRNMethod.html) methods of the [FileAdapter](dcsFileAdapterClass.html) class. It defines operational modes for these methods as listed in the table below.

ReadRandomMode Enumeration defines values in which you can select one of the choices.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
            <colgroup span="1">
              <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
              <col span="1" width="60%" />
              <col align="middles" span="1" width="10%" />
            </colgroup>
            <tr>
              <th>		Member</th>
              <th>		Description</th>
              <th>		Value</th>
            </tr>
            <tr>
              <td >Equal
								</td>
              <td >Find the first record with key (or RRN) equal to the search argument.
								</td>
              <td >13
								</td>
            </tr>
            <tr>
              <td >Greater
								</td>
              <td >Find the first record with key (or RRN) greater than the Search argument.
								</td>
              <td >14
								</td>
            </tr>
            <tr>
              <td >GTEQ
								</td>
              <td >Find the first record with key (or RRN) greater than or equal to the Search 
									argument.
								</td>
              <td >15
								</td>
            </tr>
</table>

Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL2", "CMMASTERL2");
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

  /* We retrieve the record for customer "Rand Of Distribix Fl Varnish"... */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL2");
  keyTbl.Row["CMNAME"] = "Rand Of Distribix Fl Varnish";
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
      /*... and delete it! */
      dbFile.DeleteCurrent();
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting the record: " + dgEx.Message,
      dgEx.Error.ToString());
  }</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL2", "CMMASTERL2")
  dbFile.AccessMode = AccessMode.RWCD

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, "Error")
      'Exit procedure or end application here.
  End Try

  ' We retrieve the record For customer "Rand Of Distribix Fl Varnish"... 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL2")
  keyTbl.Row.Item("CMNAME") = "Rand Of Distribix Fl Varnish"
  Try
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl)
      '... and delete it! 
      dbFile.DeleteCurrent()
  Catch dgEx As dgException
      MsgBox("Error deleting the record: " &amp; dgEx.Message, _
      MsgBoxStyle.Critical, dgEx.Error.ToString())
  End Try</pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      <span>
        [FileAdapter Class](dcsFileAdapterClass.html)
        <br />
      </span>
      <span>
        [ReadRandomKey Method](dcsFileAdapterClassReadRandomKeyMethod.html)
        <br />
      </span>
      <span>
        [ReadRandomRRN Method](dcsFileAdapterClassReadRandomRRNMethod.html)
      </span>

