---
title: AdgDataSet.GetFormatName Method

Id: dcsAdgDataSetClassGetFormatNameMethod
TocParent: dcsAdgDataSetMethods
TocOrder: 4

keywords: GetFormatName method
keywords: AdgDataSet.GetFormatName method
keywords: file formats, obtaining format name from index
keywords: format names, obtaining for file from format index
keywords: file format names from format index

---

Returns a string identifying a DataGate file format.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string GetFormatName(
   int iFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function GetFormatNew( _
   ByVal iFormat As Integer _
) As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetFormatNew Access(*Public) Type(*String)
   DclSrParm iFormat Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
          <span> *iFormat* 
          </span>
        </dt>
        <dd>
          <span />Integer identifying a file format in the **AdgDataSet** .</dd>
</dl>

Exceptions

**ASNA.DataGate.Common.dgException** is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <col span="1" style="WIDTH: 30%" />
          <col span="1" style="WIDTH: 70%" />
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

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The value of *iFormat* is not valid (see Remarks section).
</td>
          </tr>
</table>

Remarks

In **AdgDataSet,** DataTables corresponding to DataGate file formats are identified in two ways:

1. by format name, and
2. by integer index ([GetFormatIndex](dcsAdgDataSetClassGetFormatIndexMethod.html)).

**GetFormatName** provides a way to obtain the format name, given an integer index. The number of formats defined in the **AdgDataSet** is given by the [Formats](dcsAdgDataSetClassFormatsProperty.html) property. Valid values for *iFormat* are in the range 0 ≤ *iFormat* &lt; **AdgDataSet.Formats** . If *iFormat* is an invalid index, **GetFormatName** throws dgException with the Error property set to dgEINVARG.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

