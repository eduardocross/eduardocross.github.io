---
title: Page.ContinueExecution Method

Id: amfPageClassContinueExecutionMethod
TocParent: amfPageClassMethodsMain
TocOrder: 10

keywords: ContinueExecution method
keywords: Page.ContinueExecution method

keywords: .aspx files, continuing after pause
keywords: ASP.NET pages, continuing after pause
keywords: aspx files, continuing after pause
keywords: how to, continue aspx session after pause

---

Continues execution after execution has been paused.

#### Syntax
<pre class="prettyprint"> **BegSr ContinueExecution Access(*Protected) Type(Void)
   DclSrParm *key*  Type (ASNA.Monarch.WebDspF.AidKeyIBM)
   DclSrParm *resultingIndicators*  Type (*String)** </pre>

#### Parameters
<dl>
        <dt>
 *key* 
        </dt>
        <dd>A reference to an 
        [
        ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html) enumeration value that
        contains the identification of the function key used to
        focus attention on this control.</dd>
        <dt>
 *resultingIndicators* 
        </dt>
        <dd>The indicators used to pass control to the message
        handler for subsequent action.</dd>
</dl>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[Page Class](amfPageClass.html)</dd>
		<dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
        <dd>[Page Class Members](amfPageClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[ASNA.Monarch.WebDspF.AidKeyIBM](amfAidKeyIBMEnumeration.html)</dd>
</dl>

