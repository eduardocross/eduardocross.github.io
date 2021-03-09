---
title: FileAdapter.AccessMode Property

Id: dcsFileAdapterClassAccessModeProperty
TocParent: dcsFileAdapterProperties
TocOrder: 0

keywords: access mode when opening file
keywords: how to, set/return access mode for opening file
keywords: database files, access mode when opening
keywords: files, access mode when opening
keywords: database files, restrict access
keywords: files, restrict access
keywords: AccessMode property
keywords: FileAdapter.AccessMode property
keywords: enumerations [DCS 16.0 AccessMode, used by
keywords: AccessMode enumeration, used by

---

The declared mode of access enforced by the database when the file is open. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public [AccessMode](dcsAccessModeEnumeration.html) AccessMode { get; set; };** 
      </pre>
      <pre class="prettyprint">       <span class="lang">[Visual Basic] </span>
 **Public Property AccessMode As [AccessMode](dcsAccessModeEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp AccessMode Type([AccessMode](dcsAccessModeEnumeration.html))
   BegGet, BegSet** 
      </pre>

Property Value

Integer. Returns or sets an integer value for how a file will be accessed when it is opened. The valid values are defined by the [ ASNA.DataGate.Common AccessMode](dcsAccessModeEnumeration.html) enumeration. 
Remarks

The valid values are defined by the **ASNA.DataGate.Common AccessMode** enumeration.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  FileAdapter dbFile = new FileAdapter();
  dbFile.Connection = new AdgConnection("*Public/DG NET Local");
  dbFile.FileName = "*Libl/CMASTNEWL1";
  dbFile.MemberName = "CMMASTERL1";

  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 82900 and delete it! */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCustNo"] = 82900m;
  try
  {
      dbFile.DeleteKey(keyTbl);
  }
  catch(dgException dgEx)
  {
      if (dgEx.Error == dgErrorNumber.dgEaNOTFND)
      {
          MessageBox.Show("Record not found. ");
      }
  }
  dbFile.Close();
  dbFile.Connection.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim dbFile As New FileAdapter
  dbFile.Connection = New AdgConnection("*Public/DG NET Local")
  dbFile.FileName = "*Libl/CMASTNEWL1"
  dbFile.MemberName = "CMMASTERL1"

  ' Open a file for reading and deleting- this allows us to delete a record by its key value. 
  dbFile.AccessMode = AccessMode.Read Or AccessMode.Delete
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' We retrieve the record for customer number 82900 and delete it! 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  keyTbl.Row.Item("CMCustNo") = 82900
  Try
      dbFile.DeleteKey(keyTbl)
  Catch dgEx As dgException
      If (dgEx.Error = dgErrorNumber.dgEaNOTFND) Then
          MsgBox("Record not found. ")
      End If
  End Try
  dbFile.Close()
  dbFile.Connection.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [ASNA.DataGate.Common AccessMode Enumeration](dcsAccessModeEnumeration.html) <br />
	  [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

