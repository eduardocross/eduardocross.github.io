---
title: AdgDataSet.GetFormatTable(String)

Id: dcsAdgDataSetClassGetFormatTableMethodstring
TocParent: dcsAdgDataSetClassGetFormatTableMethods
TocOrder: 1

---

Returns the DataTable object for a particular file format specified by string.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public DataTable GetFormatTable(
   string strFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub GetFormatTable( _
   ByVal strFormat As String _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr GetFormatTable Access(*Public)
   DclSrParm strFormat Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>String identifying a file format in the **AdgDataSet** .</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
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

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The value of *strFormat* is not valid.
</td>
          </tr>
</table>

Remarks

**GetFormatTable** is used to access the underlying DataTable object used to model a DataGate file format in **AdgDataSet.** It may be used to easily access useful DataTable properties, such as the Rows collection. 

If *strFormat* is not a valid format name, **GetFormatTable** throws dgException with the Error property set to dgEINVARG.

To use the file format index, use [ GetFormatTable(index)](dcsAdgDataSetClassGetFormatTableMethod.html) method.
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
      [GetFormatTable(index) Method](dcsAdgDataSetClassGetFormatTableMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

