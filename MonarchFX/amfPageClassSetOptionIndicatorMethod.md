---
title: Page.SetOptionIndicator Method

Id: amfPageClassSetOptionIndicatorMethod
TocParent: amfPageClassMethodsMain
TocOrder: 95

keywords: SetOptionIndicator method
keywords: Page.SetOptionIndicator method

---

Sets the value of an option indicator.

#### Syntax
<pre class="prettyprint"> **SetOptionIndicator(string FormatName, indicator(1->99), char newValue01)** </pre>

*FormatName* is the name of the format as visible to the RPG Program. *Indicator* is the number of the indicator to be set, and can be any number between or equal to 1 and 99. The newValue is the value that the indicator will take on; it can be set to *1* (on) or *0* (off).

#### Return Value
**Char** . The value of the option indicator specified by FormatName and indicator.

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

