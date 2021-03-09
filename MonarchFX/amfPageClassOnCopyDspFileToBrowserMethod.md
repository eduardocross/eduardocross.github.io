---
title: Page.OnCopyDspFileToBrowser Method (string, integer, integer, string)

Id: amfPageClassOnCopyDspFileToBrowserMethod
TocParent: amfPageClassMethodsMain
TocOrder: 70

keywords: IndicatorArrayLengthException
keywords: OnCopyDspFileToBrowser method
keywords: Page.OnCopyDspFileToBrowser method
keywords: web browser, formulating response
keywords: web server, formulating response
keywords: .aspx files, formulating web server response
keywords: ASP.NET pages, formulating web server response
keywords: aspx files, formulating web server response
keywords: how to, formulate web server response

---

Allows you to intervene when data is being copied from the display buffer data sent to the 'dds' controls in the page. The Response is formulated here.

#### Syntax
<pre class="syntax"> **BegSr OnCopyDspFileToBrowser Modifier(*Overrides) Access(*Protected)** </pre>

#### Remarks
The **OnCopyDspFileToBrowser** callback subroutine executes right before the workstation data is sent from the Web Server to the Client (browser).

#### Example
In the example below, OnCopyDspFileToBrowser uses the [DspF](amfPageClassDspFField.html) field of the base class to get ahold of the current display file that has a reference to the [dataSet](amfWebDisplayFileClassdataSetProperty.html). Use uppercase names to get to the table corresponding to a record format and to get to columns of a row. A record is considered active if its table has at least one row.

When overriding OnCopyDspFileToBrowser, it is very important to call the base subroutine as indicating below; missing such call would result in fields in the browser not initialized to the values according to the RPG program.

In the example below, workstation record format name "FMT003" is checked; if active, the dataSetRow where the data for record FMT0003's fields is stored, gets passed to a "shared" subroutine in the class "WindowWidget", so that a non-DDS asp control, RadioButtonList (with id="FMT003_SCNOTPTY_RADIOS"), gets prepared with the choice controls's fields, to achieve an enhanced User Interface.
<pre class="example"><span style="color:blue;">BegSr</span> OnCopyDspFileToBrowser <span style="color:blue;">Modifier</span>(<span style="color:gray;">*Overrides</span>) <span style="color:blue;">Access</span>(<span style="color:gray;">*Protected</span>)
       <span style="color:blue;">If</span> (DspF.dataSet.Tables["FMT003"].Rows.Count &gt; 0 )
           WindowWidget.PrepareSngChoiceSelection(DspF.dataSet.Tables["FMT003"].Rows[0], "SCNOTPTY",FMT003_SCNOTPTY_RADIOS )
           WindowWidget.PrepareSngChoiceSelection(DspF.dataSet.Tables["FMT003"].Rows[0], "SCCPYOPT",FMT003_SCCPYOPT_RADIOS )
           WindowWidget.PrepareMltChoiceSelection(DspF.dataSet.Tables["FMT003"].Rows[0], "SCPRTOPT",FMT003_SCPRTOPT_CHECKBOXES ) 
       <span style="color:blue;">EndIf
   *base</span>.OnCopyDspFileToBrowser()   
<span style="color:blue;">EndSr</span></pre>

#### Notes
The implementation of class "WindowWidget" is not shown in this example (it can be requested to tech-support if desired). The first parameter for WindowWidget.PrepareSngChoiceSelection is declared as:
<pre class="example"><span style="color:blue;">DclSrParm</span> elements <span style="color:blue;">Type</span>(System.Data.DataRow)</pre>
for operations such as:
<pre class="example"><span style="color:blue;">If</span> elements["CHCTLFLD"] = "1"     
     radio.Selected = <span style="color:blue;">*true
EndIf</span></pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
 <dd>[Page Class](amfPageClass.html)</dd>
 <dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
 <dd>[Page Class Members](amfPageClassMembers.html)</dd>
 <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
 <dd>[Moving Data in an ASPX Session](amfconFrameworkASPXSessionMovingData.html)</dd>
</dl>

