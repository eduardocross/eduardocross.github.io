---
title: Command.RemoveLdcObject Method

Id: amfCommandClassRemoveLdcObjectMethod
TocParent: amfCommandClassMethods
TocOrder: 70

keywords: RemoveLdcObject method
keywords: Command.RemoveLdcObject method
keywords: non-display file aspx.vr, RemoveLdcObject command
keywords: aspx.vr, non-display file, RemoveLdcObject command
keywords: local data collection, non-display file
keywords: local data collection, removing
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Removes an entry from the jobs' LDC (local data collection).

#### Syntax
<pre class="syntax"> **BegFunc RemoveLdcObject Access(*Public) Type(Void)
   DclSrParm *name*  Type (*String)** 
          </pre>

<!--mine -->

#### Parameters
<dl>
            <dt>
              <code> *name* </code>
            </dt>
            <dd>The name of the entry to be removed.</dd>
</dl>

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
              </tr>
              <tr>
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
   Command.RemoveLdcObject("CompanyName")</pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html) 

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

          <!--mine -->

#### See Also
<dl>
            <dd>
              <a shape="rect" href="amfCommandClass.htm">Command Class</a>
            </dd>
            <dd>
              <a shape="rect" href="amfCommandClassMembers.htm">Command Class Members</a>
            </dd>
            <dd>
              <a shape="rect" href="amfWebDspFASNAMonarchNamespace.htm">ASNA.Monarch Namespace</a>
            </dd>
</dl>

