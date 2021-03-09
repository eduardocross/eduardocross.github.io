---
title: LockRequest Enumeration

Id: dcsLockRequestEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 17

keywords: LockRequest enumeration
keywords: enumerations [DCS 16.0 LockRequest
keywords: Default enumeration member
keywords: NoLock enumeration member
keywords: NoWait enumeration member
keywords: Read enumeration member
keywords: ReadWrite enumeration member
keywords: Write enumeration member
keywords: record locking constants
keywords: database files, record locking constants
keywords: files, record locking constants

---

Options for record locking in [FileAdapter](dcsFileAdapterClass.html) access methods. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum LockRequest;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum LockRequest** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum LockRequest Access(*Public)** 
      </pre>

Remarks

The **LockRequest** enumeration values are used by methods of the [ FileAdapter](dcsFileAdapterClass.html) class that access database records. Database providers provide default mechanisms for locking records when they are accessed. These mechanisms can be overridden by use of **LockRequest** flags passed to the access method.

**LockRequest** is a "flags" enumeration where values can be combined to create a custom value as required by the application. The enumeration defines one common combination, ' ReadWrite'. Note that the ' Default' flag cannot be usefully combined with other flags.

Note: Some **LockRequest** values are not supported by certain database providers. Most significantly, the AS/400 database provider only supports the 'NoLock' and ' Default' values; thus, the only way to override its normal locking semantics is to request no locking. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col span="1" width="10%" />
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
            <td colspan="1" rowspan="1">

Default 
</td>
            <td colspan="1" rowspan="1">

Use the default locking based on the file’s share, access and lock modes. 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NoWait
</td>
            <td colspan="1" rowspan="1">

Don’t retry a lock that cannot be obtained immediately.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Read 
</td>
            <td colspan="1" rowspan="1">

Lock for reading. 
</td>
            <td colspan="1" rowspan="1">

2 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Write 
</td>
            <td colspan="1" rowspan="1">

Lock for writing. 
</td>
            <td colspan="1" rowspan="1">

4 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

ReadWrite 
</td>
            <td colspan="1" rowspan="1">

Lock for reading and writing. 
</td>
            <td colspan="1" rowspan="1">

6 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NoLock
</td>
            <td colspan="1" rowspan="1">

Don’t lock.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
</table>

Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.RWCD;

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

  /* We're only checking these records and don't want to waste time by
   * locking every one, so we use LockRequest.NoLock. 
   * Note that a quicker way to find a record with such a specific 
   * criteria is to use the OpenSimpleQuery method of FileAdapter. 
   * This is merely an example. */
  bool EOF = false;
  while(! EOF)
  {
      try
      {
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock);
          if (Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]) &gt; 30000 &amp;&amp;
              Convert.ToString(myDS.ActiveRow["CMNAME"]).StartsWith("A"))
          {
              /* We read once backwards to get the record again, and this
               * time we lock it. */
              dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default);
              break;
          }
      }
      catch(dgException dgEx)
      {
          if (dgEx.Error == dgErrorNumber.dgEaEOF)
              EOF = true;
          else
              throw dgEx;
      }
  }
  if (EOF)
      MessageBox.Show("End of file was reached- record not found.", "Record not found.");
  else
  {
      /* We now make the name all lower case before updating the file. */
      myDS.ActiveRow["CMName"] = myDS.ActiveRow["CMName"].ToString().ToLower();

      MessageBox.Show("Customer number " + 
      Convert.ToDecimal(myDS.ActiveRow["CMCUSTNO"]).ToString() +
          ", \"" + Convert.ToString(myDS.ActiveRow["CMName"]) + 
          "\", met the search requirements.", "Customer found.");
  }
</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.RWCD

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " &amp; dgEx.Message, MsgBoxStyle.Critical, "Error")
      'Exit procedure or end application here.
  End Try

  ' We're only checking these records and don't want to waste time by
  ' locking every one, so we use LockRequest.NoLock. 
  ' Note that a quicker way to find a record with such a specIfic 
  ' criteria is to use the OpenSimpleQuery method of FileAdapter. 
  ' This is merely an example. 
  Dim EOF As Boolean = False
  While Not EOF
      Try
          dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.NoLock)
          If (Convert.ToDecimal(myDS.ActiveRow.Item("CMCUSTNO")) &gt; 30000 And Convert.ToString(myDS.ActiveRow.Item("CMNAME")).StartsWith("A")) Then
              ' We read once backwards to get the record again, and this
              ' time we lock it. 
              dbFile.ReadSequential(myDS, ReadSequentialMode.Previous, LockRequest.Default)
              Exit While
          End If
      Catch dgEx As dgException
          If (dgEx.Error = dgErrorNumber.dgEaEOF) Then
              EOF = True
          Else
              Throw dgEx
          End If
      End Try
  End While
  If EOF Then
      MsgBox("End of file was reached- record not found.", "Record not found.")
  Else
      ' We now make the name all lower case beFore updating the file. 
      myDS.ActiveRow.Item("CMName") = myDS.ActiveRow.Item("CMName").ToString().ToLower()
      MsgBox("Customer number " &amp; _
      Convert.ToDecimal(myDS.ActiveRow.Item("CMCUSTNO")).ToString() &amp; _
          ", """ + Convert.ToString(myDS.ActiveRow.Item("CMName")) &amp; _
          """, met the search requirements.", "Customer found.")
  End If
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

