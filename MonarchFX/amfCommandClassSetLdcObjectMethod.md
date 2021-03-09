---
title: Command.SetLdcObject Method

Id: amfCommandClassSetLdcObjectMethod
TocParent: amfCommandClassMethods
TocOrder: 110

keywords: SetLdcObject method
keywords: Command.SetLdcObject method
keywords: non-display file aspx.vr, SetLdcObject command
keywords: aspx.vr, non-display file, SetLdcObject command
keywords: local data collection, non-display file
keywords: local data collection, setting
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Assigns a value to an entry in the jobs' LDC (local data collection).

#### Syntax
<pre class="syntax"> **BegSr SetLdcObject Access(*Public) Type(Void)
   DclSrParm *name*   Type (*String)
   DclSrParm *value*  Type (*String)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
 *name* 
        </dt>
        <dd>The name of the entry.</dd>
        <dt>
 *value* 
        </dt>
        <dd>The value assigned to the entry name.</dd>
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

#### Remarks
If the <code> *name* </code> entry does not exist, it will be created. Otherwise, the <code> *value* </code> replaces the original value for the named entry.

The LDC can contain **any** type of object, however only those that are of type <code> **String** </code> can be sent to the Yellow side.

To access the LDC strong values from the Yellow side use this method with the following syntax
- <code>public void SetLdcObject( string name, string value )</code>

This command can be executed only when the Job is waiting in either of these states:
- Waiting for input from the user (in a <code>READ</code> or <code>EXFMT</code> of a display file)
- Accepting Commands via the <code>AcceptCommand</code> method on MonarchJob

<!--mine -->

#### Example
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
   Command.SetLdcObject("CompanyName", "ACME")</pre>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfWebDspFASNAMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.Monarch.WebDspF.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 
			Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

