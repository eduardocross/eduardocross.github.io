---
title: Page.SetSubfileOptionIndicator Method

Id: amfPageClassSetSubfileOptionIndicatorMethod
TocParent: amfPageClassMethodsMain
TocOrder: 102

keywords: SetSubfileOptionIndicator method
keywords: Page.SetSubfileOptionIndicator method

---

Sets the selected subfile option indicator.

#### Syntax
<pre class="prettyprint"> **SetSubfileOptionIndicator(FormatName, RRN(1->), indicator (1->99), char newValue01)** </pre>

*FormatName* is the name of the format as visible to the RPG Program. *Indicator* is the number of the indicator to be set, and can be any number between or equal to 1 and 99. The newValue is the value that the indicator will take on; it can be set to *1* (on) or *0* (off).

#### Return Value
**Char** . The new value of the subfile option indicator selected by the FormatName, RRN, and indicator.

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

