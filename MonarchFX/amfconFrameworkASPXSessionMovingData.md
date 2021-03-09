---
title: Moving Data between Workstation File and Display File

Id: amfconFrameworkASPXSessionMovingData
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 180

keywords: Monarch framework ASPX session overview
keywords: concepts, Monarch framework ASPX session overview
keywords: concepts, moving data between workstation file and display file
keywords: moving data between workstation file and display file
keywords: ASNA.Monarch, workstation files
keywords: workstation files, about
keywords: workstation files, using DCLWORKSTNFILE
keywords: display files, about
keywords: DCLWORKSTNFILE, about
keywords: concepts, ASNA.Monarch workstation files
keywords: concepts, ASNA.Monarch display files
keywords: ASPX sessions, workstation files
keywords: ASPX sessions, display files
keywords: ASPX sessions, code behind base class
keywords: ASNA.Monarch.WebDspF.Page class, using
keywords: procedural programs, about

---

The document provides an overview of the interaction between the **Workstation File** and the **Display File** in an ASPX session.

Handling the user interface of an interactive application is a cooperative effort between the procedural program running in the procedural thread and the code behind the page implementing the display file and running in the ASPX thread.

The procedural program uses a workstation file via issueing read and write instructions against the record formats providing or requesting data to the user. Connected to this workstation file is the **code behind** ; a web page running in the ASPX thread.

#### <code>DclWorkstnFile</code>
When the compiler processes the <code>DclWorkstnFile</code> command, it inspects the ASPX file to define the fields in the program. The compiler also creates a DataSet definition to serve as a buffer for the data read and written to the workstation file. This DataSet has one DataTable for each record format found in the ASPX and the DataTables have one DataColumn for each field found in the record format plus a couple of extra fields to hold a direction flag and a snapshot of the indicators.

When the program writes a record to the workstation file, a new DataRow is added to the DataTable of the record format populated with the values of the fields belonging to the record, a snapshot of the current state of the program indicators is also added to the DataRow. If the record format written is not a subfile, the DataTable is cleared before adding the DataRow such that at the most one row is ever present in the **DataTable. DataTables** corresponding to Subfile records are allowed to accumulate multiple **DataRows. DataRows** written by the program are marked with a direction of <code> **Out** </code>.

When the program issues a read to a non-subfile record, the corresponding DataTable is checked to see if there is a DataRow present marked with a direction of In. If there is, then data in the DataRow is used to populate the program's field and execution continues. If there is no available DataRow, then the program signals the device that ** *data is ready for the user* ** (it should be displayed in the browser) and it enters a wait state until the device is signaled with a message of ** *data is ready for the program* ** .

#### Page Class
[ ASNA.Monarch.WebDspF.Page](amfPageClass.html) is used as a base in the code behind the ASPX page and defines two empty virtual methods for which the compiler provides implementation. The compiler inspects the ASPX page and creates implementations with overriding subroutines to copy data to/from the DataSet created with DclWorkstnFile and the server controls present in the page.

ASNA.Monarch.WebDspF.Page is itself based on **System.Web.UI.Page** and it overrides certain methods of the base class. In particular, it overrides the OnPreRender method that fires after the page has been loaded and before it renders its contents as HTML.

On the <code> **OnPreRender** </code> method, ASNA.Monarch.WebDspF.Page checks to see if this request comes from a postback request. If it does, <code>OnPreRender</code> invokes the [ OnCopyBrowserToDspFile](amfPageClassOnCopyBrowserToDspFileMethod.html) to populate the DataSet with the data the user has typed in the server controls. Then the device is signalled with a ** *data is ready for the program* ** message and <code>OnPreRender</code> enters a wait state until the device receives the signal that ** *data is ready for the user* ** . Once this signal is received, <code>OnPreRender</code> invokes the <code>[ OnCopyDspFileToBrowser](amfPageClassOnCopyDspFileToBrowserMethod.html)</code> to populate the server controls of the active records with data from the DataSet. If the request was not a postback, then <code>OnCopyBrowserToDspFile</code> is not called and OnPreRender enters its wait state immediately.

You can override both **OnCopyDspFileToBrowser** and **OnCopyBrowserToDspFile** because they are virtual methods of ASNA.Monarch.WebDspF.Page. If you do, make sure that you call the corresponding base class versions within your own implementation.

**ASNA.Monarch.WebDspF.Page** provides the protected property <code>[RunProgram](amfPageClassRunProgramProperty.html)</code> that allows you to control whether the procedural program is to receive the data that just arrived in this request. There are scenarios where you may want to run the code behind the page implementing the display file but you want the program to keep waiting for its input. The most notorious cases of this scenario are when you are doing some input validation in the code behind or when you are responding to an event caused by non-Monarch controls like calendars. In those cases you can make <code>RunProgram</code> false and maintain the procedural program waiting in its **READ** or **EXFMT** until the user interface code is satisfied with the data provided by the user.

If you are providing your own versions of the **OnCopy** routines, you will probably want to get a hold of the DataSet. The following example shows how to do it.
<pre class="prettyprint"><code class="language-avr">BegSr OnCopyBrowserToDspFile Modifier(*Overrides)Access(*Protected)
   DclFld activeRow System.Data.DataRow
   *base.OnCopyBrowserToDspFile()

   If (DspF.dataSet.Tables["SFLC"].Rows.Count &gt; 0)
        activeRow = DspF.dataSet.Tables["SFLC"].Row[0]
        activeRow =["SETNAME"] = CardexList.SelectedItem.Value
   EndIf
EndSr</code></pre>

In the example above, <code>OnCopyBrowserToDspFile</code> uses the <code>[ DspF](amfPageClassDspFField.html)</code> field of the base class to get the current display file (of type ASNA.Monarch.WebDisplayFile) that has a reference to the [dataSet](amfWebDisplayFileClassdataSetProperty.html). Use uppercase names to get to the table corresponding to a record format and to get a column of a row. A record is considered active if its table has at least one row.

**ASNA.Monarch.WebDspF.Page** also provides a group of methods loosely termed the Dataflow or Convenient Access Methods. These allow developers to get or set the values of various fields and indicators within the instance of the Page class. They are further explored in the [Data Flow Overview](amfDataFlow.html) topic.

#### Next: [Message Files](amfMessageFiles.html)

#### Previous: [Monarch Framework ASPX Session Overview](amfconFrameworkASPXSessionOverview.html)

#### See Also
<dl>
	  <dd>[Data Flow Overview](amfDataFlow.html)</dd>
        <dd>[Display File Concepts](amfconDisplayFiles.html)</dd>
       <dd>[WebServer Controls Overview](amfWebServerControlsOverview.html)</dd>
       <dd>[WebDeviceClass](amfWebDeviceClass.html)</dd>
       <dd>[WebJob Class](amfWebJobClass.html)</dd>
       <dd>[Job Class](amfJobClass.html)</dd>
       <dd>[WebDisplayFile Class](amfWebDisplayFileClass.html)</dd>
       <dd>[WebDisplayFile.dataSet Property](amfWebDisplayFileClassdataSetProperty.html)</dd>
       <dd>[Page Class DspF Field](amfPageClassDspFField.html)</dd>
</dl>

