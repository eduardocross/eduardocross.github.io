---
title: Command.GetLdaField Method

Id: amfCommandClassGetLdaFieldMethod
TocParent: amfCommandClassMethods
TocOrder: 40

keywords: GetLdaField method
keywords: Command.GetLdaField method
keywords: non-display file aspx.vr, GetLdaField command
keywords: aspx.vr, non-display file, GetLdaField command
keywords: local data area, non-display file
keywords: local data area, getting
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Returns a value from a portion of the jobs' LDA (local data area).

#### Syntax
<pre class="syntax"> **BegFunc GetLdaField Access(*Public) Type(*String)
   DclSrParm *start*   Type (*Integer2)
   DclSrParm *length*  Type (*Integer2)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
          <code> *start* </code>
        </dt>
        <dd>The starting position in the local data area to begin
        retrieving data.</dd>
        <dt>
          <code> *length* </code>
        </dt>
        <dd>The length of the field to retrieve from the local data
        area.</dd>
</dl>

<!--mine -->

#### Return Value
A string containing a value from a portion of the jobs' local data area starting at the <code> *start* </code> position for the <code> *length* </code> specified.
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
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
<span style="COLOR: blue">DclFld</span> SomeString <span style="COLOR: blue">Type</span>(<span style="COLOR: gray">*String</span>)
   SomeString = Command.GetLdaField(512, 11)</pre>

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

