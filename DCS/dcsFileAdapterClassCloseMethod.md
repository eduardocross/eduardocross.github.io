---
title: FileAdapter.Close Method

Id: dcsFileAdapterClassCloseMethod
TocParent: dcsFileAdapterMethods
TocOrder: 3

keywords: database files, close
keywords: files, close
keywords: close files
keywords: how to, close files
keywords: Close method
keywords: FileAdapter.Close method

---

Closes the currently open file (synonymous with [ Dispose Method](dcsFileAdapterClassDisposeMethod.html)).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void Close();** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub Close()** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr Close Access(*Public)** 
      </pre>

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

dgException
</td>
            <td colspan="1" rowspan="1">

See table below.
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
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
</table>

Remarks

Use the **Close** or **Dispose** methods to close a file opened by a previous call to one of the open methods ([Open](dcsFileAdapterClassOpenMethod.html), [OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)). After a successful **Close** or **Dispose** call, the file may be subsequently reopened using the same **FileAdapter** object’s open methods.

**Close** releases unmanaged resources associated with the **FileAdapter** , via the **Dispose** method.
Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  AdgDataSet myDS = null;

  /* Though all open files will automatically be closed when a process
   * is terminated, it is good practice to close them as soon as you are
   * finished with them. You also may need to close a file in order
   * to reopen it with different attributes or to open it as a query file. */

  /* Read the first customer name listed for Texas. */
  string[] keys = new string[]{"CMCUSTNO"}; //The key fields used in our query.
  KeyUsages[] usages = new KeyUsages[]{KeyUsages.ASCEND}; //How we use them.

  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TX\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTexas = myDS.ActiveRow["CMName"].ToString();

  /* Going to try a new query- first we close the file to avoid 
   * throwing an exception... */
  dbFile.Close();
  /* Read the first customer name listed in Tennessee. */ 
  dbFile.OpenSimpleQuery(ref myDS, "*UNIQUE", "CMSTATE=\"TN\"", keys, usages);
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read);
  string FirstInTennessee = myDS.ActiveRow["CMName"].ToString();

  dbFile.Close();
  db.Close();</pre>
      <pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  Dim myDS As AdgDataSet = Nothing

  ' Though all open files will automatically be closed when a process
  ' is terminated, it is good practice to close them as soon as you are
  ' finished with them. You also may need to close a file in order
  ' to reopen it with dIfferent attributes or to open it as a query file. 

  ' Read the first customer name listed for Texas. 
  Dim keys As String()
  Dim usages As KeyUsages()
  keys = New String() {"CMCUSTNO"} 'The key fields used in our query.
  usages = New KeyUsages() {KeyUsages.ASCEND} 'How we use them.

  dbFile.OpenSimpleQuery(myDS, "*UNIQUE", "CMSTATE=""TX""", keys, usages)
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read)
  Dim FirstInTexas As String = myDS.ActiveRow.Item("CMName").ToString()

  ' Going to try a new query- first we close the file to avoid 
  ' throwing an exception... 
  dbFile.Close()
  ' Read the first customer name listed in Tennessee. 
  dbFile.OpenSimpleQuery(myDS, "*UNIQUE", "CMSTATE=""TN""", keys, usages)
  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Read)
  Dim FirstInTennessee As String = myDS.ActiveRow.Item("CMName").ToString()

  dbFile.Close()
  db.Close()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [
					FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [Dispose 
					Method](dcsFileAdapterClassDisposeMethod.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [
					OpenNewAdgDataSet Method](dcsFileAdapterClassOpenNewAdgDataSetMethod.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)

