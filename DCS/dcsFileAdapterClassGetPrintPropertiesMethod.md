---
title: FileAdapter.GetPrintProperties Method

Id: dcsFileAdapterClassGetPrintPropertiesMethod
TocParent: dcsFileAdapterMethods
TocOrder: 12

keywords: GetPrintProperties method
keywords: FileAdapter.GetPrintProperties method
keywords: how to, get control properties of open print file
keywords: print files, get control properties of open file
keywords: printing, about control properties of open file

---

Gets the [IPrintProperties](dcsIPrintPropertiesClass.html) of the currently open file.
<pre>       <span class="lang">[C#]</span>
 **Public [IPrintProperties](dcsIPrintPropertiesClass.html) GetPrintProperties(
   string format
);** 
      </pre>
      <pre>       <span class="lang">[Visual Basic] </span>
 **Public Function GetPrintProperties( _
   ByVal format As String _
) As [IPrintProperties](dcsIPrintPropertiesClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetPrintProperties Type( [IPrintProperties](dcsIPrintPropertiesClass.html) ) Access(*Public)
   DclSrParm format Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *format* 
        </dt>
        <dd>The name of the print file format containing print file controls.
					</dd>
</dl>

Return Value

The **IPrintProperties** object associated with the open print file.
Exceptions

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

dgEcINVFILETYPE
</td>
            <td colspan="1" rowspan="1">

This method is only supported for print files.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaBADFRMT
</td>
            <td colspan="1" rowspan="1">

The record format specified cannot be found in the file.
</td>
          </tr>
</table>

Remarks

The **IPrintProperties** object returned by this method can be used to get and set print file control property values of an open file. These control properties include fonts, images, and other display characteristics.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Will open up "CustReport" and will write a single detail, and
   * change its background color. */
  AdgConnection dataBase = new AdgConnection("DG NET Local");
  FileAdapter printFile = new FileAdapter(dataBase, "*Libl/CustReport", "*First");
  printFile.AccessMode = AccessMode.PrintPreview;
  AdgDataSet dataSet;
  printFile.OpenNewAdgDataSet(out dataSet);

  DataRow dr = dataSet.PrepareRow("rptDetail");
  dr["prtCMName"] = "This line is light blue.";

  IPrintProperties ip = printFile.GetPrintProperties("rptDetail");
  int oleColor = ColorTranslator.ToOle(Color.LightBlue);
  ip.SetValue("lblRowColor", "BackColor", oleColor);

  dataSet.AddRow("rptDetail");
  printFile.SetFormat("rptDetail");
  printFile.AddRecord(dataSet);

  printFile.Close(); /* Shows print preview - can also accomplish this with
                      * ForceEOD, which doesn't close the file. */
  dataBase.Close();</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Will open up "CustReport" and will write a single detail, and
  ' change its background color. 
  Dim dataBase As New AdgConnection("DG NET Local")
  Dim printFile As New FileAdapter(dataBase, "*Libl/CustReport", "*First")
  printFile.AccessMode = AccessMode.PrintPreview
  Dim dataSet As AdgDataSet = Nothing
  printFile.OpenNewAdgDataSet(dataSet)

  Dim dr As DataRow = dataSet.PrepareRow("rptDetail")
  dr.Item("prtCMName") = "This line is light blue."

  Dim ip As IPrintProperties = printFile.GetPrintProperties("rptDetail")
  Dim oleColor As Integer = ColorTranslator.ToOle(Color.LightBlue)
  ip.SetValue("lblRowColor", "BackColor", oleColor)

  dataSet.AddRow("rptDetail")
  printFile.SetFormat("rptDetail")
  printFile.AddRecord(dataSet)
  ' Shows print preview - can also accomplish this with
  ' ForceEOD, which doesn't close the file. 
  printFile.Close()
  dataBase.Close()</pre>

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
      <br />
      [ASNA.DataGate.Providers.IPrintProperties 
					Class](dcsIPrintPropertiesClass.html)

