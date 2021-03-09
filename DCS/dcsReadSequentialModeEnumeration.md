---
title: ReadSequentialMode Enumeration

Id: dcsReadSequentialModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 27

keywords: read sequential mode
keywords: Current enumeration member
keywords: First enumeration member
keywords: Last enumeration member
keywords: Next enumeration member
keywords: Previous enumeration member
keywords: ReadSequentialMode enumeration
keywords: enumerations [DCS 16.0 ReadSequentialMode

---

Defines modes of operation for the [ FileAdapter.ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) method.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum ReadSequentialMode;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum ReadSequentialMode** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum ReadSequentialMode Access(*Public)** 
      </pre>

Remarks

The **ReadSequentialMode** enumeration is used as a parameter by the [ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) method of the [FileAdapter](dcsFileAdapterClass.html) class. It defines operational modes for this method, as listed in the table below.

**ReadSequentialMode** defines values in which you can select one of the choices.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
            <colgroup span="1">
              <col span="1" width="20%" style="FONT-WEIGHT: bold" />
              <col span="1" width="60%" />
              <col span="1" width="10%" />
            </colgroup>
            <tr>
              <th>	Member</th>
              <th>	Description</th>
              <th>	Value</th>
            </tr>
            <tr>
              <td>Current
							</td>
              <td>Read the current record.
							</td>
              <td>3
							</td>
            </tr>
            <tr>
              <td>First
							</td>
              <td>Read the first record.
							</td>
              <td>5
							</td>
            </tr>
            <tr>
              <td>Last
							</td>
              <td>Read the last record.
							</td>
              <td>6
							</td>
            </tr>
            <tr>
              <td>Next
							</td>
              <td>Read the next record.
							</td>
              <td>1
							</td>
            </tr>
            <tr>
              <td>Previous
							</td>
              <td>Read the previous record.
							</td>
              <td>2
							</td>
            </tr>
</table>

Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET iSeries");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.ReadWrite; 
  AdgDataSet myDS = null;

  dbFile.OpenNewAdgDataSet(out myDS);
  /* We read the first customer for this file (customer number 100)-
   * the record is represented in myDS's active row property. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);

  /* We read the next customer for this file (customer number 200). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

  /* We read the last record in the file (should be customer number 100000). */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read);

  /* We read the previous record (which gives us customer number 99900).
   * We also lock the record. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Write);

  /* We unlock the record so that other users can view or update it. */
  dbFile.ReleaseCurrent();

  /* ... Some time passes... */

  /* We lock the current record by reading it again. */
  dbFile.ReadSequential(myDS, ReadSequentialMode.Current, LockRequest.Write);

  /* Close this file and open a different one. */
  dbFile.Close();
  dbFile.FileName = "*Libl/CSMASTERL1";
  dbFile.MemberName = "CSMASTERL1";

  dbFile.OpenNewAdgDataSet(out myDS);

  /* We read randomly to find the record for customer number 500.
   * In this file, several records may have that customer number. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCSMastL1"); //New file, so reinstantiate key table.
  keyTbl.Row["CSCustNo"] = 500;
  keyTbl.KeyPartCount = 1;
  dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

  /* Now we get customer number 80000 by setting the file pointer to
   * just past it and then reading backwards once. */
  keyTbl.Row["CSCUSTNO"] = 80000;
  dbFile.SeekKey(SeekMode.SetGT, keyTbl);
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Read);
  </pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET iSeries")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.ReadWrite
  Dim myDS As AdgDataSet = Nothing

  ' Note that exception trapping is omitted here for clearity.
  dbFile.OpenNewAdgDataSet(myDS)
  ' We read the first customer For this file (customer number 100)-
  'the record is represented in myDS's active row property. 
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read)

  ' We read the next customer For this file (customer number 200). 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)

  ' We read the last record in the file (should be customer number 100000). 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Last, LockRequest.Read)

  ' We read the previous record (which gives us customer number 99900).
  'We also lock the record. 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Write)

  ' We unlock the record so that other users can view or update it. 
  dbFile.ReleaseCurrent()

  ' ... Some time passes... 

  ' We lock the current record by reading it again. 
  dbFile.ReadSequential(myDS, ReadSequentialMode.Current, LockRequest.Write)

  ' Close this file and open a dIfferent one. 
  dbFile.Close()
  dbFile.FileName = "*Libl/CSMASTERL1"
  dbFile.MemberName = "CSMASTERL1"

  dbFile.OpenNewAdgDataSet(myDS)

  ' We read randomly to find the record For customer number 500.
  'In this file, several records may have that customer number. 
  'New file, so reinstantiate key table.
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCSMastL1")
  keyTbl.Row.Item("CSCustNo") = 500
  keyTbl.KeyPartCount = 1
  dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl)

  ' Now we get customer number 80000 by setting the file pointer to
  ' just past it and then reading backwards once.
  keyTbl.Row.Item("CSCUSTNO") = 80000
  dbFile.SeekKey(SeekMode.SetGT, keyTbl)
  dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Read)
 </pre>

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
        [ReadSequential Method](dcsFileAdapterClassReadSequentialMethod.html)
      </span>

