---
title: FileAdapter.OpenNewAdgDataSet Method

Id: dcsFileAdapterClassOpenNewAdgDataSetMethod
TocParent: dcsFileAdapterMethods
TocOrder: 14

keywords: FileAdapter.OpenNewAdgDataSet method
keywords: OpenNewAdgDataSet method
keywords: open a new file
keywords: files, open new
keywords: database files, open new
keywords: how to, open new database files

---

Opens a database file for access and returns a new [ AdgDataset](dcsAdgDataSetClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **Public void OpenNewAdgDataSet(
   AdgDataSet ds
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub OpenNewAdgDataSet( _
   ByRef ds As [AdgDataSet](dcsAdgDataSetClass.html) _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr OpenNewAdgDataSet Access(*Public)
   DclSrParm ds Type(AdgDataSet) By(*Reference)** 
      </pre>

Parameters

<dl>
        <dt>
 *ds* 
        </dt>
        <dd>A reference to a DataSet object ( **AdgDataSet** ) created by this method and 
						corresponding to the file to be opened.
					</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOLDSERVER 
</td>
            <td colspan="1" rowspan="1">

The file cannot be opened because the operation is not supported by the version of the database provider of the [AdgConnection](dcsAdgConnectionClass.html) object. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The [FileName](dcsFileAdapterClassFileNameProperty.html) or [ MemberName](dcsFileAdapterClassMemberNameProperty.html) properties refer to an invalid database file name. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVDMOP 
</td>
            <td colspan="1" rowspan="1">

The operation is not allowed because the database is opened for monitor access only. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFRMTID 
</td>
            <td colspan="1" rowspan="1">

A "level check" operation was requested and the check discovered a difference between an expected format and the actual format of the file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED 
</td>
            <td colspan="1" rowspan="1">

The database provider called an "exit point" program to validate the operation and the program denied the requested operation. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC 
</td>
            <td colspan="1" rowspan="1">

The database provider has found a registration for an "exit point" program to validate the operation but the database provider is not currently licensed for that capability. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING 
</td>
            <td colspan="1" rowspan="1">

The database provider has found a registration for an "exit point" program to validate the operation but no such program could be found. 
</td>
          </tr>
</table>

Remarks

[Open](dcsFileAdapterClassOpenMethod.html), **OpenNewAdgDataSet** , and [OpenSimpleQuery](dcsFileAdapterClassOpenSimpleQueryMethod.html) are the three methods available for opening database files with [ FileAdapter](dcsFileAdapterClass.html). 

**OpenNewAdgDataSet** opens the file and creates an **AdgDataSet** instance used by **FileAdapter** for containing file record data for access operations. The **AdgDataSet** instance so created is guaranteed to reflect the current record formats of the file. This is in contrast to the **Open** method, which accepts a pre-existing **AdgDataSet** instance parameter, and it is the responsibility of the program to determine the compatibility of the **AdgDataSet** and file record formats. Generally, **OpenNewAdgDataSet** is designed for use in applications, whereas **Open** is suitable for development environments such as Visual RPG.

**Open** and **OpenNewAdgDataSet** observe the current value of the [AccessMode](dcsFileAdapterClassAccessModeProperty.html) property. This property specifies how access to the file is enforced by the database. For example, to allow records to be deleted by the **FileAdapter** , use a value for **AccessMode** that includes the [ AccessMode.Delete](dcsAccessModeEnumeration.html) flag.

**Open** and **OpenNewAdgDataSet** also observe the [ OpenAttributes](dcsFileAdapterClassOpenAttributesProperty.html) property, to effect other characteristics of the opened file. These characteristics include "record blocking" for read access, and "level checking" for file format verification. The value of **OpenAttributes** is an object of type [FileOpenAttr](dcsFileOpenAttrClass.html).

Record blocking can significantly improve sequential access efficiency especially when utilized against a network database. If the value of [ FileOpenAttr.BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) is set in the object referenced by **OpenAttributes** , then read-access record blocking will be used to access the opened file.

If the user provides a value to the [ FileOpenAttr.FormatIDs](dcsFileOpenAttrClassFormatIDsProperty.html) property of the object referenced by **OpenAttributes** , then the given format identifier(s) will be used to "level check" the format(s) of the file. If the file is not at the same level when the open operation occurs, the database will return an error.
Examples 

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  /* The AdgDataSet consists of data read from the database file
   * using the FileAdapter class. It also must be used in most
   * of the FileAdapter's operations. */
  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }

  /* The code below finds the names of every data field in the 
   * file "*Libl/CMASTNEWL1" and puts them into an array list. */
  ArrayList fieldNames = new ArrayList();

  for (int i = 0; i &lt; myDS.Formats; i ++)
  {
      foreach(DataColumn column in myDS.Tables[i].Columns)
      {
          fieldNames.Add(column.ToString());
      }
  } 

  dbFile.Close();
  db.Close();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  ' The AdgDataSet consists of data read from the database file
  ' using the FileAdapter class. It also must be used in most
  ' of the FileAdapter's operations.
  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
  ' There are many reasons why opening a file can fail. Here, we
  ' catch some of the more general ones.
      If (dgEx.Error = dgErrorNumber.dgEmMNOTFND) Then
            MsgBox("Member " + dbFile.MemberName + " not found!", MsgBoxStyle.OKOnly, "Error")
      ElseIf (dgEx.Error = dgErrorNumber.dgEmFNOTFND) Then
            MsgBox("File " + dbFile.FileName + " not found!", MsgBoxStyle.OKOnly, "Error")
      Else
            MsgBox(dgEx.Message, MsgBoxStyle.OKOnly, "Error")
           'Exit procedure here.
      End If
  End Try<br />
  ' The code below finds the names of every data field in the
  ' file "*Libl/CMASTNEWL1" and puts them into an array list.
  Dim fieldNames As New ArrayList
  For i As Integer = 0 To myDS.Formats - 1
  For Each column As DataColumn In myDS.Tables(i).Columns
      fieldNames.Add(column.ToString())
  Next
  Next
  dbFile.Close()
  db.Close()</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See 
Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [OpenSimpleQuery Method](dcsFileAdapterClassOpenSimpleQueryMethod.html)
      <br />
      [FileName Property](dcsFileAdapterClassFileNameProperty.html)
      <br />
      [MemberName Property](dcsFileAdapterClassMemberNameProperty.html)
      <br />
      [AccessMode](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [BlockingFactor Property](dcsFileOpenAttrClassBlockingFactorProperty.html)
      <br />
      [FormatIDs Property](dcsFileOpenAttrClassFormatIDsProperty.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

