---
title: Page.GetSubfileDataRow Method

Id: amfPageClassGetSubfileDataRowMethod
TocParent: amfPageClassMethodsMain
TocOrder: 50

keywords: GetSubfileDataRow method
keywords: Page.GetSubfileDataRow method

---

Gets the value of a Subfile Data Row.

#### Syntax
<pre class="prettyprint"> **DataRow GetSubfileDataRow(FormatName, RRN)** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *RRN* is the Relative Record Number of the subfile row as visible to the RPG program.

#### Return Value
**DataRow** . Returns an array with a copy of the Subfile DataRow specified by FormatName and RRN.

#### Exceptions
None.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl>
        <dd>[Page Class](amfPageClass.html)</dd>
		<dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
        <dd>[Page Class Members](amfPageClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

