---
title: Command.RequestShutdown Method

Id: amfCommandClassRequestShutdownMethod
TocParent: amfCommandClassMethods
TocOrder: 80

keywords: RequestShutdown method
keywords: Command.RequestShutdown method
keywords: non-display file aspx.vr, RequestShutdown command
keywords: aspx.vr, non-display file, RequestShutdown commands
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Requests the job to shutdown. All active programs in the job will be ended.

#### Syntax
<pre class="syntax"> **BegSr RequestShutdown() Access(*Public) Type(Void)** </pre>

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
</table>

<!--mine -->

#### Example
<pre class="example"><span style="color: blue">BegSr</span> btnShutDown_Click <span style="color: blue">Access</span>(<span style="color: gray">*Private</span>) <span style="color: blue">Event</span>(<span style="color: blue">*this</span>.btnShutDown.Click)
  <span style="COLOR: blue">DclSrParm</span> <span style="color: gray">*Object</span>
  <span style="color: blue">DclSrParm</span> e System.EventArgs
  <span style="color: #0000ff">DclFld</span> Command <span style="color: #0000ff">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
  Command.RequestShutdown()
<span style="color: #0000ff">EndSr</span></pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

