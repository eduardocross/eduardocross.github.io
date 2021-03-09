---
title: Command Constructor()

Id: amfCommandClassConstructors
TocParent: amfCommandClass
TocOrder: 10

keywords: Command class, constructors
keywords: Command.Command constructors
keywords: constructors [ASNA.Monarch], Command class
keywords: aspx.vr, non-display file, constructor
keywords: non-display file aspx.vr, constructor
keywords: MonarchJobUnavailableException

---

This method constructs a new instance of a <code> **Command** </code> object.

#### Syntax
<pre class="syntax"> **BegConstructor Command Access(*Public)
   DclSrParm httpContext Type(System.Web.HttpContext)** </pre>

<!--mine -->

#### Parameters
<dl>
        <dt>
          <code> *httpContext* </code>
        </dt>
        <dd>A 
        <code> **System.Web.HttpContext** </code> object
        reference.</dd>
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
            <td><code>MonarchJobUnavailableException</code></td>
            <td>There is no Monarch Job
            available to accept commands.</td>
          </tr>
</table>

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

