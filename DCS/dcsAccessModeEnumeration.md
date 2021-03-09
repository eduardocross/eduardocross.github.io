---
title: AccessMode Enumeration

Id: dcsAccessModeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 0

keywords: AccessMode enumeration
keywords: enumerations [DCS 16.0 AccessMode
keywords: access mode constants
keywords: database files, access mode constants
keywords: files, access mode constants
keywords: database files, restrict access constants
keywords: files, restrict access constants
keywords: Arrival enumeration member
keywords: CacheWrites enumeration member
keywords: Change enumeration member
keywords: CommitmentControl enumeration member
keywords: Delete enumeration member
keywords: PrintPreview enumeration member
keywords: Read enumeration member
keywords: ReadWrite enumeration member
keywords: ReadWriteCache enumeration member
keywords: RWCD enumeration member
keywords: RWCDCache enumeration member
keywords: Write enumeration member
keywords: WriteCache enumeration member

---

Options for restricting access to open files.<span style="MARGIN-BOTTOM: 0.8em" />
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum AccessMode;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum AccessMode** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum AccessMode Access(*Public)** 
      </pre>

Remarks

**AccessMode** defines flag values which can be used alone or combined to create a custom value to suit an application’s requirements for accessing a particular file. Many common combinations, such as ReadWrite and <span>RWCD</span>, are predefined by the enumeration.

The [AccessMode](dcsFileAdapterClassAccessModeProperty.html) property of <span> **FileAdapter** </span> contains a value of AccessMode, which should be set prior to calling <span> **FileAdapter’s** </span>[Open](dcsFileAdapterClassOpenMethod.html), [ OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html), or [ OpenSimpleQuery](dcsFileAdapterClassOpenSimpleQueryMethod.html) to provide the requested access restrictions on the opened file. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col span="1" width="10%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Arrival
</td>
            <td colspan="1" rowspan="1">

Records are read from the file in relative record order (where supported).
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

CacheWrites
</td>
            <td colspan="1" rowspan="1">

<p>A file’s data buffers are not written immediately to disk after each Add, Delete or Update operation. The target machine's inherent caching is enabled.
</td>
            <td colspan="1" rowspan="1">

32
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Change
</td>
            <td colspan="1" rowspan="1">

Records in the file may be updated (changed).
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

CommitmentControl
</td>
            <td colspan="1" rowspan="1">

The file is enabled for Commitment Control.
</td>
            <td colspan="1" rowspan="1">

16
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Delete
</td>
            <td colspan="1" rowspan="1">

Records in the file may be deleted.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OutPut
</td>
            <td colspan="1" rowspan="1">

Reserved for future use.
</td>
            <td colspan="1" rowspan="1">

76
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OutPutCache
</td>
            <td colspan="1" rowspan="1">

Reserved for future use.
</td>
            <td colspan="1" rowspan="1">

108
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

PrintPreview
</td>
            <td colspan="1" rowspan="1">

PrinterFile output can be previewed prior to printing.
</td>
            <td colspan="1" rowspan="1">

256
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Read
</td>
            <td colspan="1" rowspan="1">

Records may be read from the file.
</td>
            <td colspan="1" rowspan="1">

128
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ReadWrite
</td>
            <td colspan="1" rowspan="1">

Records may be read from the file and new records may be added. (Read + Write).
</td>
            <td colspan="1" rowspan="1">

192
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ReadWriteCache
</td>
            <td colspan="1" rowspan="1">

Records may be read from the file and new records may be added. The target machine's inherent caching is enabled for added records. (Read + Write + CacheWrites).
</td>
            <td colspan="1" rowspan="1">

224
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

RWCD
</td>
            <td colspan="1" rowspan="1">

Records in the file may be read, updated, deleted and added. (Read + Change + Delete + Write).
</td>
            <td colspan="1" rowspan="1">

204
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

RWCDCache
</td>
            <td colspan="1" rowspan="1">

Records in the file may be read, updated, deleted and added. The target machine's inherent caching is enabled for added, deleted and changed records. (Read + Change + Delete + Write + CacheWrites).
</td>
            <td colspan="1" rowspan="1">

236
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Write
</td>
            <td colspan="1" rowspan="1">

New records may be added to the file.
</td>
            <td colspan="1" rowspan="1">

64
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WriteCache 
</td>
            <td colspan="1" rowspan="1">

Only new records may be added to a File and they are not written immediately to disk after each Add operation. The target machine's inherent caching is enabled. (Write + CacheWrites).
</td>
            <td colspan="1" rowspan="1">

96
</td>
          </tr>
</table>

Examples 

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  /* We need to open this file for Read as well as as Delete
   * in order search for the key value. */
  dbFile.AccessMode = AccessMode.Delete | AccessMode.Read;

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

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 82900;
  try
  {
      dbFile.DeleteKey(keyTbl);
  }
  catch(dgException dgEx)
  {
      /* We catch the dgException only if it was caused by
       * the key value not being found. */
      if (dgEx.Error != dgErrorNumber.dgEaNOTFND)
          throw dgEx;
  }
  dbFile.Close();
  db.Close();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  ' We need to open this file For Read as well as as Delete
  ' in order search For the key value. 
  dbFile.AccessMode = AccessMode.Delete Or AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, "Error")
      'Exit procedure or end application here.
  End Try

  ' We retrieve the record For customer number 82900 and delete it! 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  keyTbl.Row.Item("CMCUSTNO") = 82900
  Try
      dbFile.DeleteKey(keyTbl)
  Catch dgEx As dgException
      ' We catch the dgException only if it was caused by
      ' the key value not being found.
      If dgEx.Error &lt;&gt; dgErrorNumber.dgEaNOTFND Then
          Throw dgEx
      End If
  End Try

  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) <span style="FONT-SIZE: 8pt; FONT-FAMILY: Verdana"> <p /></span> 

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [File Adapter Class](dcsFileAdapterClass.html)
      <br />
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [OpenSimpleQuery Method](dcsFileAdapterClassOpenSimpleQueryMethod.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

