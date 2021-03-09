---
title: FileAdapter.ForceEOD Method

Id: dcsFileAdapterClassForceEODMethod
TocParent: dcsFileAdapterMethods
TocOrder: 11

keywords: FileAdapter.ForceEOD method
keywords: ForceEOD method
keywords: OLE print files, printing
keywords: OLE print files, flush current page and start printing
keywords: how to, flush current page and start printing OLE print files
keywords: printing, OLE print files
keywords: database files, flush buffers of open file
keywords: files, flush buffers of open file
keywords: database files, release locks of open file
keywords: how to, flush buffer, release lock, and seek last record of open file
keywords: files, release locks of open file
keywords: database files, seek last record of open file
keywords: files, seek last record of open file

---

Synchronizes the state of the <span> **FileAdapter** </span> object with the open database file.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public void ForceEOD();** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub ForceEOD()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ForceEOD Access(*Public)** 
      </pre>
      <br />

Exceptions

<br />

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

<br />

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error
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

For OLE print files, **ForceEOD** causes a document to start printing by first flushing the current page, then the document starts printing immediately without closing.

For database files, **ForceEOD** flushes any provider-specific buffers associated with the open file, releases locks, and seeks to the last record in the file.
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

