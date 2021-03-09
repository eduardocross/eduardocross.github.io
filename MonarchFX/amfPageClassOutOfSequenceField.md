---
title: Page.OutOfSequence Field

Id: amfPageClassOutOfSequenceField
TocParent: amfPageClassFieldsMain
TocOrder: 50

keywords: OutOfSequence field
keywords: Page.OutOfSequence field

keywords: web browser, request out of sequence
keywords: .aspx files, web browser request out of sequence
keywords: ASP.NET pages, web browser request out of sequence
keywords: aspx files, web browser request out of sequence
keywords: how to, determine correct web browser request sequence

---

A boolean value indicating the request from the browser is out of sequence.

#### Syntax
<pre class="syntax"> **BegProp OutOfSequence Access(*Protected) Type(*Boolean)** </pre>

<!--mine -->

#### Return Value
Boolean. **True** if the request from the browser is out of sequence; otherwise **False** .

#### Remarks
This field gets established in the page Load phase. The typical cause of out of sequence conditions is if the user hits the back button or jumped to a previously bookmarked page. A **True** setting can prevent the copy-browser-to-display-file and the process-business-rules phases from executing ([Control Execution Lifecycle](amfconControlExecutionLifecycle.html)).
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
</dl>

