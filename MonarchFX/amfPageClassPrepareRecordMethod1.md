---
title: Page.PrepareRecord Method (String)

Id: amfPageClassPrepareRecordMethod1
TocParent: amfPageClassPrepareRecordMethods
TocOrder: 10

---

Returns the **System.Data.DataRow** object for the subfile record format name specified in preparation for the rendering phase.

#### Syntax
<pre class="prettyprint"> **BegFunc PrepareRecord Access(*Protected) Type(System.Data.DataRow)
   DclSrParm *recordFormatName*  Type (*String)** </pre>

#### Parameters
<dl>
        <dt>
 *recordFormatName* 
        </dt>
        <dd>A name of the format that refers to a given layout of
        data in a record in the subfile.</dd>
</dl>

#### Return Value
Object for the subfile record format name specified.
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
      <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd></dl>

