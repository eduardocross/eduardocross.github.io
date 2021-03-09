---
title: FileOpenAttr.FileLocks Property

Id: dcsFileOpenAttrClassFileLocksProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 1

keywords: record locking mode
keywords: database files, record locking mode
keywords: files, record locking mode
keywords: manual record locking mode
keywords: automatic record locking mode
keywords: how to, set manual record locking mode
keywords: how to, set automatic record locking mode
keywords: FileLocks property
keywords: FileOpenAttr.FileLocks property
keywords: enumerations [DCS 16.0 FileLocks, used by
keywords: FileLocks enumeration, used by

---

Specify record locking mechanisms in opened files. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public FileLocks FileLocks { get; set; }**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property FileLocks As [Filelocks](dcsFileLocksEnumeration.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp FileLocks Type(FileLocks) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

[ASNA.DataGate.Common.FileLocks](dcsFileLocksEnumeration.html). The record locking mechanism to use.
Remarks

This property allows some control over the record locking behavior of [ FileAdapter](dcsFileAdapterClass.html) access methods. This control is dependent upon the database provider being accessed. For example, the IBM i database does not support "manual" locking.

When set to the Manual value, record locking in the opened file will only occur if explicitly specified in the **FileAdapter** access method. Also, records locked in access methods can only be unlocked explicitly with the [ReleaseCurrent](dcsFileAdapterClassReleaseCurrentMethod.html) or [ReleaseRRN](dcsFileAdapterClassReleaseRRNMethod.html) methods.

When set to the Auto value, record locking occurs automatically in **FileAdapter** access methods unless overridden by the [LockRequest](dcsLockRequestEnumeration.html) parameter. Also, locked records are automatically unlocked when another record is accessed.
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

      ' Read customer number 800 without locking it. 
      dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock)

      ' Unlock customer number 600. 
      keyTbl.Row.Item("CMCUSTNO") = 600
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.NoLock, keyTbl)
      dbFile.ReleaseCurrent()

  Catch dgEx As dgException
      MsgBox("Couldn't find one or more records. " + dgEx.Message, _
          MsgBoxStyle.Critical, dgEx.Error.ToString())
  End Try

  dbFile.Close() ' Release all locks. 
  db.Close()
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [FileOpenAttr Class Members](dcsFileOpenAttrClassMembers.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [ReleaseCurrent Method](dcsFileAdapterClassReleaseCurrentMethod.html)
      <br />
      [ReleaseRRN Method](dcsFileAdapterClassReleaseRRNMethod.html)
      <br />
      [LockRequest Enumeration](dcsLockRequestEnumeration.html)
      <br />
      [FileLocks Enumeration](dcsFileLocksEnumeration.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

