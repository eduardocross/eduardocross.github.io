---
title: Page.GetSubfileResponseIndicator Method

Id: amfPageClassGetSubfileResponseIndicatorMethod
TocParent: amfPageClassMethodsMain
TocOrder: 59

keywords: GetSubfileResponseIndicator method
keywords: Page.GetSubfileResponseIndicator method

---

Gets a copy of the value of a subfile response indicator.

#### Syntax
<pre class="prettyprint"> **Char = GetSubfileResponseIndicator(FormatName, RRN, indicator)** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *RRN* is the Relative Record Number of the subfile as visible to the RPG program; can be set to any valid integer of 1 or greater. *Indicator* is the number of the indicator to get, and can be any number between or equal to 1 and 99.

#### Return Value
**Char** . A copy of the value of the subfile response indicator defined by FormatName, and RRN.

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

