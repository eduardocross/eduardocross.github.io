---
title: Page.GetResponseIndicator Method

Id: amfPageClassGetResponseIndicatorMethod
TocParent: amfPageClassMethodsMain
TocOrder: 45

keywords: GetResponseIndicator method
keywords: Page.GetResponseIndicator method

---

Returns a copy of the selected response indicator value.

#### Syntax
<pre class="prettyprint"> **Char = GetResponseIndicator(FormatName, indicator (1->99))** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *Indicator* is the number of the indicator to get, and can be any number between or equal to 1 and 99.

#### Return Value
**Char** . A copy of the value of the selected response indicator.

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

