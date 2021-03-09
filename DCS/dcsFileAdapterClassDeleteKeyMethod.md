---
title: FileAdapter.DeleteKey Method

Id: dcsFileAdapterClassDeleteKeyMethod
TocParent: dcsFileAdapterMethods
TocOrder: 6

keywords: database files, delete record by key
keywords: files, delete record by key
keywords: record keys, delete records by
keywords: records, delete by key
keywords: delete records in a file by key
keywords: how to, delete record by key
keywords: DeleteKey method
keywords: FileAdapter.DeleteKey method

---

Deletes a database file record containing the specified key, if any.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void DeleteKey(
   [AdgKeyTable](dcsAdgKeyTableClass.html) keyTable
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub DeleteKey( _
   ByVal keyTable As [AdgKeyTable](dcsAdgKeyTableClass.html) _
)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr DeleteKey Access(*Public)
   DclSrParm keyTable Type([AdgKeyTable](dcsAdgKeyTableClass.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *keyTable* 
        </dt>
        <dd>
          [AdgKeyTable](dcsAdgKeyTableClass.html). The key of the record to 
						delete.
					</dd>
</dl>

Exceptions

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

**FileAdapter** open method has not been called (file is not open).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException
</td>
            <td colspan="1" rowspan="1">

See table below.
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of
							<br />
							dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
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

dgEaNOTFND
</td>
            <td colspan="1" rowspan="1">

A record with the specified key could not be found.
</td>
          </tr>
</table>

Remarks

**DeleteKey** deletes a record in the open file containing a specified key. First, a search for a record containing the key is performed. If such a record is not found, the method throws dgException with an Error number indicating the condition (see Exceptions above). If the record is found, it is set to be the current record of the file and subsequently deleted.

The file should be opened with the [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) property set to a value including the [AccessMode.Delete](dcsAccessModeEnumeration.html) flag in order to permit delete access to the file.
Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  /* Open a file for reading and deleting- this allows us to delete a record by its key value. */
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
  keyTbl.Row["CMCustNo"] = 82900;
  dbFile.DeleteKey(keyTbl);

  dbFile.Close();
  db.Close();</pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  ' Open a file for reading and deleting- this allows us to delete a record by its key value.
  dbFile.AccessMode = AccessMode.Delete Or AccessMode.Read

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, MsgBoxStyle.OKOnly, "Error")
      'Exit procedure or end application here.
  End Try

  ' We retrieve the record for customer number 82900 and delete it! 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  keyTbl.Row.Item("CMCustNo") = 82900
  dbFile.DeleteKey(keyTbl)

  dbFile.Close()
  db.Close()</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [AccessMode Property](dcsFileAdapterClassAccessModeProperty.html)
      <br />
      [AccessMode Enumeration](dcsAccessModeEnumeration.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

