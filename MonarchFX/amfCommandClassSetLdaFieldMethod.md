---
title: Command.SetLdaField Method

Id: amfCommandClassSetLdaFieldMethod
TocParent: amfCommandClassMethods
TocOrder: 100

keywords: SetLdaField method
keywords: Command.SetLdaField method
keywords: non-display file aspx.vr, SetLdaField command
keywords: aspx.vr, non-display file, SetLdaField command
keywords: local data area, non-display file
keywords: local data area, setting
keywords: MonarchJobUnavailableException
keywords: MonarchJobEndException

---

Assigns a value to a portion of the jobs' LDA (local data area).

#### Syntax
<pre class="syntax"> **BegSr SetLdaField Access(*Public) Type(Void)
   DclSrParm *start*     Type (*Integer2)
   DclSrParm *length*    Type (*Integer2)
   DclSrParm *newValue*  Type (*String)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
 *start* 
        </dt>
        <dd>The starting position in the local data area that the 
 *newValue*  data will be inserted.</dd>
        <dt>
 *length* 
        </dt>
        <dd>The length of the field to be inserted into the local
        data area.</dd>
        <dt>
 *newValue* 
        </dt>
        <dd>The value to assign to the local data area
        starting at the 
 *start*  position for the 
 *length*  specified.</dd>
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

#### Example
<pre class="example"><span style="COLOR: blue">DclFld</span> Command <span style="COLOR: blue">Type</span>(ASNA.Monarch.Command) <span style="COLOR: blue">New</span>(<span style="COLOR: blue">*Base</span>.Context)
   Command.SetLdaField(512, 12, "SomeNewValue")</pre>

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

