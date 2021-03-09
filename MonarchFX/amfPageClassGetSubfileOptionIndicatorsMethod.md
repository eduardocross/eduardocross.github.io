---
title: Page.GetSubfileOptionIndicators Method

Id: amfPageClassGetSubfileOptionIndicatorsMethod
TocParent: amfPageClassMethodsMain
TocOrder: 57

keywords: GetSubfileOptionIndicators method
keywords: Page.GetSubfileOptionIndicators method

---

Gets all subfile option indicators from a range of rows.

#### Syntax
<pre class="prettyprint"> **Char [100]= GetSubfileOptionIndicators(FormatName, RRN)** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *RRN* is the Relative Record Number of the Subfile as visible to the RPG program; can be set to any valid integer of 1 or greater.

#### Return Value
**Char** . Returns a char object containing a copy of the option indicator values.

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

