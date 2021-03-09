---
title: WebDevice.SetRecordIndex Method

Id: amfWebDeviceClassSetRecordIndexMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 90

keywords: SetRecordIndex method
keywords: WebDevice.SetRecordIndex method
keywords: device control, setting Record index
keywords: display files, setting Record index
keywords: Record index, setting
keywords: how to, set Record index

---

Sets the index for the format name specified.

#### Syntax
<pre class="prettyprint"> **BegSr SetRecordIndex Access(*Public) Type(*void)
   DclSrParm *fmtName*  Type(*String)
   DclSrParm *index*  Type(*integer)**       </pre>  

#### Parameters
<dl>
        <dt>
 *fmtName* 
        </dt>
        <dd>The format name of the record to set the index
        for.</dd>
        <dt>
 *index* 
        </dt>
        <dd>An integer representing the index of the record.</dd>
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

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
