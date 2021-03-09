---
title: FileLocks Enumeration

Id: dcsFileLocksEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 14

keywords: FileLocks enumeration
keywords: enumerations DCS 16.0 FileLocks
keywords: Auto enumeration member
keywords: Manual enumeration member
keywords: record locking mode constants
keywords: database files, record locking mode constants
keywords: files, record locking mode constants

---

Defines modes on how a file will be locked; either automatically or manually. 
<pre>        <span class="lang">[C#]</span>
 **public enum FileLocks;** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Enum FileLocks** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum FileLocks Access(*Public)** 
      </pre>

Remarks

The <span> **FileLocks** </span> enumeration is used as a parameter by the [ FileLocks](dcsFileOpenAttrClassFileLocksProperty.html) property of the [FileOpenAttr](dcsFileOpenAttrClass.html) class.

When set to the <code>Manual</code> value, record locking in the opened file will only occur if explicitly specified in the [FileAdapter](dcsFileAdapterClass.html) access method. Also, records locked in access methods can only be unlocked explicitly with the [ReleaseCurrent](dcsFileAdapterClassReleaseCurrentMethod.html) or [ReleaseRRN](dcsFileAdapterClassReleaseRRNMethod.html) methods.

When set to the <code>Auto</code> value, record locking occurs automatically in <span> **FileAdapter** </span> methods, unless overridden by the [LockRequest](dcsLockRequestEnumeration.html) parameter. Also, locked records are automatically unlocked when another record is accessed.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="30%" />
            <col span="1" width="5%" />
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
            <td colspan="1" rowspan="1" style="height: 43px">

Auto 
</td>
            <td colspan="1" rowspan="1" style="height: 43px">

The file will be locked automatically. 
</td>
            <td colspan="1" rowspan="1" style="height: 43px">

1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Manual 
</td>
            <td colspan="1" rowspan="1">

The file will be locked manually. 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
</table>

Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Using the FileLocks property of a FileAdapter's OpenAttributes,
   * you can set file locking to manual, which allows you to lock more
   * than one record at a time. Note that manual file locking
   * is database dependent- for instance, it will work with a Acceler8
   * database but not with an IBM i. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual;
  dbFile.AccessMode = AccessMode.RWCD;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");

  /* In the code below, we read records for customer numbers
   * 400 - 800. When it ends, we will still have locks on customer numbers
   * 500 and 700. */
  try
  {
      /* Read customer number 400 but don't lock it. */
      keyTbl.Row["CMCUSTNO"] = 400;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);

      /* Read customer number 500 and lock it. */
      keyTbl.Row["CMCUSTNO"] = 500;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl);

      /* Read customer number 600 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 700 and lock it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read);

      /* Read customer number 800 without locking it. */
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);

      /* Unlock customer number 600. */
      keyTbl.Row["CMCUSTNO"] = 600;
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl);
      dbFile.ReleaseCurrent();

  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Couldn't find one or more records. " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close(); /* Release all locks. */
  db.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Using the FileLocks property of a FileAdapter's OpenAttributes,
  ' you can set file locking to manual, which allows you to lock more
  ' than one record at a time. Note that manual file locking
  ' is database dependent- For instance, it will work with a Acceler8
  ' database but not with an IBM i. 
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.OpenAttributes.FileLocks = FileLocks.Manual
  dbFile.AccessMode = AccessMode.RWCD

  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")

  ' In the code below, we read records For customer numbers
  ' 400 - 800. When it ends, we will still have locks on customer numbers
  ' 500 and 700. 
  Try
      ' Read customer number 400 but don't lock it. 
      keyTbl.Row.Item("CMCUSTNO") = 400
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl)

      ' Read customer number 500 and lock it. 
      keyTbl.Row.Item("CMCUSTNO") = 500
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Read, keyTbl)

      ' Read customer number 600 and lock it. 
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)

      ' Read customer number 700 and lock it. 
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Read)

      ' Read customer number 800 with locking it. 
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock)

      ' Unlock customer number 600. 
      keyTbl.Row.Item("CMCUSTNO") = 600
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl)
      dbFile.ReleaseCurrent()
  Catch dgEx As dgException
      MsgBox("Couldn't find one or more records. " &amp; dgEx.Message, _
      MsgBoxStyle.Critical, dgEx.Error.ToString())
  End Try

  dbFile.Close() ' Release all locks. 
  db.Close()
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [FileLocks Property](dcsFileOpenAttrClassFileLocksProperty.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ReleaseCurrent Method ](dcsFileAdapterClassReleaseCurrentMethod.html)
      <br />
      [ReleaseRRN](dcsFileAdapterClassReleaseRRNMethod.html)
      <br />
      [LockRequest Enumeration](dcsLockRequestEnumeration.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

