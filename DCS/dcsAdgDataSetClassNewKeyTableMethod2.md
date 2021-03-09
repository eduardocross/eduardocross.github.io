---
title: AdgDataSet.NewKeyTable(integer)

Id: dcsAdgDataSetClassNewKeyTableMethod2
TocParent: dcsAdgDataSetClassNewKeyTableMethods
TocOrder: 1

---

y

Create a key buffer for keyed access operations for the specified format index.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public [AdgKeyTable](dcsAdgKeyTableClass.html) NewKeyTable(
   integer iFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function NewKeyTable(
    ByVal iFormat As Integer
) As [AdgKeyTable](dcsAdgKeyTableClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewKeyTable Access(*Public) Type([AdgKeyTable](dcsAdgKeyTableClass.html))
   DclSrParm iFormat Type(*Integer)** 
      </pre>

Parameters

<dl>
        <dt>
 *iFormat* 
        </dt>
        <dd>
 **Int32** . The zero-relative index of the format in the [
							AdgDataSet](dcsAdgDataSetClass.html).</dd>
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

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

Can occur if *iFormat* specifies an invalid format name.
</td>
          </tr>
</table>

Remarks

[FileAdapter](dcsFileAdapterClass.html) provides methods for accessing a file by key value using [AdgKeyTable](dcsAdgKeyTableClass.html). **AdgKeyTable** is a class for manipulating a DataTable which represents a DataGate file key. **NewKeyTable** generates an instance of **AdgKeyTable** corresponding to a key in a particular file format. Generally, this is the way application programs create key buffers for use in **FileAdapter** keyed access methods.

This overload of **NewKeyTable** specifies the format as an index, where zero indicates the first format.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Members](dcsAdgDataSetMembers.html)
      <br />
      [AdgKeyTable Class](dcsAdgKeyTableClass.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      <br />

