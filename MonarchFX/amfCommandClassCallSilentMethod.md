---
title: Command.CallSilent Method (string, string, string[])

Id: amfCommandClassCallSilentMethod
TocParent: amfCommandClassMethods
TocOrder: 20

keywords: CallSilent method
keywords: Command.CallSilent method
keywords: non-display file aspx.vr, CallSilent command
keywords: non-display file aspx.vr, calling program without displaying display file
keywords: aspx.vr, non-display file, CallSilent command
keywords: how to, call program without displaying display file
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException
keywords: ProgramCallException

---

<code> **CallSilent** </code> invokes an interactive program from a non-display file aspx.vr (yellow thread) and prevents the display of the program's display file in the browser.

#### Syntax
<pre class="syntax"> **BegFunc CallSilent Access(*Public) Type(ASNA.Monarch.WebDisplayFile)
   DclSrParm *assemblyName*  Type (*String)
   DclSrParm *programName*   Type (*String)
   DclSrParm *parms*         Type (*String) Rank (1)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
          <code> *assemblyName* </code>
        </dt>
        <dd>String.  The name of the assembly that
        contains the program to be called.  The assembly
        must be placed in a folder visible to the blue
        thread. This is typically the 
 **/bin**  folder of the web site.  The
        assembly name is typically the DLL name but without the
        ".DLL" extension.</dd>
        <dt>
          <code> *programName* </code>
        </dt>
        <dd>String.  The fully qualified name of the
        program to be invoked.  This name must include the
        namespace of the program.</dd>
        <dt>
          <code> *parms* </code>
        </dt>
        <dd>String.  An array of string parameters to be
        passed to the program's *ENTRY procedure.  The
        parameters are input/output.</dd>
</dl>

<!--mine -->

#### Returns
[ ASNA.Monarch.WebDisplayFile](amfWebDisplayFileClass.html).
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Value</th>
            <th>Condition</th>
          </tr>          <tr>
            <td><code>MonarchJobEndedException</code></td>
            <td>The Monarch Job has ended
            in an exception.</td>
          </tr>
          <tr>
            <td><code>MonarchJobUnavailableException</code></td>
            <td>There is no Monarch Job
            available to accept commands.</td>
          </tr>
          <tr>
            <td><code>ProgramCallException</code></td>
            <td>There was an error calling
            the program.</td>
          </tr>
</table>

<!--mine -->

#### Remarks
<code> **CallSilent** </code> can be used to invoke an interactive program from the yellow thread and prevent the display of the program's display file in the browser. When the interactive program performs an <code>EXFMT</code> (or <code>READ</code>), it will stop waiting for input from the user and <code> **CallSilent** </code> will return the WebDisplayFile object allowing the caller to inspect the dataset containing the data tables of the record formats written by the interactive program on the blue thread.

The caller of <code> **CallSilent** </code> is responsible for feeding input to the waiting interactive program. This is done by updating the appropriate rows of the data table of the WebDisplayFile and then executing the method [ PushKeyFocus](amfCommandClassPushKeyFocusMethod.html).
<!-- start -->

#### Example
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
<span style="COLOR: blue">DclFld</span> DspF    <span style="COLOR: blue">Type</span>(ASNA.Monarch.WebDisplayFile)
<span style="COLOR: blue">DclFld</span> data    <span style="COLOR: blue">Type</span>(System.Data.DataSet)
<span style="COLOR: blue">DclArray  </span> Parms <span style="COLOR: blue">Dim</span>(2)  <span style="COLOR: blue">Type</span>(<span style="COLOR: gray">*String</span>)
Parms[0] = "SFSTATE"
Parms[1] = ""
DspF = Command.CallSilent("StaterLogic","StaterLogic.CUSTPRMPT", Parms)
<span style="COLOR: blue">If</span> (DspF &lt;&gt; <span style="COLOR: blue">*Nothing</span>)
    data = DspF.DataSet     
    Command.PushKeyFocus(ASNA.Monarch.Command.AidKey.F12, 0, "")
<span style="COLOR: blue">EndIf</span></pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[Command
        Class](amfCommandClass.html)</dd>
        <dd>[Command
        Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch
        Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
        <dd>[
        ASNA.Monarch.WebDisplayFile](amfWebDisplayFileClass.html)</dd>
        <dd>[PushKeyFocus
        Method](amfCommandClassPushKeyFocusMethod.html)</dd>
</dl>

