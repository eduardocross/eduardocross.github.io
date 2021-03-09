---
title: SetActive(string,integer)

Id: dcsAdgDataSetClassSetActiveMethod2
TocParent: dcsAdgDataSetClassSetActiveMethods
TocOrder: 1

---

Establish the record, specified by format name and relative record number, as the active row.
<pre class="prettyprint">
          <span class="lang">[C#]</span>
 **public bool SetActive(
   string strFormat,
   int rrn
);** 
        </pre>

<pre class="prettyprint">
          <span class="lang">[Visual Basic] </span>
 **Public Function SetActive( _
   ByVal strFormat As String _
   ByVal rrn As Integer
) As Boolean** 
        </pre>

<pre class="prettyprint">
          <span class="lang">[Visual RPG]</span>
 **BegFunc SetActive Type(*Boolean) Access(*Public)
   DclSrParm strFormat Type(*String) Len(45)
   DclSrParm rrn Type(*Integer) Len(4)** 
        </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>
 **String** . A string identifying the format corresponding to the **DataTable** in which the **DataRow**  resides. 
						Optionally, the string can be null or empty, to indicate that the value of the [
							CurrentFormatName](dcsAdgDataSetClassCurrentFormatNameProperty.html) property will be used to identify the format. </dd>
        <dt>
 *rrn* 
        </dt>
        <dd>
 **Int32** . A positive integer referring to the **DataRow**  object's 
								position within the row collection of the **DataTable** .</dd>
</dl>

Return Value

**SetActive** returns **True** if the **DataRow** is found and successfully made the active row, and **False** otherwise.
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

Can occur if *strFormat* specifies an invalid format name.
</td>
          </tr>
</table>

Remarks

**SetActive** causes the specified DataRow object to be the current value of the [ActiveRow ](dcsAdgDataSetClassActiveRowProperty.html) property. This is helpful when using [FileAdapter](dcsFileAdapterMethods.html) methods which act upon the "active row" of the **AdgDataSet** , such as [AddRecord](dcsFileAdapterClassAddRecordMethod.html), [ ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html), and others. Whereas many read-access methods of **FileAdapter** implicitly set the active row, **SetActive** allows the program to directly influence the active row.

**SetActive** returns a value of **False** if the DataRow specified by *rrn* is not found. No validation of the *strFormat* parameter is performed. If *strFormat* does not refer to a valid format name, an exception will occur.
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
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [CurrentFormatName 
					Property](dcsAdgDataSetClassCurrentFormatNameProperty.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Methods](dcsFileAdapterMethods.html)
      <br />
      [AddRecord Method](dcsFileAdapterClassAddRecordMethod.html)
      <br />
      [ChangeCurrent Method](dcsFileAdapterClassChangeCurrentMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

