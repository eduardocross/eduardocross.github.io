---
title: Page.PrepareRecord Method (String, Integer)

Id: amfPageClassPrepareRecordMethod2
TocParent: amfPageClassPrepareRecordMethods
TocOrder: 20

---

Returns the **System.Data.DataRow** object for the subfile record format name and relative record number specified in preparation for the rendering phase.

#### Syntax
<pre class="syntax"> **BegFunc PrepareRecord Access(*Protected) Type(System.Data.DataRow)
   DclSrParm *recordFormatName*  Type (*String)
   DclSrParm *subfileRecordNumber*  Type (*Integer)** </pre>

#### Parameters
<dl>
        <dt>
 *recordFormatName* 
        </dt>
        <dd>A name of the format that refers to a given layout of
        data in a record in the subfile.</dd>
        <dt>
 *subfileRecordNumber* 
        </dt>
        <dd>A subfile relative record number of the record in the
        subfile.</dd>
</dl>

#### Return Value
Object for the subfile record format name and relative record number specified.
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

