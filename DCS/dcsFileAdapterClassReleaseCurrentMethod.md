---
title: FileAdapter.ReleaseCurrent Method

Id: dcsFileAdapterClassReleaseCurrentMethod
TocParent: dcsFileAdapterMethods
TocOrder: 21

keywords: ReleaseCurrent method
keywords: FileAdapter.ReleaseCurrent method
keywords: records, release locked
keywords: database files, release locked record
keywords: release, locked record
keywords: how to, release locked record
keywords: locked records, release

---

Release the currently locked record.
<pre>        <span class="lang">[C#]</span>
 **Public void ReleaseCurrent();** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub ReleaseCurrent()** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr ReleaseCurrent Access(*Public)** 
      </pre>
      <br />
      <br />

Exceptions

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
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

FileAdapter [open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open).
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

dgEaNOCURR
</td>
            <td colspan="1" rowspan="1">

There is not a current record associated with the file. If the file is open for "network blocking", the current record position on the server is unknown.
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
</table>

Remarks

**FileAdapter** methods which read, update, and add records may also optionally lock the current record associated with those operations, in compliance with the rules of the database provider. **ReleaseCurrent** allows DCS programs to release the lock held, if any, on the current record.
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
 /* Here, we are using a pre-initialized FileAdapter (named "dbFile")
  * which was opened using AccessMode.RWCD, which automatically locks
  * each read record read, so it will remain unchanged until we
  * update it or read a new record. Here we don't want to
  * update the record if the customer is not from Texas, and if
  * this code is being called by unknown client code it could be awhile
  * before the next read. In order to remove the lock without
  * performing some additional action, we use the ReleaseCurrent method . */
 dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default);
 if (myDS.ActiveRow["CMState"].ToString() == "TX" &amp;&amp;
     myDS.ActiveRow["CMActive"].ToString() == "0")
 {
     myDS.ActiveRow["CMActive"] = '1';
     dbFile.ChangeCurrent(myDS);
 }
 else
 {
     dbFile.ReleaseCurrent();
 }
</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
 ' Here, we are using a pre-initialized FileAdapter (named "dbFile")
 ' which was opened using AccessMode.RWCD, which automatically locks
 ' each read record read, so it will remain unchanged until we
 ' update it or read a new record. Here we don't want to
 ' update the record If the customer is not from Texas, and If
 ' this code is being called by unknown client code it could be awhile
 ' before the next read. In order to remove the lock without
 ' performing some additional action, we use the ReleaseCurrent method .
 dbFile.ReadSequential(myDS, ReadSequentialMode.Next, LockRequest.Default)
 If (myDS.ActiveRow.Item("CMState").ToString() = "TX" And _
     myDS.ActiveRow.Item("CMActive").ToString() = "0") 

     myDS.ActiveRow.Item("CMActive") = "1"
     dbFile.ChangeCurrent(myDS)
 Else
     dbFile.ReleaseCurrent()
 End If</pre>

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
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

