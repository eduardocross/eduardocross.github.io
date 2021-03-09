---
title: Data Flow Overview

Id: amfDataFlow
TocParent: amfconFrameworkASPXSessionMovingData
TocOrder: 195

keywords: message files, about
keywords: concepts, ASNA.Monarch Framework, Dataflow
keywords: ASNA.Monarch, dataflow
keywords: ASNA.Monarch, fields and indicators
keywords: dataflow, concepts
keywords: dataflow, managing

---

### The Program to User Round Trip
The dataflow that carries field and indicator values from the program to the user involves four buckets:

1. RPG Program Variables
2. <code>DataSet</code>
3. Web Control properties
4. HTML elements

When going from the program to the browser, the dataflow steps are:

- Busines Logic affects RPG Program Variables
- Write Record copies the variables to the <code>DataSet</code>
- <code>OnCopyDisplayFileToBrowser</code> copies the DataSet values to the Web Control
- Render method generates the HTML stream

On the way back, from browser to program, the steps are:

- Browser sends input values to the server, which get copied to the Web Controls
- <code>OnCopyBrowserToDisplayFile</code> copies the values to the DataSet
- The DataSet values are copied to the RPG program variables when the RPG program READs

If your application must manipulate the data in the DisplayFile code behind, it can utilize the values when they are in either the DataSet or in the Web Control properties. Typically this is done by overriding the <code>OnCopy *xxx* </code> methods. The <code>ASNA.Monarch.WebDspf.Page</code> makes available its DataSet via a property conveniently called **<code>DataSet</code>** , it also provides a set of methods to facilitate the manipulation of the values in the DataSet. The DataSet values and the methods can be used after the <code>*Base.OnLoad</code> has executed.

Indicator values have additional considerations:

Each record format holds two sets of indicators (100 each): "Option" and "Response" indicators. 

The "Option" indicators are used by the RPG program to affect the initial state of fields in the record format. These are used when the record is Written (sent to the Browser). Note that ExFmt command implies a Write).

The "Response" indicators indicate to the RPG program, the state of fields in which the user responded by using the active records while the Browser page was presented and the response was submitted to the server. These are used (affecting the RPG indicators) when active record formats are Read (through various RPG/AVR commands, such as coming back from ExFmt, ReadC, et c.)

#### Dataflow of Indicators in DataTable
![](images/DataFlow1.png)

![](images/DataFlow2.png)

![](images/DataFlow3.png)

![](images/DataFlow4.png)

![](images/DataFlow5.png)

![](images/DataFlow6.png)

5. RPG Program Write-Record operation sets indicators in DataTable with the values of the indicators of the RPG program <br /> <br /> <br /> <br /> <br />
6. Code Behind <code>SetIndicator()</code> can override DataTable option Indicators<br /> <br /> <br /> <br /> <br />
7. On <code>*Base.OnCopyDspFileToBrowser</code> uses the indicators as option indicators to affect the behavior of the DdsControls <br /> <br /> <br /> <br /> <br />
8. On <code>*Base.OnCopyBrowserToDspFile</code> sets the indicators as resulting indicators with values of <code> **1-0-x** </code> 
    depending if the indicator was used by the DdsControls of the Record  <br /> <br /> <br /> <br /> <br />
9. Code Behind <code>SetIndicator()</code> can override DataTable respone Indicators (with <code> **1-0-x** </code> values)<br /> <br /> <br /> <br /> <br />
10. RPG Program Read-Record operation Sets the indicators of the RPG Program with the <code>'1'</code> and <code>'0'</code> in the DataTable, 'x' values are ignored<br /> <br /> <br /> <br /> <br />

#### Related Methods
These methods can impact field and indicator values after the <code>*Base.OnLoad</code> has executed, for instance in: 

- <code>OnCopyDspFileToBrowser</code>
- <code>OnCopyBrowsertoDspFile</code>

And occasionally in:
- OnLoad

##### Method that Tests for Active Format
[<code>IsFormatActive</code>](amfpageClassIsFormatActiveMethod.html)
<pre>Bool IsFormatActive(FormatName)</pre>

##### Methods that Get Data
[<code>GetDataTable</code>](amfpageClassGetDataTableMethod.html)
<pre>DataTable GetDataTable(FormatName)</pre>

[<code>GetDataRow</code>](amfpageClassGetDataRowMethod.html)
<pre>DataRow GetDataRow(FormatName)</pre>

[<code>GetSubfileDataRow</code>](amfpageClassGetSubfileDataRowMethod.html)
<pre>DataRow GetSubfileDataRow(FormatName, RRN)</pre>

[<code>GetFieldValue</code>](amfpageClassGetFieldValueMethod.html)
<pre>Object GetFieldValue(FormatName, FieldName)</pre>

[<code>GetSubfileFieldValue</code>](amfpageClassGetSubfileFieldValueMethod.html)
<pre>Object GetSubfileFieldValue(FormatName, FieldName, RRN)</pre>

##### Methods that Set Field Values
[<code>SetFieldValue</code>](amfpageClassSetFieldValueMethod.html)
<pre>SetFieldValue(FormatName, FieldName, Object newValue)</pre>

[<code>SetSubfileFieldValue</code>](amfpageClassSetSubfileFieldValueMethod.html)
<pre>SetSubfileFieldValue(FormatName, FieldName, RRN, Object newValue)</pre>

##### Methods that Get Indicators
[<code>GetOptionIndicator</code>](amfpageClassGetOptionIndicatorMethod.html)
<pre>Char = GetOptionIndicator(FormatName, indicator (1->99))</pre>

[<code>GetOptionIndicators</code>](amfpageClassGetOptionIndicatorsMethod.html)
<pre>Char [100] = GetOptionIndicators(FormatName)</pre>

[<code>GetResponseIndicator</code>](amfpageClassGetResponseIndicatorMethod.html)
<pre>Char = GetResponseIndicator(FormatName, indicator (1->99))</pre>

[<code>GetResponseIndicators</code>](amfpageClassGetResponseIndicatorsMethod.html)
<pre>Char [100] = GetResponseIndicators(FormatName)</pre>

[<code>GetSubfileOptionIndicator</code>](amfpageClassGetSubfileOptionIndicatorMethod.html)
<pre>Char = GetSubfileOptionIndicator(FormatName, RRN(1->), indicator (1->99))</pre>

[<code>GetSubfileOptionIndicators</code>](amfpageClassGetSubfileOptionIndicatorsMethod.html)
<pre>Char [100]= GetSubfileOptionIndicators(FormatName, RRN (1->))</pre>

[<code>GetSubfileResponseIndicator</code>](amfpageClassGetSubfileResponseIndicatorMethod.html)
<pre>Char = GetSubfileResponseIndicator(FormatName, RRN(1->), indicator (1->99))</pre>

[<code>GetSubfileResponseIndicators</code>](amfpageClassGetSubfileResponseIndicatorsMethod.html)
<pre>Char [100]= GetSubfileResponseIndicators(FormatName, RRN (1->))</pre>

##### Methods that Set Indicators
The Setting indicator functions will rise an exception if they are called between <code>*Base.OnCopyDspFileToBrowser</code> and <code>*Base.OnCopyBrowserToDspFile</code> is irrelevant.

[<code>SetOptionIndicator</code>](amfpageClassSetOptionIndicatorMethod.html)
<pre>SetOptionIndicator(string FormatName, indicator (1->99), char newValue01)</pre>

[<code>SetResponseIndicator</code>](amfpageClassSetResponseIndicatorMethod.html)
<pre>SetResponseIndicator(string FormatName, indicator (1->99), char newValue01X)</pre>

[<code>SetSubfileOptionIndicator</code>](amfpageClassSetSubfileOptionIndicatorMethod.html)
<pre>SetSubfileOptionIndicator(FormatName, RRN(1->), indicator (1->99), char newValue01)</pre>

[<code>SetSubfileIndicator</code>](amfpageClassSetSubfileResponseIndicatorMethod.html)
<pre>SetSubfileResponseIndicator(FormatName, RRN(1->), indicator (1->99), char newValue01X)</pre>

#### See Also
<dl>
       <dd>[Reference
        Library](amfReferenceMain.html)</dd>
       <dd>[WebDspf.Page Class](amfPageClass.html)</dd>
       <dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
</dl>

