---
title: FileOpenAttr.ShareTypes Property

Id: dcsFileOpenAttrClassShareTypesProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 4

keywords: ShareTypes property
keywords: FileOpenAttr.ShareTypes property
keywords: database files, concurrent access specified
keywords: files, concurrent access specified
keywords: share an open file
keywords: concurrent access of an open file
keywords: open file, concurrent access
keywords: open file, sharing
keywords: ShareTypes enumeration, used by
keywords: enumerations [DCS 16.0 ShareTypes, used by

---

Specify concurrent access on the open file.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public ShareTypes ShareTypes { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property ShareTypes As [ShareTypes](dcsShareTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp ShareTypes Type(ShareTypes) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

[ASNA.DataGate.Common.ShareTypes](dcsShareTypesEnumeration.html). Specifies concurrent access locking on the open file.
Remarks

Applications may need to open a file for access exclusively to prevent access by other processes as data is being updated. Other applications may need to place no restrictions on concurrent access so that updates are immediately available in the open file. These requirements and others for sharing open file resources can be controlled with the <span> **ShareTypes** </span> property.

Set the value of **ShareTypes** to request the type of sharing required by your application. The access restrictions requested will be enforced by the database when the file is opened and until the file is closed. If the file cannot be opened with the level of sharing specified by <span> **ShareTypes** </span>, then the [ FileAdapter.Open](dcsFileAdapterClassOpenMethod.html) method will throw an exception.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* We open the file in order to delete all of its records. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  /* Its generally good practice to make sure you have an exclusive lock
   * on a file that you are deleting all of the records from, but some
   * databases do not require it. */
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  AdgDataSet myDS = null;

  try
  {
      dbFile.Open(myDS);
      dbFile.DeleteAllRecords();
  }
  catch(dgException dgEx)
  {
      db.Close();
      if (dgEx.Error == dgErrorNumber.dgEmBUSYOBJ)
      {
          MessageBox.Show("Couldn't open the file for exclusive access.", "Error opening file.");
          //Exit routine or procedure here to avoid preceding file operations.
      }
      else 
          throw dgEx;
  }
  dbFile.DeleteAllRecords();

  dbFile.Close();
  db.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' We open the file in order to delete all of its records. 
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER")
  dbFile.AccessMode = AccessMode.Delete
  ' Its generally good practice to make sure you have an exclusive lock
  ' on a file that you are deleting all of the records from, but some
  ' databases do not require it. 
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive
  Dim myDS As AdgDataSet = Nothing

  Try
      dbFile.Open(myDS)
      dbFile.DeleteAllRecords()
  Catch dgEx As dgException
      db.Close()
      If dgEx.Error = dgErrorNumber.dgEmBUSYOBJ Then
          MsgBox("Couldn't open the file For exclusive access.", MsgBoxStyle.Critical, "Error opening file.")
          'Exit routine or procedure here to avoid preceding file operations.
      Else
          Throw dgEx
      End If
  End Try

  dbFile.Close()
  db.Close()</pre>

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
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [ShareTypes Enumeration](dcsShareTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

