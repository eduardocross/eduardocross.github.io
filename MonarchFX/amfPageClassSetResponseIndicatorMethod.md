---
title: Page.SetResponseIndicator Method

Id: amfPageClassSetResponseIndicatorMethod
TocParent: amfPageClassMethodsMain
TocOrder: 97

keywords: SetResponseIndicator method
keywords: Page.SetResponseIndicator method

---

Sets the value of a response indicator.

#### Syntax
<pre class="prettyprint"> **SetResponseIndicator(string FormatName, indicator(1->99), char newValue(01x)** </pre>

*FormatName* is the name of the format as visible to the RPG Program. *Indicator* is the number of the indicator to be set, and can be any number between or equal to 1 and 99. The newValue is the value that the indicator will take on; it can be set to *1* (on), *0* (off), or *x* (ignore). Any other character will be interpreted as "x".

#### Return Value
**Char** . The value of the response indicator specified by FormatName and indicator.

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

