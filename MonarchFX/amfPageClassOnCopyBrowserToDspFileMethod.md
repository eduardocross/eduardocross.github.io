---
title: Page.OnCopyBrowserToDspFile Method

Id: amfPageClassOnCopyBrowserToDspFileMethod
TocParent: amfPageClassMethodsMain
TocOrder: 65

keywords: OnCopyBrowserToDspFile method
keywords: Page.OnCopyBrowserToDspFile method
keywords: web browser, formulating request
keywords: web server, formulating request
keywords: .aspx files, formulating web server request
keywords: ASP.NET pages, formulating web server request
keywords: aspx files, formulating web server request
keywords: how to, formulate web server request

---

Allows you to intervene when data is being copied from the data sent by the browser to the display buffer's data set. The **Request** is processed here.

#### Syntax
<pre class="syntax"> **BegSr OnCopyBrowserToDspFile Modifier(*Overrides) Access(*Protected)** </pre>

#### Remarks
The **OnCopyBrowserToDspFile** callback subroutine executes right before the data submitted from the Client (browser) is copied to the workstation data on the Web Server.

#### Example
In the example below, OnCopyBrowserToDspFile uses the [DspF](amfPageClassDspFField.html) field of the base class to get the current display file that has a reference to the [dataSet](amfWebDisplayFileClassdataSetProperty.html). Use uppercase names to get to the table corresponding to a record format and to get a column of a row. A record is considered active if its table has at least one row.

When overriding OnCopyBrowserToDspFile, it is very important to call the base subroutine as indicated below; missing such call would result in the RPG fields not having the values submitted by the user.

In the example below, workstation record format named "FMT003" is checked; if active, then the dataSetRow where the data for record FMT003's fields is stored, gets passed to a "shared" subroutine in the class "WindowWidget", so that certain selection field (for example, "SCNOTPTY") is updated based on the selection of the RadioButtonList (with id = "FMT003_SCNOTPTY_RADIOS") - an asp control manually inserted into the page to modernize the User Interface.
<pre class="prettyprint"><code class="language-avr">BegSr OnCopyBrowserToDspFile Modifier(*Overrides) Access(*Protected)   
    *base.OnCopyBrowserToDspFile()
    If ( DspF.dataSet.Tables["FMT003"].Rows.Count &gt; 0 )
           WindowWidget.UpdateSngChoiceField(DspF.dataSet.Tables["FMT003"].Rows[0], "SCNOTPTY",FMT003_SCNOTPTY_RADIOS )
           WindowWidget.UpdateSngChoiceField(DspF.dataSet.Tables["FMT003"].Rows[0], "SCCPYOPT",FMT003_SCCPYOPT_RADIOS )
           WindowWidget.UpdateMltChoiceFields(DspF.dataSet.Tables["FMT003"].Rows[0], "SCPRTOPT",FMT003_SCPRTOPT_CHECKBOXES ) 
    EndIf
EndSr</code></pre>

#### Notes
The implementation of class "WindowWidget" is not shown in this example (it can be requested to tech-support if desired). The first parameter for WindowWidget.UpdateSngChoiceField is declared as: 
<pre class="example"><span style="color:blue;">DclSrParm</span> elements <span style="color:blue;">Type</span>(System.Data.DataRow)</pre>
so that an operation such as: 
<pre class="example">elements["SCNOTPTY"] = "1"</pre>
may be executed, to affect RPG fields with values resulting from the use of non-DDS asp controls, to achieve a particular special desired behavior.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dd>[Page Class](amfPageClass.html)</dd>
<dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
    <dd>[Page Class Members](amfPageClassMembers.html)</dd>
     <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
      <dd>[Moving Data in an ASPX Session](amfconFrameworkASPXSessionMovingData.html)</dd></dl>

