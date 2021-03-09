---
title: WebDevice.GetRecordIndex Method

Id: amfWebDeviceClassGetRecordIndexMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 40

keywords: GetRecordIndex method
keywords: WebDevice.GetRecordIndex method
keywords: device control, getting record index
keywords: display files, getting record index
keywords: record index, getting
keywords: how to, get record index

---

Gets an integer containing the index for the record format specified.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegFunc GetRecordIndex Access(*Public) Type(*Integer)
   DclSrParm *fmtName*  Type(*String)**       </code></pre>

#### Parameters
<dl>
        <dt>
          <code> *fmtName* </code>
        </dt>
        <dd>The format name of the Record to get the index
        for.</dd>
</dl>  

<!--mine -->

#### Returns
An integer representing the index of the record.
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

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
