---
title: FileAdapter.MemberName Property

Id: dcsFileAdapterClassMemberNameProperty
TocParent: dcsFileAdapterProperties
TocOrder: 8

keywords: FileAdapter.MemberName property
keywords: MemberName property
keywords: files, member name
keywords: database files, member name
keywords: how to, set/return the member name of database file

---

<span>The name of the member of the currently-opened file. </span> 
<pre>        <span class="lang">[C#]</span>
 **Public string MemberName { get; set; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Property MemberName As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp MemberName Type(*String) Access(*Public)** 
      </pre>

Property Value

String. Returns or sets the name of the member of the currently-opened file.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* We attempt to open the class variable FileAdapter "dbFile" 
   * which may or may not have been initialized another routine. */
  public void OpenFile(){
      AdgDataSet myDS = null;
      if (dbFile == null)
      {
          MessageBox.Show("FileAdapter not initialized.");
          return;
      }
      try
      {
          dbFile.OpenNewAdgDataSet(out myDS);
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          {
              MessageBox.Show("Member " + dbFile.MemberName + " not found!");
          }
          else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          {
              MessageBox.Show("File " + dbFile.FileName + " not found!");
          }
          else 
          {
              MessageBox.Show("Couldn't open file!" + dgEx.Message, "");
          } 
          // Exit routine or end application here.
      }
  }
 </pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' We attempt to open the class variable FileAdapter "dbFile" 
  ' which may or may not have been initialized another routine. 
  Public Sub OpenFile()
      Dim myDS As AdgDataSet = Nothing
      If dbFile Is Nothing Then
          MsgBox("FileAdapter not initialized.")
          Return
      End If
      Try
          dbFile.OpenNewAdgDataSet(myDS)
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEmMNOTFND) Then
              MsgBox("Member " + dbFile.MemberName &amp; " not found!")
          ElseIf (dgEx.Error = dgErrorNumber.dgEmFNOTFND) Then
              MsgBox("File " + dbFile.FileName &amp; " not found!")
          Else
              MsgBox("Couldn't open file!" &amp; dgEx.Message)
          End If
          ' Exit routine or end application here.
      End Try
  End Sub</pre>

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

