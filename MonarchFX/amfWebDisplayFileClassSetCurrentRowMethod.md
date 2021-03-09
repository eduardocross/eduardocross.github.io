---
title: WebDisplayFile.SetCurrentRow Method

Id: amfWebDisplayFileClassSetCurrentRowMethod
TocParent: amfWebDisplayFileClassMethods
TocOrder: 130

keywords: SetCurrentRow method
keywords: WebDisplayFile.SetCurrentRow method
keywords: display files, setting current row
keywords: setting current row of display file
keywords: current row of display file
keywords: how to, set current row of display file

---

Sets the current row to the row and format name specified.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr SetCurrentRow Access(*Public) Type(Void)
  DclSrParm *formatName*  Type(*String)
  DclSrParm *row*  Type(*Integer)** </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *formatName* </code>
        </dt>
        <dd>The format name to set as the current row.</dd>
        <dt><code>row</code></dt>
        <dd>The row number to set as the current row.</dd>
</dl>
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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ WebDisplayFile Class](amfWebDisplayFileClass.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html)
