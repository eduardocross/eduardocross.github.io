---
title: FileAdapter.ExtendedResults Property

Id: dcsFileAdapterClassExtendedResultsProperty
TocParent: dcsFileAdapterProperties
TocOrder: 4

keywords: FileAdapter.ExtendedResults property
keywords: ExtendedResults property
keywords: how to, access extended information associated a files
keywords: database files, extended status of
keywords: files, extended status of
keywords: OLE print files, extended status of
keywords: status, extended information associated with a file

---

Specialized collection of status information associated with the file.
<pre class="syntax">
        <span class="lang">[C#]</span>
 **public Hashtable ExtendedResults { get; }** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ExtendedResults As Hashtable** 
      </pre>
      <pre class="syntax">
        <span class="lang">[Visual RPG]</span>
 **BegProp ExtendedResults Type(Hashtable) Access(*Public)
   BegGet** 
      </pre>

Property Value

Read-only. System.Collections.Hashtable. A set of properties' values, keyed by name, associated with specialized DataGate files. 
Remarks

Properties associated with specialized files will be found in the **ExtendedResults** collection. Items in the collection are keyed by string values identifying them.

DataGate OLE print files, when written to, communicate information about the document being printed through ExtendedResults. The following table summarizes the information available for open OLE print files, after a record has been added to the file.
<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 15%; font-weight:bold" />
            <col span="1" style="WIDTH: 85%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Property Key Name
						</th>
            <th colspan="1" rowspan="1">
							Property Value
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

CursorY
</td>
            <td colspan="1" rowspan="1">

Integer. The position that the printer is from the top of the page. Print Units are measured in 1/100th of a millimeter.

- To get the measurement in millimeters, divide by 100.
- To get the measurement in centimeters, divide by 1,000.
- To get the measurement in inches, divide by 2,540.

</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

PageLength
</td>
            <td colspan="1" rowspan="1">

Integer. The total page length based on the page orientation selected. Print Units are measured in 1/100th of a millimeter.

- To get the measurement in millimeters, divide by 100.
- To get the measurement in centimeters, divide by 1,000.
- To get the measurement in inches, divide by 2,540.

</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

PageWidth
</td>
            <td colspan="1" rowspan="1">

Integer. The total page width based upon the page orientation selected. Print Units are measured in 1/100th of a millimeter.

- To get the measurement in millimeters, divide by 100.
- To get the measurement in centimeters, divide by 1,000.
- To get the measurement in inches, divide by 2,540.

</td>
          </tr>
</table>

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

