---
title: AdgDataSet.GetFormatTable(integer)

Id: dcsAdgDataSetClassGetFormatTableMethod
TocParent: dcsAdgDataSetClassGetFormatTableMethods
TocOrder: 0

---

Returns the DataTable object for a particular file format specified by index.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public DataTable GetFormatTable(
   int iFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub GetFormatTable( _
   ByVal iFormat As Integer _
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr GetFormatTable Access(*Public)
   DclSrParm iFormat Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *iFormat* 
        </dt>
        <dd>Integer identifying a file format in the **AdgDataSet** .</dd>
</dl>

Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
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

dgEINVARG
</td>
            <td colspan="1" rowspan="1">

The value of *iFormat* is not valid (see Remarks section).
</td>
          </tr>
</table>

Remarks

**GetFormatTable** is used to access the underlying DataTable object used to model a DataGate file format in **AdgDataSet** . It may be used to easily access useful DataTable properties, such as the Rows collection. 

The number of formats defined in the **AdgDataSet** is given by the [ Formats](dcsAdgDataSetClassFormatsProperty.html) property. Valid values for *iFormat* are in the range 0 ≤ *iFormat* &lt; **AdgDataSet.Formats** . If *iFormat* is an invalid index, **GetFormatTable** throws dgException with the Error property set to dgEINVARG.

To use the file format name, use [ GetFormatTable(string)](dcsAdgDataSetClassGetFormatTableMethodstring.html) method.
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
      [Formats Property](dcsAdgDataSetClassFormatsProperty.html)
      <br />
      [GetFormatTable Method 
					(string)](dcsAdgDataSetClassGetFormatTableMethodstring.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

