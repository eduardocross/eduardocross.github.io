---
title: Page.GetSubfileResponseIndicators Method

Id: amfPageClassGetSubfileResponseIndicatorsMethod
TocParent: amfPageClassMethodsMain
TocOrder: 60

keywords: GetSubfileResponseIndicators method
keywords: Page.GetSubfileResponseIndicators method

---

Gets all subfile response indicators from a range of rows.

#### Syntax
<pre class="prettyprint"> **Char [100]= GetSubfileResponseIndicators(FormatName, RRN)** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *RRN* is the Relative Record Number of the Subfile as visible to the RPG program; can be set to any valid integer of 1 or greater.

#### Return Value
**Char** . Returns a char object containing a copy of the response indicator values.

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

