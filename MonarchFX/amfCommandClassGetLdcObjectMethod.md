---
title: Command.GetLdcObject Method

Id: amfCommandClassGetLdcObjectMethod
TocParent: amfCommandClassMethods
TocOrder: 50

keywords: GetLdcObject method
keywords: Command.GetLdcObject method
keywords: non-display file aspx.vr, GetLdcObject command
keywords: aspx.vr, non-display file, GetLdcObject command
keywords: local data collection, non-display file
keywords: local data collection, getting
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Returns the value for an entry from the jobs' LDC (local data collection).

#### Syntax
<pre class="syntax"> **BegFunc GetLdcObject Access(*Public) Type(*String)
   DclSrParm *name*  Type (*String)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
          <code> *name* </code>
        </dt>
        <dd>The name of the object whose value is to be
        returned.</dd>
</dl>

<!--mine -->

#### Return Value
A string containing a value for the named entry from the jobs' local data collection.
<!--mine -->

#### Exceptions
The following exceptions may be encountered during the execution of this method.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <code><th>Value</th></code>
            <th>Condition</th>
          </tr>          <tr>
            <code><td>MonarchJobEndedException</td></code>
            <td>The Monarch Job has ended
            in an exception.</td>
          </tr>
          <tr>
            <code><td>MonarchJobUnavailableException</td></code>
            <td>There is no Monarch Job
            available to accept commands.</td>
          </tr>
</table>

<!--mine -->

#### Remarks
he LDC can contain **any** type of object, however only those that are of type **<code>String</code>** can be sent to the Yellow side.

To access the LDC strong values from the Yellow side use this method with the following syntax
- <code>public string GetLdcObject( string name )</code>

This command can be executed only when the Job is waiting in either of these states:
- Waiting for input from the user (in a READ or EXFMT of a display file)
- Accepting Commands via the AcceptCommand method on MonarchJob

#### Example
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
<span style="COLOR: blue">DclFld</span> CompanyName <span style="COLOR: blue">Type</span>(<span style="COLOR: gray">*String</span>)
   CompanyName = Command.GetLdcObject("CompanyName")</pre>

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

