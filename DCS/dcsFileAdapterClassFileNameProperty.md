---
title: FileAdapter.FileName Property

Id: dcsFileAdapterClassFileNameProperty
TocParent: dcsFileAdapterProperties
TocOrder: 6

keywords: FileAdapter.FileName property
keywords: FileName property
keywords: files, database path name
keywords: database files, file path name
keywords: how to, set/return the file path name of database file

---

The path name of the database file, excluding the member name (see [ MemberName Property](dcsFileAdapterClassMemberNameProperty.html)). 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public string FileName { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property FileName As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp FileName Type(*String) Access(*Public)
   BegGet, BegSet** 
      </pre>

Property Value

String. Returns or sets the path name of the database file. 
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* In this simple routine we wish to write the format names 
   * of a file to a combo box using the FileAdapter "dbFile" 
   * and its accompanying AdgDataSet "myDS", which may or 
   * may not have been initialized and opened elsewhere. */
  if (dbFile == null)
  {
      MessageBox.Show("Error- FileAdapter not initialized.");
      return;
  }
  if (dbFile.Status != FileAdapter.AdapterStatus.Open)
  {
      MessageBox.Show("Error- "+ dbFile.FileName + " not open.");
      return;
  }
  if (myDS == null)
  {
      MessageBox.Show("DataSet not initialized!");
      return;
  }

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      /* List the format names in the combo box "cbFmtNames". */
      cbFmtNames.Items.Add(myDS.GetFormatName(i));
  }
</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' In this simple routine we wish to write the format names 
  ' of a file to a combo box using the FileAdapter "dbFile" 
  ' and its accompanying AdgDataSet "myDS", which may or 
  ' may not have been initialized and opened elsewhere. 
  If dbFile Is Nothing Then
      MsgBox("Error- FileAdapter not initialized.")
      Return
  End If
  If (dbFile.Status &lt;&gt; FileAdapter.AdapterStatus.Open) Then
      MsgBox("Error- " + dbFile.FileName + " not open.")
      Return
  End If
  If myDS Is Nothing Then
      MsgBox("DataSet not initialized!")
      Return
  End If

  For i As Integer = 0 To myDS.Formats - 1
      ' List the format names in the combo box "cbFmtNames". 
      cbFmtNames.Items.Add(myDS.GetFormatName(i))
  Next i
</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [MemberName Property](dcsFileAdapterClassMemberNameProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

