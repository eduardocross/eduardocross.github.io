---
title: FileAdapter.ExactSeek Property

Id: dcsFileAdapterClassExactSeekProperty
TocParent: dcsFileAdapterProperties
TocOrder: 3

keywords: ExactSeek property
keywords: FileAdapter.ExactSeek property
keywords: how to, determine record seek status
keywords: records, seek status
keywords: database files, seek records status
keywords: files, seek records status
keywords: seek status
keywords: status of record seek
keywords: exact match status

---

This property is **True** if the seek operation resulted in an exact match.
<pre class="syntax">
        <span class="lang">[C#]</span>
 **public bool ExactSeek { get; }** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ExactSeek As Boolean** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual RPG]</span>
 **BegProp ExactSeek Type(*Boolean) Access(*Public)
   BegGet** 
      </pre>

Property Value

Read-only. Boolean. Returns **True** when a seek operation resulted in an exact match. 
Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  using (FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1"))
  {
      dbFile.AccessMode = AccessMode.Read;
      AdgDataSet myDS = null;
      dbFile.OpenNewAdgDataSet(out myDS);

      /* Seek the file pointer to just before Customer number 3000. */
      AdgKeyTable key = myDS.NewKeyTable("RCMMastL1");
      key.Row["CMCustNo"] = Convert.ToDecimal(3000);
      dbFile.SeekKey(SeekMode.SetGE, key);
      /* We check to see if we matched 3000 or if we went beyond it. */
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 3000 exists.");
      else
          MessageBox.Show("Record 3000 not found.");
      /* Now we try to find Customer number 1125. */
      key.Row["CMCustNo"] = Convert.ToDecimal(1125);
      dbFile.SeekKey(SeekMode.SetGE, key);
      if (dbFile.ExactSeek)
          MessageBox.Show("Record 1125 exists.");
      else
          MessageBox.Show("Record 1125 not found.");
  }//Using statement automatically closes dbFile.
  db.Close();</pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As AdgConnection = New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)

  ' Seek the file pointer to just before Customer number 3000. 
  Dim key As AdgKeyTable = myDS.NewKeyTable("RCMMastL1")
  key.Row.Item("CMCustNo") = Convert.ToDecimal(3000)
  dbFile.SeekKey(SeekMode.SetGE, key)
  ' We check to see If we matched 3000 or If we went beyond it. 
  If (dbFile.ExactSeek) Then
      MsgBox("Record 3000 exists.")
  Else
      MsgBox("Record 3000 not found.")
  End If
  ' Now we try to find Customer number 1125. 
  key.Row.Item("CMCustNo") = Convert.ToDecimal(1125)
  dbFile.SeekKey(SeekMode.SetGE, key)
  If (dbFile.ExactSeek) Then
      MsgBox("Record 1125 exists.")
  Else
      MsgBox("Record 1125 not found.")
  End If
  dbFile.Close()
  db.Close()</pre>

Remarks

The <span> **ExactSeek** </span> property is set to **true** if a seek operation results in placing the file pointer on a record containing a specified key or RRN. 
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
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)  

