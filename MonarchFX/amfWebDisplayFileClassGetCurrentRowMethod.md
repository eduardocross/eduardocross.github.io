---
title: WebDisplayFile.GetCurrentRow Method

Id: amfWebDisplayFileClassGetCurrentRowMethod
TocParent: amfWebDisplayFileClassMethods
TocOrder: 60

keywords: GetCurrentRow method
keywords: WebDisplayFile.GetCurrentRow method
keywords: display files, returning current row
keywords: current row of display file
keywords: how to, return current row of display file

---

Returns the current row number for the format name specified.

#### Syntax
<pre class="prettyprint"> **BegFunc GetCurrentRow Access(*Public) Type(*Integer)
  DclSrParm *formatName*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *formatName* 
        </dt>
        <dd>The format name to get the row number for.</dd>
</dl>
<!--mine -->

#### Return Value
Integer value containing the row number of the format requested.
<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td>Windows Server 2008 R2, Windows Server 2012,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
