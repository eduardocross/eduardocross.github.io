---
title: ASNA Monarch Control Execution Lifecycle Concepts

Id: amfconControlExecutionLifecycle
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 50

keywords: Control Execution Lifecycle
keywords: ASNA Monarch, control execution lifecycle
keywords: concepts, ASNA.  Control Execution Lifecycle

---

This document provides information regarding the Control Execution Lifecycle showing the phase, action and / or method or event that is triggered. See **ASP.NET Page Object Model or Control Execution Lifecycle** in the MSDN help for further detail about the ASP.NET phases.

The <code> **CreateChildControls** </code> method is not listed in the table because it is called whenever the ASP.NET page framework needs to create the controls tree and this method call is not limited to a specific phase in a control's life cycle. For example, <code> **CreateChildControls** </code> can be invoked when loading a page, during data binding, or during rendering.

#### Control Execution Lifecycle Table
<table class="mytable" style="border-spacing: 2px" cellspacing="0" width="90%">
          <colgroup span="1">
            <col span="1" style="WIDTH: 25%" />
            <col span="1" style="WIDTH: 40%" />
            <col span="1" style="WIDTH: 35%" />
          </colgroup>
          <tr>
            <th>Phase</th>
            <th>Action</th>
            <th style="width: 292px">Method or Event to
            Override</th>
          </tr>
          <tr>
            <td>Initialize</td>
            <td>Initialize settings needed
            during the lifetime of the incoming Web request.</td>
            <td style="width: 292px"> **Init**  event / 
 **OnInit**  method</td>
          </tr>
          <tr>
            <td>Load view state</td>
            <td>At the end of this phase,
            the 
 **ViewState**  property of a control is automatically
            populated.</td>
            <td style="width: 292px"> **LoadViewState**  method</td>
          </tr>
          <tr>
            <td>Process postback data</td>
            <td>Process incoming form data
            and update properties accordingly.</td>
            <td style="width: 292px"> **LoadPostData**  method</td>
          </tr>
          <tr>
            <td>Load</td>
            <td>Perform actions common to
            all requests, such as setting up a database query. At
            this point, server controls in the tree are created and
            initialized, the state is restored, and form controls
            reflect client-side data.</td>
            <td style="width: 292px"> **Load**  event / 
 **OnLoad**  method</td>
          </tr>
          <tr>
            <td>Send postback change
            notifications</td>
            <td>Raise change events in
            response to state changes between the current and
            previous postback.</td>
            <td style="width: 292px"> **RaisePostDataChangedEvent**  method</td>
          </tr>
          <tr>
            <td>Handle postback events</td>
            <td>Handle the client-side
            event that caused the postback and raise appropriate
            events on the server.</td>
            <td style="width: 292px"> **RaisePostBackEvent**  method</td>
          </tr>
          <tr>
            <td>Prerender</td>
            <td>Perform any necessary
            pre-rendering steps prior to saving view state and
            rendering content.</td>
            <td style="width: 292px"> **PreRender**  event / 
 **OnPreRender**  method</td>
          </tr>
          <tr>
            <td> **NEW Monarch Phase:** 
              <br clear="none" />Copy browser to display file</td>
            <td>(Also see 
            [
            Page.OutOfSequence](amfPageClassOutOfSequenceField.html)) If this request is a postback,
            the data sent by the browser is copied to the display
            buffer data set. Code-behind logic here can stop the
            next phase.</td>
            <td style="width: 292px"> **OnCopyBrowserToDspFile**  method 
- [
                Page.OnCopyBrowserToDspFile](amfPageClassOnCopyBrowserToDspFileMethod.html)

</td>
          </tr>
          <tr>
            <td> **NEW Monarch Phase:** 
             Process Business Rules</td>
            <td>Program waiting on an 
 **EXFMT**  
            continues to run until a new 
 **EXFMT**  is found (or read).</td>
            <td style="width: 292px"> **AVR program** 
            </td>
          </tr>
          <tr>
            <td> **NEW Monarch Phase:
              <br clear="none" />** 
              Copy display file to browser</td>
            <td>Data is copied from the
            display buffer data set to the "dds" controls in the
            page. Perform any updates before the output is
            rendered. Any changes made to the state of controls can
            be saved, while changes made in the rendering phase are
            lost.</td>
            <td style="width: 292px"> **OnCopyDspFileToBrowser**  method 
- [
                Page.OnCopyDspFileToBrowser](amfPageClassOnCopyDspFileToBrowserMethod.html)

</td>
          </tr>
          <tr>
            <td>Save state</td>
            <td>The 
 **ViewState**  property of a control is automatically persisted
            to a string object after this stage.</td>
            <td style="width: 292px"> **SaveViewState**  method</td>
          </tr>
          <tr>
            <td style="height: 22px">Render</td>
            <td style="height: 22px">Generate output to be
            rendered to the client.</td>
            <td style="height: 22px; width: 292px"> **Render**  method</td>
          </tr>
          <tr>
            <td>Unload</td>
            <td>Perform any final cleanup
            before the control is torn down. Control authors
            generally perform cleanup in 
 **Dispose**  and do not handle this event.</td>
            <td style="width: 292px"> **UnLoad**  event / 
 **OnUnload**  method</td>
          </tr>
</table>

#### Next: [Monarch Job and Program Classes](amfconMonarchJobandProgramClasses.html)

#### Previous: [Execution Context](amfconExecutionContext.html)

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
